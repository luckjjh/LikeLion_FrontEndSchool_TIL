# ๐LikeLion_FrontEndSchool_TIL 5์ 4์ผ (์)

## ์ดํธ์ค ๊ฐ์ฌ๋ ๊ฐ์

### JavaScript

#### Array

* Array Method
  > `Array.prototype.func()`์ธ ๊ฒฝ์ฐ ์์ฑํ ๋ฐฐ์ด ๊ฐ์ฒด์ ํจ์๊ฐ ์์ด ๋ฐ๋ก ํธ์ถ ๊ฐ๋ฅํ๊ณ  `Array.func()`์ธ ๊ฒฝ์ฐ Array ๊ฐ์ฒด์ ํจ์๋ฅผ ์ฌ์ฉํ๊ณ  ์ธ์๋ก ๋ฐฐ์ด์ ์ ๋ฌํด์ค๋ค.


  1) `Array.prototype.indexOf()`

        ์ธ์๋ก ์ ๋ฌํ ๊ฐ์ ๋ฐฐ์ด์์ ์ฐพ์ ํด๋น ์์์ ์ธ๋ฑ์ค๋ฅผ ๋ฐํํ๋ method๋ก ์ ๋ฌํ ๊ฐ์ด ๋ฐฐ์ด์ ์๋ค๋ฉด `-1`์ ์ถ๋ ฅํ๋ค.

        ```js
        const cafe = ['coffee', 'cake', 'tea', 'cookie']

        cafe.indexOf('tea')
        //expected output: 2

        cafe.indexOf('coffe', 1)
        //expected output: -1

        cafe.indexOf('bread')
        //expected output: -1
        ```

  2) `Array.isArray()`

        ํจ์์ ์ธ์๋ก ์ ๋ฌ๋๋ ๊ฐ์ด ๋ฐฐ์ด์ธ์ง ์๋์ง ํ๋จํด boolean ๊ฐ์ผ๋ก ๋ฐํํ๋ method.

        ```js
        Array.isArray('coffee');
        //expected output: false

        Array.isArray(false);
        //expected output: false

        Array.isArray([1]);
        //expected output: true
        ```

  3) `Array.prototype.join()`

        ๋ฐฐ์ด ๋ด ์์๋ค์ ์ฐ๊ฒฐํด ํ๋์ srting์ผ๋ก ๋ฐํํ๋(์๋ณธ๋ฐฐ์ด ์์  x) method๋ก ์ธ์์ ๊ฐ์ ์ ๋ฌํ๊ฒ ๋๋ฉด ์ฐ๊ฒฐ๋๋ ์์๋ค ์ฌ์ด์ฌ์ด์ ์ธ์ ๊ฐ์ด ์์นํ๋ค.

        ```js
        const cafe = ['coffee', 'cake', 'tea', 'cookie']
        cafe.join('/')
        //expected output: 'coffee/cake/tea/cookie'
        cafe.join('')
        //expected output: 'coffeecaketeacookie'

        const example = ['coffee', null, undefined, 'cake']
        example.join('')
        //expected output: 'coffeecake'
        ```

  4) `Array.prototype.fill()`

        ๋ฐฐ์ด์ ์ธ์๋ก ์ ๋ฌํ ๊ฐ์ผ๋ก ์ฑ์์ฃผ๋ method. ๋ฐฐ์ด ์์ฒด๋ฅผ ๋ณ๊ฒฝํ๊ธฐ ๋๋ฌธ์ ๋ฐฐ์ด์ ์ด๊ธฐํํ  ํ์๊ฐ ์๋ ๊ฒฝ์ฐ์ ์ฌ์ฉํ๋ฉด ์ข์ ๊ฒ ๊ฐ๋ค.
        ```js
        const cafe = ['coffee', 'cake', 'tea', 'cookie']

        cafe.fill('bread')
        //expected output: ['bread', 'bread', 'bread', 'bread']
        ```
        cf. ๋๋ฒ์งธ ๋งค๊ฐ๋ณ์๋ฅผ ์๋ ฅํ๋ค๋ฉด ์ด๋ ๋ถ๋ถ๋ถํฐ ๋ฐฐ์ด์ ์ฑ์ธ ์ง๋ฅผ ์ง์ ํ๋ ๊ฒ์ด ๊ฐ๋ฅํ๋ค.
    
  5) `Array.prototype.flat()`

        ๋ฐฐ์ด์ด 2์ฐจ์ ์ด์์ ์ฐจ์์ ๊ฐ์ ๋ ์ธ์๋ก ์ ๋ฌํ ์ซ์๋งํผ ์ฐจ์์ ๋ฎ์ถฐ์ฃผ๋ method.
        ```js
        let arr = [[1, 2, 3], [4, 5, 6], [7, 8, [9, [10, 11]]]]
        arr.flat();
        //(9)ย [1, 2, 3, 4, 5, 6, 7, 8, Array(2)]
        arr.flat(2);
        //(10)ย [1, 2, 3, 4, 5, 6, 7, 8, 9, Array(2)]
        arr.flat(3);
        //(11)ย [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11]
        ```

  6) `Array.prototype.includes()`

        ์ธ์๋ก ์ ๋ฌํ ๊ฐ์ด ๋ฐฐ์ด์ ํฌํจ๋์ด ์๋์ง๋ฅผ ํ์ธํด์ฃผ๋ method๋ก ์ธ์๊ฐ string์ธ ๊ฒฝ์ฐ ๋์๋ฌธ์๋ฅผ ๊ตฌ๋ถํด ํ์ํ๋ค. ๋๋ฒ์งธ ์ธ์์ ๊ฒฝ์ฐ ํ์์ ์์ํ  ์ธ๋ฑ์ค๋ฅผ ์๋ฏธํ๋ค.
        ```js
        const cafe = ['coffee', 'cake', 'tea', 'cookie']

        cafe.includes('bread');
        //expected output: false

        cafe.includes('cake');
        //expected output: true

        //์์๋ ์ธ๋ฑ์ค๋ก ์ฌ์ฉ ๊ฐ๋ฅ
        cafe.includes('cake', -3);
        //expected output: true
        
        cafe.includes('cake', -2);
        //expected output: false
        ```

  7) `Array.prototype.find()`

        ๋ฐฐ์ด์์ ํน์  ์กฐ๊ฑด์ ๋ถํฉํ๋ 1๊ฐ์ ๊ฐ์ ์ฐพ์ ๋ฐํํ๋ method. ๋จ ํ๋์ ์์๋ง ์ฐพ๊ณ , ์กฐ๊ฑด์ ๋ง๋ ๊ฐ์ด ์ฌ๋ฌ๊ฐ ์๋ ๊ฒฝ์ฐ ์ ์ผ ์์ ์๋ ์์๋ฅผ ๋ฐํํ๋ค. ์กฐ๊ฑด์ ๋ง๋ ๊ฐ์ด ์๋ค๋ฉด undefined๋ฅผ ๋ฐํํ๋ค.
        ```js
        const arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

        arr.find(i => i > 5);
        //expected output: 6
        ```
  8) `Array.prototype.filter()`

        ๋ฐฐ์ด์์ ํน์  ์กฐ๊ฑด์ ๋ถํฉํ๋ ๊ฐ์ ์ฐพ๊ณ  ๊ทธ ๊ฐ๋ค๋ก ์ด๋ฃจ์ด์ง ์๋ก์ด ๋ฐฐ์ด์ ๋ง๋ค์ด ๋ฐํํ๋ method. ์กฐ๊ฑด์ ๋ง๋ ๊ฐ์ด ์๋ค๋ฉด ๋น ๋ฐฐ์ด์ ๋ฐํํ๋ค. ์ฝ๋ฐฑํจ์๋ฅผ ํ์ฉํด ์กฐ๊ฑด๋ฌธ์ ์์ฑํ๊ณ  ๋ฐํ ๊ฐ์ด ture์ธ ๊ฐ๋ง ๋ฐฐ์ด์ ๋ฃ๊ณ  false์ธ ๊ฐ์ ์ ์ธํ๋ ๋ฐฉ์์ผ๋ก ์ฌ์ฉ์ด ๊ฐ๋ฅํ๋ค.
        ```js
        let arr = [{
            'name' : '์๋1',
            'contents' : 'contents1',
            'dataNum' : 1
        }, {
            'name' : '์๋2',
            'contents' : 'contents2',
            'dataNum' : 2
        }, {
            'name' : 'title3',
            'contents' : 'contents3',
            'dataNum' : 3
        }, {
            'name' : 'title4',
            'contents' : 'contents4',
            'dataNum' : 4
        }, {
            'name' : 'title5',
            'contents' : 'contents5',
            'dataNum' : 5
        }];
        //(5)ย [{โฆ}, {โฆ}, {โฆ}, {โฆ}, {โฆ}]
        arr.filter(i => i.name.includes('tit'))
        //0: {name:'title3', ...}
        //1: {name:'title4', ...}
        //2: {name:'title5', ...}
        arr.filter(i => i.name.includes('์๋'))
        //0: {name:'์๋1', ...}
        //1: {name:'์๋2', ...}
        ```

  9) `Array.prototype.findIndex()`

        ์ธ์๋ก ์ฃผ์ด์ง ์กฐ๊ฑด์ ๋ถํฉํ๋ ๋ฐฐ์ด์ ์ฒซ๋ฒ์งธ ์์์ ์ธ๋ฑ์ค๋ฅผ ๋ฐํํ๋ method. `find()`๋ ์กฐ๊ฑด์ ๋ง๋ ์ฒซ๋ฒ์งธ ์์์ ๊ฐ์ ๋ฐํํ๊ณ  `findIndex()`๋ ์กฐ๊ฑด์ ๋ง๋ ์ฒซ๋ฒ์งธ ์์์ ์ธ๋ฑ์ค๋ฅผ ๋ฐํํ๋ค๋ ์ฐจ์ด์ ์ด ์๋ค.

        ```js
        let cafe = [{
            'item' : 'coffee',
            'amount' : 5
        },{
            'item' : 'cake',
            'amount' : 4
        },{
            'item' : 'tea',
            'amount' : 7
        },{
            'item' : 'cookie',
            'amount' : 3
        }];

        let index = cafe.findIndex(obj => obj.item.length <= 3)
        //index = 2
        ```

  10) `Array.prototype.map()`

        ๋ฐฐ์ด์ ๊ฐ ์์์ ์ค๋ฆ์ฐจ์์ผ๋ก ์ ๊ทผํด ์ฃผ์ด์ง callbackํจ์๋ฅผ ํธ์ถํ ๊ฒฐ๊ณผ๋ฅผ ๋ชจ์ ์๋ก์ด ๋ฐฐ์ด์ ๋ฐํํ๋ method. ๊ธฐ์กด์ ๊ฐ์ ์ฌ์ ์ํ๊ฑฐ๋ ์๋ก์ด ํํ์ ๊ฐ์ ์ ์ํ๋ ๊ฒ์ด ๊ฐ๋ฅํ๋ค. ์ฃผ๋ก ๊ฐ์ฒด๋ json ํํ์ ๋ฐ์ดํฐ๋ฅผ ํ์ํ๋ ์ฉ๋๋ก ์ฌ์ฉ๋์ด ํด๋น ๊ณผ์ ์์ ์๋ก์ด ํํ์ ๊ฐ์ ์ ์ํ๋ ๊ฒฝ์ฐ๊ฐ ๋ง๋ค.

        ```js
        let arr = [{
            'name' : 'title1',
            'contents' : 'contents1',
            'dataNum' : 1,
            '์ง์ญ๊ณผ๋ ์ง' : [
                'ํ๊ตญ',
                [22, 5, 4]
            ]
        }, {
            'name' : 'title2',
            'contents' : 'contents2',
            'dataNum' : 2,
            '์ง์ญ๊ณผ๋ ์ง' : [
                'ํ๊ตญ',
                [22, 5, 4]
            ]
        }, {
            'name' : 'title3',
            'contents' : 'contents3',
            'dataNum' : 3,
            '์ง์ญ๊ณผ๋ ์ง' : [
                'ํ๊ตญ',
                [23, 5, 4]
            ]
        }, {
            'name' : 'title4',
            'contents' : 'contents4',
            'dataNum' : 4,
            '์ง์ญ๊ณผ๋ ์ง' : [
                'ํ๊ตญ',
                [23, 5, 4]
            ]
        }, {
            'name' : 'title5',
            'contents' : 'contents5',
            'dataNum' : 5,
            '์ง์ญ๊ณผ๋ ์ง' : [
                'ํ๊ตญ',
                [22, 5, 4]
            ]
        }];

        arr.map(i => i.์ง์ญ๊ณผ๋ ์ง[1][0]).filter(val => val===22);
        //arr์์ 22๋ง ์ถ์ถํ๊ธฐ
        ```

  11) `Array.prototype.forEach()`

        ๋ฐฐ์ด ๊ฐ ์์๋ค์ ์ํํ๋ฉฐ ์ง์ ํ ๋์์ ์ํํด์ฃผ๋ method๋ก map๊ณผ ๋ค๋ฅด๊ฒ ๋ฐฐ์ด์ ๋ฐํํ์ง ์๊ณ  ๋ฐฐ์ด์ ์ํ๋ง ํ๋ค.

        ```js
        const arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

        arr.forEach(i => console.log(i));
        // expected output: 1
        // expected output: 2
        // expected output: 3
        // expected output: 4
        // expected output: 5
        // expected output: 6
        // expected output: 7
        // expected output: 8
        // expected output: 9
        // expected output: 10
        ```
  12) `Array.prototype.reduce()`

        ๋ฐฐ์ด์ ์ํํ๋ฉฐ ๋ฐํ๋๋ ๊ฐ์ ๋์ ํ๋ฉฐ ์คํํด ์ฃผ๋ method๋ก ๋ฐ๋ก ์ง์  ์คํ๋ ํจ์์ ๋ฐํ๊ฐ์ ์ ์ฅํ๋ ๋์ ๊ฐ, ์ํ๋ฅผ ๋๋ ํ์ฌ ๊ฐ, ํ์ฌ ์์์ index, array ์ ์ฒด ๊ฐ ์ด๋ ๊ฒ 4๊ฐ์ ๋งค๊ฐ๋ณ์๋ฅผ ๊ฐ๋๋ค. ๋ณดํต index์ array๋ ์๋ตํ๋ค.

        ```js
        arr.reduce((๋์ ๊ฐ, ํ์ฌ๊ฐ, index, array) => {
            console.log(๋์ ๊ฐ);
            console.log(ํ์ฌ๊ฐ);
            console.log(index);
            console.table(array);
            return ๋์ ๊ฐ+ํ์ฌ๊ฐ;
        });
        ```

        ๊ตฌ๊ฐ ํฉ์ ๊ตฌํ๊ฑฐ๋, ์ต๋/์ต์๊ฐ์ ๊ตฌํ  ๋ ์ฌ์ฉํ  ์ ์์ ๊ฒ ๊ฐ๋ค.

  13) `Array.from()`

        ๋ฐฐ์ด, ๋ฌธ์์ด ์ฒ๋ผ ๋ฐ๋ณต์ด ๊ฐ๋ฅํ ๊ฐ์ฒด(์ ์ฌ๋ฐฐ์ด)๋ฅผ ๋ฐ์ ์๋ก์ด ๋ฐฐ์ด ๊ฐ์ฒด๋ก ๋ง๋ค์ด์ฃผ๋ method. ์ฌ๋ฌ ๊ฐ์ฒด๋ฅผ ๋ฐฐ์ด๋ก ๋ง๋ค๋ ์ฌ์ฉํ๊ณ  ๊ฐ์ฒด ๋ด ๋ชจ๋  ์์๋ฅผ ์์ ๋ณต์ฌํ๊ธฐ ๋๋ฌธ์ ์๋ณธ ๊ฐ์ฒด๊ฐ ๋ณํํ์ง๋ ์๋๋ค.

        ```js
        Array.from('hello world');
        //expected output: ['h', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd']

        Array.from([1, 2, 3], x => x ** 2);
        //expected output: [1, 4, 9]

        Array.from([{'value':100}, {'value':200}, {'value':300}], x => x.value);
        //expected output: [100, 200, 300]
        ```

  14) `Array.prototype.concat()`

        ์ธ์๋ก ์ฃผ์ด์ง ๊ฐ, ๋ฐฐ์ด์ ๊ธฐ์กด๋ฐฐ์ด์ ์ถ๊ฐํ๋ method๋ก ํ๋ฒ์ ์ฌ๋ฌ๊ฐ์ ๊ฐ์ ์๋ ฅํ๋ ๊ฒ์ด ๊ฐ๋ฅํ๋ค.

        ```js
        const cafe = ['coffee'];

        cafe.concat(['cake']);
        //expected output: ['coffee', 'cake']

        cafe.concat(['tea'], 'cookie');
        //expected output: ['coffee', 'tea', 'cookie']
        ```

  15) `Array.prototype.some()`

        ์ธ์๋ก ์ฃผ์ด์ง ์กฐ๊ฑด์ ๋ง๋ ์์๊ฐ ๋ฐฐ์ด์ ํ๊ฐ๋ผ๋ ์กด์ฌํ  ๊ฒฝ์ฐ `true`๋ฅผ ๋ฐํํ๋ method.

        ```js
        const cafe = [{
            'item' : 'coffee',
            'amount' : 5
        },{
            'item' : 'cake',
            'amount' : 4
        },{
            'item' : 'tea',
            'amount' : 7
        },{
            'item' : 'cookie',
            'amount' : 3
        }];

        const order = cafe.some ( i => {
            return i.amount >= 5
        });

        order
        //expected output: true
        ```


  16) `Array.prototype.every()`

        ๋ชจ๋  ๋ฐฐ์ด์ ์์๊ฐ ์ธ์๋ก ์ ๋ฌ๋ ์กฐ๊ฑด์ ๋ง์์ผ `true`๋ฅผ ๋ฐํํ๋ method.
        
        ```js
        const cafe = ['coffee', 'cake', 'tea', 'cookie']

        const cafe = [{
            'item' : 'coffee',
            'amount' : 5
        },{
            'item' : 'cake',
            'amount' : 4
        },{
            'item' : 'tea',
            'amount' : 7
        },{
            'item' : 'cookie',
            'amount' : 3
        }];

        const order = cafe.every( i => i.amount >= 3)

        order
        //expected output: true
        ```

#### ์กฐ๊ฑด๋ฌธ

  * ์ผํญ์ฐ์ฐ์
      > `์กฐ๊ฑด์ ? ์ฐธ์ผ๊ฒฝ์ฐ ์คํ : ๊ฑฐ์ง์ผ๊ฒฝ์ฐ ์คํ`

      * Example

        ```js
        let item = true ? console.log('true') : console.log('false');
        console.log(item);
        //true ์ถ๋ ฅ
        ```

      * ์ค์ฒฉ ์ฌ์ฉ

        ```js
        let price = 5000;

        let message = (price>6000) ? '๋น์ธ์!' : 
                      (price<3000) ? '์์ฒญ์ธ์!' : '์ ๋นํด์!';

        // ์์ ์ฝ๋๋ ์๋์ ๊ฐ๋ค.
        let price = 5000;
        let message = '';

        if (price > 6000) {
                message = '๋น์ธ์!';
        } else if (price < 3000) {
                message = '์์ฒญ์ธ์!';
        } else {
                message = '์ ๋นํด์!';
        }
        ```