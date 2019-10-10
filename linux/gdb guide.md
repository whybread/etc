# GDB Guide

This document is written with reference to the sites below.

- [gdb 자주 쓰이는 명령어들 정리 :: Unique Life](https://horae.tistory.com/entry/gdb-%EC%9E%90%EC%A3%BC-%EC%93%B0%EC%9D%B4%EB%8A%94-%EB%AA%85%EB%A0%B9%EC%96%B4%EB%93%A4-%EC%A0%95%EB%A6%AC)

### TUI모드 여는 단축키

	ctrl + xa

### gdb로 프로그램 실행할 때 args 주는 법

	$gdb --args path/to/executable -every -arg you can=think < of
다음의 두 명령어를 비교해보면 이해할 수 있다.

	$bomb input.txt
	$gdb --args bomb input.txt
그냥 gdb bomb으로 프로그램을 실행한 후, gdb 내부에서 run할 때 args를 주는 방법도 있다.
	
	(gdb)run input.txt

### 레지스터 확인

	(gdb)info reg
	(gdb)info regsisters

### 메모리 확인
esp 레지스터가 가리키는 메모리로부터 높은 주소쪽으로 4byte씩 20개 값을 16진수로 출력

	(gdb)x/20wx $esp
eip 레지스터가 가리키는 메모리의 명령어로부터 10줄의 어셈블리어를 출력

	(gdb)x/10i $eip
메모리 주소 0x8040000에서 시작하는 문자열을 출력

	(gdb)x/s 0x8040000
