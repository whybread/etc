
# Ubuntu Guide
## 0. README
This document is actually made for myself to study and store as much as I can about ubuntu os and bash shell executed on it,
and I just studied from these sites below.

- [R.U Ready? :: 리눅스 계정 관리](https://psman2.tistory.com/entry/%EB%A6%AC%EB%88%85%EC%8A%A4-%EA%B3%84%EC%A0%95-%EA%B4%80%EB%A6%AC)

- [[UNIX / Lunux] 사용자 정보, 그룹 정보 :: 오늘도 난, 하하하](https://eunguru.tistory.com/88?category=667830)

## 1. Users and Groups
### 1-1. Users
There are three types of users in ubuntu.

1. Administrative account (Super user)
2. Regular account (Normal)
3. Service account (System account)
### 1-2. User Manager
When you startup your ubuntu in GUI mode, you will see your all user accounts listed on the screen in the login phase.

1. When your system uses `AccountsService`

	In this case, you  **can not**  hide a user from the greeter screen by reconfiguring  `lightdm`  because it defers to  `AccountsService`. That is stated very clearly in the comments in  `/etc/lightdm/users.conf`.
	
	To hide a user named  `XXX`, create a file named

	```
	/var/lib/AccountsService/users/XXX
	```
	containing two lines:
	```
	[User]
	SystemAccount=true
	```
	If the file already exists, make sure you append the  `SystemAccount=true`  line to the  `[User]`  section.

2. Otherwise, you can modify the file: `/etc/lightdm/users.conf`.

> For more information, see this reference: [lightdm - How do I hide a particular user from the login screen? - Ask Ubuntu](https://askubuntu.com/questions/92349/how-do-i-hide-a-particular-user-from-the-login-screen).
