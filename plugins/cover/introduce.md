# **Gitbook Plugin：封面**

---



* **Github Source**

  [Cover Generation for GitBook](https://github.com/GitbookIO/plugin-autocover)


* **安裝方式**

  需要先安裝 [Canvas](https://github.com/Automattic/node-canvas)

  ```
  apt-get update
  apt-get install libcairo2-dev libjpeg8-dev libpango1.0-dev libgif-dev build-essential g++
  npm install canvas -g

  ```

  至 nodejs gitbook 安裝目錄下的 node\_modules 目錄

  ```
  cd /usr/lib/node_modules/gitbook/node_modules
  npm install gitbook-plugin-autocover

  ```

  編輯 book.json

  ```
  "plugins": ["autocover"]

  ```

* **使用方式** 後續使用請修改 book.json

  ```
  {
    "output": null,
    "generator": "site",
    "title": "Cowman's Gitbook",
    "plugins": ["autocover"],
    "pluginsConfig": {
        "autocover": {
            "title": "Cowman's Gitbook",
            "author": "Cowman",
            "font": {
                "size": null,
                "family": "Impact",
                "color": "#FFF"
            },
            "size": {
                "w": 1800,
                "h": 2360
            },
            "background": {
                "color": "#09F"
            }
        }
    }
  }

  ```

  當重新啟動 gitbook serve 以後會在書本的靜態網頁資料夾中發現 \(\_book\/\) 兩個檔案，cover.jpg、cover\_small.jpg


