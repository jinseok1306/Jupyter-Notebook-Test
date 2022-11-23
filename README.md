# Jupyter-Notebook-Test
Jupyter-Notebook 주요 기능을 테스트한 프로젝트이다.

## 기본 환경 세팅 방법
### 1. Jupyter Notebook이란?

Jupyter Notebook은 웹 브라우저상에서 Python 코드를 단계적으로 쉽게 실행하고, 시각적으로 빠르게 확인해 볼 수 있도록 해주는 프로그램이다. 이러한 방식은 탐색적 데이터 분석에 아주 적합하여 많은 데이터 분석가가 Jupyter Notebook을 사용하고 있다.

Jupyter Notebook의 장점은 셀 단위로 작성하여 실행할 수 있기에 큰 Python 파일도 셀 단위로 나누어 번역, 실행하면서 인터랙티브한 동작이 가능하다는 점이다.  또한 데이터 분석을 위한 Python 파일 작성 후 실행하였을 때 차트, 표 등의 결과값 출력도 바로 직관적으로 볼 수 있고, 이후 Github에 Jupyter Notebook의 결과 출력 방식 그대로 올릴 수 있다는 장점도 가지고 있다.  

<img src="/scan/Hello World.png"  width="800">  

### 2. Jupyter Notebook 설치

Jupyter Notebook을 설치하기 위해서는 Python을 설치해주어야 한다. Python을 설치하면 함께 설치되는 pip 패키지 매니저를 이용해서 설치를 진행한다.  

**1) [https://www.python.org/downloads/](https://www.python.org/downloads/) 접속 후 최신버전 Python다운로드**  

<img src="/scan/python 사이트.png"  width="800"> 

**2) Phthon 설치되었는지 확인**

터미널 창에서 py를 입력했을 때 아래와 같이 실행되는지 확인한다.  

<img src="/scan/python 설치 확인.png"  width="800"> 

**3) 터미널을 다시 열고 pip를 이용해서 설치**

설치 도중 오류가 발생한다면 관리자 권한으로 터미널을 실행하면 된다.

```powershell
pip3 install jupyter
```

4**) 설치 완료 후 jupyter 실행**

실행은 현재 터미널에 세팅된 경로를 기준으로 Jupyter Notebook이 실행된다.

```powershell
jupyter notebook
```  

<img src="/scan/jupyter 실행.png"  width="800">  

### 3. Jupyter의 기본 사용법

**1) 새 파일 생성**

New 클릭 후 원하는 옵션으로 파일 생성이 가능하다. 생성된 파일은 해당 경로에 추가된다.  

<img src="/scan/jupyter 새파일 생성.png"  width="800">  

<img src="/scan/jupyter 새파일 생성2.png"  width="800">  

**2) 편집 / 명령 모드**

편집 모드에서는 셀의 내용을 편집할 수 있고(셀의 테두리가 초록색), 명령 모드는 편집중이 아닌 상태 또는 세 자체에 조작을 가하는 상태(셀의 테두리가 파란색)이다. 명령 모드에서 편집 모드로 들어가려면 `Enter` 키를, 반대로는 `ESC` 키를 누르면 된다.  

<img src="/scan/편집,명령모드.png"  width="600">  

**3) 셀의 타입**

Code 타입, Markdown 타입이 있다. Code 타입은 일반 코드를 실행할 수 있는 셀이다. 기본적으로 셀을 생성하면 Code 타입으로 생성된다. Markdown 타입은 Markdown으로 셀의 내용을 작성할 수 있다.  코드를 코드로 실행되지는 않으며, 수식을 작성할 수 있다. 수식은 MathJax에 의해 지원된다. 

Markdown 타입으로 변경하면 Markdown 코드를 작성할 수 있다. `Shift + Enter` 키를 누르면 마크다운이 실제 보여지는 방식으로 변경되며, 다시 수정하려면 `Enter` 또는 더블 클릭하면 편집 가능하다.  

<img src="/scan/셀의 타입.png"  width="800">  

**4) 셀 실행**

실행하고 싶은 셀의 아무곳에나 커스를 위치시킨 후 `Shift + Enter` 키를 누른다. 실행하면 셀 아래쪽에는 실행 결과가 표시되고, 셀 옆의 ‘In[ ]’과 ‘Out[ ]’에 몇 번째로 실행시켰는지를 나타내는 숫지가 표시된다. 여러 번 실행하면 계속 숫자가 올라간다.  

<img src="/scan/셀 실행.png"  width="800">  

**5) 강제중단/재실행**

제목 아래 줄 탭에 Kernel 탭이 있다. 커널은 IPython 대화창 아래에서 백그라운드 비슷하게 실행되는 일종의 운영체제 같은 개념이다. IPython 대화창을 관리한다고 보면 된다.  

<img src="/scan/강제중단,재실행.png"  width="800">  

Kernel 탭의 모든 버튼은 코드를 삭제하지 않는다. 각 버튼의 기능은 다음과 같다.

- Interrupt : 실행중인 코드를 강제 중지한다. 중지하면 에러가 발생하며 실행이 중지된다.
- Restart : 실행중인 코드가 중지되며 재시작된다. 코드나 실행 결과는 삭제되지 않는다.
- Restart & Clear Output : 코드는 중지되며 실행 결과도 삭제한다.
- Restart & Run All : 재시작 후 모든 셀의 코드를 위에서부터 순차적으로 한 번씩 실행한다.
- Reconnect : 인터넷 연결이 끊어졌을 때 연결을 재시도한다.
- Shutdown : 커널을 종료한다. 이 버튼을 누르면 실행 결과는 삭제되지 않으나 완전 종료된 상태로 더 이상 메모리를 잡아먹지 않는다.  

**6) 주요 단축키**

공용 단축키

- `Shift + Enter` : 액티브 셀을 실행하고 아래 셀을 선택한다.
- `Ctrl + Enter` : 액티브 셀을 실행한다.
- `Alt + Enter` :  액티브 셀을 실행하고 아래에 셀을 하나 생성한다.

편집 모드 단축키

- `Ctrl + Z` : Undo 명령이다.
- `Ctrl + Shift + Z` : Redo 명령이다.
- `Tab` : 자동완성 또는 Indent를 추가한다.
- `Shift + Tab` : 툴팁 또는 변수의 상태를 표시한다.
- `Ctrl + Shift + -` : 커서의 위치에서 셀을 잘라 두 개로 만든다.

명령 모드 단축키

- `↑, ↓` :  셀 선택
- `A` :  액티브 코드 셀의 위에 셀을 하나 생성한다.
- `B` : 액티브 코드 셀의 아래에 셀을 하나 생성한다.
- `Ctrl + S` :  Notebook 파일을 저장한다.
- `Shift + L` :  줄 번호 표시를 토글한다.
- `D, D` : (D 두번 연속으로 타이핑) 액티브 코드 셀을 삭제한다.
- `Z` :  삭제한 셀을 하나 복원한다.
- `Y` :  액티브 코드 셀을 Code 타입(코드를 기술하는 타입)으로 한다.
- `M` :  액티브 코드 셀을 Markdown 타입으로 한다.
- `O, O` : 커널을 재시작한다.
- `P` :  명령 팔레트를 연다.
- `H` :  단축키 목록을 표시한다. `Enter` 키로 숨긴다.

### 4. Jupyter의 기능

**1) DocString의 표시**

선언한 변수 뒤에 `?`를 붙여서 셀을 실행하는 것으로 해당 변수의 상태를 확인할 수 있다. 약간 다른 방법으로 변수를 타이핑한 후 `Shift + Tab` 을 누르면 툴팁이 표시된다. 툴팁에는 DocString의 일부 내용이 표시된다.

**2) 이미지 첨부하기**

Drag & Drop으로 첨부할 수 있다.

**3) shell(명령 프롬프트)의 이용**

명령창에서 쓰는 명령을 그대로 쓰되, 맨 앞에 ! 를 입력하여 사용 가능하다.

**4) 매직 명령어 이용**

맨 앞에 %를 붙이고 특정 명령을 수행할 수 있다. 이는 파이썬 문법에는 포함되지 않은 Jupyter notebook만의 기능이다.

매직 명령어

- `%pwd` : 현재 디렉토리 경로 출력
- `%time 코드` : 코드의 실행 시간을 측정하여 표시
- `%timeit 코드` : 코드를 여러 번 실행한 결과를 요약하여 표시
- `%history -l 3` : 최근 3개의 코드 실행 이력 취득
- `%ls` : 윈도우의 dir, Linux의 ls 명령과 같음
- `%autosave n` : 자동저장 주기를 설정한다. 초 단위이며, 0이면 무효로 한다.
- `%matplotlib` : 그래프를 그리는 코드 위에 따로 설정한다. %matplotlib inline 으로 설정하면 코드 셀의 바로 아래에, %matplotlib tk 로 설정하면 별도 창에 그래프가 출력된다. %matplotlib notebook 으로 하면 코드 셀 바로 아래에 동적으로 그래프를 조작할 수 있는 그래프가 생성된다.

### 5. 라이브러리 설치

주피터에서 사용할 라이브러리는 명령 프롬프트에서 설치할 수 있다. 관리자모드로 명령 프롬프트 실행 후 아래와 같이 명령어를 입력하면 된다.

```powershell
pip install 해당 라이브러리
```  

▶ 출처  
https://sdc-james.gitbook.io/onebook/2.-1/1.6./1.1.1.-jupyter-notebook  
https://greeksharifa.github.io/references/2019/01/26/Jupyter-usage/  
https://mapled.tistory.com/entry/Python-%EC%A3%BC%ED%94%BC%ED%84%B0-%EB%85%B8%ED%8A%B8%EB%B6%81Jupyter-Notebook-%EC%84%A4%EC%B9%98
