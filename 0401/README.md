# ๐LikeLion_FrontEndSchool_TIL 4์ 01์ผ (๊ธ)

## ์ด์ข์ฐฌ ๊ฐ์ฌ๋ CSS ํน๊ฐ

### ๊ฐ์ ๋ด์ฉ

1. CSS ์ด๋ก 

   - CSS ๊ตฌ์กฐ ์ค๊ณ ํ๋ก์ธ์ค


     ![image](https://user-images.githubusercontent.com/68142773/161249479-14277839-fd7d-407a-841f-588c6da6a281.png)

     1. ์ค๊ณํ  ์น์ ์ ์ฒด์ ์ธ ๋ฉ์ด๋ฆฌ ๋๋๊ธฐ

     2. ๊ตฌ๋ถ์ ์ํด ์๊ฐ์ ์ผ๋ก ๋ฐฑ๊ทธ๋ผ์ด๋ ์ปฌ๋ฌ์ฃผ๊ธฐ
     3. ๊ธฐ๋ณธ(๋ ์ด์์ ๊ด๋ จ) ์คํ์ผ๋ง ์์ฑํด tag ์์ ๋ด์ฉ๋ฌผ ์ถ๊ฐํ  ๊ณต๊ฐ ๋ง๋ จ
     4. CSS ํ์ผ ์๋จ์ ์ด๊ธฐํ ์ฝ๋ ์์ฑํด ๊ฐ tag๋ค rawํ ์ํ๋ก ๋ง๋ค๊ธฐ
     5. class ์ฌ์ฉํด ์์ฑ ๋ถ์ฌํ๊ณ  ์์ ๋ฐฐ์นํ๋ฉด์ ์ฌ์ธํ ์์ ์์

   * type selector <br>
     ๊ฐ์ฅ ๊ธฐ๋ณธ์ ์ธ ์ ํ์๋ก HTML ํ๊ทธ์ ์์ฑ์ ์ง์ ํ๋ ์ ํ์<br>
     ๋ธ๋ผ์ฐ์ ๋ง๋ค ๊ธฐ๋ณธ ์ฌ์ฉ์ ์์ด์ ํธ ์คํ์ผ ์ํธ(MDN์์ ํ์ธ ๊ฐ๋ฅ)๊ฐ ๋ค๋ฅด๊ธฐ ๋๋ฌธ์ ์ด๊ธฐ๊ฐ์ ์ง์ ํด ํ๊ทธ๋ฅผ ๋ค๋ฃจ๊ธฐ ์ฝ๊ฒ ๋ง๋ค์ด์ผํจ </br>
     ![image](https://user-images.githubusercontent.com/68142773/161250251-416a215f-45a4-42e0-b4c7-ff80490a19a4.png)

     ```css
     body,
     p,
     ul {
       margin: 0;
       padding: 0;
     }

     h1,
     h2 {
       margin: 0;
       font-size: inherit;
       font-weight: inherit;
     }
     ```

     > type selector๋ฅผ ํ์ฉํด ๊ฐ์ ์ด๊ธฐํํ ๋ชจ์ต
     > type selector๋ html ๋ฌธ์์ ์ฌ์ฉ๋๋ ๋ชจ๋  tag์ ์์ฑ์ ๋ค๋ฃจ๊ธฐ ๋๋ฌธ์ ์ํํจ => ์ด๊ธฐํ ํ๋๋ฐ๋ง ์ฌ์ฉ

     - initial๊ณผ inherit

       tag์ ์ฌ์ฉ์ ์์ด์ ํธ ์คํ์ผ์ ์ด๊ธฐํํ  ๋ initial๋ก ์ด๊ธฐํ ํ๋ ๊ฒฝ์ฐ ์์(๋ถ๋ชจ) ์์์ ์์ฑ ๊ฐ๋ณด๋ค ์ด๊ธฐํํ ์์์ ์ฐ์ ์์๊ฐ ๋ ๋๊ธฐ ๋๋ฌธ์ ๋ถ๋ชจ์ ์์ฑ์ ์์๋ฐ์ง ๋ชปํจ. ์ด๋ฅผ ํด๊ฒฐํ๊ธฐ ์ํด inherit๋ฅผ ์ฌ์ฉํด ๋ถ๋ชจ์ ์์ฑ์ ์์ ๋ฐ๋๋ก ํจ.
       cf. "ํด๋น ์์ฑ์ ๋ถ๋ชจ์๊ฒ ์์ ๋ฐ์๊ฑฐ๋ค" ๋ผ๋ ์๋ฏธ

   * ๊ณต๋ฐฑ์ ๋ฐ๋ผ ๋ฌ๋ผ์ง๋ selector
     - `div.abc{ property }`
       class ์ด๋ฆ์ด abc์ธ div tag๋ฅผ ์ ํํจ.
     - `div abc{ property }`
       div tag์ ํ์์ ์๋ ์์๋ค ์ค class ์ด๋ฆ์ด abc์ธ ์์ ์ ํํจ.
     - ` div > p{ property }`
       div tag์ ์์ ์์ ์ค p๋ฅผ ์ ํํจ.
   * margin ์ค์ฒฉ ํ์

     ์ด๋ค ๋ ๊ฐ ์ด์ ๋ธ๋ก ์์์ ์ํ ๋ง์ง์ด ๊ฒน์น  ๋ ์ด๋ ํ ์ชฝ์ ๊ฐ๋ง ์ ์ฉํ๋ ๋ธ๋ผ์ฐ์  ๋ ๋๋ง ๊ท์น. ๋ ํฐ ๋ง์ง์ด ์์ ๋ง์ง์ ์์ ์ํจ๋ค.

   * ๋ค์ค class
     HTML์์์ ๋๊ฐ์ง ์ด์์ class๋ฅผ ์ ์ฉํ  ์ ์์.

     ```html
     <div class="footer">
       <a class="icon github" href="">GitHub</a>
       <a class="icon facebook" href="">Facebook</a>
       <a class="icon contact" href="">Contact</a>
     </div>
     ```

     > a tag์ icon๊ณผ ๊ฐ tag์ ๋ง๋ class๊ฐ ์ถ๊ฐ๋์ด ์๋ค.

     ```css
     .icon {
       /*a tag๋ inline element => inline element๋ width์ height์ ๊ฐ๋ ์กด์ฌํ์ง ์์*/
       width: 48px;
       height: 48px;
       display: inline-block; /* ํ์คํธ์ baseline ๊ธฐ์ค์ ์ผ๋ก ํ์คํธ์ ํฌํค๋งํผ w,h๋ก ์์ ๋ฐฐ์นํจ. 
       left, center, right ํํ ๊ฐ๋ฅ*/
       /* element๋ฅผ ๋ค๋ฅธ style๋ก ํํํ๊ณ  ์ถ์๋ ์ฌ์ฉ */
       border-radius: 30px;
       margin: 10px 0;
       border: 2px solid #ddd;
       color: white;
       background-image: url(images/icons.png);
       text-indent: -9999px;
       background-size: 144px 96px;
     }

     .icon.github {
       background-color: black;
       background-position: left top;
     }
     .icon.facebook {
       background-color: dodgerblue;
       background-position: center top;
     }
     .icon.contact {
       background-color: orangered;
       background-position: right top;
     }

     /* pseudo class */
     .icon:hover {
       background-position-y: bottom;
     }
     ```

     > ๊ณตํต์ ์ธ ํน์ง์ icon class์์ property๋ฅผ ์ง์ ํ๊ณ  ์ธ๋ถ์ ์ธ ํน์ง์ ๊ฐ class์์ ๋ฐ๋ก ์ง์ ํจ์ผ๋ก์จ ์ฝ๋๋ฅผ ํจ์จ์ฑ ์๊ฒ ์์ฑ์ด ๊ฐ๋ฅํจ.

   * block, inline, inline-block

     - block

       ํฌ๊ธฐ๋ฅผ ์ง์ ํ  ์ ์๊ณ  ์ธ๋ก ๋์ด ์์๋ก ์์ ์ฌ์ด์ ๊ณต๋ฐฑ์ด ์๋ค. => margin์ด ์ค์ฒฉ ์๋จ

     - inline

       ๊ฐ๋ก ๋์ด ์์๋ก ์์ ์ฌ์ด์ ๊ณต๊ฐ์ด ์๊ณ  ํฌ๊ธฐ๋ฅผ ์ง์ ํ๋ ๊ฒ์ด ๋ถ๊ฐ.

     - inline-block

       inline์ ๋จ์ ์ ๋ณด์ํ์ฌ ์ ์ฉํ ์์๋ก block์ ํฌ๊ธฐ๊ฐ ์กฐ์  ๊ฐ๋ฅํ๋ฉด์ ๊ฐ๋ก ๋์ด ์์์ด๋ค.

   * ์ด๋ฏธ์ง ์คํ๋ผ์ดํธ ๊ธฐ๋ฒ

     ![image](https://user-images.githubusercontent.com/68142773/161387308-f49a1071-b48e-4406-bb21-fab6fcbd5e25.png)

     > ์ฌ๋ฌ ์ด๋ฏธ์ง๋ค์ ํ๋์ ์ด๋ฏธ์ง๋ก ๋ง๋ค์ด background-position ์์ฑ์ผ๋ก ์ด๋ฏธ์ง ์ขํ ๊ฐ์ ์ด์ฉํ์ฌ ์ฌ์ฉํ๋ ๊ธฐ๋ฒ์ด๋ค.

     - ์ฅ์ 

       - ์๋กญ๊ฒ ๋ก๋ฉ๋๋ ๊ฒฝ์ฐ ๊น๋ฐ์ ํ์ ์๊ณ  ์ด๋ฏธ์ง๊ฐ ์ค์ ๋ก ์ฌ์ฉ๋๊ธฐ ์  ๊น์ง ๋ ๋๋ง ๋์ง ์๋๋ค.
       - HTTP ์์ฒญ ํ์๋ฅผ ์ค์ฌ ๋ก๋ฉ ์๊ฐ ์ ์ฝ ๊ฐ๋ฅ
       - ๋ชจ๋ ํํ๋ก ๋ชจ์์ ๊ด๋ฆฌ๊ฐ ๊ฐ๋ฅ

     - ๋จ์ 
       - ์ด๋ฏธ์ง ์ฉ๋์ด ํฌ๋ฉด ๋ก๋ฉ์ ๋งค์ฐ ์ค๋๊ฑธ๋ฆฌ๊ฒ ๋จ.
       - ์ด๋ฏธ์ง๋ฅผ ๋ถ๋ฌ์ค๊ธฐ ์ํด์ ํด๋น ์ด๋ฏธ์ง์ position์ ์์์ผํจ.

   * width:100%์ width:auto

     - width:100%

       ๋ถ๋ชจ๊ฐ ๊ฐ๊ณ ์๋ ์ฌ์ฉ ๊ฐ๋ฅํ ํฌ๊ธฐ๋งํผ ๊ฐ๋ ์ฑ์

     - width:auto
       ๋ถ๋ชจ๊ฐ ๊ฐ๊ณ ์๋ ์ฌ์ฉ ๊ฐ๋ฅํ ํฌ๊ธฐ๋ฅผ ์๋์ผ๋ก ์ฑ์
       > margin์ ์์์ ๋ถ์ฌํ  ๋ auto๋ ์๋์ผ๋ก margin์ ํฌํจํด ๊ณ์ฐํ์ง๋ง, 100%๋ width๋ฅผ 100% ๊ทธ๋๋ก ์ ์งํ๊ธฐ ๋๋ฌธ์ auto๊ฐ ์ข๋ ์ ์ฐํ๋ฉด์ ๋ฌด์กฐ๊ฑด ์ข์ ๊ฐ๋์ด๋ค.

   * box-sizing

     > CSS์ ํ๋๋ฆฌ ์์ญ์ ํฌ๊ธฐ๋ฅผ ๊ฒฐ์ ํ๋ ์์ฑ. content-box์ border-box๊ฐ ๊ฐ์ผ๋ก ์กด์ฌ.

     - content-box (default)

       ์ง์ ํ CSS width ๋ฐ height๋ฅผ ์ปจํ์ธ  ์์ญ์๋ง ์ ์ฉํด border, margin, padding์ ๋ฐ๋ผ ์ ์ฒด ์์ญ์ด ์ปค์ง ์ ์์.

     - border-box

       ์ง์ ํ CSS width ๋ฐ height๋ฅผ ์ ์ฒด ์์ญ์ ์ ์ฉํด width์ ์ํฅ ์ฃผ์ง ์๊ณ  padding ๋ถ์ฌ ๊ฐ๋ฅํ๋ค.

   * text-align:center์ margin:0 auto
   * text-align:center

     tag ๋ด์ text๊ฐ ๊ฐ์ด๋ฐ๋ก ๋ฐฐ์น๋ ๊ฒ. tag๋ ๊ทธ๋๋ก์ด๋ค.

   * margin:0 auto

     tag ์์ฒด๋ฅผ ๊ฐ์ด๋ฐ ์ ๋ ฌํ ๊ฒ.

   * CSS selector ์ฐ์ ์์

     > ๋ ๊ตฌ์ฒด์ ์ธ selector ์ผ์๋ก ์ฐ์ ์์๊ฐ ๋๋ค.
     > ์ฐ์ ์์๊ฐ ๊ฐ๊ณ  ๊ฐ์ selector๋ผ๋ฉด ๋ค์ชฝ์ ๋์จ selector๊ฐ ์์์ style์ ๋ฎ์ด์์

     ![image](https://user-images.githubusercontent.com/68142773/161387774-ab120806-fd1a-41cb-a6a6-84b2da207784.png)

   * background ์์
     ![image](https://user-images.githubusercontent.com/68142773/161387833-b5a62e1e-c63d-4eae-a937-c7a9b26c7505.png)

2. PROFILE ๊ตฌํ ์ค์ต
   ![127 0 0 1_5500_allday-css_profile_index html](https://user-images.githubusercontent.com/68142773/161387896-667ba801-203e-4951-9850-d88f413eb90f.png)

   - ๊ฐ์ ์ 
     - CSS ์์ ์ถ๊ฐ EX) ํธ๋ฐ
     - sementic html ์ฌ์ฉ

3. Bukket List ๊ตฌํ ์ค์ต
   ![127 0 0 1_5500_allday-css_challenges_challenge01_index html](https://user-images.githubusercontent.com/68142773/161387956-cea3674e-6e3d-4eec-9da5-81b6e55d9d16.png)
   - ๊ฐ์ ์ 
     - sementic html ์ฌ์ฉ
     - hover ํจ๊ณผ ์ ๋ฆฌ
     - CSS ๋ฌธ์ ์ ๋ฆฌ
     - CSS ์์ ์ถ๊ฐ 
