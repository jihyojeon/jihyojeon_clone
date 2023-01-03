
```css
@media mediaqueries { /* style rules  */ }
```

**미디어 타입**
-   all, braille, embossed, handheld, print, projection, screen, speech, tty, tv

**미디어 특성**
-   width, height, device-width, device-height, orientation, aspect-ratio, device-aspect-ratio, color, color-index, monochrome, resolution, scan, grid  
width는 뷰포트의 너비, 즉 브라우저 창의 너비를 말합니다.(스크린의 크기 x)
orientation은 미디어가 세로모드인지 가로모드인지를 구분합니다.

**미디어 쿼리 Syntax**
```css
media_query_list
 : S* [media_query [ ',' S* media_query ]* ]?
 ;
media_query
 : [ONLY | NOT]? S* media_type S* [ AND S* expression ]*
 | expression [ AND S* expression ]*
 ;
expression
 : '(' S* media_feature S* [ ':' S* expr ]? ')' S*
 ;
```

-   **[ a ]** : a가 나올 수도 있고 나오지 않을 수도 있습니다.
-   **a | b** : a 또는 b 둘 중에 하나를 선택합니다.  
-   **a?** :  a가 0번 나오거나 1번만 나올 수 있음
-   **a*** : a가 0번 나오거나 그 이상 계속 나올 수 있음
-   **_media_type_** : all, screen, print 등 명세에 정의된 미디어 타입
-   _**media_feature**_ : width, orientation 등 명세에 정의된 미디어 특성

**예제 코드**  

위에서 정의한 Syntax 따라 유효한 미디어 쿼리 예제 코드를 살펴보고 어떻게 해석이 되는지 같이 봅니다.

