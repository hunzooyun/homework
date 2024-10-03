# html에 대해 정리글 2번째

## 정리(anchor, list, , blockquote)

### anchor(하이퍼링크)

#### 1. Framement 식별자 방식으로 name 속성으로 위치 지정하기

```
<a name="start"></a>
<h1 id="heading">하이퍼링크 요소</h1>
```

---

#### 2. 웹사이트(URL)로 하이퍼링크 : 절대경로

```
<p>
  <a href="https://likelion.net/school">테킷 프론트엔드 스쿨(부트캠프)</a>
</p>
```

---

#### 3. target 속성의 값으로 \_blank를 지정하면 새창, 새탭에 링크 결과 보기

```
<a href="https://github.com/hunzooyun" target="_blank">
<p>윤헌주의 Github</p></a>
```

target 속성의 값으로 \_blank로 설정할때는 rel 속성의 값으로 noopener noreferrer를 지정해야 함.  
**noopener**: 열린 페이지가 기존페이지로 접근 못하게 막음
**noreferrer**: 새로 열리는 링크가 정보 전달 못하게 막음

```
<a href="https://www.naver.com/" target="_blank" title="네이버로 이동합니다" rel="noopener noreferrer">네이버</a>
<a href="https://www.daum.net/" target="_blank" title="다음으로 이동합니다" rel="noopener noreferrer">다음</a>
```

---

#### 4. a 안에 a가 들어갈 수 없음(문법 오류의 예시)

```
<p>
<a href="https://github.com/hunzooyun/homework">과제 저장소 - <a href="https://github.com/hunzooyun/homework/blob/main/about-me.md">자기소개</a></a>
```

---

#### 5. 이미지 링크

```
<a href="https://likelion.net/school"><img src="./../assets/icon/plus-on.svg" alt="테킷 스쿨 더보기" /> </a>
```

---

#### 6. 로컬 파일로 링크:상대경로(GitHub에선 절대경로 불가)

```
<a href="./../../index.html">처음으로</a>
```

---

#### 7. 파일 다운로드 링크

```
<a href="./../assets/pdf/search-engine-optimization-starter-guide.pdf" download="search-engine-optimization-starter-guide.pdf">구글 SEO 가이드</a>
```

---

#### 8. 전화번호, 이메일 주소 하이퍼 링크

```
<a href="mailto:gjswn7@naver.com?subject=문의사항">윤헌주 이메일</a>
<a href="tel:+820223456789">고객센터</a>
```

---

#### 9. name, id 위치로 이동

```
<a href="#start">맨위로</a>
<a href="#heading">맨위로</a>
```

### list

#### 1. unordered list

순서 상관 없이 독립된 아이템을 포장하는 목록
ul과 li로만 구성됨

```
<ul>
  <li>카페W 만의 특별함을 경험할 수 있는 최상의 선택 음료</li>
  <li>카페W 커피와 완벽한 어울림을 자랑하는 푸드</li>
  <li>사용한 시도와 디자인으로 가치를 더하는 상품</li>
  <li>소중한 사람에게 마음을 전하는 가장 좋은 방법</li>
</ul>
```

---

#### 2. ordered list

순서가 중요한 독립된 아이템을 포장하는 목록
ol과 li로만 구성됨

```
<ol>
  <li>UI 구조 &amp; 디자인</li>
  <li>모바일 웹 UI 제작 실습</li>
  <li>UI 인터렉션 주니어</li>
  <li>React 프로그래밍</li>
</ol>
```

---

#### 3. definition list

용어와 그 설명을 구성할 때 정의형 목록을 사용할 수 있음
**dl**:정의형 목록의 컨테이너 역할  
**dt**:정의할 용어  
**dd**:해당 용어의 정의나 설명
dt 하나에 여러개의 dd가 들어 갈 수 있음.
dt와 dd의 셋트를 구별하기위해 div로 감쌀 수도 있음

---

### 인용문과 줄바꿈

**blockquote** : 인용문 컨테이너 박스 역할  
**br**: 강제 줄바꿈  
**hr**: 수평줄 그으면서 줄바꿈  
**cite**: 인용문 출처

```
<blockquote>
  <p>
  우리가 할 수 있는 노력은 과정이 전부야.
  <br />
  결과는 우리 손 안에 있는 게 아니야.
  </p>
  <cite>드라마 &lt;미생&gt; 중에서</cite>
</blockquote>
```
