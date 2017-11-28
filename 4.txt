.586
.MODEL FLAT
INCLUDE io.h
.STACK 4096

.DATA
     
	 y BYTE " Enter Number of Pennies " , 0 
	 x BYTE " Enter Number of Nickels" , 0
	 y1 BYTE "Enter Number of Dimes" , 0 
	 x1 BYTE "Enter Number of  Quarters" , 0
	 y2 BYTE "Enter Number of Fifty-cent pieces" , 0 
	 x2 BYTE "Enter Number of Dollar " , 0
	 y3 BYTE "The Total Value of The Coins" , 0 
	 x3 BYTE "The Number of  Coins " , 0
	 

	 e1 DWORD 11 , 0
	 e2 DWORD 11 , 0
	res DWORD 11 DUP(?)

.CODE
	_MainProc PROC

	   input y , e1 , 11
	   atod e1
	   mov ebx , eax
	   mov ecx , eax

	   input x , e2 , 11
	   atod e2
	   add ecx , eax
	   imul eax , 5
	   add ebx ,eax
       

       input y1 , e2 , 11
	   atod e2
	   add ecx , eax
	   imul eax , 10
	   add ebx ,eax

	   input x1 , e2 , 11
	   atod e2
	   add ecx , eax
	   imul  eax , 25
       add ebx ,eax
	   
	  input y2 , e2 , 11
	   atod e2
	   add ecx , eax
	   imul eax , 50
	   add ebx ,eax

	   input x2 , e2 , 11
	   atod e2
	   add ecx , eax
	   imul  eax , 100
       add ebx ,eax


	  

	   dtoa res , ebx
	   output y3 , res

	  dtoa res , ecx
	   output x3 , res

	  

		mov eax , 0
		ret
	_MainProc ENDP

END