# πLikeLion_FrontEndSchool_TIL 4μ 13μΌ (μ)

## μ΄νΈμ€ κ°μ¬λ κ°μ

### CSS

1. CSS Selector μ¬ν

   1. μμ± μ νμ

      > tagμ μ΄λ¦, class μ΄λ¦, id μ΄λ¦ μΈμ μ¬λ¬ μμ±μ νμ©ν΄ μ κ·Όμ κ°λ₯νκ² νλ μ νμ

      1. `tag[μμ±μ΄λ¦]`

         EX) `div[class]{ ... }` div tagμ΄λ©΄μ class μμ±μ κ°λ λͺ¨λ  μμλ₯Ό μ ννλ€.

      2. `tag[μμ±μ΄λ¦="value"]`

         EX) `div[class="red"]{ ... }` div tagμ΄λ©΄μ class μμ±μ κ°μ΄ μ ννκ² "red"μΈ μμλ₯Ό **λͺ¨λ** μ ννλ€. (μλ²½νκ² μΌμΉν΄μΌ ν¨)

      3. `tag[μμ±μ΄λ¦~="value"]`

         EX) `div[class~="red"]{ ... }` div tagμ΄λ©΄μ class μμ±μ κ°μ΄ "red"μΈ μμλ₯Ό **λͺ¨λ** μ ννλ€.(λ¨μ΄ λ¨μλ‘ μΌμΉν¨μ νμΈ)

      4. `tag[μμ±μ΄λ¦*="value"]`

         EX) `div[class*="red"]{ ... }` div tagμ΄λ©΄μ class μμ±μ κ°μ΄ "red" λ¬Έμμ΄μ ν¬ν¨νλ μμλ₯Ό **λͺ¨λ** μ ννλ€.(λ¬Έμμ΄ λ¨μλ‘ μΌμΉν¨ νμΈ)

      5. `tag[μμ±μ΄λ¦^="value"]`

         EX) `div[class^="sky"]{ ... }` div tagμ΄λ©΄μ class μμ±μ κ°μ΄ "sky"λ‘ μμνλ μμλ₯Ό **λͺ¨λ** μ ννλ€.

      6. `tag[μμ±μ΄λ¦$="value"]`

         EX) `div[class$="pink"]{ ... }` div tagμ΄λ©΄μ class μμ±μ κ°μ΄ "pink"λ‘ λλλ μμλ₯Ό **λͺ¨λ** μ ννλ€.

      7. `tag[μμ±μ΄λ¦|=value]`

         EX) `div[class|="pink"]{ ... }` div tagμ΄λ©΄μ class μμ±μ κ°μ΄ "pink"μ΄κ±°λ "pink"λ‘ μμνλ μμλ₯Ό **λͺ¨λ** μ ννλ€.

   2. κ°μ ν΄λμ€ μ νμ

      > `:hover`, `p:nth-child(1)`μ κ°μ΄ μ€μ λ‘ htmlμ μ‘΄μ¬νμ§ μλ ν΄λμ€μ§λ§ λ§μΉ ν΄λμ€κ° μ‘΄μ¬νλ κ²μ²λΌ μλνλ μ νμ.

      - μνΈμμ©μ μν κ°μ ν΄λμ€

        1. `:hover`: μ¬μ©μκ° μμμ λ§μ°μ€λ₯Ό μ¬λ Έμ λ μ μ©λλ ν΄λμ€.

        2. `:active`: μ¬μ©μκ° μμλ₯Ό μ€νν  λ μ μ©λλ ν΄λμ€.

        3. `:focus`: μμμ ν¬μ»€μ€κ° μμ λ μ μ©λλ ν΄λμ€. ν΄λ¦­μ΄ κ°λ₯ν μμλ input, selectμ κ°μ΄ μνΈ μμ© ν  μ μλ λͺ¨λ  μμμλ ν¬μ»€μ€κ° κ°λ₯.

   3. κ°μ μμ μ νμ

      > λ§ν¬μμ΄ μλ μμλ₯Ό μ½μνλ μ νμλ‘ `::after`μ `::before`λ₯Ό κ°μ₯ λ§μ΄ μ¬μ©νλ€.

      - κ°μ μμ μ νμμ κ°μ ν΄λμ€ μ νμμ μ°¨μ΄μ 
        1. κ°μ μμ μ νμλ ':'μ΄ 2κ°(κ°μ ν΄λμ€ μ νμλ 1κ°)
        2. κ°μ μμ μ νμλ λ§ν¬μ μλ μμλ₯Ό μ½μ(κ°μ ν΄λμ€ μ νμλ ν΄λμ€ μλ μμμ ν΄λμ€ μ½μ)

2. CSS Combinator

   > μ νμμ μ νμλ₯Ό κ²°ν©ν΄ μ¬μ©νλ μ νμλ₯Ό CombinatorλΌ νλ€.

   1. μμ Combinator
      ```css
      section ul {
        text-shadow: none;
      }
      ```
      μ μμμ μμμΈ λ€ μμλ₯Ό μ ννλ Combinatorλ‘ κ³΅λ°±μΌλ‘ νμνκ³  μμ μ κ²½μ° sectionμ μμμΌλ‘ μ‘΄μ¬νλ λͺ¨λ  ulμ μ ννλ€.
   2. μμ Combinator

      ```css
      section > ul {
        text-shadow: none;
      }
      ```

      μ μμμ λ°λ‘ μλ μμ μμλ₯Ό μ ννλ Combinatorλ‘ '>'μΌλ‘ νμνκ³  μμ μ κ²½μ° sectionμ λ°λ‘ μλ μμ μμλ‘ μ‘΄μ¬νλ ulμ μ ννλ€.

   3. μΈμ  νμ  Combinator

      ```css
      h1 + ul {
        color: red;
      }
      ```

      '+'λ₯Ό κΈ°μ€μΌλ‘ μ λ°© μ νμ μ§νμ λμ€λ νλ°© νμ  μ νμλ₯Ό μ ννκ³  μμ μ κ²½μ° h1 λ°λ‘ λ€μ μ€λ νμ  μμ ul μμλ₯Ό μ ννλ€.

   4. μΌλ° νμ  Combinator

      μ λ°© μ νμ κΈ°μ€μΌλ‘ λ€μ λμ€λ λͺ¨λ  νλ°© νμ  μ νμλ₯Ό μ ννλ€.

      ```html
         <style>
            h1 ~ ul {
                  color:red;
            }
         </style>
      </head>
      <body>
         <ul>
            <li>hello world</li>
            <li>hello world</li>
            <li>hello world</li>
         </ul>
         <h1>hello world</h1>
         <ul>
            <li>hello world</li>
            <li>hello world</li>
            <li>hello world</li>
         </ul>
         <ul>
            <li>hello world</li>
            <li>hello world</li>
            <li>hello world</li>
         </ul>
         <h2>hello world</h2>
         <ul>
            <li>hello world</li>
            <li>hello world</li>
            <li>hello world</li>
         </ul>
         <div>
            <ul>
                  <li>hello world</li>
                  <li>hello world</li>
                  <li>hello world</li>
            </ul>
         </div>
      ```

      > ![image](https://user-images.githubusercontent.com/68142773/163215440-d9fd9f91-664c-42c5-9c60-61a97b96af9c.png)<br>
      > h1 λ€μ μμΉνλ νμ  μμμ€ tagκ° ulμΈ μμλ₯Ό λͺ¨λ μ ννλ κ²μ νμΈν  μ μλ€.

3. Flex

   > Contentλ₯Ό μ λ ¬νκ±°λ κ³΅κ°μ λλ μ μλ CSS μμ±μ μ§ν©.

   1. Flexμ μμ±λ€

      - flex-direction

        > μ λ ¬ λ°©ν₯μ κ²°μ νλ μμ±

        ```css
        .container {
          display: flex;
          flex-direction: value;
          /* value: row, column, row-reverse, column-reverse */
        }
        ```

        - row
          > ![image](https://user-images.githubusercontent.com/68142773/163234172-2b5a0f3b-2375-47b8-a7fb-07156043f0ba.png) > `.contatiner` μμ μμλ€μ΄ ν λ°©ν₯μΌλ‘ μ λ ¬λλ€.
        - row-reverse
          > ![image](https://user-images.githubusercontent.com/68142773/163234305-9edd9366-65b4-45fc-ba63-1e41e8cc1823.png) > `.contatiner` μμ μμλ€μ΄ ν μ­μ λ°©ν₯μΌλ‘ μ λ ¬λλ€.
        - column
          > ![image](https://user-images.githubusercontent.com/68142773/163234403-70ba9c42-e2ca-48aa-b7ef-ea1812f13c44.png) > `.contatiner` μμ μμλ€μ΄ μ΄ λ°©ν₯μΌλ‘ μ λ ¬λλ€.
        - column-reverse
          > ![image](https://user-images.githubusercontent.com/68142773/163234465-335cfb31-3153-4d73-983b-d976f40f657b.png) > `.contatiner` μμ μμλ€μ΄ μ΄ μ­μ λ°©ν₯μΌλ‘ μ λ ¬λλ€.

      - justyfy-content
        > μΆμ κΈ°μ€μΌλ‘ λ°°μ΄μ μμΉλ₯Ό μ‘°μ’νκ±°λ μμ΄ν κ°μ κ°κ²©μ μ€μ ν  μ μλ μμ±μΌλ‘ μΆμ κΈ°μ€μΌλ‘ νκΈ° λλ¬Έμ flex-directionμ μ§μ ν κ°μ λ°λΌ κ²°κ³Ό κ°μ΄ λ€λ₯΄κ² λμ¬ μ μλ€.
        ```css
        .container {
          display: flex;
          /* justify-content: flex-start; */
          /* justify-content: flex-end; */
          /* justify-content: center; */
          /* justify-content: space-between; */
          /* justify-content: space-around; */
        }
        ```
        - flex-start
          > μΆ μμ κΈ°μ€μΌλ‘ μ λ ¬ (rowμ κ²½μ° μΌμͺ½)
        - flex-end
          > μΆ λ κΈ°μ€μΌλ‘ μ λ ¬ (rowμ κ²½μ° μ€λ₯Έμͺ½)
        - center
          > μΆ κΈ°μ€ μ€μ μ λ ¬
        - space-between
          > μΆ κΈ°μ€ μμλ€ μ¬μ΄ λμΌν κ°κ²©μ μ£Όλ©° μ λ ¬
        - space-around
          > μΆ κΈ°μ€ μμλ€ μ£Όμμ λμΌν κ°κ²©μ μ£Όλ©° μ λ ¬
      - Axisμ Cross-Axis
        > flexμλ axisμ μ§μ μ΄λ£¨λ cross-axisκ° μ‘΄μ¬νλ€. axisκ° row μνλΌλ©΄ cross-axisλ column μ΄κ³ , axis κ° column μ΄λ©΄ cross-axisλ row μ΄λ€.
        > ![image](https://user-images.githubusercontent.com/68142773/163236891-1586650e-5dcf-420c-abd2-b24a0d4ae8a4.png)
      - align-items
        > align-items: cross-axis κΈ°μ€μΌλ‘ μ΄λ
        ```css
        .container {
          display: flex;
          /* align-items: stretch; (κΈ°λ³Έκ°) */
          /* align-items: center; */
          /* align-items: flex-start; */
          /* align-items: flex-end; */
        }
        ```

      * align-content
        > align-content: flex-container μ cross-axis μΆμ μμ΄νλ€μ΄ μ¬λ¬ μ€μΌ λ μ¬μ© κ°λ₯(flex-wrap:wrapμΈ μνμμ μ¬μ©ν΄μΌν¨)

      - flex-wrap
        > μμμμκ° λμΉ λ μ΄λ€ μμΌλ‘ κ°μΈμ€ μ§μ λν μμ±.
        ```
        .container {
           display: flex;
           flex-direction: column;
           justify-content: space-between;
           /* flex-wrap: wrap; */
           /* flex-wrap: nowrap; */
           /* flex-wrap: wrap-reverse; */
        }
        ```
