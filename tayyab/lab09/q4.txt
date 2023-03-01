; Program Template           (Template.asm)

; Program Description:
; Author:
; Creation Date:
; Revisions: 
; Date:              Modified by:
include irvine32.inc
.386
.model flat,stdcall
.stack 4096
ExitProcess PROTO, dwExitCode:DWORD
.data
; declare variables here
     fmsg byte "Welcome to Studytonight :-) ",0
	 smsg byte "=====  Program to Determine whether String is Palindrome or not, in CPP  ===== ",0
	 cvar dword 'a'
	 n1 dword ?
	 i dword 0
	 s1 dword 100 dup(?)
	 msg byte "Enter the String you want to check : ",0
.code
main PROC
	; write your code here
	call crlf
	call crlf
	mov edx,offset fmsg
	call writestring
	call crlf
	call crlf
	call crlf

	mov edx,offset smsg
	call writestring
	call crlf
	call crlf
	call crlf
	call crlf

	mov edx,offset msg
	call writestring
	call readstring
	call writestring



	INVOKE ExitProcess,0
main ENDP
; (insert additional procedures here)
END main