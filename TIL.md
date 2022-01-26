# Day 1

---

## 1) CLI기초

---

### [1] Git 설치 (Mac)

- Git이 기본적으로 내장 되어 있어, 별도의 설치가 필요없다.
- ```terminal```을 연다.
- 터미널을 열면 기본적으로 HOME 폴더로 경로가 설정되어있다. (```/Users/현재 사용자 계정```)
- ```open .``` 입력하여 HOME 폴더를 연다.

### [2] GUI vs CLI

1. ```GUI (Graphic User Interface)``` : 그래픽을 통해 사용자와 컴퓨터가 상호 작용하는 방식
2. ```CLI (Command Line Interface)``` : 터미널을 통해 사용자와 컴퓨터가 상호 작용하는 방식

### [3] 경로

#### (1) 루트, 홈 디렉토리

1. 루트 디렉토리(Root Directory, ```/```)

   : 모든 파일과 폴더를 담고 있는 최상위 폴더

2. 홈 디렉토리(Home Directory, ```~```)
   - ```Tilde(틸드)``` , 현재 로그인 된 사용자의 홈 폴더
   - ```/Users/현재 사용자 계정``` (Mac의 경우)

#### (2) 절대 경로와 상대 경로

1. 절대 경로 : 어디든 상관없는 위치
2. 상대경로 
   - 내 현재 위치 기준
   - ```./``` : 현재 작업하고 있는 폴더
   - ```../``` : 현재 작업하고 있는 폴더의 부모 폴더

### [4] 터미널 명령어

1. ```ls(list segments)``` : 현재 디렉토리내의 폴더 & 파일을 보여줌

   - ls -a : all 옵션, 숨긴 폴더 & 파일을 보여줌.
   - ls -l : long 옵션, 용량, 수정 날짜 등 파일 정보를 자세히 보여줌

   ```bash
   # 기본사용
   $ ls
   
   # all 옵션
   $ ls -a
   
   # all, long 옵션 함께
   $ ls -a -l
   
   # 여러 옵션 축약
   $ ls -al
   ```

2. ```clear``` : 지우기

   

3. ``` 화살표 키 ▲``` : 최근 기입한 명령어를 보여줌

   

4. ```touch``` : 파일 생성

   ```bash
   touch a.txt : a.txt 파일 생성
   touch a.txt b.txt c.txt : 띄어쓰기로 구분하여 여러 파일을 한번에 생성
   ```

5. ```mkdir(make directory)``` : 폴더 생성

   ```bash
   mkdir test : test 라는 폴더 생성
   mkdir test test : test 라는 폴더 2개 생성 > 중복된 이름으로 오류 발생
   mkdir "test test" : test test 라는 이름의 폴더 생성
   ```

6. ```cd(change directory)``` : 위치 이동 / 홈 위치로

   - cd ~ :  홈 디렉토리로 이동 (cd 라고만 입력해도 동일)

   - cd .. : 부모 디렉토리로 이동 (위로가기)

   - cd - : 바로 전 디렉토리로 이동 (뒤로가기)

     

7. ```mv(move)``` : 폴더 & 파일을 다른 폴도 내로 이동/ 이름 바꾸기

   - mv a.txt b.txt : a.txt를 b.txt 로 이름 바꾸기

   - mv a.txt test : a.txt 를 test 폴더 안으로 이동

     

8. ```rm(remove)``` : 삭제 (휴지통을 거치지 않고)

   - rm 파일명 : 파일 삭제

   - rm -r 폴더명 :  폴더 삭제

   - *(asterisk, wildcard) : all

   - rm *.txt : 현재 위치내의 txt 파일 전체 삭제

   - rm -rf : 강제 삭제

   - rm -rf* : 전체 강제 삭제 (절대 사용 금지!!)

     

9. ```단축키```

   - Ctrl + l : 화면 정리 (스크롤 올리면 과거 내역 조회 가능)
   - tap : 폴더 & 파일 이름 자동 완성

## 2) Markdown

---

### 마크다운 문법

1. ```#``` : 제목 (h1~h6)

   ```markdown
   # h1
   ## h2
   ### h3
   #### h4
   ##### h5
   ###### h6
   ```

2. ```목록(list)```

   - 순서가 없는 목록 : ``` - * +```
   - 순서가 있는 목록 : ``` 1. 2. 3.```
   - 들여쓰기 : ```tap 키```
   - 내어쓰기 : ```shift + tap 키```

   

3. ```인용``` : ```> + 스페이스바```

   > 인용문
   >
   > > 개수에 따라 중첩 가능

   

4. ```코드```

   -  '''(백틱)으로 코드를 감싸준다

   - ``` markdown
     block code : ``` + enter
     ```

5. ```링크```

   - ```[표시할 글자] (이동할 주소)``` 형태로 작성

   - ``` markdown
     [google] (http://google.com) 을 눌러서 구글로 이동하세요.
     ```

6. ```이미지```

   - ```! [대체 텍스트] (이미지 주소)``` 형태로 작성
   -  대체 텍스트 란 이미지를 정상적으로 불러오지 못했을 때 표시되는 문구
   - Typora에서는 이미지 파일을 끌어와서 놓아도 자동 업로드 가능

   ```markdown
   Git 로고입니다.
   
   ![Git로고](https://git-scm.com/images/logo@2x.png)
   ```

7. ```표(Table)```

   - ```option + command + t``` (Mac 기준)
   - ```파이프( | )``` 와 ```하이픈( - )```로 행과 열 구분
   - 표의 양쪽 끝의 파이프는 생략 가능
   - 헤더 셀을 구분할 때는 ```3개 이상의 하이픈( - )``` 사용
   - 행을 늘릴 때는 ```command + enter``` 

   ```bash
   | 동물 | 종류 | 다리 개수 |
   | --- | --- | ------ |
   | 사자 | 포유류 | 4개 |
   | 닭 | 조류 | 2개 |
   |도마뱀|파충류| 4개 |
   ```

   | 동물   | 종류   | 다리 개수 |
   | ------ | ------ | --------- |
   | 사자   | 포유류 | 4개       |
   | 닭     | 조류   | 2개       |
   | 도마뱀 | 파충류 | 4개       |





# Day 2

## 1) Git

### [1] Git 초기 설정

최초 한 번만 설정. 매번 설정할 필요가 없다.

1. 누가 커밋 기록을 남겼는지 확인할 수 있도록 이름과 이메일을 설정

   작성자를 수정하고 싶을 때는 이름, 메일 주소만 다르게 하여 동일하게 입력

   ```bash
   $ git config --global user.name "이름"
   $ git config --global user.email "메일 주소"
   ```

2. 작성자가 올바르게 설정되었는지 확인 

   ```bash
   $ git config --global -l
   
   또는
   
   $ git config --global --list
   ```

### [2] Git 기본 명령어

1. ```git init``` : 현재 폴더를 깃이 관리하는 폴더로 만들어 줌

   - 홈 폴더에서 기입하지 ❌
   - ✅최초 1번만 기입
   - ls -a 로 확인 가능

   

2. ```git status``` : 현 상황을 보여줌

1. ```git add``` : 무대에 올리기

   - git add a.txt : a.txt 올리기
   - git add . : 전부 올리기

   

2. ```git commit -m '메시지'``` : 촬영 후 저장소로

   - 올라온 파일의 변경 사항을 하나의 버전(커밋)으로 저장하는 명령어
   - `커밋 메세지`는 현재 변경 사항들을 잘 나타낼 수 있도록 `의미` 있게 작성하는 것을 권장

   

3. ```git log``` : (저장된 파일) 버전 확인

   - 커밋의 내역(ID, 작성자, 시간, 메세지 등)을 조회할 수 있는 명령어

   - ```git log --oneline``` : 한 줄로 축약해서 보여줌 (checkout에 쓰임)
   - ```git log --graph``` : 브랜치와 머지 내역을 그래프로 보여줌

   

4. 과거물 보기

   - `git checkout + 해쉬값` : 입력한 해쉬값으로 되돌아감
   - `git checkout head~숫자` : 입력한 숫자값만큼 되돌아감
   - `git checkout master` : 원래대로 돌아옴

   

   ```
   8b158f5 (HEAD -> master) fifth commit - case
   23733d5 fourth commit - glass
   2a3acd8 third commit -shoe
   c85ebf8 second commit - glove
   78c98bb first commit -hat equipped
   
   git checkout 2a3acd8
   HEAD의 현재 위치는 2a3acd8 third commit -shoe
   
   git checkout master
   이전 HEAD 위치는 2a3acd8 third commit -shoe
   'master' 브랜치로 전환합니다
   
   git checkout head~3
   HEAD의 현재 위치는 c85ebf8 second commit - glove
   ```

7. ```브릿지```

   - 브릿지 잇기 : `git remote add origin + 주소`
   - 브릿지 확인 : `git remote -v`

   

8. ```올리기```

   - git push origin master

   

