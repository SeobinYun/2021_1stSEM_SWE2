# 2021_1stSEM_SWE2

git & GitHub 연습

## GitHub Repository URL

<https://github.com/SeobinYun/2021_1stSEM_SWE2>

---

## **1. add**

- 현재 기존 파일들을 수정하고, 새로운 파일도 만든 상태이다.
- 이를 staging Area(원격저장소로 commit을 실행하기 전의 임시 저장된 상태 정도...)에 옮기고 싶다.
- 이를 위해서 git 명령어 'add'를 사용했다.
- 따라서 명령어 'add'는 **원격저장소로 commit을 하기 전, 파일들을 원격저장소에 올릴 수 있게, staging area로 옮기는 명령어**이다.

- **사용법**

> **git add [filename|-A]**  
> - 'filename' : filename이라는 file을 staging area로 옮김  
> - '-A' : 모든 파일들을 staging area로 옮김

- 사용 예시

>  
    - 사진과 같이 test라는 파일을 새로 만들었고, 과제1 파일을 '1. Get Started' 부분을 작성하여 수정하였다.  
![image](https://user-images.githubusercontent.com/54767707/117528581-e51eda80-b00d-11eb-9132-2763cdd18b80.png)  

>  
    - 처음 git status를 실행했을 때, 과제1이라는 파일이 수정되었고, 새로운 test파일이 추가되었다는 안내 메세지가 뜬다.  
    이후 git add filename 명령어를 통해 test 파일만 staging area로 옮기고, status로 다시 상태를 확인했을 때, test 파일만 staging area로 옮겨진 것을 확인할 수 있다.  
    다음, git add -A 명령어로 모든 파일들을 staging area로 옮겼다. 
    
    ! 참고: 필자가 과제1을 수행하기 전 test1 파일을 생성했다 지워서, test1 파일이 지워졌다는 알림을 확인할 수 있다.
![image](https://user-images.githubusercontent.com/54767707/117528628-11d2f200-b00e-11eb-9365-96d8e54340a4.png)


---

## **2. branch**

- 현재 문서 작업을 master에서 진행하고 있다.
- 하지만 내 생각만을 작성할 수 있는 그런 공간인 'my_space'라는 독립적인 작업 영역을 만들어 그곳에서 작업하고 싶다.
- 이를 위해서 git 명령어 'branch'를 사용했다.
- 따라서 명령어 'branch'는 **독립적인 작업 영역을 만들어주는 명령어**이다. my_space에서 수정된 문서작업은 별다른 명령을 실행해주지 않으면 master branch에 영향을 미치지 않는다.

- **사용법**

> **git branch** : branch 목록확인  
**git branch branch_name** : branch_name이라는 branch 생성  
**git branch -d branch_name** : branch_name이라는 branch 삭제

- 사용 예시  

![branch](https://user-images.githubusercontent.com/54767707/117507543-27bac580-afc2-11eb-8b3a-74b068bcb1a8.png)
*맨처음 branch 명령어로 branch 목록들을 확인했을 때, 'master'이라는 branch 밖에 없었다. 하지만 그 후 'git branch my_space'를 통해 'my_space'라는 독립적인 작업 영역을 만들어주었다.*

---

## **3. checkout**

- 현재 'master'라는 공간에서 작업을 하고 있었다.

- 하지만 'master'에서 벗어나 'my_space'라는 공간에서 작업을 하고 싶다.
- 이를 위해서 git 명령어 'checkout'을 사용했다.
- 따라서 명령어 'checkout'은 **브랜치를 이동할 때 사용하는 명령어**이다.

- **사용법**

> **git checkout (option) branch_name** : branch_name으로 된 branch로 이동해라.

- 옵션  

> '-b' : branch_name이라는 branch를 만들고 branch_name에서 시작(이동)하라.  

- 사용 예시  

![image](https://user-images.githubusercontent.com/54767707/117508728-078c0600-afc4-11eb-8005-06377174ede2.png)

*아까 branch 명령어에서 우리는 my_space라는 branch를 만들었고, 사진의 처음에선 my_space로 이동하라 했다.  
branch 명령어를 사용해 이동을 확인한 후, 'git chechout -b his_space' 명령어를 사용해 his_space라는 branch를 만든 뒤 그쪽에서 시작하라는 명령을 내렸다. 이상 branch를 통해 이동을 확인할 수 있다.*

---

## **4. clone**

- 현재 원격저장소(GitHub)에 있는 repository를 새로운 clone_test 폴더에 내려받고 싶다.
- 이를 위해서 git 명령어 'clone'을 사용하였다.
- 따라서 명령어 'clone'은 **원격저장소의 repositoty에서 클라이언트로 파일을 복사 붙여넣기 할 수 있는 명령어**이다.

- **사용법**

> **git clone URL**

- 사용 예시

> 다음과 같이 clone_test 파일은 빈 폴더이다.
![image](https://user-images.githubusercontent.com/54767707/117529527-01714600-b013-11eb-82bc-014b0e6990f3.png)  

> cd 명령어를 이용해 clone_test로 위치를 옮겨준 후, git clone URL 명령어를 이용해 원격저장소에 있는 repository를 복사해보았다.
![image](https://user-images.githubusercontent.com/54767707/117529538-0c2bdb00-b013-11eb-9aa9-9864d732c878.png)  

> 사진과 같이 링크의 2021_1stSEM_SWE2 repository가 잘 복제된 것을 확인할 수 있다
![image](https://user-images.githubusercontent.com/54767707/117529531-046c3680-b013-11eb-85b8-6643d3ba6c9d.png)
![image](https://user-images.githubusercontent.com/54767707/117529534-0930ea80-b013-11eb-87be-a912be8ebef6.png)
---

## **5. commit**

- 현재 우리는 문서를 수정한 뒤, 무엇이 수정되었는지 설명을 달아 원격저장소(GitHub)에 올리고 싶다.
- 이를 위해서 git 명령어 'commit'을 사용하였다.
- 따라서 명령어 'commit'은 **원격저장소로 push를 할 때, 변경사항을 기록하고 싶을 때 사용하는 명령어**이다.  

- **사용법**

> **git commit (option) "message"**

- 옵션

> - '-m' : 메세지와 함께 커밋하기  
    '-am' : 스테이징과 커밋을 메세지와 함께 올리기  
    '--amend' : 방금 커밋한 메세지 수정하기

- 사용 예시


---

## **1. config**  

- 우선 git을 맨 처음 시작했을 때의 상태에 있다.
- 이 상태에서 사용자 이름과 이메일을 설정해주고 싶다. 왜냐하면 user가 설정되어 있지 않을 경우 Github에 push한다고 해도, commit count 집계도 안되고 해당 커밋의 작성자 프로필 아이콘도 ?로 표시되기 때문에 name과 email 주소를 설정한다.
- 이를 위해서 git 명령어 'config'를 사용했다.
- 따라서 'config' 명령어는 **git의 일반적인 설정을 담당하는 명령어**이다.  

- **사용법**

> **git config (option) [user.name|user.email]**  
*// 이 상태로 사용할 시 저장소별로 사용자명/이메일이 구성된다.*

> **git config (option) --list**  
*// 설정정보 조회 명령어*

- **옵션**

> '--global' : 전역설정을 지정할 때 사용
![화면 캡처 2021-05-08 045549](https://user-images.githubusercontent.com/54767707/117501902-ae1ed980-afb9-11eb-803f-b6d21cc477af.png)

- 사용 예시

> 설정  
![이름이메일설정](https://user-images.githubusercontent.com/54767707/117499518-4c10a500-afb6-11eb-9369-9b18dda5acd5.png)

> 설정 후 확인
![화면 캡처 2021-05-08 043943](https://user-images.githubusercontent.com/54767707/117500340-757e0080-afb7-11eb-83d8-98f595775c3a.png)
![화면 캡처 2021-05-08 045330](https://user-images.githubusercontent.com/54767707/117501690-5c764f00-afb9-11eb-9126-685fe85ae0e7.png)

---

## **3. init**

- 현재 로컬저장소를 원격저장소와 연결하지 않은 상태이다.  

- 연결 전, 빈 git repository를 초기화해야한다.
- 이를 위해서 git 명령어 'init'을 사용했다.
- 따라서 'init' 명령어는 **새로운 git 저장소(repository)를 만들거나 이미 있는 repository를 초기화할 때 사용하는 명령어 (.git 파일을 만드는 명령어)**이다.  

- **사용법**

> **git init**

- 사용예시

![image](https://user-images.githubusercontent.com/54767707/117527072-2c07d280-b004-11eb-87e8-4c861310ccc9.png)
*git init을 실행하니 initialized 되었다는 안내문구가 뜬다.  
참고 : 필자는 사진 속 init 실행 전 이미 init 명령어를 실행해서 Reinitialized 되었다고 뜸.  
최초로 init을 실행할 시에는 그냥 initialized 되었다고 뜰 것임.*


---

## **8. log**

- 현재 문서 작업을 어느 정도까지 하여, 원격저장소에 여러번 commit한 상태이다.

- 이때까지 한 commit history를 보고 싶다.

- 이를 위해서 git 명령어 'log'를 사용했다.

- 따라서 명령어 'log'는 **commit history를 조회할 수 있는 명령어**이다.

- 사용법

> **git log (option)**

- 옵션
>  
    - '-p' : 각 커밋의 diff 결과를 보여줌  
    - '--stat' : 각 커밋의 통계 정보를 조회할 수 있음. (어떤 파일이 수정됬는지, 얼마나 많은 파일이 변경됬는지, 얼마나 많은 라인을 추가하거나 삭제했는지 보여줌, 요약정보는 가장 뒤쪽에...)  
    - '--shortstat' : '--stat' 명령의 결과 중에서 수정한 파일, 추가된 라인, 삭제된 라인만 보여줌.  
    - '--name-only' : 커밋 정보중에서 수정된 파일의 목록만 보여줌.  
    - '--name-status' : 수정된 파일의 목록을 보여줄 뿐만 아니라 파일을 추가한 것인지, 수정한 것인지, 삭제한 것인지도 보여줌.  
    - '--relative-date' : '2 week ago'와 같이 상대적인 형식으로 시간을 보여줌.  
    - '--graph' : 브랜치와 머지 히스토리 정보까지 아스키 그래프로 보여줌.

- 사용 예시

> git log -p 사용  
![image](https://user-images.githubusercontent.com/54767707/117527858-fb2a9c00-b009-11eb-99e5-ce439107a455.png)  

> git log --stat 사용  
![image](https://user-images.githubusercontent.com/54767707/117527862-05e53100-b00a-11eb-96f4-afd7eeac509f.png)  

> git log --shortstat 사용  
![image](https://user-images.githubusercontent.com/54767707/117527869-10072f80-b00a-11eb-8de5-d7c9d7c2102b.png)

> git log --name-only 사용  
![image](https://user-images.githubusercontent.com/54767707/117527878-24e3c300-b00a-11eb-9b49-71e8d4e68b98.png)

> git log --name-status 사용  
![image](https://user-images.githubusercontent.com/54767707/117527887-3200b200-b00a-11eb-9b1f-caacac7f0566.png)  

> git log --relative-date 사용  
![image](https://user-images.githubusercontent.com/54767707/117527892-3927c000-b00a-11eb-97e2-a4f55aa69f91.png)

> git log --graph 사용![image](https://user-images.githubusercontent.com/54767707/117527898-43e25500-b00a-11eb-94e9-5a08028908b2.png)



---

## **9. merge**

---

## **10. pull**

- 현재 협업을 하고 있는 과정에서 동료가 수정된 파일을 원격저장소(GitHub)에 올린 상태이다.
- 이 동료가 수정한 파일을 해당 폴더로 가져오고 싶다.
- 이를 위해서 git 명령어 'pull'을 사용하였다.
- 따라서 명령어 'pull'은 

-**사용법**
> git pull 

---

## **11. push**

- 과제1 문서를 사진과 같이 수정한 상태이다.
![수정1_과제1](https://user-images.githubusercontent.com/54767707/117504440-6306c580-afbd-11eb-8aee-e1b20c6bd9ff.png)

- 이 수정한 문서를 원격저장소(GitHub)에도 올려 관리하고 싶다.  
- 이를 위해 git 명령어 'push'를 사용했다.
- 따라서 명령어 'push'는 **외부에서 수정한 파일을 원격저장소(GitHub)에 올리고 싶을 때 사용하는 명령어**이다.

- **사용법**  

> **git push**

- 옵션

> git push origin master

- 사용 예시  
 ~~*물론 push하는 과정에서 'add', 'commit' 명령어도 수반된다.*~~  
![수정1 이후 push](https://user-images.githubusercontent.com/54767707/117504643-c264d580-afbd-11eb-9655-442fc3896f3f.png)

> push 사용 후 원격저장소에 업데이트 되었는지 확인  
~~*잘 push 되었다.*~~
![수정1 이후 push-github_과제1](https://user-images.githubusercontent.com/54767707/117504691-d577a580-afbd-11eb-8f0c-b4c2c09c657f.png)

---

## **12. rebase**

---

## **13. remote**

- 현재 생성 초기 단계로, 컴퓨터에서 작업한 작업물들을 인터넷이나 네트워크 어딘가에 있는 저장소와 연결해 업데이트 하고 싶다.

- 이를 위해서 git 명령어 'remote'를 사용했다.

- 따라서 명령어 'remote'는 **원격 저장소를 관리할 수 있는 명령어**이다.

- **사용법**

> **git remote (option)** : 현재 프로젝트에 등록된 리모트 저장소 확인  
> **git remote add name url** : name이라는 이름으로 원격 저장소 주소를 등록  
> **git remote remove name** : name이란 원격 저장소를 지울 때 사용  
> **git remote rename name1 name2** : name1이라는 리모트 저장소의 이름을 name2로 바꿈

- 옵션

> '-v' : 단축이름과 URL을 함께 보고 싶을 때 사용

- 사용 예시

![remote](https://user-images.githubusercontent.com/54767707/117527303-e51adc80-b005-11eb-8e63-bbd48ed635a2.jpg)
*첫번째 밑줄: git remote를 통해 등록된 리모트 저장소가 없는 걸 확인  
두번째 밑줄: origin이라는 이름으로 원격 저장소 주소를 등록*

![image](https://user-images.githubusercontent.com/54767707/117527360-66726f00-b006-11eb-8a18-995e49c1bb15.png)
*git remote로 등록된 리모트 저장소 확인  
'-v' 옵션을 사용하여 URL까지 확인*


---

## **14. reset**

- --hard

---

## **2. status**

- 1. 현재 저장소 생성 초기 단계로, git과 GitHub repository를 연결하고 싶다.
- 2. 또한 문서들을 수정한 뒤, 현재 폴더상태를 확인하고 싶다.
- 이를 위해 git 명령어 'status'를 사용했다.  
~~*물론 연결시엔 status 말고도 다른 명령어들도 같이 사용함*~~
  
 - 따라서 'status' 명령어는 **문서의 상태를 확인할 때 사용**한다.  

 - **사용법**  

 > **git status (option)**

 - **옵션**

> '-s' : 파일의 상태를 짧게 보고싶을 경우 사용  

- 사용 예시

> ㄱ. 1번 상황  
![git과github연결1](https://user-images.githubusercontent.com/54767707/117502802-02768900-afbb-11eb-936e-7ca0e8cf9309.png)  

> ㄴ. 2번 상황 & 옵션 '-s' 사용
![수정1했을때 상태](https://user-images.githubusercontent.com/54767707/117502821-099d9700-afbb-11eb-9489-1f20c7f769db.png)  

---

## **16. tag**  


---

## ***Table***  

|index|명령어|수행여부|링크|
|:---|:---|:---|:---|
|5|add|O
||branch|O|
||checkout|O|
||clone|O|
|6|commit|
|1|config|O|
|3|init|O|
|9|log|O|
||merge|
|8|pull|
|7|push|O|
||rebase|
|4|remote|O|
|10|reset|
|2|status|O|
||tag|