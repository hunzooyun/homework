# HTML에 대해 정리

## 정리

### 인코딩 선언 방식

1. HTML4.01, xhtml1.0에서 문자 인코딩을 선언하는 방식

```
<meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />
```

2. html5에서 문자 인코딩을 선언하는 방식(기존 방식에 비해 간소화 됨)

```
<meta charset="UTF-8" />
```

### head에 추가할 수 있는 조합

1. 디자인 상 존재하지 않지만 콘텐츠 구조상 필요해서 추가한 숨김 처리 가능

```
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
  }
```

속성으로 class="sr-only"를 추가 할 수 있음

2.  svg-img 클래스가 적용된 이미지 요소의 가로 크기를 50px로 지정하기 위한 CSS 선언

```
.svg-img {
 width: 50px;
 }
```

### 이미지 삽입방법

#### 1. 상대경로

```
  <img
    src="./../assets/food/icecream.webp"
    alt="벤앤제리스 파인트 아이스크림 6종"/>
```

#### 2. 절대경로

```
<img
  src="/src/assets/food/icecream.webp"
  alt="벤앤제리스 파인트 아이스크림 6종"/>
```

#### 3. 벡터 이미지(img요소)

```
<img
  class="svg-img"
  src="./../assets/svg/chitchat.svg"
  role="img"
  alt="메세지"
  />
```

#### 4. 벡터 이미지 (svg요소)

```
<svg
  class="svg-img"
  viewBox="0 0 40 40"
  xmlns="http://www.w3.org/2000/svg"
  aria-labelledby="message">
  <title id="message">메시지</title>
  <defs>
    <linearGradient x1="50%" y1="0%" x2="50%" y2="100%" id="a">
      <stop stop-color="#2397B3" offset="0%"></stop>
      <stop stop-color="#13577E" offset="100%"></stop>
    </linearGradient>
    <linearGradient x1="50%" y1="0%" x2="50%" y2="100%" id="b">
      <stop stop-color="#73DFF2" offset="0%"></stop>
      <stop stop-color="#47B1EB" offset="100%"></stop>
    </linearGradient>
  </defs>
  <g fill="none" fill-rule="evenodd">
    <path
      d="M28.872 22.096c.084.622.128 1.258.128 1.904 0 7.732-6.268 14-14 14-2.176 0-4.236-.496-6.073-1.382l-6.022 2.007c-1.564.521-3.051-.966-2.53-2.53l2.007-6.022A13.944 13.944 0 0 1 1 24c0-7.331 5.635-13.346 12.81-13.95A9.967 9.967 0 0 0 13 14c0 5.523 4.477 10 10 10a9.955 9.955 0 0 0 5.872-1.904z"
      fill="url(#a)"
      transform="translate(1 1)"
    ></path>
    <path
     d="M35.618 20.073l2.007 6.022c.521 1.564-.966 3.051-2.53 2.53l-6.022-2.007A13.944 13.944 0 0 1 23 28c-7.732 0-14-6.268-14-14S15.268 0 23 0s14 6.268 14 14c0 2.176-.496 4.236-1.382 6.073z"
      fill="url(#b)"
      transform="translate(1 1)"
    ></path>
    <path
      d="M18 17a2 2 0 1 0 0-4 2 2 0 0 0 0 4zM24 17a2 2 0 1 0 0-4 2 2 0 0 0 0 4zM30 17a2 2 0 1 0 0-4 2 2 0 0 0 0 4z"
      fill="#FFF"
    ></path>
  </g>
</svg>
```

#### 5. 피규어 요소(캡션으로 마크업)

```
<figure>
  <img src="./../assets/drama/culinary-class-wars-wide.jpg" alt="" />
  <figcaption>흑백요리사</figcaption>
</figure>
```

#### 6. Lazy Loading(이미지 지연로딩 시키기)

```
<img
  src="./../assets/drama/mon-friend-son-narrow.webp"
  alt="엄마친구아들"
  loading="lazy"
  width="284"
height="398"
/>
```
