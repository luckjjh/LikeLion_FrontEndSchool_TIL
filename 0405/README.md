# ๐LikeLion_FrontEndSchool_TIL 4์ 05์ผ (ํ)

## ํ์ฌํ ๊ฐ์ฌ๋ ๊ฐ์

1.  ๊ณผ์  ๋ฆฌ๋ทฐ
    - ๊ตฌํ ํ๋ฉด
      ![127 0 0 1_5500_%EC%8B%A4%EC%8A%B5_index html](https://user-images.githubusercontent.com/68142773/161545863-0a093390-ad82-4f1f-931f-04de7124079d.png)
    - ์ฝ๋
      ```html
      <header class="header">
        <h1 class="title">๋์ ์ ๋ง๋ ํ์ฌ๋?</h1>
        <p>๊ฐ๊ณ  ์ถ์ ํ์ฌ์ ๋ํ ํธ๊ฐ๋๋ฅผ ์กฐ์ฌํฉ๋๋ค. ์์ด๊ณ  ์๋ฏธ ์๋ค.</p>
      </header>
      <main class="main">
        <section class="form-wrapper">
          <form action="">
            <fieldset class="fieldset">
              <legend class="invisible">์ง๋ฌธ 1</legend>
              <p>๋ค์ ๋ฌธ์์ค์ ์ ์ง ๋ง์์ ๋๋ ๊ฒ์ ํ๋ ๊ณ ๋ฅด์ธ์.</p>
              <label class="input-box">
                <input
                  type="radio"
                  name="user-want"
                  id="naver"
                  value="naver"
                  required
                />
                ๋ค
              </label>
              ...
              <fieldset class="fieldset">
              <legend class="invisible">์ง๋ฌธ 7</legend>
              <p>์๋ฌด๋ฅผ ์์ ํ๊ธฐ์ ๊ฐ์ฅ ์ ๋นํ ์๊ฐ์ ๊ณ ๋ฅด์ธ์.</p>
              <input type="time" class="time-box" required />
            </fieldset>
            <div class="footer-wrapper">
              <button class="btn">์ ์ถ</button>
              <a href="index.html" class="erase-btn"> ์์ ์ง์ฐ๊ธฐ </a>
            </div>
          </form>
        </section>
      </main>
      ```
    - ํผ๋๋ฐฑ
      - [Web Validation](https://validator.w3.org/) ์น์ฌ์ดํธ์์ ์ฝ๋์ ๋ฌธ์ ์ ์ด ์๋์ง ํญ์ ํ์ธํ๊ธฐ
        > ![image](https://user-images.githubusercontent.com/68142773/161741867-587f165a-9156-4210-9810-52abe43d7bdd.png)
        > ํ์ธ ๊ฒฐ๊ณผ `<section>` tag์ heading์ด ์๋ค๋ ๊ฒฝ๊ณ  ๋ง๊ณ ๋ ๋ณ๋ค๋ฅธ ๋ฌธ์ ๋ ์์๋ค.
      - `<fieldset>` tag๋ `<form>`์ ๋ด์ฉ์ด ๋ฐฉ๋ํ  ๋ ๊ฐ์ ๋ด์ฉ์ ๋ฌถ๋ ์ฉ๋๋ก ์ฌ์ฉ๋๋ค.
        > ๊ฐ ๋ฌธํญ๋ง๋ค `<fieldset>`์ ์ฌ์ฉํด ๋ฌถ์ด ์ฌ๋ฐ๋ฅด์ง ์์ ๋ฐฉ์์ผ๋ก ๊ตฌํํ ๊ฒ ๊ฐ๋ค. `<fieldset>` > `<ul>` > `<li>` ์์๋ฅผ ์ฌ์ฉํด ๋ฌธํญ๋ค์ ๋ถ๋ฆฌํ์ผ๋ฉด ๋ ์ด์์ ์ธ ์ฝ๋๊ฐ ๋์ ๊ฒ ๊ฐ๋ค.
2.  Table

    > ํ์ด๋ธ(ํ)์ ์์ฑํ  ๋ ์ฌ์ฉํ๋ ์์. ์ปจํ์ด๋ ์์๋ก ์ฌ๋ฌ๊ฐ์ง ๋ค๋ฅธ ์์๋ค์ ๋ฌถ์ด์ฃผ๋ ์์์ด๋ค.
    > ![image](https://user-images.githubusercontent.com/68142773/161917835-addf7cff-c311-40f1-9751-368da0deaa76.png)
    > ์์ ๋ด๋ถ์๋ `<caption>`, `<tr>`, `<col>`, `<td>`, `<th>` ๋ฑ์ ์์๋ค์ด ์ฌ์ฉ๋  ์ ์๋ค.

    - `<caption>`

      ํ์ด๋ธ์ ์ ๋ชฉ์ด๋ ์ค๋ช์ ์๋ฏธํ๊ณ  ๋ฐ๋์ ์ฒซ๋ฒ์งธ ์์ ์์๋ก ์ฌ์ฉ๋์ผํ๋ค.

    - `<thead>`, `<tbody>`, `<tfoot>`

      ๊ฐ๊ฐ ๋จธ๋ฆฌ๊ธ, ๋ณธ๋ฌธ, ๋ฐ๋ฅ์ ์๋ฏธํ๋ค. ํ์ด๋ธ์ ๋ด์ฉ์ด ๋ง์ ๋ ๊ตฌ์ญ์ ๋๋๋ ์์๋ก ์ฌ์ฉ๋๋ค.(ํ์์์๋ ์๋)

    * `<tr>`, `<th>`, `<td>`

      `<tr>`์ ํ์ด๋ธ์ ํ์ ๋๋ ๋ ์ฌ์ฉํ๋ค.

      `<td>`๋ `<tr>`๋ก ๋๋ ํ์์ ์์ ๋ถ๋ฆฌํ  ๋ ์ฌ์ฉํ๋ค.

      `<th>`๋ ํ, ์ด์ ๋จธ๋ฆฌ๋ง(ํด๋น ํ,์ด์ ์๋ฏธ)์ ๋ํ๋ด๋ ๋ฐ ์ฌ์ฉํ๋ค.

    * `<rowspan>`, `<colspan>`
      `<td>`๋ `<th>`์์๋ฅผ ํ/์ด ๋ณํฉํ๊ธฐ ์ํ ์์.
      ![image](https://user-images.githubusercontent.com/68142773/161919477-454007a8-56c6-4b0d-ad10-8b29baa0f296.png)

      > ๊ธฐ์กด table

      ![image](https://user-images.githubusercontent.com/68142773/161919251-072e9c53-5c96-4cb9-8cd5-a778d187318b.png)

      > ์ค๋ฅธ์ชฝ ๋ ํ ๋ณํฉํ๋ ์ฝ๋๋ฅผ ์์ฑํ ๊ฒฐ๊ณผ

      ```html
      <table>
        <caption>
          ์ด๋ฌ์ ์ฑ ํ๋งค๋
        </caption>
        <thead>
          <tr>
            <th>๊ตฌ๋ถ</th>
            <th>์ด๋ฆ</th>
            <th>ํ๋งค๋</th>
            <!-- ์ด๊ฐ ๋ณํฉ -->
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>1</td>
            <td>ํด๋ฆฌํฌํฐ</td>
            <td rowspan="2">100</td>
          </tr>
          <tr>
            <td>1</td>
            <td>ํด๋ฆฌํฌํฐ2</td>
          </tr>
        </tbody>
        <tfoot></tfoot>
      </table>
      ```

    * `<colgroup>`๊ณผ `<col>`

      `<colgroup>`์ ์์์์๋ก ์ฐ์ด๋ `<col>`์์๋ฅผ ํตํด ํน์  ์ด์ ๊ณตํต์ ์ธ ์คํ์ผ์ ์ฃผ๋ ๊ฒ์ด ๊ฐ๋ฅํ๋ค.

    * `scope`

      `<th>`์์์ `scope` ์์ฑ์ ์ฌ์ฉํด `<td>`์์ ์ฐ๊ฒฐ๊ด๊ณ๋ฅผ ํํํ  ์ ์๋ค. ์น ์ ๊ทผ์ฑ์ ํ์ํ ์์์ด๋ค.

    * `<table>` ํ์ฉ ์ค์ต - 2022 ์นดํ๋ฅด ์๋์ปต ์กฐ ์ถ์ฒจ ๊ฒฐ๊ณผ ๊ตฌํํ๊ธฐ
      ![image](https://user-images.githubusercontent.com/68142773/161921111-4cf642e2-d824-4ee8-b8db-a2054ce06761.png)

      ```html
      <h1>2022 ์นดํ๋ฅด ์๋์ปต</h1>
      <table>
        <caption>
          ๋ณธ์  ์กฐ ์ถ์ฒจ ๊ฒฐ๊ณผ
        </caption>
        <tr>
          <th scope="col">GROUP A</th>
          <th scope="col">GROUP B</th>
          <th scope="col">GROUP C</th>
          <th scope="col">GROUP D</th>
        </tr>
        <tr>
          <td>์นดํ๋ฅด</td>
          <td>์๊ธ๋๋</td>
          <td>์๋ฅดํจํฐ๋</td>
          <td>ํ๋์ค</td>
        </tr>
        ...
        <tr>
          <th scope="col">GROUP E</th>
          <th scope="col">GROUP F</th>
          <th scope="col">GROUP G</th>
          <th scope="col">GROUP H</th>
        </tr>
        <tr>
          <td>์คํ์ธ</td>
          <td>๋ฒจ๊ธฐ์</td>
          <td>๋ธ๋ผ์ง</td>
          <td>ํฌ๋ฅดํฌ๊ฐ</td>
        </tr>
        ...
      </table>
      ```

      > `<table>`์ ํ๋ ์์ฑํ๊ณ  `<th>`๋ฅผ 2๋ฒ ๋๋  ์ฌ์ฉํด ๊ตฌํํด์ผ ํ๋ ํ๋ฉด๊ณผ ๊ฐ์ ํ๋ฅผ ํํํ๋ค.

## ์ดํธ์ค ๊ฐ์ฌ๋ ๊ฐ์

1. block & inline
   ![image](https://user-images.githubusercontent.com/68142773/161922937-a2a5ad37-80dc-4dc7-b5b2-5a3dd1447a57.png)

   - block level ์์

     ๋ธ๋ผ์ฐ์  ํ๋ฉด์ ๊ฐ๋กํญ์ ๋ชจ๋ ์ฐจ์งํ๋ค. ๋๋น, ๋์ด ์กฐ์ ์ด ๊ฐ๋ฅํ๋ค.

   - inline level ์์

     ์ปจํ์ธ  ์์ ์ ํฌ๊ธฐ๋งํผ ์์ญ์ ๊ฐ์ง๋ ์์. ํ์ค์ ๋ค ์ฐจ์งํ์ง ์๊ธฐ ๋๋ฌธ์ ๊ฐ๋ก ์ ๋ ฌ์ด ๊ฐ๋ฅํ์ง๋ง, ๋๋น, ๋์ด ์กฐ์ ์ด ๋ถ๊ฐ๋ฅํ๋ค.

   - inline-block

     ์ปจํ์ธ  ์์ ์ ํฌ๊ธฐ๋งํผ ์์ญ์ ๊ฐ์ผ๋ฉด์ block level ์์์ ํน์ฑ๋ ๊ฐ๊ณ ์์ด ๋๋น, ๋์ด ์กฐ์ ์ด ๊ฐ๋ฅํ๋ค.

2. `<table>`์ ํ์ฉํด ๋ฌ๋ ฅ ๊ตฌํํ๊ธฐ
   ![image](https://user-images.githubusercontent.com/68142773/161923873-25e189ac-c473-470d-aedd-962bde961572.png)

   ```html
   <main>
     <h2></h2>
     <ol class="season-box">
       <li class="month-box">
         <table>
           <caption class="month">
             1
           </caption>
           <tbody>
             <tr>
               <th scope="col" class="weekend">SUN</th>
               <th scope="col">MON</th>
               <th scope="col">TUE</th>
               <th scope="col">WED</th>
               <th scope="col">THU</th>
               <th scope="col">FRI</th>
               <th scope="col">SAT</th>
             </tr>
             ...
           </tbody>
         </table>
       </li>
     </ol>
   </main>
   ```

   > ๊ฐ ์์ ํ๋์ `<table>`์์๋ก ์๊ฐํ๊ณ , ์์๋๋ก ๋ฐฐ์ด๋๋ ์์์ด๊ธฐ ๋๋ฌธ์ `<ol>` > `<li>`๋ฅผ ์ฌ์ฉํด `<table>`๋ค์ ๋ฌถ์ด์ฃผ์๋ค.

   ```css
   .month-box td:first-child {
     color: #ee595a;
   }
   ```

   > ์ผ์์ผ์ ๋ํ๋ด๋ ๋ ์ง ๊ธ์จ์์ ๋ถ์์์ผ๋ก ํํํ๊ธฐ ์ํด ํญ์ row์ ์ฒซ๋ฒ์งธ ์์์์์์ ์ด์ฉํด ๊ฐ์ class์ธ first-child๋ฅผ ์ฌ์ฉํ๋ค.
