
; You may customize this and other start-up templates; 
; The location of this template is c:\emu8086\inc\0_com_template.txt

include emu8086.inc
.model small
.stack 100h
.data      
.code

main proc 

mov bx,1    

out_loop:
mov cx,bx

in_loop:

mov ah,02h
mov dl,'*'
int 21h 

dec cx

cmp cx,0
jne in_loop
printn 
inc bx

cmp bx,5

jle out_loop



ret
    
    

ret




