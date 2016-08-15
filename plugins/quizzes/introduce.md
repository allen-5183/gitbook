# **Gitbook Plugin：互動問答**


* **Github Source**

  [GitBook plugin-quizzes](https://github.com/GitbookIO/plugin-quizzes)


* **安裝方式**

  預設已經安裝，僅需編輯 book.json 啟動功能

  ```
  "plugins": ["quizzes"],

  ```

* **配置**
 
  可以定制 "pluginsConfig" 中的參數，我用的設置如下:
  ```
  "pluginsConfig": {
        "quiz": {
            "labels": {
                "showCorrect"       : "顯示正確答案",
                "check"             : "確認",
                "showExplanation"   : "查看解釋",
                "explanationHeader" : "Explanation"
            },
            "text": {
                "noChosen"    : "",
                "incomplete"  : ""
            },
            "buttons": {
                "showCorrect"       : true, 
                "showExplanation"   : true
            }
        }
    }
  ```

* **使用方式**


**範例一**

**具體寫法類似html語法**

```
<quiz>
    <question>
        <p>1 + 1 = ?</p>
        <answer>1024</answer>
        <answer correct>2</answer>
    </question>
</quiz>
```

這個例子實現的效果如下：

<quiz>
    <question>
        <p>1 + 1 = ?</p>
        <answer>1024</answer>
        <answer correct>2</answer>
    </question>
</quiz>



**範例二**
---

Here's a quiz about Gitbook

|                  | Good | Bad |
| ---------------- | ---- | --- |
| What is Gitbook? | (x)  | ( ) |

> Gitbook is good

What does Gitbook support?
- [x] Table-based questions with radio buttons
- [x] Table-based questions with checkboxes
- [ ] Telepathy
- [x] List-based questions with checkboxes
- [x] List-based questions with radio buttons
- [ ] Moon-on-a-stick

> Gitbook supports table and list based quiz questions using either radio buttons or checkboxes.
>
> Gitbook is not telepathic and does not give you the moon on a stick.

**範例三**
---
<quiz name="Gitbook Quiz">
    <question multiple>
        <p>What is gitbook used for?</p>
        <answer correct>To read books</answer>
        <answer>To book hotel named git</answer>
        <answer correct>To write and publish beautiful books</answer>
        <explanation>GitBook.com lets you write, publish and manage your books online as a service.</explanation>
    </question>
    <question>
        <p>Is it quiz?</p>
        <answer correct>Yes</answer>
        <answer>No</answer>
    </question>
    <question>
        <p>This is multiple dropdown quiz, in each dropdown select a correct number corresponding to the dropdown's order</p>
        <answer>
            <option correct>First</option>
            <option>Second</option>
            <option>Third</option>
            <option>Fourth</option>
        </answer>
        <answer>
            <option>First</option>
            <option correct>Second</option>
            <option>Third</option>
            <option>Fourth</option>
        </answer>
        <answer>
            <option>First</option>
            <option>Second</option>
            <option correct>Third</option>
            <option>Fourth</option>
        </answer>
        <answer>
            <option>First</option>
            <option>Second</option>
            <option>Third</option>
            <option correct>Fourth</option>
        </answer>
    </question>
</quiz>


**範例四**
---


Define a variable `x` equal to 10.

```js
var x =
```

```js
var x = 10;
```

```js
assert(x == 10);
```

```js
// This is context code available everywhere
// The user will be able to call magicFunc in his code
function magicFunc() {
    return 3;
}
```

---


**範例五**
---


Here is the introduction for the quiz

This is Question 1:
- [x] This is the proposition 1 (the correct one)
- [ ] This is the proposition 2

> This is a help message when the answer to question 1 is wrong

This is Question 2:
- [ ] This is the proposition 1
- [x] This is the proposition 2 (correct)
- [x] This is the proposition 3 (correct)

> This is a help message when the answer to question 2 is wrong


**範例六**
---
<quiz name="Gitbook Quiz">
    <question multiple>
        <p>What is gitbook used for?</p>
        <answer correct>To read books</answer>
        <answer>To book hotel named git</answer>
        <answer correct>To write and publish beautiful books</answer>
        <explanation>GitBook.com lets you write, publish and manage your books online as a service.</explanation>
    </question>
    <question>
        <p>Is it quiz?</p>
        <answer correct>Yes</answer>
        <answer>No</answer>
    </question>
    <question>
        <p>This is multiple dropdown quiz, in each dropdown select a correct number corresponding to the dropdown's order</p>
        <answer>
            <option correct>First</option>
            <option>Second</option>
            <option>Third</option>
            <option>Fourth</option>
        </answer>
        <answer>
            <option>First</option>
            <option correct>Second</option>
            <option>Third</option>
            <option>Fourth</option>
        </answer>
        <answer>
            <option>First</option>
            <option>Second</option>
            <option correct>Third</option>
            <option>Fourth</option>
        </answer>
        <answer>
            <option>First</option>
            <option>Second</option>
            <option>Third</option>
            <option correct>Fourth</option>
        </answer>
    </question>
</quiz>

**範例七**
---