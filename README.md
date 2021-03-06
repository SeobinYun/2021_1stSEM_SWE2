# 2021_1stSEM_SWE2

git & GitHub 연습

## GitHub Repository URL

<https://github.com/SeobinYun/2021_1stSEM_SWE2>

## **Intro | 기본적으로 알아야 할 것들**

### **1. git과 원격저장소(GitHub) 연결 | 쉬운 방법만**

- GitHub에서 새로운 Repository를 만든다.  
- 그럼 다음과 같이 git을 연결하라는 안내창이 뜬다.  
![image](https://user-images.githubusercontent.com/54767707/117538897-d9014000-b042-11eb-988f-fab107e67496.png)
- git과 GitHub를 연결하는 가장 쉬운 방법은 명령창에 2번째 또는 3번째 옵션을 복사 붙여넣기하는 방법이다. (이 과정안에 init, remote 등등의 명령어 과정이 포함됨)

### **2. 원격저장소로 push하는 방법 | 보통 쓰는 방법**

- git status *-> 문서 상태들 확인 (modified, deleted 등등..)*
- git add -A *-> 수정된 모든 문서들을 staging area로 옮김*
- git commit -m "message" *-> "message"를 덧붙여 commit함*
- git push *-> GitHub에 업데이트*
- 위의 명령어들을 차례대로 입력하면 된다.

---

## **git 명령어들**

---

## **1. config**  

- 우선 git을 맨 처음 시작했을 때의 초기상태에 있다.
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

> git config user.name "myname"으로 이름을 지정해줌.
![이름이메일설정](https://user-images.githubusercontent.com/54767707/117499518-4c10a500-afb6-11eb-9369-9b18dda5acd5.png)

> 설정 후 git config user.name으로 설정 확인
![화면 캡처 2021-05-08 043943](https://user-images.githubusercontent.com/54767707/117500340-757e0080-afb7-11eb-83d8-98f595775c3a.png)
![화면 캡처 2021-05-08 045330](https://user-images.githubusercontent.com/54767707/117501690-5c764f00-afb9-11eb-9126-685fe85ae0e7.png)

---

## **2. status**

- 1. 현재 저장소 생성 초기 단계로, git과 GitHub repository를 연결하고 싶다.
- 2. 또는 문서들을 수정한 뒤, 현재 폴더상태를 확인하고 싶다.
- 이를 위해 git 명령어 'status'를 사용했다.  
~~*물론 연결시엔 status 말고도 다른 명령어들도 같이 사용함*~~
  
- 따라서 'status' 명령어는 **작업공간의 상태를 확인할 때 사용**한다.  

- **사용법**  

> **git status (option)**

- **옵션**

> '-s' : 파일의 상태를 짧게 보고싶을 경우 사용  

- 사용 예시

> *ㄱ. 1번 상황*
![git과github연결1](https://user-images.githubusercontent.com/54767707/117502802-02768900-afbb-11eb-936e-7ca0e8cf9309.png)  
> *ㄴ. 2번 상황 & 옵션 '-s' 사용 -> 파일 2개가 수정되었다는 걸 확인 가능*
![수정1했을때 상태](https://user-images.githubusercontent.com/54767707/117502821-099d9700-afbb-11eb-9489-1f20c7f769db.png)  

---

## **3. init**

- 현재 로컬저장소를 원격저장소와 연결하지 않은 상태이다.  

- 연결 전, 빈 git repository를 초기화해야한다.
- 이를 위해서 git 명령어 'init'을 사용했다.
- 따라서 'init' 명령어는 **새로운 git 저장소(repository)를 만들거나, 이미 있는 repository를 초기화할 때 사용하는 명령어**이다.  

- **사용법**

> **git init**

- 사용예시

![image](https://user-images.githubusercontent.com/54767707/117527072-2c07d280-b004-11eb-87e8-4c861310ccc9.png)
*git init을 실행하니 initialized 되었다는 안내문구가 뜬다.  
**참고** : 필자는 사진 속 init 실행 전 이미 init 명령어를 실행해서 Reinitialized 되었다고 뜸.  
최초로 init을 실행할 시에는 그냥 initialized 되었다고 뜰 것임.*

---

## **4. remote**

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

> *첫번째 밑줄: git remote를 통해 등록된 리모트 저장소가 없는 걸 확인  
두번째 밑줄: origin이라는 이름으로 원격 저장소 주소를 등록*
![remote](https://user-images.githubusercontent.com/54767707/117527303-e51adc80-b005-11eb-8e63-bbd48ed635a2.jpg)
*git remote로 등록된 리모트 저장소 확인  
'-v' 옵션을 사용하여 URL까지 확인*
![image](https://user-images.githubusercontent.com/54767707/117527360-66726f00-b006-11eb-8a18-995e49c1bb15.png)

---

## **5. add**

- 현재 기존 파일들을 수정하고, 새로운 파일도 만든 상태이다.
- 이를 staging Area(원격저장소로 commit을 실행하기 전의 임시 저장된 상태 정도...)에 옮기고 싶다.
- 이를 위해서 git 명령어 'add'를 사용했다.
- 따라서 명령어 'add'는 **원격저장소로 commit을 하기 전, 파일들을 원격저장소에 올릴 수 있게, staging area로 옮기는 명령어**이다.

- **사용법**

> **git add [filename|-A]**  
> - 'filename' : filename이라는 file을 staging area로 옮김  
> - '-A' : 모든 파일들을 staging area로 옮김

- 사용 예시

> *사진과 같이 test라는 파일을 새로 만들었고, 과제1 파일의 '1. Get Started' 부분을 수정하였다.*
![image](https://user-images.githubusercontent.com/54767707/117528581-e51eda80-b00d-11eb-9132-2763cdd18b80.png)  
> *처음 'git status'를 실행했을 때, 과제1 파일이 수정되었고, 새로운 test파일이 추가되었다는 안내 메세지가 뜬다.  
이후 'git add filename' 명령어를 통해 test 파일만 staging area로 옮기고,  
status로 상태를 다시 확인했을 때, test 파일만 staging area로 옮겨진 것을 확인할 수 있다.  
다음, git add -A 명령어로 모든 파일들을 staging area로 옮겼다.  
**참고**: 필자가 이 예시를 실행하기 전 test1 파일을 생성했다 지워서, test1 파일이 지워졌다는 안내를 확인할 수 있다.*
![image](https://user-images.githubusercontent.com/54767707/117528628-11d2f200-b00e-11eb-9365-96d8e54340a4.png)

---

## **6. commit**

- 현재 우리는 문서를 수정한 뒤, 무엇이 수정되었는지 설명을 달아 원격저장소(GitHub)에 올리고 싶다.
- 이를 위해서 git 명령어 'commit'을 사용하였다.
- 따라서 명령어 'commit'은 **원격저장소로 push를 할 때, 변경사항을 기록하고 싶을 때 사용하는 명령어**이다.  

- **사용법**

> **git commit (option) "message"**

- 옵션

> '-m' : 메세지와 함께 커밋하기  
'-am' : 스테이징과 커밋을 메세지와 함께 올리기  

- 사용 예시

> *첫번째 사진과 같이 과제1 파일에 "2. Cheat Sheet" 부분의 내용을 추가함*
![image](https://user-images.githubusercontent.com/54767707/117530243-f3252900-b016-11eb-9faa-39b3c35e7a7c.png)
*'-am' 옵션을 사용해 별도의 add 과정을 거치지 않고 "add 2. Cheat Sheet"이라는 메세지를 달아 commit함.*
![image](https://user-images.githubusercontent.com/54767707/117530169-a3466200-b016-11eb-98a6-ed904b1aab2a.png)
> *GitHub에 "add 2. Cheat Sheet"이라는 메세지가 추가된 것을 확인할 수 있음.*
![image](https://user-images.githubusercontent.com/54767707/117530219-df79c280-b016-11eb-8b7d-ab1211809624.png)

---

## **7. push**

- 과제1 문서를 사진과 같이 수정한 상태이다.
![수정1_과제1](https://user-images.githubusercontent.com/54767707/117504440-6306c580-afbd-11eb-8aee-e1b20c6bd9ff.png)

- 이 수정한 문서를 원격저장소(GitHub)에도 올려 관리하고 싶다.  
- 이를 위해 git 명령어 'push'를 사용했다.
- 따라서 명령어 'push'는 **외부에서 수정한 파일을 원격저장소(GitHub)에 올리고 싶을 때 사용하는 명령어**이다. **push 전에는 add와 commit이 수반되어야 한다!**

- **사용법**  

> **git push**

- 사용 예시  

> ![수정1 이후 push](https://user-images.githubusercontent.com/54767707/117504643-c264d580-afbd-11eb-9655-442fc3896f3f.png)
> push 사용 후 원격저장소에 업데이트 되었는지 확인  
~~*잘 push 되었다.*~~
![수정1 이후 push-github_과제1](https://user-images.githubusercontent.com/54767707/117504691-d577a580-afbd-11eb-8f0c-b4c2c09c657f.png)

---

## **8. pull**

- 현재 원격저장소(GitHub)에 수정된 파일이 올려진 상태이다.
- 수정된 파일을 해당 작업환경에 가져오고 싶다.
- 이를 위해서 git 명령어 'pull'을 사용하였다.
- 따라서 명령어 'pull'은 **원격저장소의 변경 사항(이력)을 받아오는 명령어**이다.

- **사용법**

> **git pull origin master**

- 사용 예시

> *사진과 같이 GitHub내에서 과제1을 수정하고 commit했다. (3-10내용 추가)*  
![image](https://user-images.githubusercontent.com/54767707/117535763-380a8900-b032-11eb-8fba-9071c8bb3f2b.png)  
*그 후 GitHub에 올라와 있는 수정파일을 'git pull origin master' 명령어를 사용해, 현재 작업 공간으로 가져와주었다.*  
![image](https://user-images.githubusercontent.com/54767707/117535766-3a6ce300-b032-11eb-8598-fc58d4449fd3.png)  
*아래 사진과 같이 잘 끌어온 것을 확인할 수 있다.*  
![image](https://user-images.githubusercontent.com/54767707/117535779-48226880-b032-11eb-88b3-911c8ea598a3.png)

---

## **9. log**

- 현재 문서 작업을 어느 정도까지 하여, 원격저장소에 여러번 commit한 상태이다.

- 이때까지 한 commit history를 보고 싶다.

- 이를 위해서 git 명령어 'log'를 사용했다.

- 따라서 명령어 'log'는 **commit history를 조회할 수 있는 명령어**이다.

- 사용법

> **git log (option)**

- 옵션
> - '-p' : 각 커밋의 차이점을 보여줌  .
> - '--stat' : 각 커밋의 통계 정보를 조회할 수 있음. (어떤 파일이 수정됬는지, 얼마나 많은 파일이 변경됬는지, 얼마나 많은 라인을 추가하거나 삭제했는지 보여줌, 요약정보는 가장 뒤쪽에...)  
> - '--shortstat' : '--stat' 명령의 결과 중에서 수정한 파일, 추가된 라인, 삭제된 라인만 보여줌.  
> - '--name-only' : 커밋 정보중에서 수정된 파일의 목록만 보여줌.  
> - '--name-status' : 수정된 파일의 목록을 보여줄 뿐만 아니라 파일을 추가한 것인지, 수정한 것인지, 삭제한 것인지도 보여줌.  
> - '--relative-date' : '2 week ago'와 같이 상대적인 형식으로 시간을 보여줌.  
> - '--graph' : 브랜치와 머지 히스토리 정보까지 아스키 그래프로 보여줌.

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
> git log --graph 사용  
![image](https://user-images.githubusercontent.com/54767707/117527898-43e25500-b00a-11eb-94e9-5a08028908b2.png)

---

## **10. reset**

- 이전 커밋으로 돌아가고 싶다.
- 이를 위해 git 명령어 'reset'을 사용했다.
- 따라서 명령어 'reset'은 **특정 commit 상태로 되돌아가는 명령어**이다.

- **사용법**

> **git reset (option) specified_commit**  
*- 옵션을 적지않으면 mixed로 동작함. 이력을 되돌리고, 변경된 내용에 대해서는 남아있지만, 인덱스는 초기화된 상테*

- 옵션

> '--hard' : 돌아가려는 특정 commit 이후의 모든 내용을 지워버린다.  
'--soft' : 돌아가려는 특정 commit으로 돌아가지만, 이후의 내용이 지워지지 않고, 해당 내용의 스테이지도 그대로 있음. -> 다시 commit할 수 있는 상태로 남아있는 것  

- 사용 예시

> *과제1의 문서에 '!reset test!'등의 comment를 추가함.*
![image](https://user-images.githubusercontent.com/54767707/117534542-d0057400-b02c-11eb-83df-96a9effc6725.png)  
> *위의 수정사항을 add, commit해주고 log 명령어를 활용해 commit history를 확인함. 이때 빨간색 밑줄이 그어진 commit으로 reset한다 가정.*
![image](https://user-images.githubusercontent.com/54767707/117534552-d7c51880-b02c-11eb-97d2-22c51ac53a48.png)  
> *'git reset specified_commit' 명령어를 사용하여 특정 commit부분으로 reset했음.  
이때는 --hard 옵션을 사용하지 않았기 때문에 '!reset test!' 그때의 상태로 돌아갈 수 있음.*
![image](https://user-images.githubusercontent.com/54767707/117534557-dac00900-b02c-11eb-8453-e6ff9566e05d.png)  

> *반면, --hard 옵션을 test하는 경우임.  
아까 원래의 '!reset test!'의 특정 commit으로 돌아왔음.*
![image](https://user-images.githubusercontent.com/54767707/117535178-908c5700-b02f-11eb-906d-ef9ba7e91f93.png)  
> *--hard 옵션을 사용해서 다시 93887e.. 그때의 commit으로 돌아는 걸 시도해봄.  
하지만 --hard옵션을 사용했기 때문에, 다시 이전의 상태로 되돌아가는 것은 불가능함.  
따라서 사진의 체크한 곳을 보면 위의 사진과 다르게 commit 주소가 지워진 것을 확인할 수 있음.*
![image](https://user-images.githubusercontent.com/54767707/117535039-e4e30700-b02e-11eb-92a5-2205c237c533.png)  

---

## **11. clone**

- 현재 원격저장소(GitHub)에 있는 repository를 새로운 clone_test 폴더에 내려받고 싶다.
- 이를 위해서 git 명령어 'clone'을 사용하였다.
- 따라서 명령어 'clone'은 **원격저장소의 repositoty에서 클라이언트로 파일을 복사 붙여넣기 할 수 있는 명령어**이다.

- **사용법**

> **git clone URL**

- 사용 예시

> *다음과 같이 clone_test 파일은 빈 폴더이다.*
![image](https://user-images.githubusercontent.com/54767707/117529527-01714600-b013-11eb-82bc-014b0e6990f3.png)  
> *cd 명령어를 이용해 clone_test로 위치를 옮겨준 후, git clone URL 명령어를 이용해 원격저장소에 있는 repository를 복사해보았다.*
![image](https://user-images.githubusercontent.com/54767707/117529538-0c2bdb00-b013-11eb-9aa9-9864d732c878.png)  
> *사진과 같이 링크의 2021_1stSEM_SWE2 repository가 잘 복제된 것을 확인할 수 있다.*
![image](https://user-images.githubusercontent.com/54767707/117529531-046c3680-b013-11eb-85b8-6643d3ba6c9d.png)
![image](https://user-images.githubusercontent.com/54767707/117529534-0930ea80-b013-11eb-87be-a912be8ebef6.png)

---

## **12. branch**

- 현재 문서 작업을 master에서 진행하고 있다.
- 하지만 내 생각만을 작성할 수 있는 그런 공간인 'my_space'라는 독립적인 작업 영역을 만들어 그곳에서 작업하고 싶다.
- 이를 위해서 git 명령어 'branch'를 사용했다.
- 따라서 명령어 'branch'는 **독립적인 작업 영역을 만들어주는 명령어**이다. my_space에서 수정된 문서작업은 별다른 명령을 실행해주지 않으면 master branch에 영향을 미치지 않는다.

- **사용법**

> **git branch** : branch 목록확인  
**git branch branch_name** : branch_name이라는 branch 생성  
**git branch -d branch_name** : branch_name이라는 branch 삭제

- 사용 예시  

> *맨처음 branch 명령어로 branch 목록들을 확인했을 때, 'master'이라는 branch 밖에 없었다. 하지만 그 후 'git branch my_space'를 통해 'my_space'라는 독립적인 작업 영역을 만들어주었다.*  
![branch](https://user-images.githubusercontent.com/54767707/117507543-27bac580-afc2-11eb-8b3a-74b068bcb1a8.png)  
> *'git branch -d branch_name' 명령어를 활용해 his_space branch를 삭제하였다.*  
![image](https://user-images.githubusercontent.com/54767707/117536096-1f9b6e00-b034-11eb-983b-4ca43dc6426c.png)

---

## **13. checkout**

- 현재 'master'라는 공간에서 작업을 하고 있었다.

- 하지만 'master'에서 벗어나 'my_space'라는 공간에서 작업을 하고 싶다.
- 이를 위해서 git 명령어 'checkout'을 사용했다.
- 따라서 명령어 'checkout'은 **브랜치를 이동할 때 사용하는 명령어**이다.

- **사용법**

> **git checkout (option) branch_name** : branch_name으로 된 branch로 이동해라.

- 옵션  

> '-b' : branch_name이라는 branch를 만들고 branch_name에서 시작(이동)하라.  

- 사용 예시  

> *아까 branch 명령어에서 우리는 my_space라는 branch를 만들었고, 'git checkout my_space' 명령어를 사용해 my_space로 이동하도록 했다.  
'branch' 명령어를 사용해 이동을 확인한 후, 'git checkout -b his_space' 명령어를 사용해 his_space라는 branch를 만든 뒤 그쪽에서 시작하라는 명령을 내렸다.  
이상 branch를 통해 이동을 확인할 수 있다.*
![image](https://user-images.githubusercontent.com/54767707/117508728-078c0600-afc4-11eb-8005-06377174ede2.png)

---

## **14. merge**

- my_space라는 독립적인 공간(branch)에서 수정한 과제1이 마음에 들어 master에 적용시키고 싶다.
- 이를 위해서 git 명령어 'merge'를 사용하였다.
- 따라서 명령어 'merge'는 **한 branch의 수정사항 등을 다른 branch에 병합하는 명령어**이다.
- **사용법**

> **git merge branch_name** : branch_name이라는 branch를 master에 병합

- 사용 예시

> *my_space로 이동한 뒤, 과제1을 수정하였다. (상단에 merge test!등의 문구를 추가, 그리고 3-4까지 내용 작성)*
// *master로 이동한 후 merge*
![image](https://user-images.githubusercontent.com/54767707/117531504-b446a180-b01d-11eb-9fc7-66764ad66da5.png)
// *git에 push*
![image](https://user-images.githubusercontent.com/54767707/117531552-ee17a800-b01d-11eb-957b-fb56c772428e.png)

> 사진과 같이 my_space의 수정사항이 master에 merge된 것을 확인할 수 있음.
![image](https://user-images.githubusercontent.com/54767707/117531495-abee6680-b01d-11eb-8cb8-62f1d3ab4bf3.png)

---

## **15. rebase**

- 현재 master branch와 my_space branch가 나눠져있다.
- 이 두개를 그냥 하나로 깔끔하게 정리하고 싶다.
- 이를 위해서 git 명령어 'rebase'를 사용하였다.
- 따라서 명령어 'rebase'는 **나누어진 branch들의 뿌리를 하나의 베이스로 재정의함으로써 새롭게 commit line을 정리하여 히스토리를 깔끔하게 볼 수 있게 해주는 명령어**이다.

- **사용법**

> "git rebase branch_name"

- 사용 예시

> *branch 명령어를 사용해 rebase를 test할 새로운 branch, rbstest를 만들었다. 그 후 rbstest로 이동해 과제1의 내용을 밑의 사진과 같이 수정하였다. (Author, Email 등등 작성함)*
![image](https://user-images.githubusercontent.com/54767707/117536994-37c1bc00-b039-11eb-8330-527fc16bf441.png)
*rbstest에서 과제1을 수정했으므로, status로 상태를 확인했을 때 과제1이 수정되었다고 뜬다. 따라서 add 명령어로 staging area에 올려주고, commit을 해준다.*  
*그 후 'git rebase master' 명령어를 이용하여 merge 해준다.*
![image](https://user-images.githubusercontent.com/54767707/117536942-f03b3000-b038-11eb-9c97-72e50c63b3b4.png)
*master로 돌아와 log --graph을 통해 rebase가 된 것을 시각화하여 확인할 수 있다.*
![image](https://user-images.githubusercontent.com/54767707/117536952-021cd300-b039-11eb-813d-bd0eaba3d82f.png)

---

## **16. tag**  

- 현재 문서를 수정한 후 commit을 여러번 실행한 상태이다.
- 이때 특정 commit을 tag해두고 싶다.
- 이를 위해서 git 명령어 'tag'를 사용했다.
- 따라서 명령어 'tag'는 **특정 commit을 태그해두는 (특정 commit을 가리키는 링크라고 생각해도 OK) 명령어**이다.보통 SW버전을 release할 때 사용한다.
- **사용법**

> **git tag** : 태그 조회  
**git tag tagname** : Lightweight 태그 생성  
**git tag -a tagname -m message** : Annotated 태그 생성, 메세지를 남겨야하므로 -m 옵션 사용  
**git tag -a tagname specified_commit** : 특정 커밋에 태그 생성

- 추가  

> 1. 태그를 원격 저장소에 push  
> **git push origin tagname** : tagname을 원격저장소에 push
> **git push origin --tags** : 모든 태그 push
> 2. **git show tagname**  태그 정보와 커밋 정보 확인

- 사용 예시

> *아래 사진과 같이 과제1의 상단에 '//tag test'라는 comment를 추가하였다.*  
![image](https://user-images.githubusercontent.com/54767707/117533867-ed850e80-b029-11eb-8f4c-28969f4961ef.png)
> *수정사항을 add, commit 해주고 'git tag -a tagname -m "message"' 명령어를 통해 ver1이라는 tag를 생성해주었다.  
그 후 'git tag' 명령을 통해 존재하는 tag의 정보들을 확인해주었다.  
(참고: ver0 tag는 ver1을 만들기 전 실수로 만들어버린 태그임...)*  
 ![image](https://user-images.githubusercontent.com/54767707/117533806-bdd60680-b029-11eb-91fa-2723fe017c0a.png)  
 > *'git show tagname' 명령어를 사용해 ver1의 태그정보와 커밋 정보를 확인해주었다.*  
![image](https://user-images.githubusercontent.com/54767707/117533821-caf2f580-b029-11eb-9e8c-4d8ad9f1cc08.png)  
> *'git push origin --tags'를 사용해 모든 tags를 원격저장소에 push 해주었다.*  
![image](https://user-images.githubusercontent.com/54767707/117533827-cd554f80-b029-11eb-80a1-44be51441fbd.png)  
> *원격저장소(GitHub)에 tag가 push된 것을 확인할 수 있다.*  
![image](https://user-images.githubusercontent.com/54767707/117533836-d6462100-b029-11eb-9af6-e518e4aca9f6.png)

---

## ***Table***  

|index|명령어|수행여부|링크|
|:---|:---|:---|:---|
|1|config|O|[click!](https://github.com/SeobinYun/2021_1stSEM_SWE2#1-config)
|2|status|O|[click!](https://github.com/SeobinYun/2021_1stSEM_SWE2#2-status)
|3|init|O|[click!](https://github.com/SeobinYun/2021_1stSEM_SWE2#3-init)
|4|remote|O|[click!](https://github.com/SeobinYun/2021_1stSEM_SWE2#4-remote)
|5|add|O|[click!](https://github.com/SeobinYun/2021_1stSEM_SWE2#5-add)
|6|commit|O|[click!](https://github.com/SeobinYun/2021_1stSEM_SWE2#6-commit)
|7|push|O|[click!](https://github.com/SeobinYun/2021_1stSEM_SWE2#7-push)
|8|pull|O|[click!](https://github.com/SeobinYun/2021_1stSEM_SWE2#8-pull)
|9|log|O|[click!](https://github.com/SeobinYun/2021_1stSEM_SWE2#9-log)
|10|reset|O|[click!](https://github.com/SeobinYun/2021_1stSEM_SWE2#10-reset)
|11|clone|O|[click!](https://github.com/SeobinYun/2021_1stSEM_SWE2#11-clone)
|12|branch|O|[click!](https://github.com/SeobinYun/2021_1stSEM_SWE2#12-branch)
|13|checkout|O|[click!](https://github.com/SeobinYun/2021_1stSEM_SWE2#130checkout)
|14|merge|O|[click!](https://github.com/SeobinYun/2021_1stSEM_SWE2#14-merge)
|15|rebase|O|[click!](https://github.com/SeobinYun/2021_1stSEM_SWE2#15-rebase)
|16|tag|O|[click!](https://github.com/SeobinYun/2021_1stSEM_SWE2#16-tag)
