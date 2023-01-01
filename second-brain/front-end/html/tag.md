https://developer.mozilla.org/en-US/docs/Web/HTML/Element

**Heading `<h1>`**
: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements
**Paragraph`<p>`**
**Linebreak `<br>`**
**Text**
-   `<b>` : bold 태그는 글자를 굵게 표현하는 태그입니다.
-   `<i>` : italic 태그는 글자를 기울여서 표현하는 태그입니다.  
-   `<u>` : underline 태그는 글자의 밑줄을 표현하는 태그입니다.
-   `<s>` : strike 태그는 글자의 중간선을 표현하는 태그입니다. (예전에 존재했던 strike 태그와는 다른 태그로, strike 태그는 폐기되어 더는 사용할 수 없습니다.)

**`<a>`**
`<a>`(anchor 태그)는 a태그, 앵커, 링크 등 여러 이름으로 불립니다.
https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a

```markup
<a href="http://www.naver.com/" target="_blank">네이버</a>
```

**href 속성**
링크를 만들기 위해 `<a>`는 반드시 href(hypertext reference) 속성을 가지고 있어야 합니다.
href 속성의 값은 링크의 목적지가 되는 URL입니다.

**target 속성**
target 속성은 링크된 리소스를 어디에 표시할지를 나타내는 속성입니다.

- 속성값으로는 `_self`, `_blank`, `_parent`, `_top`이 있습니다.
- `_self`: 현재 화면에 표시한다는 의미로, target 속성이 선언되지 않으면 기본적으로 self와 같이 동작합니다.
- `_blank`: 새로운 창에 표시한다는 의미로 외부 페이지가 나타나게끔 하는 속성입니다.
- `_parent`와 `_top`은 프레임이라는 특정 조건에서만 동작하는 속성으로, 최근에는 프레임을 잘 쓰지 않기 때문에 따로 다루지 않고 넘어가겠습니다.

**내부링크**
: # 이용
```markup
<a href="#some-element-id">회사 소개로 이동하기</a>
```

**의미없이 요소를 묶기 위한**
`<div>` & `<span>`

**리스트**
`<ul>`
`<ol>`
`<dl>`
```markup
<dl>
    <dt>리플리 증후군</dt>
    <dd>허구의 세계를 진실이라 믿고 거짓된 말과 행동을 상습적으로 반복하는 반사회적 성격장애를 뜻하는 용어</dd>
    <dt>피그말리온 효과</dt>
    <dd>타인의 기대나 관심으로 인하여 능률이 오르거나 결과가 좋아지는 현상</dd>
    <dt>언더독 효과</dt>
    <dd>사람들이 약자라고 믿는 주체를 응원하게 되는 현상</dd>
</dl>
```

**img**

`<img>`는 문서에 이미지를 삽입하는 태그로, 닫는 태그가 없는 빈 태그 입니다.
```markup
<img src="./images/pizza.png" alt="피자">
```

- **src 속성**
`<img>`의 필수 속성으로 이미지의 경로를 나타내는 속성입니다.
- **alt 속성**
이미지의 대체 텍스트를 나타내는 속성입니다.
대체 텍스트는 이미지를 대체하는 글을 뜻하며, 웹 접근성 측면에서 중요한 속성입니다.
src 속성과 더불어 반드시 들어가야 하는 속성입니다.
- **width/height 속성**
둘 중 하나만 선언하면 나머지 한 속성은 선언한 속성의 크기에 맞춰 자동으로 비율에 맞게 변경됩니다.
반면 두 속성 모두 선언하면 이미지는 비율과 무관하게 선언한 크기대로 변경됩니다.

**Table**
-   `<table>` : 표를 나타내는 태그
-   `<tr> `: 행을 나타내는 태그
-   `<th>` : 제목 셀을 나타내는 태그
-   `<td>` : 셀을 나타내는 태그
-   `<caption>`: 표의 제목을 나타내는 태그
-   `<thead>`: 제목 행을 그룹화하는 태그
-   `<tfoot>`: 바닥 행을 그룹화하는 태그  
-   `<tbody>`: 본문 행을 그룹화하는 태그
```markup
<table> 
    <caption>Monthly Savings</caption>
    <thead>
        <tr>
            <th>Month</th>
             <th>Savings</th>
        </tr>
    </thead>
    <tbody>
        <tr>
             <td>January</td>
            <td>$100</td>
        </tr>
        <tr>
             <td>February</td>
            <td>$80</td>
        </tr> 
    </tbody>
    <tfoot>
        <tr>
             <td>Sum</td>
            <td>$180</td>
        </tr>
    </tfoot>
 </table>
```

<table> 
    <caption>Monthly Savings</caption>
    <thead>
        <tr>
            <th>Month</th>
             <th>Savings</th>
        </tr>
    </thead>
    <tbody>
        <tr>
             <td>January</td>
            <td>$100</td>
        </tr>
        <tr>
             <td>February</td>
            <td>$80</td>
        </tr> 
    </tbody>
    <tfoot>
        <tr>
             <td>Sum</td>
            <td>$180</td>
        </tr>
    </tfoot>
 </table>


- 셀 병합 = rowspan, colspan 속성을 사용하면 됨
- https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table

**Form Element**
- type="text"
```markup
<input type="text" placeholder="ㅇㅇㅇ">
```
주로 아이디, 이름, 주소, 전화번호 등 단순한 텍스트를 입력할 때 사용합니다.
type="text"에는 placeholder 속성이 존재합니다.
placeholder 속성은 사용자가 입력하기 전 미리 화면에 노출하는 값으로, 입력하는 값의 양식을 표현할 수 있습니다. 
- type="password"
```markup
<input type="password">
```
암호와 같이 공개할 수 없는 내용을 입력할 때 사용합니다.
화면에는 type="text"와 같게 나타나지만 실제로 입력할 때 값을 노출하지 않습니다.
- type="radio"
```markup
<input type="radio" name="gender"> 남자
<input type="radio" name="gender"> 여자
```
라디오 버튼을 만들 때 사용합니다.
라디오 버튼은 중복 선택이 불가능하며 하나의 항목만을 선택해야 합니다.
- type="checkbox"
```markup
<input type="checkbox" name="hobby"> 등산
<input type="checkbox" name="hobby"> 독서
<input type="checkbox" name="hobby"> 운동
```
체크박스를 만들 때 사용합니다.
체크박스는 중복 선택이 가능합니다.
- type="file"
```markup
<input type="file">
```
파일을 서버에 올릴 때 사용합니다.
브라우저에 따라 표현되는 형태는 조금씩 다르지만, 모두 같은 역할을 합니다.
- type="submit|reset|image|button"
```markup
<form action="./test.html">
    메시지: <input type="text" name="message"><br>
    <input type="submit">
    <input type="reset">
    <input type="image" src="http://placehold.it/50x50?text=click" alt="click" width="50" height="50">
    <input type="button" value="버튼">
</form>
```
submit, reset, image, button 타입은 모두 클릭 가능한 버튼을 만듭니다.
-   submit : form의 값을 전송하는 버튼
-   reset : form의 값을 초기화하는 버튼
-   image : 이미지를 삽입할 수 있는 버튼 (submit과 동작이 동일함)
-   button : 아무 기능이 없는 버튼

**`<select>`**
`<select>`는 선택 목록 상자 또는 콤보박스라고도 합니다.
몇 개의 선택지를 리스트 형태로 노출하고 그중 하나를 선택할 수 있게 하는 태그입니다. (multiple 속성을 사용하면 다중 선택도 가능합니다.)
```markup
<select>
    <option>서울</option>
    <option>경기</option>
    <option>강원</option>
    ...
</select>
```
`<select>`내부의 `<option>`으로 각 항목을 나타냅니다.
`<option>`의 속성으로는 selected가 있으며 이는 선택된 항목을 의미합니다.

**`<textarea>`**
한 줄만을 입력할 수 있는 `<input type="text" >`와 달리 여러 줄의 텍스트를 입력할 때 사용합니다.
```markup
<textarea rows="5" cols="30">
    ...
</textarea>
```
`<textarea>`에는 텍스트 상자의 크기를 조절하는 rows, cols 속성이 있습니다.
-   cols : 가로 크기를 조절하는 속성(한 줄에 들어가는 글자의 수, 수치의 의미는 평균적인 글자의 너비로 정확히 글자 수를 나타내지는 않습니다.)
-   rows : 세로 크기를 조절하는 속성(화면에 보여지는 줄 수)

**`<button>`**
버튼을 만들 때 사용하며 submit, reset, button 3가지의 타입이 있습니다.

```markup
<button type="submit|reset|button">ㅇㅇㅇ</button>
```

각 버튼은 이전에 배웠던 input 타입의 submit, reset, button과 모두 같은 기능을 가진 버튼입니다.
다만, 빈 태그가 아니며 내용을 안에 직접 넣을 수 있으므로 좀 더 자유로운 스타일 표현이 가능합니다.

**`<label>`** : 웹 접근성 향상
`<label>`은 form 요소의 이름과 form 요소를 명시적으로 연결시켜주기 위해 사용합니다.
모든 form 요소에 사용할 수 있습니다.

```markup
<label for="name">이름</label>: <input type="text" id="name"><br>
<label for="nickname">이름</label>: <input type="text" id="nickname"><br>
<label for="address">이름</label>: <input type="text" id="address"><br>
```

form 요소의 id 속성값과 `<label>`의 for 속성값을 같게 적어주어야 합니다.
`<label>`을 사용하면 이를 클릭했을 경우 해당 form 요소를 클릭한 것처럼 동작합니다.
또한, 스크린 리더기를 통해 듣게 되면 해당 form 요소에 접근 시 `<label>`을 함께 읽어주게 됩니다.
`<label>`은 사용성, 접근성적인 측면으로 중요한 역할을 하므로 반드시 써주는 것이 좋습니다.

**`<fieldset>`, `<legend>`**

`<fieldset>`, `<legend>`는 form 요소를 구조화 하기 위해 필요한 태그입니다.
-   `<fieldset>` : 여러 개의 폼 요소를 그룹화하여 구조적으로 만들기 위해 사용
-   `<legend>` : 폼 요소의 제목으로 `<fieldset>` 내부에 작성
`<fieldset>`은 보통 form의 성격에 따라 구분합니다.
`<legend>`는 `<fieldset>`의 자식으로 반드시 최상단에 위치해야 합니다.

```markup
<fieldset>
    <legend>기본 정보</legend>
    ... 폼 요소들 ...
</fieldset>
<fieldset>
    <legend>부가 정보</legend>
    ... 폼 요소들 ...
</fieldset>
```

<fieldset>
    <legend>기본 정보</legend>
    ... 폼 요소들 ...
</fieldset>
<fieldset>
    <legend>부가 정보</legend>
    ... 폼 요소들 ...
</fieldset>

```markup
<form action="" method="">
    <fieldset>
        <legend>기본 정보</legend>
        ... 폼 요소들 ...
    </fieldset>
    <fieldset>
        <legend>부가 정보</legend>
        ... 폼 요소들 ...
    </fieldset>
</form>
```

<form action="" method="">
    <fieldset>
        <legend>기본 정보</legend>
        ... 폼 요소들 ...
    </fieldset>
    <fieldset>
        <legend>부가 정보</legend>
        ... 폼 요소들 ...
    </fieldset>
</form>

`<form>`에는 대표적인 2가지 속성이 있습니다.
-   action: 데이터를 처리하기 위한 서버의 주소
-   method: 데이터를 전송하는 방식을 지정
method 속성값에는 get/post 2가지 방식이 존재합니다.
get 방식은 데이터가 전송될 때 주소창에 파라미터 형태로 붙어 데이터가 노출됩니다.
반면, post 방식은 데이터가 전송될 때 데이터가 노출되지 않습니다.

https://developer.mozilla.org/en-US/docs/Web/HTML/Element#forms