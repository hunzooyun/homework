# 3주차 과제

## 제출 자료 링크

[login](./../login/login.html)  
[login](./../login/styles/login.css)

### 과제 조건

#### 마크업

```
- 로고 이미지는 <svg> 요소로 마크업 할 것
- 웹접근성을 고려하여 로그인 폼 서식을 마크업 할 것
    (레이블 제공의 경우 WAI-ARIA가 아닌 HTML 네이티브 방식으로 구현)
- 아이디와 비밀번호는 필수 입력 서식임을 알 수 있도록 구현할 것
- IP 보안 텍스트 클릭 시 미리 제공 된 `pages/ip_secruity.html` 파일이 새창에 열리도록 구현할 것
- 로그인 상태 유지와 IP 보안 ON/OFF UI는 마우스 이외에 `키보드로도 조작 가능`하도록 구현할 것
```

위 조건을 달성하기 위해 svg요소부터 저장을 따로 해서 assets 파일에 넣어두는 작업부터 하였습니다.  
아이디와 비밀번호는 필수입력하게 하기 위하여 required를 사용하여 입력 안 할 시 경고문이 나오게 해두었습니다.

#### `스타일링`

```
- 미디어 쿼리를 사용하여 반응형으로 구현할 것(768px 미만 모바일 / 768px 이상 데스크탑)
- 모바일 퍼스트로 스타일링 할 것
(공통 스타일과 모바일 스타일을 먼저 구현한 후 데스크탑 스타일을 재정의)
```

이것을 하기 위해 마지막에 @media를 추가하여 768px 이상은 데스크탑 모델로 나올 수 있게 설정하였습니다.

```
- 글자 크기 및 여백(margin 및 padding)은 모두 rem 단위로 설정할 것
- 기본 글자 크기는 `16px,` 기본 글자 색상은 `#121212`로 사용할 것
(Custom Properties 활용 추천)
```

전체 요소를 통해 선언해두었습니다.

```
- 로고
    가로 230px, 가운데 배치
```

로고 또한 svg 요소로 주어졌기 때문에 링크를 걸고 배치하였습니다.

```
- 포커스 스타일을 기본 색상이 아닌 커스텀 스타일로 변경할 것(색상 `#24388d`)
- 모바일 로그인 폼 로그인 폼의 가로 크기는 `100%`(좌/우 여백 각 20px 포함)로 설정할 것
- 모바일 환경에서 IP 보안 ON/OFF 스위치 UI는 사용자에게 제공되지 않도록 구현할 것
- 데스크탑 로그인 폼의 가로 크기는 500px(좌/우 여백 각 20px 포함)로 설정할 것
- 입력 서식 글자크기 및 세로 크기, 테두리 선 색상, 배경 색상은 다음과 같이 지정할 것
    `기본 상태` : 14px, 45px, #dadada, #fff
    `포커스 상태` : #03cf5d, #e9f0fd

- `로그인 버튼`의 글자 크기, 세로 크기, 글자 색상, 배경색상, 위쪽 여백은 다음과 같이 지정할 것
    16px, 45px, #fff, #03cf5d, 20px

- 로그인 상태 유지 및 IP 보안 ON/OFF `스위치 UI` 영역의 위쪽 여백은 10px로 지정할 것
- 로그인 상태유지 체크박스 배경 이미지 및 크기와 여백은 다음과 같이 지정할 것
    `선택안함` : unchecked.svg (제공한 <svg> 코드를 활용하여 이미지로 저장하여 사용)
    `선택함` : checked.svg (제공한 <svg> 코드를 활용하여 이미지로 저장하여 사용)
    가로 * 세로 : 24px * 24px
    배경 이미지 오른쪽 여백 : 5px

- `IP 보안` 스위치의 글자 크기는 16px, 글자 색상은 #121212로 지정할 것
```

자주 사용할 거 같은 단위는 따로 변수 처리 해두었습니다.  
IP 보안 UI는 모바일에서 제공 되지 않도록 하기 위해 @media를 통해서 676이하에선 보이지 않도록 제공하였습니다.

### 과정

처음 과제를 받았을때 Figma에 비슷한 예제가 있다는걸 알고 먼저 그걸로 마크업 준비를 시작하였습니다.  
[마크업](./../assets/login/모바일.png)  
상세한 마크업은 하지 못하였지만 대략적인 방향을 잡고 html 문서를 작성해나갔습니다.  
기존에 배우면서 저장해두었던 문서들을 참고해가면서 마크업을 어느정도 해두고 CSS를 작성하였습니다.  
위의 조건들을 만족시키기 위해 처음부터 전역으로 설정해두고 위에서부터 차례대로 스타일링을 하였습니다.

### 문제점

제일 헤맨 곳은 체크박스를 만들어내는 방법이였습니다.  
2개를 어떻게 바꿔가면서 할까 하다가 [custom checkbox](https://velog.io/@florence_y/TIL-Custom-checkbox) 글을 통해 기존 체크박스를 크기를 작게 만들고 대신 svg 요소를 넣어서 체크박스형식으로 만들 수 있었습니다.  
2번째로 헤맸던 곳은 만들고 실행해보니 로그인 유지 박스와 IP 보안 박스가 왼쪽에 같이 붙어있는데 아무리 해봐도 이동이 안되던거였습니다.  
그걸 위해 form 내부 span요소에 flex를 주고 ip 보안에 flexbox를 줘서 margin을 왼쪽에서 auto를 줌으로서 오른쪽으로 붙일 수 있었습니다.

### 마무리

글을 쓰는게 제일 힘들다 보니 두서없이 쓴거 같지만 그동안 배운 과정들을 조합하여서 대부분 할 수 있었다는게 좋았습니다. 계속 배우겠지만 이전 내용도 안 까먹고 잘 유지할 수 있게 철저히 복습을 해야되겠다는 결론이 내려졌습니다.
