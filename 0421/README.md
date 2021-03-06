# ๐LikeLion_FrontEndSchool_TIL 4์ 21์ผ (๋ชฉ)

## ์ดํธ์ค ๊ฐ์ฌ๋ ๊ฐ์

### CSS

#### Media Query

> ํน์  ์กฐ๊ฑด(๋จ๋ง๊ธฐ์ ์ ํ, ํ๋ฉด ํด์๋, ๋ทฐํฌํธ์ ๋๋น)์์ ํน์  ์คํ์ผ๋ง ์ ์ฉ๋๋๋ก ๋ง๋ค์ด์ฃผ๋ ๊ธฐ๋ฅ

![image](https://user-images.githubusercontent.com/68142773/164896395-e41f9827-8aa5-4ca0-af74-38280f0a1cd5.png)

> ๊ฐ ๋๋ฐ์ด์ค์ ๋๋น๋ง๋ค ๋ค๋ฅธ UI๋ฅผ ๊ตฌ์ฑํ๋ค. (๋ชจ๋ฐ์ผ (390px), PC(1920px, 1440px), ํ๋ธ๋ฆฟ(834px))

- Example

  ```css
  body {
    background-color: tomato;
  }
  @media screen and (max-width: 1000px) {
    body {
      background-color: green;
    }
  }
  @media screen and (max-width: 500px) {
    body {
      background-color: violet;
    }
  }
  ```

  > ์ง์ ํ `max-width`๋ณด๋ค ์คํฌ๋ฆฐ์ ํฌ๊ธฐ๊ฐ ์์์ง๋ฉด ํด๋น ์คํ์ผ๋ค์ด ์ ์ฉ๋๋ค.

  - `max-width`์ `min-width` ๊ตฌ๋ณ ๋ฐฉ๋ฒ

    > `max-width`๋ ๋ง์๋ ์ด์ ๋๋ณด๋ค ํฌ๋ฉด ์๋๋ค. `min-width`๋ ์ ์ด๋ ์ด์ ๋๋ณด๋ค ์์ผ๋ฉด ์๋๋ค.
    > ![image](https://user-images.githubusercontent.com/68142773/164896903-f0e7b8ad-fdff-4ada-aaab-828fe138db6f.png)

- Bootstrap
  > Bootstrap์ ํ์ฉํด ๋ณด๋ค ํธ๋ฆฌํ๊ฒ ๋ฐ์ํ ์น์ ๋์์ธ ๊ฐ๋ฅํ๋ค.
  - Example
    ```html
    <div class="item col-lg-4 col-md-6 col-sm-12">
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nesciunt sunt
      consequatur illo placeat nisi delectus, porro pariatur excepturi esse
      recusandae laboriosam omnis doloribus commodi nihil nulla architecto
      aperiam possimus non?
    </div>
    ```
    > Bootstrap์ container๋ 12๊ฐ์ col์ ๊ฐ๊ณ  ์์ด ์ด๋ฅผ ํ์ฉํด ์์๋ฅผ ๋ฐฐ์นํ๋ ๊ฒ์ด ๊ฐ๋ฅํ๋ค. ๊ทธ๋์ `div`์์์ ์๋ ๊ฐ class ๊ฐ์ ํด๋น ์์๊ฐ lg์ ํด๋นํ  ๋ col์ 4๊ฐ ์ฐจ์ง, ํด๋น ์์๊ฐ md์ ํด๋นํ  ๋ col์ 6๊ฐ ์ฐจ์ง, ํด๋น ์์๊ฐ sm์ ํด๋นํ  ๋ col์ 12๊ฐ ์ฐจ์งํจ์ ๋ปํ๋ค. ๊ฐ break point๋ ์๋ ์ด๋ฏธ์ง์ ๊ฐ๋ค.
    > ![image](https://user-images.githubusercontent.com/68142773/164898589-26dd131a-3fc5-41a8-a1b1-62b07d94afff.png)

* ์ค์ต

  > ![image](https://user-images.githubusercontent.com/68142773/164900181-ca3db28d-38b4-4c76-8334-3035e2112bfa.png) ํด๋น ๋ฐ์ํ ์น media query ํ์ฉํด์ ๊ตฌํํ๊ธฐ

  - ์ฃผ์ ์ฝ๋

  ```css
  /* ํ๋ธ๋ฆฟ */
  @media (max-width: 768px) {
    .wrap {
      margin-top: 10rem;
      flex-direction: column;
    }
    .section-text p {
      font-size: 1.8rem;
    }
    .section-field {
      flex-basis: max-content;
    }
    .section-field ul {
      flex-direction: row;
      margin-top: 6rem;
    }
    .section-field ul li a {
      font-size: 2.4rem;
    }
    .section-field .field-title {
      top: 3rem;
      left: 3rem;
    }
    .section-field .field-go {
      bottom: 2rem;
      right: 2rem;
    }
  }

  /* ๋ชจ๋ฐ์ผ */
  @media (max-width: 500px) {
    .wrap {
      max-width: calc(100% - 3.4rem);
    }
    .section-text h1 {
      font-size: 3.6rem;
    }

    .section-text p {
      margin-top: 1.4rem;
      font-size: 1.4rem;
    }
    .section-field ul {
      flex-direction: column;
      margin-top: 4rem;
    }
  }
  ```

  - ๊ฒฐ๊ณผ

    1. ์๋ณธ
       ![127 0 0 1_5500_ll_0421_responsive_web_using_media_query_assgin_index html](https://user-images.githubusercontent.com/68142773/164902669-2cc94f5b-8704-4cbf-8f77-3278c583e6d6.png)
    2. 768px ์ดํ ์ผ๋
       ![127 0 0 1_5500_ll_0421_responsive_web_using_media_query_assgin_index html (1)](https://user-images.githubusercontent.com/68142773/164902638-590c3ff3-7a14-46c5-9a9d-c8f93d555ef2.png)
    3. 500px ์ดํ ์ผ๋
       ![127 0 0 1_5500_ll_0421_responsive_web_using_media_query_assgin_index html (2)](https://user-images.githubusercontent.com/68142773/164902681-4120ae7f-6ab8-42f3-9011-92762630db71.png)

#### SVG

> ํ์ฅ ๊ฐ๋ฅํ ๋ฒกํฐ ๊ทธ๋ํฝ์ผ๋ก XML ๊ธฐ๋ฐ์ 2์ฐจ์ ๊ทธ๋ํฝ์ด๋ค. HTML ํ๊ทธ์ ์งํฉ์ผ๋ก ์ด๋ฃจ์ด์ ธ ์์ด css์ JavaScript๋ก ์ ์ด ๊ฐ๋ฅํ๋ค.

- ์ฌ์ฉ ๋ฐฉ๋ฒ

  1. img ํ๊ทธ๋ก ์ฌ์ฉํ๊ธฐ

     ```html
     <img src="frog.svg" alt="" />
     ```

  2. css background๋ก ์ฌ์ฉํ๊ธฐ

     ```css
     .cont-svg {
       width: 100vw;
       height: 100vh;
       background: url(frog.svg) no-repeat 0 0;
       background-size: contain;
     }
     ```

  3. ์ธ๋ผ์ธ์ผ๋ก ๊ตฌํํ๊ธฐ

     ```html
     <svg
       width="624"
       height="465"
       fill="none"
       xmlns="http://www.w3.org/2000/svg"
     >
       <path
         d="m446.529 308.502 79.386-37.479c-37.824-34.863-111.48-58.521-196.146-58.521-123.264 0-223.191 50.142-223.191 112.002 0 61.857 99.927 112.002 223.191 112.002 94.674 0 175.575-29.586 208.011-71.334l-91.251-56.67Z"
         fill="#00A249"
       />

       .. ์ค๋ต ...

       <path
         d="M383 129c0 16.016-13.208 29-29.5 29S324 145.016 324 129s13.208-29 29.5-29 29.5 12.984 29.5 29Z"
         stroke="#000"
       />
       <ellipse
         class="eye-right"
         cx="353.5"
         cy="129"
         rx="12.5"
         ry="12"
         fill="#000"
       />
     </svg>
     ```

  4. object ํ๊ทธ ์ฌ์ฉํ๊ธฐ
     ```html
     <object data="./image.svg" type="image/svg+xml"></object>
     ```

  > 3, 4 ๋ฒ ๋ฐฉ์์ผ๋ก svg๋ฅผ ์ฌ์ฉํ๋ ๊ฒฝ์ฐ css, JavaScript๋ฅผ ํ์ฉํด ๊ฐ svg๋ฅผ ๊ตฌ์ฑํ๋ ์์๋ค์ ์ ์ดํ๋ ๊ฒ์ด ๊ฐ๋ฅํ์ง๋ง, 1, 2๋ฒ ๋ฐฉ์์ ๋ถ๊ฐ๋ฅํ๋ค. ์ด๋ฅผ ์ธ์งํ๊ณ  ์๋ง์ ๋ฐฉ์์ผ๋ก svg๋ฅผ ์ฌ์ฉํด์ผ ํ๋ค.
