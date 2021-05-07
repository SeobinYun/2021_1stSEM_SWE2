# 2021_1stSEM_SWE2

git & GitHub 연습

## GitHub Repository URL

<https://github.com/SeobinYun/2021_1stSEM_SWE2>

---

## **1. add**

---

## **2. branch**

---

## **3. checkout**

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

- 확인

![이름이메일설정](https://user-images.githubusercontent.com/54767707/117499518-4c10a500-afb6-11eb-9369-9b18dda5acd5.png)

> 설정 후
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
- 2. 또한 문서들을 수정한 뒤 GitHub에 올릴 때, 현재 폴더상태를 확인하고 싶다.
- 이를 위해 git 명령어 'status'를 사용했다.  
~~*물론 연결시엔 status 말고도 다른 명령어들도 같이 사용함*~~

 - 따라서 'status' 명령어는 문서의 상태를 확인할 때 사용한다.  
 - **사용법**  
 > **git status (option)**
 - **옵션**
> '-s' : 파일의 상태를 짧게 보고싶을 경우 사용  

- 확인
> ㄱ. 1번 상황  
![git과github연결1](https://user-images.githubusercontent.com/54767707/117502802-02768900-afbb-11eb-936e-7ca0e8cf9309.png)

> ㄴ. 2번 상황 & 옵션 '-s' 사용
![수정1했을때 상태](https://user-images.githubusercontent.com/54767707/117502821-099d9700-afbb-11eb-9489-1f20c7f769db.png)  
 
---

## **16. tag**
