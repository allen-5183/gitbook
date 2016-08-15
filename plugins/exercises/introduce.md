# **Gitbook Plugin：課後練習**

* **Github Source**

  [GitBook plugin-exercises](https://github.com/GitbookIO/plugin-exercises)


* **安裝方式**

  預設已經安裝，僅需編輯 book.json 啟動功能

  ```
  "plugins": ["exercises"],

  ```

* **使用方式**

  使用 3個 "-" 或 "\*" 將區塊包起來，並使用 "&gt;" 說明錯誤原因，以下示範原始碼使用 "'" 取代 "\`"

      ---
      Define a variable `x` equal to 10.

      '''js
      var x =
      '''

      '''js
      var x = 10;
      '''

      '''js
      assert(x == 10);
      '''

      '''js
      // This is context code available everywhere
      // The user will be able to call magicFunc in his code
      function magicFunc() {
         return 3;
      }
      '''
      ---



## Exercise

Define a variable `x` equal to 10.

1

var x =

[Submit](https://cowmanchiang.me/gitbook/gitbook/contents/plugin/exercises.html#)

