# css-good-skill
1. color-mix : 혼합색상 만들기  
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
 2. accent-color 커스터마이징이 어려웠던 HTML 요소의 색상 변경 가능 ex(Radio 버튼, 체크 박스, 진행 표시줄, 범위 슬라이더)
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
