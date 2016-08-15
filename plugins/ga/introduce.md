# **Gitbook Plugin：Google Analytics**

---

* Github Source

  [GitBook gitbook-plugin-ga](https://github.com/GitbookIO/plugin-ga) 
* 安裝方式

  ```
   $ npm install -g gitbook-plugin-ga

   在 Gitbook 目錄下設定 book.json 檔案（若沒有該檔案則自行建立）， 填入 Google Analytics 追蹤的 ID，或是自訂ㄧ些設定 。
  ```


> ```
> "plugins": ["ga"],
> "pluginsConfig": {
>    "ga": {
>        "token": "XXXXXXX",
>        "configuration": {
>               "cookieName": "new_cookie_name",
>               "cookieDomain": "mynew.domain.com"
>        }
>    }
> }
> ```

