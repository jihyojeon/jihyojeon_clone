
**뷰포트 설정**

뷰포트를 설정하는 태그는 <meta> 태그로 <head> 태그에 위치해야 합니다.
name 속성에 "viewport"라고 선언하며 content 속성에 뷰포트를 설정하는 내용이 들어갑니다. 

```
<meta name="viewport" content=" 뷰포트의 설정 값" >
```

content에는 몇 가지 설정을 할 수 있습니다.
-   width(height) : 뷰포트의 가로(세로) 크기를 지정합니다. px단위의 수치가 들어갈 수 있지만, 대부분 특수 키워드인 "device-width(height)"를 사용합니다.(뷰포트의 크기를 기기의 스크린 width(height) 크기로 설정한다는 의미입니다.)
-   initial-scale : 페이지가 처음 나타날 때 초기 줌 레벨 값을 설정합니다.(소수값)
-   user-scalable : 사용자의 확대/축소 기능을 설정할 수 있습니다.

대부분의 모바일 웹 사이트의 뷰포트 설정은 아래와 같습니다. 기타 다른 설정은 필요에 따라 하시면 됩니다.

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```