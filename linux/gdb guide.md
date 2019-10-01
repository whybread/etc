# GDB Guide

### TUI모드 여는 단축키

	ctrl + xa

### gdb로 프로그램 실행할 때 args 주는 법

	$gdb --args path/to/executable -every -arg you can=think < of
예를 들어 원래

	$bomb input.txt
위의 명령어는

	$gdb --args bomb input.txt
아래와 같이 쓸 수 있다.
