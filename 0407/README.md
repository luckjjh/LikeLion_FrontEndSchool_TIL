# ๐LikeLion_FrontEndSchool_TIL 4์ 07์ผ (๋ชฉ)

## ์ดํธ์ค ๊ฐ์ฌ๋ ๊ฐ์

1. ๊ณผ์  ๋ฆฌ๋ทฐ

   ์๋ ์ฝ๋์์ ์ด๋ค li๊ฐ ๋นจ๊ฐ ๋ฐฐ๊ฒฝ์ด๊ณ  ์ด๋ค li๊ฐ ๊ธ์ํฌ๊ธฐ๊ฐ ๋ณ๊ฒฝ๋๋์ง์ ๋ํด ์ค๋ชํ์ธ์.

   ```html
   <!DOCTYPE html>
   <html lang="ko">
     <head>
       <title></title>
       <style>
         h1 + p + p + p {
           color: red;
         }
         .a + li {
           background: red;
         }
         li + li + li {
           font-size: 30px;
         }
       </style>
     </head>
     <body>
       <h1>hello world</h1>
       <p>hello world</p>
       <p>hello world</p>
       <p>hello world</p>
       <p>hello world</p>
       <p>hello world</p>
       <ul>
         <li>Apple</li>
         <li class="a">Mango</li>
         <li class="a">Banana</li>
         <li>Melon</li>
         <li>Strawberry</li>
       </ul>
     </body>
   </html>
   ```

   > selector ์ฌ์ด์ ์กด์ฌํ๋ `+`๋ ์ธ์  ํ์  Selector๋ผ ํ๋ค.
   > selectorA + selectorB ํํ๋ก ์์ฑํ๊ณ  selectorA ๋ฐ๋ก ๋ค์ ์์นํ๋ selector B๋ฅผ ์ ํํ๋ค.
   > EX) `.a + li ` ์ ๊ฒฝ์ฐ class="a"์ธ ์์ ๋ค์ ์๋ li๋ฅผ ์ ํํ๋ฏ๋ก ์ ์ฝ๋์์๋ Banana์ Melon์ด ์ ํ๋๋ค.

2. CSS

   - vmin/vmax

     > viewport min/max์ ์ฝ์ด๋ก ๋ธ๋ผ์ฐ์ ์ ๋๋น์ ๋์ด ์ค ํฌ๊ฑฐ๋ ์์ ๊ฒ ๊ธฐ์ค์ผ๋ก ๋จ์๋ฅผ ์ธก์ ํ๋ค. ์ฃผ๋ก ๋ชจ๋ฐ์ผ์์ ๋ง์ด ์ฌ์ฉ๋๋ค.
     > EX) 1vmin์ด๋ฉด ๋๋น, ๋์ด ์ค ์์ ๊ฒ์ ๊ณ ๋ฅด๊ณ  100์ ๊ธฐ์ค์ผ๋ก ์ก์ 100์ค 1์ ์๋ฏธ

     ```html
     <style>
       body {
         margin: 0;
         background-color: palevioletred;
       }
       div {
         width: 50vmax;
         height: 50vmin;
         background-color: white;
       }
     </style>
     <body>
       <div></div>
     </body>
     ```

     ![image](https://user-images.githubusercontent.com/68142773/162620257-566fbb0d-afed-4caf-bff8-3856aebcf990.png)

     > ํด๋น ๋ธ๋ผ์ฐ์  ํ๋ฉด์ ๋๋น๊ฐ ์๋์ ์ผ๋ก ํฌ๊ณ  ๋ธใ ์ด๊ฐ ์๋์ ์ผ๋ก ์๋ค. `div`์ width๋ 50vmax ๋จ์๋ก ์ง์ ํ์์ผ๋ก ์๋์ ์ผ๋ก ํฐ ๋๋น ๊ธฐ์ค 50๋งํผ์ width๋ฅผ ๊ฐ๊ฒ๋๊ณ  height๋ 50vmin ๋จ์๋ก ์ง์ ํ์์ผ๋ก ์๋์ ์ผ๋ก ์์ ๋๋น ๊ธฐ์ค 50 ๋งํผ์ height๋ฅผ ๊ฐ๊ฒ๋๋ค.

   - overflow

     > ์์๋ด์ ์ปจํ์ธ ๊ฐ ์์๋ณด๋ค ์ปค์ ๋์น๋ ๊ฒฝ์ฐ ๊ทธ๊ฒ์ ์ด๋ป๊ฒ ๋ณด์ผ์ง ์ง์ ํ๋ ์์ฑ์ด๋ค.

     - values
       - visible: default ๊ฐ์ผ๋ก ๋์น ๊ฒฝ์ฐ ์ปจํ์ธ ๊ฐ ์์ ๋ฐ์ผ๋ก ๋ณด์
       - hidden: ๋์น๋ ๋ถ๋ถ์ ์๋ผ์ ์จ๊น
       - scroll: ๋์น๋ ๋ถ๋ถ์ ์คํฌ๋กค๋ฐ๋ฅผ ํตํด ๋ณผ ์ ์๊ฒํจ
       - auto: ์ปจํ์ธ  ์์ ๋ฐ๋ผ ์คํฌ๋กค๋ฐ๋ฅผ ์ถ๊ฐํ ์ง ์๋์ผ๋ก ๊ฒฐ์ .

     > overflow-x, overflow-y ์์ฑ์ ํตํด x,y์ถ์ ๊ฐ๊ฐ ์ ์ดํ๋ ๊ฒ๋ ๊ฐ๋ฅํ๋ค.

   - background

     > ์์์ ๋ฐฐ๊ฒฝ์ ์ง์ ํ๋ ์์ฑ์ด๋ค. background-size, background-repeat ๋ฑ์ ํตํด ์ธ๋ถ์ ์ธ ์ ์ด๊ฐ ๊ฐ๋ฅํ๋ค.

     ```html
       <style>
         div {
           width: 800px;
           height: 300px;
           background-image: url("https://www.tvn-2.com/nacionales/Imagen-ilustrativa-gato-medio-bosque_18585331.jpg");
           background-size: cover;
           background-repeat: no-repeat;
         }
       </style>
     </head>
     <body>
       <div></div>
       <img
         src="https://www.tvn-2.com/nacionales/Imagen-ilustrativa-gato-medio-bosque_18585331.jpg"
         alt=""
       />
     </body>
     ```

     ![image](https://user-images.githubusercontent.com/68142773/162620613-c834b3b4-9644-4032-84d2-f440dbaf813b.png)

     > ์ ์ฌ์ง์ `div`์ background๋ก ์ง์ ๋ image, ์๋ ์ฌ์ง์ `img` ์์๋ก ์ง์ ํ image

   - line height

     > ๊ธ์์ ๋์ด๋ฅผ ์ง์ ํ๋ ์์ฑ

     - value
       - normal: ํฐํธ์ font-family์ ๋ฐ๋ฅธ ๊ธ์์ ๊ธฐ๋ณธ ๋์ด(์ฌ์ฉํ๋ font์ ๋ฐ๋ผ ๊ธฐ๋ณธ ๊ฐ์ด ๋ค๋ฅด๋ค.)
       - number: ์ซ์๋ก ๊ฐ์ ์ค์ ํ  ์ ์๋ค. 1์ font-size ๋งํผ์ line-height๋ฅผ ์๋ฏธ.
         line-height:1์ text์ leading ์์ญ์ ์์  ํฐํธ ๋์ด์ ํ์คํธ๊ฐ ๋ฑ ๋ถ๊ฒ ๋๋ค.
       - px,em,%: ํด๋น unit์ ๋ง์ถฐ ๊ธ์์ ๋์ด๊ฐ ์ค์ ๋๋ค. ๋ถ์ ์ ํ UI๊ฐ ๊ตฌํ๋๋ ์ํฉ์ด ๋ง์ ๊ถ์ฅ๋์ง ์๋๋ค.

   - letter spacing

     > ๊ธ์ ์ฌ์ด ๊ฐ๊ฒฉ์ ์กฐ์ ํ๋ ์์ฑ

     ```html
       <style>
         p {
           /* default ๊ฐ์ 1 */
           letter-spacing: 1.6px;
         }
       </style>
     </head>
     <body>
       <p>
         Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore dicta
         eum deserunt perspiciatis neque dolor dolorem id consequatur ut ratione
         non maiores aliquam est eius sed veniam, doloribus rerum earum?
       </p>
     </body>
     ```

     ![image](https://user-images.githubusercontent.com/68142773/162621005-f313a4f1-1f09-44c1-8d52-678fb9804cc2.png)

   - vertiacl align

     > ์์์ ์์ง ์ ๋ ฌ์ ์ง์ ํ๋ ์์ฑ. ์ธ๋ผ์ธ ๋ ๋ฒจ์์์ ์ ์ฉ์ด ๊ฐ๋ฅํ๋ค.

     - value
       - baseline: default ๊ฐ์ผ๋ก ์๋ฌธ์ x๋ฅผ ๊ธฐ์ค์ผ๋ก ํ๋จ ๋ผ์ธ์ ์๋ฏธ. ๋ถ๋ชจ ์์์ ๊ธฐ์ค ์ ์ ๋ง์ถ๋ค.
       - sub: ๋ถ๋ชจ ์๋ ์ฒจ์ ๊ธฐ์ค ์ ๋ ฌ
       - super ๋ถ๋ชจ ์ ์ฒจ์ ๊ธฐ์ค ์ ๋ ฌ

     ```html
     <style>
       .container {
         border: 1px solid black;
         line-height: 1;
       }
       .one {
         border: 1px solid red;
         vertical-align: baseline;
         /*vertical-align: top; 
             */
         font-size: 40px;
       }
       .two {
         border: 1px solid red;
         vertical-align: sub;
         font-size: 40px;
       }
       .three {
         border: 1px solid red;
         vertical-align: super;
         font-size: 40px;
       }
       img {
         /* ํ๋จ์ ์ฌ๋ฐฑ ์๊ธฐ๋ ๊ฒฝ์ฐ ์ฌ์ฉํ ๋งํ ๋ฐฉ๋ฒ */
         vertical-align: top;
       }
     </style>
     ...
     <div class="container">
       <sapn class="one">Lorem ipsum</sapn>
       <sapn class="two">dolor sit amet</sapn>
       <sapn class="three">consectetur adipisicing</sapn>
     </div>
     <div class="container">
       <img
         width="100px"
         src="https://www.tvn-2.com/nacionales/Imagen-ilustrativa-gato-medio-bosque_18585331.jpg"
         alt=""
       />
     </div>
     ```

     ![image](https://user-images.githubusercontent.com/68142773/162621195-3f2abfd2-f771-4551-a1b1-de8d36a4cffd.png)

   - text align

     > ํ์คํธ ์ ๋ ฌ์ ํ๋๋ฐ ์ฌ์ฉ๋๋ ์์ฑ

     ```html
     <style>
       .content {
         width: 100px;
         height: 70px;
         background-color: blueviolet;
       }
       .text_left {
         text-align: left;
       }
       .text_right {
         text-align: right;
       }
       .text_center {
         text-align: center;
       }
       .one {
         margin-left: 50%;
         transform: translateX(-50%);
       }
     </style>
     ...
     <div class="one">
       <div class="content one"></div>
     </div>
     <div class="text_left">
       <span>์ผ์ชฝ์ ๋ ฌ</span>
     </div>
     <div class="text_right">
       <span>์ค๋ฅธ์ชฝ์ ๋ ฌ</span>
     </div>
     <div class="text_center">
       <span>์ค์์ ๋ ฌ</span>
     </div>
     ```

     ![image](https://user-images.githubusercontent.com/68142773/162621285-0c3ada4c-c9f8-4ba8-a450-8d1a7f8cb520.png)

   - CSS ์ค์ ์ ๋ ฌ

     [CSS ์ค์ ์ ๋ ฌ ๋งํฌ](https://velog.io/@luckjjh/CSS-%EC%A4%91%EC%95%99%EC%A0%95%EB%A0%AC-%EC%A0%95%EB%A6%AC)
