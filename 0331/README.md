# ๐LikeLion_FrontEndSchool_TIL 3์ 31์ผ (๋ชฉ)
## ์ ์ฃผ์ฝ๋ฉ๋ฒ ์ด์ค์บ ํ ์ดํธ์ค ๊ฐ์ฌ๋์ ๊ฐ์
### ๊ณผ์ 
1. git๊ณผ github์ ๋ํด ๋ฐฐ์ด ๊ฒ ์ ๋ฆฌ
2. ํ์๊ฐ์ form ๋ง๋ค๊ธฐ

### ๊ฐ์๋ด์ฉ
1. Git๊ณผ GitHub
	 Git: **๋ฒ์  ๊ด๋ฆฌ ๋๊ตฌ**
     GitHub: **Git์ ํด๋ผ์ฐ๋ ํ๊ฒฝ์์ ์ฌ์ฉ**ํ  ์ ์๊ฒ ์ ๊ณตํ๋ ๊ณต๊ฐ.
	* git์ ์ฃผ์ ๋ช๋ น์ด </br>
    ![image](https://user-images.githubusercontent.com/68142773/161069167-d5422806-fa0b-47d3-a06a-7ab1eab6db64.png)
	  * pull: ํ์ฌ ์์ํ๋ repository์ ๋ค๋ฅธ ์ฌ๋์ด ์์ํ ๋ด์ฉ์ ์ถ๊ฐ.
      * add: ์์ํ ์ฝ๋๋ฅผ ๋๊ธฐ ์ํค๋ ๊ณผ์  ```git add . ```์ ํตํด ๋ชจ๋  ํ์ผ์ ๋๊ธฐ ์ํฌ ์ ์์.
      * commit: ๋๊ธฐํ๊ณ  ์๋ ์ฝ๋ ๋ณด๋ผ ์ค๋น๋ฅผ ์๋ฃํ ๊ณผ์ .
      * push: ์ค๋น๋ฅผ ์๋ฃํ ์ฝ๋๋ฅผ repository์ ์๋ก๋.
      
      
	* GitHub์ ์ฅ์ 
      * ์ ์ง๋ณด์
      * ์ ์ฅ์ฉ๋
      * ์ธ์  ์ฝ๋๊ฐ ์์ ๋์๋ ์ง ํ์ธ
      * ์ฝ๋ ๊ณต์ 
      * ๋ฒ์  ๊ด๋ฆฌ
    * .gitignore ํ์ผ
    	๋ฌด์ํ  ํ์ผ์ ๊ธฐ์ํด ํด๋น ํ์ผ์ ๋ฒ์  ๊ด๋ฆฌ์์ ์ ์ธํจ. ์ฃผ๋ก node_module ๊ฐ์ด ํฐ ํ์ผ๋ค์ ์ ์ธ์ํด.
    
2. Embedded content
   * ```<iframe>```
    htmlํ์ด์ง์์ ๋๋ค๋ฅธ html ํ์ด์ง๋ฅผ ๋ณด์ฌ์ฃผ๊ณ  ์ถ์ ๋ ์ฌ์ฉ. width, height ์์ฑ์ผ๋ก ํฌ๊ธฐ ์กฐ์ (default 150px, 300px).
    src ์์ฑ์ผ๋ก ๋ถ๋ฌ์ฌ HTML ๋งํฌ๋ฅผ ์ค์ ํ  ์ ์์ผ๋ฉฐ ๋ณดํต youtube ์์์ ๋ถ๋ฌ์ฌ ๋ ๋ง์ด ์ฌ์ฉ.
      * youtube ์์ ์๋ก๋
      ```html
      <iframe
        width="894"
        height="503"
        src="https://www.youtube.com/embed/POJ5S2aUizA"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
      ```
      ![image](https://user-images.githubusercontent.com/68142773/161072214-b918f172-a1d6-4298-b50a-16bcfbd6c7af.png)
    	
        * frameborder: ํ๋๋ฆฌ๋ฅผ ๊ทธ๋ฆด ์ง(0 or 1) ๊ฒฐ์ ํ๋ ์์ฑ.
        * allow: iframe์์ ํ์ฉํ  ๊ธฐ๋ฅ ์ง์ .
        * allowfullscreen: ์ ์ฒดํ๋ฉด ์ง์.
        * autoplay: ์๋ ์ฌ์ ๊ธฐ๋ฅ. ์ผ๋ถ ๋ชจ๋ฐ์ผ ๋ธ๋ผ์ฐ์ ์์ ์๋ํ์ง ์๊ณ  ์๋ํ์ง ์์ ํธ๋ํฝ์ ์ ๋ฐํ๊ณ  ์ ๊ทผ์ฑ ์ธก๋ฉด(์๊ฐ์ฅ์ ์ธ์ด ๊ฐ์์ค๋ฌ์ด ์๋ฆฌ ๋๋ฌธ์ ๋๋)์์ ์ข์ง ์์ ์ ์์ด mute ์์ฑ๊ณผ ํจ๊ป ์ฌ์ฉ๋์ผ ํจ.
      * Web ํ๋ฉด ๋ณด์ด๊ธฐ
      ``` html
     <!-- ์ถ๋ ฅ ๋จ -->
      <iframe
	     width="1000px"
	     height="500px"
	     src="http://paullab.co.kr/"
	     frameborder="0"
	  ></iframe>
	 <!-- ์ถ๋ ฅ ์๋จ -->
	  <iframe
	      width="300px"
	      height="300px"
	      src="http://www.naver.com/"
	      frameborder="0"
	  ></iframe>
      ```
      
      ๋ณด์์ ์ด์ ๋ก ```<iframe>```์ ๋ง์๋๋ ์น ์ฌ์ดํธ๊ฐ ์์. ์๋ฒ ์ด์ ์ ํด์ผํ๋ ๊ฒฝ์ฐ ์ตํ์ ์๋จ์ผ๋ก ์ํ๋ ํ์ด์ง๋ง ๋ฐ์ค๋ ๋ฐฉ์์ผ๋ก ์ฌ์ฉ ๊ฐ๋ฅ. 
    * ``` <audio> ```
    	์์ ์ปจํ์ธ  ์ฌ์ํ๊ธฐ ์ํ ํ๊ทธ. src ์์ฑ์ ํ์ผ์ ์์น, ํ์ผ๋ช์ ์์ฑํด์ผํจ.
        ```html
        <!-- ์์ฑ ์์๋๋ก -->
        <!-- ์ค๋์ค ์ปจํธ๋กค๋ฌ/ ์๋์ฌ์/ ๋ฐ๋ณต -->
        <audio controls autoplay loop class="bgm">
      <!-- src์ ๋ค์ด๊ฐ ๊ฒฝ๋ก๊ฐ ์ ๋ ๊ฒฝ๋ก๋ผ audio ํ์ผ์ด ๋ฐ๋ก ์์ด๋ ์ฌ์์ด ๋จ -->
          <source
            src="https://drive.google.com/uc?export=download&id=1xbevC0q-fNUDuoFCSLUdot0OIO81LgpE"
            type="audio/mp3"
        />
        ```
        ![image](https://user-images.githubusercontent.com/68142773/161074389-9576b7de-e5d4-4a0c-8cdd-526d3b77b385.png)
    * ``` <video> ```
    	๋์์ ํ์ผ์ ์ฌ์ํ๊ธฐ ์ํ ํ๊ทธ.
        * src: ๋ธ๋ผ์ฐ์ ์๊ฒ ๋น๋์ค ํ์ผ์ ์์น, ํ์ผ๋ช์ ์๋ฆผ.
        * controls: ์์ ํ์ผ์ ์ฌ์ํ๋๋ฐ ํ์ํ ์ปจํธ๋กค๋ฌ ๋ถ๋ฌ์ด.
        * autoplay: ๋ก๋ฉ์ด ์๋ฃ๋๋ฉด ์๋์ผ๋ก ์์ ํ์ผ ์ฌ์
        * loop: ์์ ๋ฐ๋ณต
      ```html
      <video controls width="250">
            <source
              src="https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.webm"
              type="video/webm"
            />

            <source
              src="https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.mp4"
              type="video/mp4"
            />

            Sorry, your browser doesn't support embedded videos.
      </video>
      ```
      ์์ ๊ฐ์ ์ฝ๋๋ก ํฌ๋ก์ค๋ธ๋ผ์ฐ์ง๊ณผ, ์ข ๋ ์ฌ์ฉ์ ์นํ์ ์ธ ๋น๋์ค ๊ตฌํ ๊ฐ๋ฅ.</br>
      ![image](https://user-images.githubusercontent.com/68142773/161074587-f201a3fb-9db6-41f9-85f6-0734c8238f7e.png)
      
   cf. ์ ๋๊ฒฝ๋ก์ ์๋๊ฒฝ๋ก
   	์ ๋๊ฒฝ๋ก๋ ์ฒ์๋ถํฐ ์์ํด ๋ชฉ์ ์ง๊น์ง์ ์ ๋์ ์ธ ๊ฒฝ๋ก๋ฅผ ๋งํจ. ์์์ง์ ๋ถํฐ ๋๊น์ง ๊ฒฝ๋ก๊ฐ ๋ชํํ๊ธฐ ๋๋ฌธ์ ์ด๋ค ๋ฌธ์์์๋ ์ ๋๊ฒฝ๋ก์ ์๋ ํ์ผ์ ์ ๊ทผ ๊ฐ๋ฅ.
    ์๋๊ฒฝ๋ก๋ ํ์ฌ ์์น๋ฅผ ๊ธฐ์ค์ผ๋ก ํด ๋ชฉ์ ์ง๊น์ง์ ์๋์ ์ธ ๊ฒฝ๋ก๋ฅผ ๋งํจ. ์์์ง์ ์ด ๋ชํํ์ง ์์ ๋๊ฐ ์ด๋์ ๊ฒฝ๋ก๋ฅผ ๋ฐ๋ผ๊ฐ๋์ง์ ๋ฐ๋ผ ๋์ฐฉ์ง๊ฐ ๋ฌ๋ผ์ง๊ณ  ์ ๊ทผ์ ๋ชป ํ ์๋ ์์.
    
    | None | ์ ๋๊ฒฝ๋ก | ์๋๊ฒฝ๋ก |
    | ---- | ------- | ------ |
    | ์ปดํ์ผ ์๋ | ๋๋ฆผ | ๋น ๋ฆ |
    | ํด๋น ์์ค ์์น ๋ณํ์ | ๊ฒฝ๋ก ๋ค์ ์ง์  | ๊ธฐ์ค ํด๋๊ฐ ๊ทธ๋๋ก์ธ ์ด์ ๊ฒฝ๋ก ์ง์  ํ์ ์์ |
    | ๋ถ์ค ๊ฐ๋ฅ์ฑ | ๋ฎ์ | ๋์ |
    | ์ฌ์ฉ์ฉ๋ | ํ ๊ฐ๋ฐ์ ์์ค ๋งํฌ์ | ๊ฐ๋ฐํ ๋ด ์์ค ๋งํฌ์ |
    

3. forms
> ์ ๋ณด๋ฅผ ์๋ ฅํ๋ ์์ญ์ผ๋ก ๋ก๊ทธ์ธ ํ๋ฉด์์ ID, PW๋ฅผ ์๋ ฅํ๋ ๊ฒ, ํ์ ๊ฐ์์ ์ ๋ณด๋ฅผ ์๋ ฅํ๋ ์์ ๋ฑ์ ํผ์ด ์ด์ฉ๋๋ค. ํผ์ ์๋ ฅ ํ submit์ ํตํด ๋ฐ์ดํฐ๋ฅผ ์๋ฒ๋ก ์ ์ก์ด ๊ฐ๋ฅํ๋ค.

   ![image](https://user-images.githubusercontent.com/68142773/161077043-a3d714b9-da09-425e-a58a-55c941b11a4f.png)
   * ํผ ๋์ ๋ฐฉ์
    	1. ์น ํ์ด์ง์ ์๋ form์ ๋ฐ์ดํฐ๋ฅผ ์๋ ฅ
        2. ์น ํ์ด์ง ๋ด ์ก์์ด ์ผ์ด๋๊ฒ ๋๋ฉด ๋ฐ์ดํฐ๋ ์น์๋ฒ๋ก ์ด๋ํ๊ฒ ๋จ
        3. ์น ์๋ฒ๋ฅผ ๋ฐ์ดํฐ ์ฒ๋ฆฌ๋ฅผ ์ํด APP์ ํธ์ถ
        4. ํ์์ ๋ฐ๋ผ APP์ด DB๋ก ๋ฐ์ดํฐ ์ ์ก
        5. DB์์ CRUD(Create, Read, Update, Delete)์์ ์ผ์ด๋๊ณ  ๊ฒฐ๊ณผ๋ฅผ APP -> Web ์์ผ๋ก ์ ์ก
        6. ์น ์๋ฒ๋ ๋ฐ์ ๊ฒฐ๊ณผ๋ฅผ Client ๋ธ๋ผ์ฐ์ ์๊ฒ ๋ณด๋
        7. ๋ธ๋ผ์ฐ์ ๊ฐ ๊ฒฐ๊ณผ๋ฅผ ๋๋๋งํด ์ฌ์ฉ์์๊ฒ ๋ณด์
    
   * ```<form>```์ ์์ฑ
      * action: ์๋ ฅ ๊ฐ์ ์ ์กํ  ํ์ด์ง ๋ํ๋.
      * method: ๋ฐ์ดํฐ๋ฅผ ์ ์กํ  ๋ฐฉ๋ฒ์ ์ ์. get๊ณผ post๊ฐ ์กด์ฌ. get์ ์น ์๋ฒ์ ๋ฐ์ดํฐ๋ฅผ ์์ฒญํ  ๋, post๋ ํ์ผ์ด๋ ๋ณด์์ด ํ์ํ ๋ฐ์ดํฐ๋ฅผ ์ ์กํ  ๋ ์ฌ์ฉ.
      cf. get์ ์ฃผ์์ ๋ฐ์ดํฐ๋ฅผ ์๋ ฅํ๋ query string ๋ฐฉ์์ด๊ธฐ ๋๋ฌธ์ ์ ๋ณด๊ฐ URL์ ๋ธ์ถ๋จ.
      post๋ body์ ๋ฐ์ดํฐ๋ฅผ ์๋ ฅํ๋ ๋ฐฉ์์ด๊ธฐ ๋๋ฌธ์ ์ ๋ณด๊ฐ ๋ธ์ถ๋์ง ์์.
      
 * ```<input>```
    ์ฌ์ฉ์๊ฐ ๋ค์ํ๊ฒ ํผ ํ๊ทธ์ ์๋ ฅํ  ์ ์๋ ๊ณต๊ฐ์ ๋ง๋ค์ด ์ฃผ๊ณ , ์ฌ์ฉ์์๊ฒ ์ ๋ณด๋ฅผ ์๋ ฅ๋ฐ์.
    
    * ```<label>```
    ```<input>``` tag๋ฅผ ์ค๋ชํ๋ ํ์คํธ๋ฅผ ๋ถ์ฌ ๋ฌด์์ ์๋ ฅํ๋์ง ์ค๋ช. semanticํ label์ ์ฌ์ฉํด ์ ๊ทผ์ฑ์ ์ฌ๋ ค์ผํจ.
    
    * form ์์๋ค์ ํ์ฉํ ์์ 
    
    ```html
    <!-- get => URL๋ก์จ ์์ฒญ์ ๋ณด๋ธ๋ค. -->
    <form action="/form.html" method="get">
      <input type="text" name="userId" />
      <input type="password" name="userPw" />
      <!-- button์ submit ์์ฑ default ๊ฐ์ submit -->
      <button type="submit">๋ก๊ทธ์ธ</button>
    </form>
    <!-- => http://127.0.0.1:5500/form.html?userId=%EC%95%84%EC%9D%B4%EB%94%94&userPw=qlalfqjsgh
    ์ฟผ๋ฆฌ ์คํธ๋ง-->

    <form action="/form.html" method="post">
      <input type="text" name="userId" />
      <input type="password" name="userPw" />
      <!-- button์ submit ์์ฑ default ๊ฐ์ submit -->
      <button type="submit">๋ก๊ทธ์ธ</button>
    </form>
    <!-- post => URL์ด ์๋ body๊ฐ์ผ๋ก ์์ฒญ์ ๋ณด๋ -->
    ```
    
    ![image](https://user-images.githubusercontent.com/68142773/161080598-40c734d4-cdf4-4b8a-90f3-9257589bd1d5.png)
    
    ```html
    <form action="">
      <input type="text" name="userId" /></form><br>
      <input type="password" name="userPw" /><br>
      <input type="checkbox" name="" id="" /><br>
      <!-- checkbox = ์ค๋ณต ์ ํ -->
      <label for="men">๋จ</label>
      <!-- input ์ฐฝ์ ์ค๋ชํ๋ tag -->
      <input type="radio" name="์ฑ๋ณ" id="man" />
      <label for="female">์ฌ</label>
      <input type="radio" name="์ฑ๋ณ" id="female" /><br>
      <!-- radiobox = ๋จ์ผ ์ ํ -->
      <input type="color" name="" id="" /><br>
      <input type="date" name="" id="" /><br>
      <input type="datetime" name="" id="" /><br>
      <input type="email" name="" id="" /><br>
      <input type="hidden" name="" id="" /><br>
      <!-- hidden์ ์๋ ฅ๋ ์ ๋ณด๋ฅผ ์ ์ฅํ๊ณ  ์ ์กํด์ผ ํ๋ ๊ฒฝ์ฐ๊ฐ ์๊น -->
      <input type="range" name="" id="" /><br>
      <input type="number" name="" id="" /><br>
      <input type="url" name="" id="" /><br>
      <input type="file" name="" id="" /><br>
      <button type="submit">๋ก๊ทธ์ธ</button>
    </form>
    ```
    
    ![image](https://user-images.githubusercontent.com/68142773/161080694-072d4b44-3c68-4e29-b78d-fcc585f07dd0.png)
    
   * ๊ณผ์  ํ์๊ฐ์ ํ์ด์ง ๊ตฌํ
    
    ```html
   <!DOCTYPE html>
	<html lang="ko">
	  <head>
	    <meta charset="UTF-8" />
	    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
	    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
	    <style>
	      @import url("https://fonts.googleapis.com/css2?family=Nanum+Gothic&display=swap");
	      * {
		font-family: "NanumGothic";
	      }
	      h1 {
		margin: 0px;
		padding: 10px;
		background-color: black;
		color: white;
	      }
	      input {
		margin: 5px;
	      }
	      fieldset {
		font-size: 23px;
		margin-bottom: 10px;
	      }
	      .signupBtn {
		color: white;
		background-color: black;
		width: 20%;
		height: 40px;
		font-size: 20px;
	      }
	      label {
		font-size: 20px;
	      }
	    </style>
	    <title>ํ์๊ฐ์</title>
	  </head>
	  <body>
	    <header>
	      <h1>ํ์๊ฐ์</h1>
	      <hr />
	    </header>
	    <main>
	      <section>
		<form action="#" method="post">
		  <fieldset>
		    <legend>๋ก๊ทธ์ธ ์ ๋ณด</legend>
		    <label for="userID">์์ด๋</label><br />
		    <input type="text" name="์์ด๋" id="userID" /><br />
		    <label for="userPW">๋น๋ฐ๋ฒํธ</label><br />
		    <input type="password" name="๋น๋ฐ๋ฒํธ" id="userPW" /><br />
		    <label for="userPWConfirm">๋น๋ฐ๋ฒํธ ํ์ธ</label><br />
		    <input type="password" name="๋น๋ฐ๋ฒํธํ์ธ" id="userPWConfirm" />
		  </fieldset>
		  <fieldset>
		    <legend>ํ์ ์ ๋ณด</legend>
		    <label for="userName">์ด๋ฆ</label><br />
		    <input type="text" name="์ด๋ฆ" id="userName" /><br />
		    <label for="userBirth">์๋์์ผ</label><br />
		    <input type="date" name="์๋์์ผ" id="userBirth" /><br />
		    <label for="userSex">์ฑ๋ณ</label><br />
		    <input type="radio" name="์ฑ๋ณ" id="userSex" value="male" />๋จ
		    <input
		      type="radio"
		      name="์ฑ๋ณ"
		      id="userSex"
		      value="female"
		    />์ฌ<br />
		    <label for="userEmail">์ด๋ฉ์ผ</label><br />
		    <input type="email" name="์ด๋ฉ์ผ" id="userEmail" /><br />
		    <label for="userPhone">ํด๋์ ํ</label><br />
		    <input type="tel" name="ํด๋์ ํ" id="userPhone" /><br />
		  </fieldset>
		  <fieldset>
		    <legend>๊ฐ์ธ์ ๋ณด ์ ๊ณต ๋์</legend>
		    <p>
		      Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio,
		      exercitationem beatae totam porro officia amet pariatur. Unde
		      neque, nostrum sunt facere itaque repellendus voluptatum fugit
		      obcaecati eius nemo nulla explicabo?
		    </p>
		    <label for="checkAgree">๊ฐ์ธ์ ๋ณด ์ ๊ณต์ ๋์ํฉ๋๋ค.</label>
		    <input type="checkbox" name="๋์๋ฐ์ค" id="checkAgree" />
		  </fieldset>
		  <button class="signupBtn">ํ์๊ฐ์</button>
		</form>
	      </section>
	    </main>
	    <footer></footer>
	  </body>
	</html>
    ```
    ![image](https://user-images.githubusercontent.com/68142773/161082811-e48bb1f5-5d8c-4301-a0ae-83914fc5f1a0.png)
    
