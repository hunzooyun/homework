# Markdown에 대해 정리

## 1. 제목

대제목인 1은 1개까지만 사용 가능

    # 제목 1
    ## 제목 2
    ### 제목 3
    #### 제목 4
    ##### 제목 5
    ###### 제목 6

---

## 2. 폰트

```
*기울여 쓰기*
_기울여 쓰기_
__굵게 쓰기__
~~취소선~~
<u>밑줄</u>
<span style="color:red">빨간색</span>
<span style="color:#00FF00">Green</span>  (`#`을 넣은 뒤 16진수로 R, G, B 값을 입력해서 지정할 수 있다.)
<span style="color:rgb(0, 255, 0)">rgb(245, 235, 13)</span>
```

### 결과

_기울여 쓰기_  
_기울여 쓰기_  
**굵게 쓰기**  
~~취소선~~  
<u>밑줄</u>  
<span style="color:red">빨간색</span>  
<span style="color:#00FF00">Green</span> (`#`을 넣은 뒤 16진수로 R, G, B 값을 입력해서 지정할 수 있다.)  
<span style="color:rgb(0, 255, 0)">rgb(245, 235, 13)</span>

---

## 3. 목록

```
- 순서가 필요 없이 점으로 목록 생성 시
* -, *, + 기호가 사용 가능
  - 두 칸을 띄어쓰면
   + 서브 목록을 붙일 수 있음

1. 순서대로 번호를 붙일 경우
2. 앞에 숫자와 점을 붙인 뒤 한칸 띄기
    1. 서브목록에서도
    2. 가능

3. 숫자와 기호는
    - 섞어서
        + 사용 가능
```

### 결과

- 순서가 필요 없이 점으로 목록 생성 시

* -, \*, + 기호가 사용 가능
  - 두 칸을 띄어쓰면
  * 서브 목록을 붙일 수 있음

1. 순서대로 번호를 붙일 경우
2. 앞에 숫자와 점을 붙인 뒤 한칸 띄기

   1. 서브목록에서도
   2. 가능

3. 숫자와 기호는
   - 섞어서
     - 사용 가능

---

## 4. 인용문

```
>블럭 인용 문자를 사용할 수 있다.
>이것은 인용문이다. - 작성자
>>내부에 다시 한번 사용 가능하다. 이것은 이중 인용문이다. - 작성자
```

### 결과

> 블럭 인용 문자를 사용할 수 있다.  
> 이것은 인용문이다. - 작성자
>
> > 내부에 다시 한번 사용 가능하다. 이것은 이중 인용문이다. - 작성자

---

## 5. 코드 블럭

````
`인라인 코드 푠현 시`
`void function(){}`
~~~cpp
블럭으로 표현 시
void function(){}
~~~
```python
또는 물결로도 표시 가능
def function():
    pass
````

### 결과

`인라인 코드 푠현 시`  
`void function(){}`

```cpp
블럭으로 표현 시
void function(){}
```

```python
또는 물결로도 표시 가능
def function():
    pass
```

---

## 6. 수평선 넣기

`-` 또는 `*` 또는 `_` 기호를 3개 이상 작성하여 구현 가능

### 결과

---

---

---

---

## 7. 문단 나누기

```
문장 1
(빈 줄)
문장 2<br/><br/>
또는 마지막에
세 칸 이상 띄우기
```

### 결과

문장 1  
(빈 줄)  
문장 2<br/><br/>  
또는 마지막에  
세 칸 이상 띄우기

---

## 8. 링크

인라인 링크, url링크, 참조링크 기능을 활용해 웹페이지 주소, 이메일 주소를 추가할 수 있습니다.

사용법

```
인라인 - [title](link)
url링크: <URL/>
E-mail: <abc@abc.com>
```

예시

[google](https://www.google.com)  
<https://www.google.com/>

<email@abc.com>

---

## 9. 이미지 넣기

이미지 삽입  
사용법

1. 이미지만 삽입할 경우  
   ![이미지](이미지 링크)
2. 사이즈를 조절할 경우 - HTML 태그로 처리  
   <img src=이미지링크, width="450px" height="300px" title="크기변경">
3. 이미지 삽입 후 링크 걸기  
   [![이미지](링크)(연결할 링크)]

### 결과

![메이플스토리](./assets/md/image/메이플.png)  
<img src=./assets/md/image/메이플.png, width="450px" height="300px" title="크기변경">  
[![./assets/md/image/메이플.png](https://maplestory.nexon.com/Home/Main)(https://maplestory.nexon.com/Home/Main)]

---

## 10. 표 삽입

| 표        |    셀1     |        셀2 |
| :-------- | :--------: | ---------: |
| 왼쪽 정렬 | 가운데정렬 | 오른쪽정렬 |

---

## 11. 체크박스

`-`, `*`, `+` 뒤에 한칸 띄어쓴 후 `대괄호([,])`를 추가하면 체크박스 생성이 가능합니다. `대괄호([ ])`사이에 `x`를 넣으면 체크된 체크박스가 생성됩니다.

사용법

- [ ] 공부

* [x] 놀기
