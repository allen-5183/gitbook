# **Gitbook Plugin：序列圖**

---

* **Github Source**

  [JS Sequence Diagram Plugin](https://github.com/gmassanek/gitbook-plugin-js-sequence-diagram)


* **安裝方式**

  至 nodejs gitbook 安裝目錄下的 node\_modules 目錄

  ```
  cd /usr/lib/node_modules/gitbook/node_modules
  npm install gitbook-plugin-js-sequence-diagram

  ```

  編輯 book.json

  ```
  "plugins": ["js-sequence-diagram"]

  ```

* **使用方式 \(這邊使用'取代\`\)**

  ```
  '''sequence
  Title: Here is a title
  A->B: Normal line
  B-->C: Dashed line
  C->>D: Open arrow
  D-->>A: Dashed open arrow
  '''

  ```

  呈現方式

  ![](/assets/serial#1.jpg)

* **修正**

  使用 Chrome 可能會出現 "GET [http:\/\/Server\/gitbook\/plugins\/gitbook-plugin-js-sequence-diagram\/build\/sequence-diagram-min.js.map](http://server/gitbook/plugins/gitbook-plugin-js-sequence-diagram/build/sequence-diagram-min.js.map) 404 \(Not Found\)" 錯誤，此時請先觀察使用的 sequence-diagram-min.js 版本為何?

  檔案位置在 \/usr\/lib\/node\_modules\/gitbook\/node\_modules\/gitbook-plugin-js-sequence-diagram\/book\/sequence-diagram-min.js

  ```
  /** js sequence diagrams 1.0.4
  *  http://bramp.github.io/js-sequence-diagrams/
  *  (c) 2012-2013 Andrew Brampton (bramp.net)
  *  @license Simplified BSD license.
  */

  ```

  確認版本後，建立資料夾 build 並下載同版本的 sequence-diagram-min.js.map 檔案

  ```
  cd /usr/lib/node_modules/gitbook/node_modules/gitbook-plugin-js-sequence-diagram/book
  mkdir build
  download https://cdnjs.cloudflare.com/ajax/libs/js-sequence-diagrams/1.0.4/sequence-diagram-min.js.map

  ```

  接著重新啟動 gitbook 即可




 

