# 프론트 앤드 개발

## 클라이언트-서버 시스템(모델)

> 클라이언트-서버 시스템은 복잡한 네트워크 연결중 양 끝단에 연결된 사용자와 공급자의 관계를 의미한다
> 
> 클라이언트 : 사용자가 사용하는 디바이스 또는 디바이스에서 실행되는 어플리케이션
> 
> ex) 웹브라우저
> 
> 서버 : 데이터, 네트워크 서비스가 공급되는 디바이스 또는 디바이스에서 실행되는 서버소프트웨어
> 
> ex) 아파치 서버

## HTML 기본 개념

> HTML - hyper Text Markup Language
> 
> 웹페이지에 구성 요소를 표시하는 언어
> 
> 구성요소 : 콘텐츠, 구조

## HTML 기본구조

`(이름 : backtick)

```
<!DOCTYPE html>
<html>
  <head></head>
  <body></body>
</html>
```

- DOCTYPE : html문서 타입
- html : html 영역 표시
- head : 해당 웹페이지의 부연설명, 부가정보가 포함
- body : 웹페이지의 콘텐츠를 표시하는 영역

## html 요소 기본 개념

### 요소 문법

```
<starttag>contents</endtag>
<시작태그>내용</종료태그>
```

### 포함관계

> 요소의 영역안에 다른 요소를 포함하는 관계
> 
> 직계 포함하는 요소 : 부모(parent)요소
> 
> 직계 포함되는 요소 : 자식(child)요소
> 
> 직계가 아닌 포함하는 요소 : 조상(ancestor)요소
> 
> 직계가 아닌 포함되는 요소 : 자손(descendant)요소

### Empty element(빈 요소)

> 시작태그만 있고 종료 태그가 없는 요소


### HTML 속성(Attribute)

> html element에 대해 추가정보(이동경로, 파일명...)을 제공
> 
> 시작태그에 입력
> 
> 형식 : 속성이름 = "속성값"

### HTML로 표현할 수 있는 콘텐츠(웹페이지에서 표현할 수 있는 콘텐츠)

> 텍스트 콘텐츠
> 
> 멀티미디어 콘텐츠
>  - 이미지
>  - 비디오
>  - 오디오
> 
### 제목 요소(Heading Element)
> h1~h6(h : heading)

### 단락 요소(Paragraph Element)
> p : Paragraph

> hr : horizontal riles
>   - 단락을 구분하는 수평선 표시 
>   - 빈요소

> br : Line Break
>   - 같은 단락 안에서 강제 줄바꿈
>   - 빈요소

### 하이퍼링크 요소(Hyper Link Element)
> a : anchor

```
<a href="url">링크텍스트</a>
ex) <a href="http://www.naver.com">네이버</a>
```

> href : hyper tect reference - 이동하고자 하는 목적의 위치/경로를 표시하는 속성
> - url(Uniform Resource locator) : 이동하고자 하는 목적지의 위치/경로 값

### 목록 요소(List Element)
> 순서있는/없는 목록
  
  >ol(Ordered List), ul(Unordered List), li(List Item)
  >
> 설명목록

주제와 설명이 한 세트로 구성되는 목속
 >dl(Description List), dt(Description Term), dd(Description Data)

### Table Element (https://www.tablesgenerator.com/html_tables)
> table, thead, tbody, tfoot, tr, th, td, caption

```
<table>
  <caption></caption>
  <thead>
    <tr>
      <th></th>
    </tr>
  </thead>
  <tbody>
      <tr>
      <td></td>
    </tr>
  </tbody>
  <tfoot>
      <tr>
      <td></td>
    </tr>
  </tfoot>
</tavle>
```

> table : table의 영역을 설정
> 
> thead, tbody, tfoot : table 데이터의 그룹을 표시
> 
> tr(table row) : 행
> 
> th(table head) : 제목 칸(셀)
> 
> td(table data) : 데이터 칸(셀)
> 
> caption : 테이블의 제목, 설명

###Image element
 > img
 > attribute : src(source), alt(alternative)

```
<img src="imge.jpg" alt= image>
```

>img 태그를 사용할 때 src, alt 속성은 반드시 사용해야 함 
>
### Video element
> <vldeo></video>
> attrubute
> - controls : 비디오 컨트롤바 표시
> - loop : 반복재생
> - muted : 음소거
> - aytoplay : 자동재생 ( muted와 같이 사용 )

### 절대경로/상대경로 (File Paths)

> 절대경로 : 콘텐츠 파일을 불러오고자 하는 HTML 페이지가 어떤 위치에 있던 동일하게 찾아올 수 있도록 자세하게 표시하는 경로
>
> 상대경로 : 콘텐츠 파일을 불러오고자 하는 HTML 페이지의 위치를 기준으로 콘텐츠 파일의 위치를 표시하는 경로

```
ex)

절대경로 : <img src="https://w3schools.com/imges/picture.jpg">

상대경로 : <img src="imges/picture.jpg>

상대경로(상위폴더로) : <img src="../imges/picture.jpg">

root(시작점) 상대경로 : <img src="/images/picture.jpg">
```


### Block/Inline Element

> 화면에 표시되는 형태의 기준으로 구분하는 방식
>
> Block Element 
> 
> - 화면에 줄바꿈 되어 표시되는 요소
> 
> - 사용 가능한 전체 너비를 항상 사용함
>
> Inline Element
> 
> - 화면에 줄바꿈 되지 않고 나란히 표시되는 요소
> 
> - 요소에 포함된 콘텐츠가 필요한 만큼만 사용함
>
> div(division)
> - 단순 영역 구분 요소

### 폼 요소

> input, button

```
<input type="text">

<input type="password">

<input type="button" value="이름"> 일반버튼
<input type="submit" value="이름"> 전송
<input type="reset" value="이름">  내용취소

<button type="button">이름</button>
<button type="submit">이름</button>
<button type="reset">이름</button>
```

###인터넷 주소체계

> IP address : 192.168.0.1
>
> Domain address : http://naver.com
>
> - 기본주소(IP) => 의미있는 영어단어로 변환 : 도메인 주소
>
> www.naver.com/inages/picture.jpg => URL
