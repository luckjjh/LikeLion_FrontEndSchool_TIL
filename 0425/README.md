# ๐LikeLion_FrontEndSchool_TIL 4์ 25์ผ (์)

## ์ดํธ์ค ๊ฐ์ฌ๋ ๊ฐ์

### SASS / SCSS
> ์คํ์ผ์ํธ๊ฐ ์ ์  ๋ ์ปค์ง๊ณ  ๋ณต์กํด์ง์๋ก ์ ์ง๋ณด์๊ฐ ์ด๋ ค์์ง๋๋ฐ ์ผ๋ฐ ํ๋ก๊ทธ๋๋ฐ ์ธ์ด์ ๊ฐ์ ๋ฌธ๋ฒ๋ค์ ์ ๊ณตํด CSS๋ฅผ ํธ๋ฆฌํ๊ฒ ์์ฑํ๊ฒ ํด์ฃผ๋ ์คํ์ผ ์ํธ ํ์ฅ ์ธ์ด. CSS๋ก ์ปดํ์ผ์ด ๋๋ค.
    
  * ์ฃผ์ ๋ฌธ๋ฒ
    
    * Nesting

        ์ค์ฒฉ์ด๋ผ๋ ๋ป์ ๊ฐ์ง ๋จ์ด๋ก Nesting์ ์ฌ์ฉํด html์ ์๊ฐ์  ๊ณ์ธต ๋ฐฉ์๊ณผ ๋์ผํ๊ฒ CSS๋ฅผ ์ค์ฒจํด์ ์์ฑํ๋ ๊ฒ์ด ๊ฐ๋ฅํ๋ค. CSS๊ฐ ๊ตฌ์กฐํ๋์ด ๊ฐ๋์ฑ์ด ๋์์ง๋ฉฐ, ์ ์ง๋ณด์๊ฐ ํธ๋ฆฌํด์ง๋ค.

        Example
        > 
        ```css
        .add-icon {
            background : {
                image: url("./assets/arrow-right-solid.svg");
                position: center center;
                repeat: no-repeat;
                size: 14px 14px;
            }
        }
        ```

    * ๋ถ๋ชจ์ ํ์ &

        "&"๋ ์์์ ์๋ ๋ถ๋ชจ์ ํ์๋ฅผ ์ง์ ํ๋ ๋ช๋ น์ด๋ก &๋ฅผ ์ด์ฉํด after, hover ๋ฑ์ ๊ฐ์ ์์๋ ๊ฐ์ ํด๋์ค๋ฅผ ์์ฑํ๋ ๊ฒ์ด ๊ฐ๋ฅํ๋ค.

        Example
        > 
        ```css
        .box {
            height: 100px;
            width: 100px;
            background-color: red;
            transition: all 0.5s;
            &:hover {
                background-color: green;
            }
        }
        ```

    * ๋ณ์ ์ ์ธ

        ๊ฐ์ด ๋ ๋ฒ ์ด์ ๋ฐ๋ณต๋๊ฑฐ๋ ๊ธฐ์กด์ ๊ฐ์ ํ๋ฒ์ ๋ณ๊ฒฝํด์ผ ํ๋ ๊ฒฝ์ฐ ํด๋น ๊ฐ์ ๋ณ์๋ก ์ฌ์ฉํ๋ค. list๋ map ํ์์ผ๋ก ์ฌ์ฉํ๋ ๊ฒ๋ ๊ฐ๋ฅํ๋ค.

        Example
        >
        ```css
        //์์
        $red: #ee4444;
        $black: #222;
        $bg-color: #3e5e9e;
        $link-color: red;
        $p-color: #282a36;

        //ํฐํธ์ฌ์ด์ฆ
        $font-p: 13px;
        $font-h1: 28px;

        //ํฐํธ
        $base-font: "Noto Sans KR", sans-serif;

        body {
        background-color: $bg-color;
        font-size: $font-p;
        font-family: $base-font;
        }

        h1 {
        font-size: $font-h1;
        color: $black;
        }

        p {
        font-size: $font-p;
        color: $black;
        }

        a {
        color: $link-color;
        }
        ```


    * Mixin

        ์ฝ๋๋ฅผ ์ฌ์ฌ์ฉํ๊ธฐ ์ํด ๋ง๋ค์ด์ง ๊ธฐ๋ฅ์ผ๋ก ์ ํ์๋ค ์ฌ์ด์์ ๋ฐ๋ณต๋๊ณ  ์๋ ์ฝ๋๋ฅผ mixin์ ์ฌ์ฉํด ์ฝ๋์ ๋ฐ๋ณต์ ์ค์ฌ์ค๋ค.
        ```scss
        @mixin ์ด๋ฆ(๋งค๊ฐ๋ณ์) //์์ฑ
        @include ์ด๋ฆ(์ธ์)  //์ฌ์ฉ
        ```

        Example
        >
        ```scss
        @mixin center-xy {
            display: flex;
            justify-content: center;
            align-items: center;
            }

            .card {
            @include center-xy; // ์ ์ํ center-xy mixin์ ์ฌ์ฉํ์ฌ ์ฝ๋ ํ์ค์ด๋ฉด ๋!
            }

            .aside {
            @include center-xy;
        }
        ```

    * ์กฐ๊ฑด๋ฌธ, ๋ฐ๋ณต๋ฌธ
        ๊ธฐ์กด ํ๋ก๊ทธ๋๋ฐ ์ธ์ด๋ค์์ ์ฌ์ฉ๋๋ ์กฐ๊ฑด๋ฌธ, ๋ฐ๋ณต๋ฌธ์ ์ฌ์ฉํด ์ฝ๋์ ์ฌ์ฌ์ฉ์ ์ค์ด๋ ๊ฒ์ด ๊ฐ๋ฅํ๋ค.

        Example
        > ์กฐ๊ฑด๋ฌธ
        ```scss
        @mixin button($color) {
            @if $color == black {
                font-size: 32px;
                color: $color;
                background-color: white;
            } @else if $color == white {
                font-size: 24px;
                background-color: black;
                color: $color;
            } @else {
                font-size: 16px;
                background-color: blue;
                color: $color;
            }
        }

        .btn-1 {
            @include button(black);
        }

        .btn-2 {
            @include button(red);
        }

        .btn-3 {
            @include button(white);
        }
        ```
        > ๋ฐ๋ณต๋ฌธ
        ```scss
        @for $hojun from 1 through 7 {
            .photo-box:nth-child(#{$hojun}) {
                background-image: url("../assets/phoster#{$hojun}.png");
            }
        }
        ```
