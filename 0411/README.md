# πLikeLion_FrontEndSchool_TIL 4μ 11μΌ (μ)

## μ΄νΈμ€ κ°μ¬λ κ°μ

### CSS

1.  `vertical-align`

    > μΈλΌμΈ λΈλ‘ λ±μ ν¬ν¨ν λͺ¨λ  μΈλΌμΈ μμμ μμ§ μ λ ¬μ μν΄ μ¬μ©λλ μμ±μΌλ‘ λΈλ‘ λ λ²¨ μμμλ μν₯μ λ―ΈμΉμ§ μλλ€.

    ```css
    .one {
      vertical-align: top;
      /* μ΄λ―Έμ§κ° λΆλͺ¨μμ μμμ λ°°μΉ λ λ λ¨λ κ²μ ν΄κ²°νκΈ° μν¨*/
    }
    ```

    - `.one` μλ κ²½μ°

      ![image](https://user-images.githubusercontent.com/68142773/163122294-e79f79d1-f3ba-457a-bfdc-bc4e74ce914c.png)

    - `.one` μλ κ²½μ°

      ![image](https://user-images.githubusercontent.com/68142773/163122122-66cbeb9a-e5fe-45db-a8b3-fc0f302db156.png)

    > μμ κ°μ΄ μ΄λ―Έμ§ μμκ° λ°°μΉλ  λ κ³΅λ°±μ΄ μκ²¨ λ¨λ κ²μ ν΄κ²°νκΈ° μν΄ μ¬μ©λκΈ°λ νλ€.

2.  `text-align`

    > νμ€νΈλ₯Ό μ λ ¬νλλ° μ¬μ©νλ μμλ‘ `left`, `right`, `center` λ±μ valueλ₯Ό ν΅ν΄ textλ₯Ό μ λ ¬ κ°λ₯νλ€.

    - μ λ ¬ κ°λ₯ν μμ

      1. μμμΈ inline block μμ
      2. μμμΈ block μμμ content
      3. μμμΈ inline μμ
      4. text

3.  `text-indent`

    > νμ€νΈ λΌμΈμμ νμ€νΈκ° μμνκΈ° μ μ λΉκ³΅κ°μ μ€μ ν  μ μλ€. μμ κ°λ κ°λ₯νλ€.

    ```html
    <style>
        .a {
            text-indent: 10px;
        }
        .b {
            text-indent: -10px;
            /*μμ κ° κ°λ₯ν¨*/
        }
        </style>
    </head>
    <body>
        <p class="a">Hello World!</p>
        <p class="b">Hello World!</p>
    </body>
    ```

    > ![image](https://user-images.githubusercontent.com/68142773/163124068-2b984b60-11a7-4bf3-ab75-73b4a8b052a9.png)

4.  `position`

    > html tagλ id, class λ°μ€ λ±μ μμΉλ₯Ό μ§μ ν΄ μ£Όλ μμ±μΌλ‘ μ΄λ₯Ό μ΄μ©ν΄ νμ΄μ§μ λ μ΄μμμ κ²°μ ν  μ μλ€.

    1. static
       > `position`μ default κ°μΌλ‘ htmlμ μμ±ν νκ·Έ μμΌλ‘ μμΉκ° μ§μ λλ€. `position`μ΄ staticμΈ μμλ top,leftμ κ°μ κ°μΌλ‘ μμΉλ₯Ό μ‘°μ ν΄λ μμΉκ° λ°λμ§ μλλ€.
    2. relative
       > μλμ μ΄λΌλ μλ―Έλ‘ μλ μμ μ΄ μμ΄μΌ νλ μμΉ(static)μ μλμ μΈ μμΉμ΄λ€. top, left λ±μ κ°λ€λ‘ μμΉλ₯Ό μ‘°μ νλ κ²μ΄ κ°λ₯νλ€.
    3. absolute
       > κΈ°λ³Έμ μΌλ‘ κΈ°μ€μ μ΄ html μμμ μκΈ° λλ¬Έμ μΉμ μ’μΈ‘ μλ¨μ λ³Έλ μμΉλ‘ μΈμνκ³  ν΄λΉ μμΉλ₯Ό κΈ°μ€μΌλ‘ μμ§μ΄κ² λλ€. νμ§λ§, λΆλͺ¨μμκ° `relative`, `absolute`, `fixed`μ κ°μ `position` μμ±μ κ°λ λ€λ©΄ κ°μ₯ κ°κΉμ΄ λΆλͺ¨ λ°μ€μ μ’μΈ‘ μλ¨μ κΈ°μ€μΌλ‘ μμΉνκ² λλ€.

    ```html
    <style>
      .container {
        width: 500px;
        height: 500px;
        position: relative;
        margin-left: 100px;
        border: 5px solid black;
        background-color: aqua;
      }

      .one {
        width: 100px;
        height: 100px;
        border: 1px solid black;
        color: white;
      }
      .one:nth-child(1) {
        position: absolute;
        left: 200px;
        top: 200px;
        background-color: red;
      }
      .one:nth-child(2) {
        position: relative;
        /* μλ μκΈ° μμΉμμ μ’ν μ‘°μ  κ°λ₯ */
        top: 10px;
        left: 10px;
        background-color: green;
      }
      .one:nth-child(3) {
        position: static;
        left: 50px;
        /* static μ΄κΈ° λλ¬Έμ left μμμ κ°μ μ€μ ν΄λ μμκ° μμ§μ΄μ§ μλλ€. */
        background-color: blue;
      }
      .two {
        width: 100px;
        height: 100px;
        position: absolute;
        left: 50px;
        top: 50px;
        background-color: blueviolet;
      }
    </style>
    </head>
    <body>
      <div class="container">
        <div class="one">box1</div>
        <div class="one">box2</div>
        <div class="one">box3</div>
      </div>
      <div class="two"></div>
    </body>
    ```

    > ![image](https://user-images.githubusercontent.com/68142773/163186674-4abefb67-7f58-4888-b0b4-c6efda67421f.png)
    > μ½λμ λ°ν κ²°κ³Ό μ΄λ―Έμ§λ₯Ό νμΈν΄ λ³΄λ©΄ κ° `position` μμ±λ€μ νΉμ§μ΄ λνλ κ²μ μ μ μλ€. λΉ¨κ°μ λ°μ€μ λ³΄λΌμ λ°μ€λ λλ€ `position`μ΄ absoluteμ΄μ§λ§, λΉ¨κ°μ λ°μ€λ `position`μ΄ relativeμΈ `.container`μ μμ μμμ΄λ―λ‘ `.container`μ μ’μΈ‘ μλ¨μ κΈ°μ€μΌλ‘ μμ§μ΄κ³  λ³΄λΌμ λ°μ€μ κ²½μ° positionμ΄ μ§μ λ λΆλͺ¨μμκ° μ‘΄μ¬νμ§ μκΈ° λλ¬Έμ html μμλ₯Ό κΈ°μ€μΌλ‘ μμ§μΈ κ²μ νμΈν  μ μλ€.

    4. fixed

       > μ€ν¬λ‘€μ μ¬λ¦¬κ±°λ λ΄λ¦΄ λ, νΉμ  λ°μ€κ° κ³ μ λμ΄μΌ νλ κ²½μ° μ¬μ©λλ€. μ¬μ©μκ° νμ¬ λ³΄κ³ μλ λ·°ν¬νΈλ₯Ό κΈ°μ€μΌλ‘ νλ©΄μ λΆμ κ² μ²λΌ κ·Έ μλ¦¬λ₯Ό κ³μ μ μ§νκ² λλ€.

       ```html
          <style>
            body {
              margin: 0;
            }
            .nav {
              font-family: "Pacifico", cursive;
              position: fixed;
              position: fixed;
              padding: 10px;
              background-color: brown;
              color: white;
              font-weight: 900;
              font-size: 28px;
              width: 100%;
              height: 45px;
            }
            .container {
              /*margin-top: 0;*/
              padding-top: 120px;
              margin-left: 10px;
            }
          </style>
        </head>
        <body>
          <div class="nav">Hello world</div>
          <div class="container">
            Lorem ipsum dolor sit amet,
            ...
       ```

       > ![chrome-capture-2022-3-13 (1)](https://user-images.githubusercontent.com/68142773/163188955-229476a7-c80d-4f3c-a6ac-f0f550bb1093.gif) > `position`μ΄ fixedμΈ μμκ° νλ©΄μ μ€ν¬λ‘€ν΄λ μμΉλ₯Ό κ·Έλλ μ μ§νλ κ²μ νμΈν  μ μλ€.

       - cf. `position`μ΄ fixedμΈ μμμ νμ  μμμκ² marginμ μ£Όκ²λλ€λ©΄ μλ μ¬μ§κ³Ό κ°μ΄ fixed μμ μμ marginμ΄ μκΈ°λ κ²μ νμΈν  μ μλ€.
         ![image](https://user-images.githubusercontent.com/68142773/163190335-0748ccef-d5ac-4c07-a22b-79ab9ce56d60.png)
         μ΄ λν, λ§μ§ λ³ν© νμμ νλλ‘ νμ  μμμ marginμ΄ fixed μμμ κ²Ήμ³ fixed μμμ marginμ΄ μΆκ°λλ―λ‘ μ£Όμν΄μΌνλ€.

    5. sticky

       > fixedμ λΉμ·ν μ±μ§μ κ°μ§λ§ stickyμ κ²½μ° sticky μμλ stickyμ λΆλͺ¨μμκ° νλ©΄ μλ¨κ³Ό λ§λλ©΄ κ·Έλ λΆν° fixedμ μ±μ§μ κ°λ μμμ΄λ€.

       ```html
         <style>
           section {
             height: 1000px;
             border: 3px solid black;
           }

           h2 {
             position: -webkit-sticky;
             position: sticky;
             top: 0;
             background: greenyellow;
           }
         </style>
       </head>

       <body>
         <h1>sticky test</h1>
         <section>
           <h2>μ€λμ λ©λ΄</h2>
           <ul>
             <li>
               Lorem ipsum dolor
               ...
       ```

       ![chrome-capture-2022-3-13](https://user-images.githubusercontent.com/68142773/163192198-f7013b4e-f21d-4ece-812e-20077885b074.gif)
