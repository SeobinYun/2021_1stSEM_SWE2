# 2021_1stSEM_SWE2

git & GitHub 연습

## GitHub Repository URL

<https://github.com/SeobinYun/2021_1stSEM_SWE2>

---

## **1. add**

---

## **2. branch**

- 현재 문서 작업을 master에서 협업으로 진행하고 있다.
- 하지만 내 생각만을 작성할 수 있는 그런 공간인 'my_space'라는 독립적인 작업 영역을 만들어 그곳에서 작업하고 싶다.
- 이를 위해서 git 명령어 'branch'를 사용했다.
- 따라서 명령어 'branch'는 독립적인 작업 영역을 만들어주는 명령어이다. my_space에서 수정된 문서작업은 별다른 명령을 실행해주지 않으면 master branch에 영향을 미치지 않는다.
- **사용법**
> **git branch** : branch 확인  
**git branch branch_name** : branch_name이라는 branch 생성  
**git branch -d branch_name** : branch_name이라는 branch 삭제

- 사용 예시
![branch](https://user-images.githubusercontent.com/54767707/117507543-27bac580-afc2-11eb-8b3a-74b068bcb1a8.png)
*맨처음 branch 명령어를 실행했을 때, 'master'이라는 branch 밖에 없었다. 하지만 그 후 'git branch my_space'를 통해 'my_space'라는 독립적인 작업 영역을 만들어주었다.*

---

## **3. checkout**
- 현재 'master'라는 공간에서 작업을 하고 있었다.
- 하지만 'master'에서 벗어나 'my_space'라는 공간에서 작업을 하고 싶다.
- 이를 위해서 git 명령어 'checkout'을 사용했다.
- 따라서 명령어 'checkout'은 브랜치를 이동할 때 사용하는 명령어이다.
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

---

## **5. commit**

---

## **6. config**  

- 우선 git을 맨 처음 시작했을 때의 상태에 있다.
- 이 상태에서 사용자 이름과 이메일을 설정해주고 싶다. 왜냐하면 user가 설정되어 있지 않을 경우 Github에 push한다고 해도, commit count 집계도 안되고 해당 커밋의 작성자 프로필 아이콘도 ?로 표시되기 때문에 name과 email 주소를 설정한다.
- 이를 위해서 git 명령어 'config'를 사용했다.
- 따라서 'config' 명령어는 git의 일반적인 설정을 담당하는 명령어이다. 
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

## **7. init**

---

## **8. log**

---

## **9. merge**

---

## **10. pull**

---

## **11. push**
- 과제1 문서를 사진과 같이 수정한 상태이다.
![수정1_과제1](https://user-images.githubusercontent.com/54767707/117504440-6306c580-afbd-11eb-8aee-e1b20c6bd9ff.png)

- 이 수정한 문서를 원격저장소(GitHub)에도 올려 관리하고 싶다.  
- 이를 위해 git 명령어 'push'를 사용했다.
- 따라서 명령어 'push'는 외부에서 수정한 파일을 원격저장소(GitHub)에 새로 올리고 싶을 때 사용하는 명령어이다.
- **사용법**  
> **git push**

- 옵션
> git push 
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

---

## **14. reset**

- --hard

---

## **15. status**

- 1. 현재 생성 맨 처음 단계로, git과 GitHub repository를 연결하고 싶다.
- 2. 또한 문서들을 수정한 뒤, 현재 폴더상태를 확인하고 싶다.
- 이를 위해 git 명령어 'status'를 사용했다.  
~~*물론 연결시엔 status 말고도 다른 명령어들도 같이 사용함*~~

 - 따라서 'status' 명령어는 문서의 상태를 확인할 때 사용한다.  
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
|1|add|
|2|branch|
|3|checkout|
|4|clone|
|5|commit|
|6|config|O|
|7|init|
|8|log|
|9|merge|
|10|pull|
|11|push|O|
|12|rebase|
|13|remote|
|14|reset|
|15|status|O|
|16|tag|