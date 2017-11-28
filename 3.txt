.586
.MODEL FLAT
INCLUDE io.h
.STACK 4096

.DATA
	 y BYTE "Enter Length  ",0
	 d BYTE "Enter Width  ",0
	 x BYTE "The Rectangle’s perimeter is " , 0
	 e1 DWORD 11 , 0
	res DWORD 11 DUP(?)

.CODE
	_MainProc PROC

	   input y , e1 , 11
	   atod e1
	   mov ebx , eax
  
       input d , e1 , 11
	   atod e1


	   add ebx , eax
	   imul ebx , 2
	   
	    
	  dtoa res , ebx
	  output x , res
	  
		mov eax , 0
		ret
	_MainProc ENDP

END