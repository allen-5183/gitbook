# **Gitbook Plugin：流程圖**

---

* **Github Source**

  [gitbook-plugin-mermaid](https://github.com/JozoVilcek/gitbook-plugin-mermaid)


* **安裝方式**

  至 nodejs gitbook 安裝目錄下的 node\_modules 目錄

  ```
  cd /usr/lib/node_modules/gitbook/node_modules
  npm install gitbook-plugin-mermaid

  ```

  編輯 book.json

  ```
  "plugins": ["gitbook-plugin-mermaid"]

  ```

  或是下面這一部份也行

  ```
  npm install gitbook-mermaid

  ```

  編輯 book.json

  ```
  "plugins": ["gitbook-mermaid"]

  ```

* **使用方式 \(這邊使用'取代\`\)**

  ```
  '''mermaid
  graph TD;
   A-->B;
   A-->C;
   B-->D;
   C-->D;
  '''

  ```

  呈現方式

  ![](../../assets/flow-1.jpg)

