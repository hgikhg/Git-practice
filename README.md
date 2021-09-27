﻿# Git assignment 

## 시작
Git를 설치한 후, Github에 repository를 생성한다.   
다른 사림들이 볼 수 있게 하려면 public로 설정하고, 그렇지 않을 경우 private로 설정한다.

## 로컬 저장소 생성
저장소는 말 그대로 파일이 저장되는 곳이다. 
### 저장소 초기화
원하는 디렉토리에서 폴더를 하나 만들고, 그 폴더 내에서 Git Bash를 이용하여 다음 명령어를 입력한다. 
```
git init 
```
이러면 새로운 저장소를 만들 수 있다.
### 저장소 복제
`git clone` 을 이용하면 원격 저장소를 복제하거나, 로컬 저장소를 복제해 올 수 있다.  

#### 로컬 저장소의 경우 
내 PC에 저장되어 있는 저장소를 복제할 수 있다.
```
git clone [경로]
```
예를 들면
```
git clone C:/Users/.../assignment
```
#### 원격 저장소의 경우
Github와 같은 원격 저장소 서버에 있는 저장소를 복제할 수 있다.
```
git clone [주소] [DIR]
```
[주소]는 저장소의 주소를 의미한다. 이 저장소를 복제한다면 https://github.com/hgikhg/Git-pratice.git 을 입력하면 된다.  
[DIR]은 저장소를 로컬에 복제할 위치를 지정하는데, 생략 가능하다.

## 저장소의 구조
### working directory(작업 트리)
컴퓨터 내 저장소에 있는 실제 파일을 의미한다. 

### index
저장소와 head 사이에 있는 공간이다.  
`commit`은 작업 트리에 있는 파일을 기록하는 게 아니라, 이 인덱스에 있는 파일을 기록하게 된다.  
`git add [파일]` 또는 `git add *` 을 입력하면 변경된 파일이 인덱스에 반영된다. 

### head
`git commit`을 하게 되면, 파일이 `head`에 반영된다.  
단, 커밋을 하더라도 원격 저장소에는 반영이 되지 않는다. 

## branch
Git에서의 branch는
처음 커밋을 하면 자동으로 `master` branch가 생성된다.  

branch를 만드는 방법은 다음과 같다.
``` 
git branch [branch 이름]
```
branch는 여러개가 있을 수 있지만, head는 한 가지의 branch만을 가리킨다.  
대신 원하는 branch로 갈아탈 수 있다.
```
git checkout [branch 이름]
```
갈아탄 후에 커밋을 해 주면 head는 새로 갈아탄 branch를 가리키게 된다. 
이전의 branch는 이전



## push
`head`에 있는 파일을 웹 상의 원격 저장소에 올리기 위해 명령을 실행해야 한다.  
그 전에, 만약 기존에 있던 원격 저장소를 복제한 것이 아니라 새로운 원격 저장소를 만들었다면 Git에게 알려줘야 한다. 
```
git remote add origin [원격 저장소 주소]
```
내 저장소 주소를 알려준다고 한다면, 
```
git remote add origin https://github.com/hgikhg/Git-pratice.git
```

원격 저장소가 git과 연동되면, `push`를 실행해도 된다. 
```
git push origin [branch 이름]
```

만약 처음 `push`를 하게 되면 인증 절차(로그인)를 걸쳐야 한다.  
`push`가 실행되면 로컬 저장소와 원격 저장소는 동일한 상태가 된다. 




