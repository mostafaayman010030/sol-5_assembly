.586
.MODEL FLAT
INCLUDE io.h
.STACK 4096

.DATA
	 y BYTE "Enter Number  ",0
	 x BYTE "The value is " , 0
	 e1 DWORD 11 , 0
	res DWORD 11 DUP(?)

.CODE
	_MainProc PROC

	   input y , e1 , 11
	   atod e1
	   mov ebx , eax
  
       input y , e1 , 11
	   atod e1
	   mov ecx , eax

	   input y , e1 , 11
       atod e1
	 
		 
	   
	   add ebx , ecx
	   imul ebx , 2
	   add ebx , eax
	    
	   dtoa res , ebx
	   output x , res
	  
		mov eax , 0
		ret
	_MainProc ENDP

END