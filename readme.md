# local font 확인

[MDN font-face 문서에 따르면](https://developer.mozilla.org/ko/docs/Web/CSS/@font-face)

> 아래 예제에서는 로컬에 설치된 "Helvetica Neue Bold" 폰트가 사용된다. 만약 해당 폰트가 설치되어 있지 않다면(다른 2개의 폰트를 적용하기 위한 시도를 하고), 다운로드 가능한 "MgOpenModernaBold.ttf" 폰트가 대신 사용된다.

```css
@font-face {
  font-family: MyHelvetica;
  src: local("Helvetica Neue Bold"), local("HelveticaNeue-Bold"),
    url(MgOpenModernaBold.ttf);
  font-weight: bold;
}
```

라고 선언한 순서에 대해 우선순위를 부여한다고 쓰여져있지만, `with-url.html`을 실행해보면 url이 뒤에 있어도 우선하여 실행되는 것을 볼 수 있다.
