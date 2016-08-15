# **Gitbook 語法：圖片**

---

插入圖片的方法會跟前一節 [連結](https://cowmanchiang.me/gitbook/gitbook/contents/how/links.html) 很像，差別只在於最前面多了一個 "!" 符號，或是可使用 HTML 內嵌的方式進行

* 使用'!【圖片提示文字】\(圖片連結\)'進行 \(示範語法中以 "【 】" 取代 "\[ \]" 以免發生誤判\)

  ```
  ![Cowman](../../assets/images/77326.jpg)

  ```

  ![](../../assets/77326.jpg)

* 使用註解方式進行 \(示範語法中以 "【 】" 取代 "\[ \]" 以免發生誤判\)

  ```
  !【Cowman】【1】

  【1】: ../../assets/images/77326.jpg

  ```

  ![](../../assets/77326.jpg)


* 使用 HTML 內嵌

  ```
  <img src="../../assets/images/77326.jpg" alt="Cowman" width="240" height="180" border="10" />

  ```

  ![](../../assets/773261.jpg)


