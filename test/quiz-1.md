
**範例一**
---
配置

可以定制"pluginsConfig中的参数，我用的设置如下：
---
"pluginsConfig": {
        "quiz": {
            "labels": {
                "showCorrect"       : "显示正确答案",
                "check"             : "确认",
                "showExplanation"   : "查看解释",
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
---
使用

具體寫法類似html語法
---
<quiz>
    <question>
        <p>1 + 1 = ?</p>
        <answer>1024</answer>
        <answer correct>2</answer>
    </question>
</quiz>
---

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

**範例三**
---

**範例四**
---

**範例五**
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
