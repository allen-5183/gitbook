# GITBOOK Plugin

---

gitbook 專案本身是 open source，讓開發者可以參與外，GitBook 也提供 Plugins 的設計，讓需要特殊功能的書籍，可以在不需要修改 gitbook 主專案的情況下，利用新的 GitBook Plugin 來擴充功能。

例如官方的 Exercise 與 Quizze 兩種範本，就是加入 Plugin 的使用，讓電子書可以提供習題的互動功能。

「book.json」設定檔的 plugins 用來指定啟用哪些 GitBook Plugins。

1. {

2. "plugins": \[ "exercises", "quizzes" \]

3. }


GitBook 直接利用 NPM 來提供 Plugins Repository，在 NPM 網站搜尋「gitbook-plugin」，找到一系列以「gitbook-plugin」開頭命名的 package，就是可以被使用的 GitBook Plugins。

NPM 搜尋「gitbook-plugin」 —  https:\/\/www.npmjs.com\/search?q=gitbook-plugin

這個架構讓任何開發者都可以建立自己需要的 GitBook Plugins。

舉例來說，如果想要建立一個名為「greeting」的 Plugin，只要這些步驟：

1.建一個 gitbook-plugin-greeting 專案（放在 GitHub 或其他地方）。

2.申請一組 NPM 網站帳號。

3.參考 Sample Plugin 建立 Node.js 程式碼。

4.正確修改 package.json 設定檔。

5.使用「npm publish」將套件發佈到 NPM 伺服器。

如此一來，就可以在 GitBook 專案的 book.json 中使用名為「greeting」的專案。

1. {

2. "plugins": \[ "greeting" \]

3. }



