# css-good-skill
1. color-mix - 혼합색상 만들기  
ex) 레드 블루 50% 혼합
```
.container {
backgrountd-color: color-mix(red 30%, blue 70%); 
}
```
ex) 브랜드 색상으로 색상 도출하는데 매우 유용
```
:root {
 --brandColor: blue;
}
.container {
 background-color: color-mix(var(--brandColor) 50%, white 10%);
 }
 ```
 2. accent-color - 커스터마이징이 어려웠던 HTML 요소의 색상 변경 가능 ex(Radio 버튼, 체크 박스, 진행 표시줄, 범위 슬라이더)
 ex)
 ```
 <style>
  :root {
   accent-color: blue;
   }
   </style>
</head>
<body>
<input type= "checkbox" checked />
<input type= "radio" checked />
<input type= "range" />
<progress max="100" value="50"> 50%</progress>
```
3. color-contrast() - 색 대비로 글씨가 잘 보이도록 함
ex) 
```
.box {
 background-color: red;
 color: color-contrast(red);
 }
 ```
 ex) 검정, 흰이 아닌 옵션을 선택 가능
 ```
 color: color-contrast(blue vs pink, yellow, green);
 ```
 4.inert - 페이지의 섹션을 고정 할 수 있다\
 ex)
 ```
 <form inert>
  <input type="..." />
  <button>Save</button>
 </form>
 ```
 5. :has() - 부모 요소에 특정 자식이 있는지 여부에 따라 부모 요소의 스타일이 가능
 ex)
 ```
 form:has(button) {
 }
 ```
 ex) 목록 항목에 스타일 추가 가능
 ```
 li:has(a) {
 }
 ```
 ex) 이미지 주변에 있는 링크의 모양을 변경 할 수 있음
 ```
 a:has(> img) {
 }
 ```
 6. Viewport Units - 웹 사이트를 볼 수 있는 영역 또는 윈도우  
* lvh : 가장 큰 viewport 높이 
* svh : 가장 작은 viewport 높이 
* dvh : 동적 viewport 높이 
 7. @nest
 ex) 동일한 결과
 ```
 nav { 
  ...;
 }
 nav ul {
  ...;
 }
 nav ul li {
  ...;
 }
 ```
 ```
 nav {
  & ul {
   & li {
   }
  }
 }
 ```
ex) &기호 플레이스 홀더
```
.foo {  
color: red:  
@nest : not(&) {  
 color: blue;  
 }
}
```
```
.foo {  
 color: red;  
 }  
 :not(.foo) {  
  color: blue;  
 }
```
