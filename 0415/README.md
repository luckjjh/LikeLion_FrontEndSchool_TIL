# ๐LikeLion_FrontEndSchool_TIL 4์ 15์ผ (๊ธ)

## Code Lion ๊ฐ์

### ์ผ๋จ ๋ง๋๋ JavaScript

1. ๋ก๋ ๋ฒํธ ์ถ์ฒจ๊ธฐ

   > ![image](https://user-images.githubusercontent.com/68142773/163807191-915f9bb0-298b-4399-ac01-56d58b10c1a2.png)</br>
   > 1~45๊น์ง์ randomํ๊ณ  ์ค๋ณต๋์ง ์๋ ์๋ฅผ 6๊ฐ ์ถ๋ ฅํ๋ค.

   - code

     ```js
     let ball = [];
     while (ball.length < 6) {
       let num = parseInt(Math.random() * 45 + 1);
       if (ball.indexOf(num) == -1) {
         //๋ฐฐ์ด์ num ์์ผ๋ฉด -1 ๋ฐํ ๋๋ ํจ์
         ball.push(num);
       }
     }
     ball.sort((a, b) => a - b);
     /* (a, b) => a - b ์์ ์๋ ฅ ์ํ๋ฉด ์์๋ฆฌ ์๋ถํฐ ๋น๊ตํด์ ์ ๋ ฌํจ */
     document.write("<div class='container'>");
     for (let i = 1; i <= 6; i++) {
       document.write(
         "<div class='ball ball" + i + "'>" + ball[i - 1] + "</div>"
       );
     }
     document.write("</div>");
     ```

     - `parseInt(Math.random() * 45 + 1)`

       `Math.random()` ํจ์๋ 0~1๊น์ง์ randomํ ์๋ฅผ ๋ฐํํ๋ ํจ์๋ก 1~45๊น์ง์ ์๋ฅผ ์ป๊ธฐ ์ํด 45๋ฅผ ๊ณฑํ๊ณ  1์ ๋ํด์ค ๋ค `parseInt` ํจ์๋ฅผ ํ์ฉํด randomํ ์๋ฅผ ์ ์ ํํ๋ก ๋ฐํํ๋ค.

     - `ball.indexOf(num)`

       `indexOf()` ํจ์๋ ํจ์๋ฅผ ํธ์ถํ ๋ฐฐ์ด์์ parameter ๊ฐ์ด ์๋ ๊ฒฝ์ฐ ํด๋น index๋ฅผ ๋ฐํํ๊ณ  ์๋ ๊ฒฝ์ฐ -1์ ๋ฐํํ๋ค. ์ค๋ณต๋์ง ์๋ 6๊ฐ์ ์๋ฅผ ๋ฐฐ์ด์ ์ ์ฅํด์ผํ๋ฏ๋ก ํด๋น ํจ์๋ฅผ ํ์ฉํด -1์ด ๋ฐํ๋๋ ๊ฒฝ์ฐ์๋ง ๋ฐฐ์ด์ ์๋ฅผ ์๋ ฅํ๋ค.

     - `ball.sort((a, b) => a - b);`

       parameter๋ฅผ void๋กํ๊ณ  ํจ์๋ฅผ ํธ์ถํ๋ ๊ฒฝ์ฐ ์์ ์์๋ฆฌ๋ถํฐ ๋น๊ตํด ์ฌ์  ์์ผ๋ก ์๋ฅผ ์ ๋ ฌํ๊ฒ๋๋ฏ๋ก `(a, b) => a - b` ํ์ดํ ํจ์๋ฅผ parameter๋ก ๋ฃ์ด ์ค๋ฆ์ฐจ์์ผ๋ก ๋ฐฐ์ด์ด ์ ๋ ฌ๋๊ฒ ํ๋ค.

2. ๊ธ์์ ๊ณ์ฐ๊ธฐ

   > ![chrome-capture-2022-3-18](https://user-images.githubusercontent.com/68142773/163808482-a269b75d-6176-4817-a12e-713b1ef585c3.gif)</br>
   > textarea์ ์๋ ฅ๋๋ ๊ธ์์๋ฅผ ์ธ์ค๋ค.

   - code

     ```js
     countText();
     function countText() {
       let content = document.getElementById("jasosoel").value;
       if (content.length > 200) {
         content = content.substring(0, 200);
         document.getElementById("jasosoel").value = content;
       }
       document.getElementById("count").innerHTML =
         "(" + content.length + "/200)";
     }
     ```

     - `content.substring(0, 200)`
       ์ต๋ ๊ธ์์๋ฅผ ์ ํํ๊ธฐ ์ํด content์ length๊ฐ 200์ด ๋๋ ๊ฒฝ์ฐ `substring()` ํจ์๋ฅผ ํ์ฉํด ์๋ ฅ์ ํด๋ ์๋ ฅํ ํ์คํธ๊ฐ ์ฌ๋ผ์ง๊ฒ ํ๋ค.
     - `onkeydown="countText()"`
       textarea์ onkeydown ์์ฑ์ `countText()` ํจ์๋ก ์ง์ ํด ํค๋ณด๋๊ฐ ๋๋ฆด ๋๋ง๋ค ๊ธ์์๋ฅผ ์ธ ๋ฐ์ํ๋๋ก ํ๋ค.

3. jQuery ๊ธฐ์ด & jQuery ํ์ฉ ๊ฐ๋จํ StarCraft ๊ฒ์

   - jQuery ๊ธฐ๋ณธ ๋ฌธ๋ฒ

     `$("element's name(class, id)").function()`

   > ![chrome-capture-2022-3-18 (1)](https://user-images.githubusercontent.com/68142773/163809443-e24c6320-a359-4c55-90a1-e1580bfbe4d1.gif)</br>
   > ๋๋ก  ์ด๋ฏธ์ง๋ฅผ ํด๋ฆญํ๋ฉด ๋ฒ์ปค์ ๊ณต๊ฒฉ์ ํ๋ฉฐ HP๊ฐ ์ค์ด๋ ๋ค.

   - code

     ```js
     let hp = 3;
     $("#drone").click(function () {
       $("#spit").fadeIn();
       $("#spit").animate({
         left: "+=250",
       });
       $("#spit").fadeOut(function () {
         //callback ํจ์ ํ์ฉ
         hp--;
         $("#hp").text("HP: " + hp);
         if (hp == 0) {
           $("#bunker").fadeOut();
         }
       });
       $("#spit").css({
         left: "150px",
       });
     });
     ```

     - `$("#drone").click()`

       id๊ฐ `drone`์ธ ์์๋ฅผ ํด๋ฆญํ๋ฉด ๋์ํ๋ query๋ก `click()` ํจ์ ๋ด๋ถ์ ์ต๋ช ํจ์๋ฅผ ์ ์ธํด ํด๋ฆญ๋์ ๋์ ๋์์ ์ ์ดํ  ์ ์๋ค.

     - `fadeout()`, `fadeIn()`

       ์ด๋ฏธ์ง๋ฅผ ๋ํ๋ด๊ฑฐ๋ ์ฌ๋ผ์ง๊ฒํ๋ ํจ์

### ์ค๊ฒ์ ์ค๋ฅด๋ ์ธ๋ ๊ฒํฐ ๋๋ฌผ ํ์คํธ ๋ง๋ค๊ธฐ

๐[Repository Link](https://github.com/luckjjh/MBTI-test-web)
