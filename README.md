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
 
