# SE_assignment1

# GFM : Github Flavored Markdown
GFM은 Github.com에서 더 쉽게 작업할 수 있도록 제공하는 마크다운입니다. 기존에 마크다운이 가지고 있는 문법들을 따르는 편이지만, comments나 Pull requests에 대한 기능은 GFM에서만 가능합니다.

---
---

## 1. Syntax Highlighting
### Fenced Code Block
마크다운에서 기본 코드 블럭은 1tab 혹은 4spaces이다. 그러나 GFM에서는 3개의 (\`) backticks를 연달아 작성하는 것으로 구문강조 코드 블럭을 지원한다. 이 구문강조 코드 블럭을 fenced code block이라고 한다.
[GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown)

```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```

**4 칸으로 코드를 들여 쓰기**

```javascript
    function fancyAlert(arg) {
      if(arg) {
        $.facebox({div:'#foo'})
      }
    }
```

**구문 강조(X) 파이썬 코드 예**

```
def foo():
    if not bar:
        return True
```

## 2. Task Lists
To-Do list의 박스를 생각하면 이해가 쉽다. []를 사용하여 표현하며 완료된 업무를 표현하고자 할 떄에는 안에 X로 표시해준다.
```
- [x] SE01 Lecture
- [ ] SE02 Lecture
- [ ] SE assignment1 submit
```

- [x] SE01 Lecture
- [ ] SE02 Lecture
- [ ] SE assignment1 submit

+) 추가적으로 만약 task list item이 parenthesis로 시작한다면 탈출이 필요하다(\) 
```
- []\(optional) Open a followup issue
```
[Task List items](https://github.github.com/gfm/#task-list-items-extension-)


## 3. Tables
사실 지금 나열된 것들은 그냥 마크다운에서 되는 것들이다.. 테이블도 마크다운에서 만들 수 있다.
테이블은 하이픈(-)으로 나눠 만들며 각각의 칼럼은 (|)으로 분리한다.
```
칼럼 이름1 | 칼럼 이름2
------------|-----------
내용 1 | 내용 2
내용 3 | 내용 4
```
칼럼 이름1 | 칼럼 이름2
------------|-----------
내용 1 | 내용 2
내용 3 | 내용 4

## 4. Mentioning people and teams
이 부분은 정말 GFM만 가능한 것. Github에서는 @username or teamname으로 멘션(언급)이 가능하다. 이렇게 언급을 할 경우, 해당 작업에 변화 등이 생길 경우 이를 바로 파악할 수 있다. 이는 Github에서의 특징적인 기능이므로 일반 마크다운에서는 불가능하나 GFM에서는 사용 가능하다.
@github/what is variable here?

## 5. Referencing issues and pull requests
이슈 또는 Pull request의 모든 번호가 자동 링크로 변환되는 과정. 
[Autolinked references and URLs](https://docs.github.com/en/github/writing-on-github/autolinked-references-and-urls)

+) [SHA-1 hash](http://en.wikipedia.org/wiki/SHA-1) 는 자동으로 GitHub에 커밋에 대한 링크로 변환됩니다.

```
16c999e8c71134401a78d4d46435517b2271d6ac
mojombo@16c999e8c71134401a78d4d46435517b2271d6ac
mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac
```
## 6. Content Attachments
URL을 활용하여 자동으로 클릭 가능한 링크로 변환된다. 하지만 모든 링크가 가능한 것은 아니며 github app이 있어야 하며 github에 정보를 제공한 상태여야지만 가능하다.

## 7. Using emojis
Github에서는 이모티콘을 지원한다.
@jykim701 👍 💥
단축키가 존재하긴 하지만 :EMOJICODE: 의 형태이므로 사용방법은 어렵지 않다.

## 8. Ignoring Markdown formatting
마크다운 양식을 무시할 수도 있습니다. 깃허브만의 방식을 사용하기 위해 escape할 때 사용하는 (\)를 활용하여 마크다운 포맷을 무시합니다.
