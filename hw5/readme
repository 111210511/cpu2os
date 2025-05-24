## 李昱欣

產生組合語言.s檔
```
gcc -S power.c -o power.s
```

產生目的檔.o檔
```
gcc -c power.c -o power.o
```
將該目的檔反組譯
```
objdump -d power.o
```
```sh
power.o:     file format elf64-x86-64


Disassembly of section .text:

0000000000000000 <power>:
   0:	55                   	push   %rbp
   1:	48 89 e5             	mov    %rsp,%rbp
   4:	89 7d fc             	mov    %edi,-0x4(%rbp)
   7:	89 75 f8             	mov    %esi,-0x8(%rbp)
   a:	c7 45 f4 01 00 00 00 	movl   $0x1,-0xc(%rbp)
  11:	c7 45 f0 00 00 00 00 	movl   $0x0,-0x10(%rbp)
  18:	eb 16                	jmp    30 <power+0x30>
  1a:	8b 45 f4             	mov    -0xc(%rbp),%eax
  1d:	0f af 45 fc          	imul   -0x4(%rbp),%eax
  21:	89 45 f4             	mov    %eax,-0xc(%rbp)
  24:	83 45 f0 01          	addl   $0x1,-0x10(%rbp)
  28:	8b 45 f0             	mov    -0x10(%rbp),%eax
  2b:	3b 45 f8             	cmp    -0x8(%rbp),%eax
  2e:	7c ea                	jl     1a <power+0x1a>
  30:	8b 45 f4             	mov    -0xc(%rbp),%eax
  33:	5d                   	pop    %rbp
  34:	c3                   	ret    

0000000000000035 <main>:
  35:	55                   	push   %rbp
  36:	48 89 e5             	mov    %rsp,%rbp
  39:	be 03 00 00 00       	mov    $0x3,%esi
  3e:	bf 02 00 00 00       	mov    $0x2,%edi
  43:	e8 b8 ff ff ff       	callq  0 <power>
  48:	5d                   	pop    %rbp
  49:	c3                   	ret
  ```
  印出該目的檔的表頭
  ```
  objdump -h power.o
  ```
  ```
  power.o:     file format elf64-x86-64

Sections:
Idx Name          Size      VMA       LMA       File off  Algn
  0 .text         0000004a  00000000  00000000  00000040  2**4
                  CONTENTS, ALLOC, LOAD, RELOC, READONLY, CODE
  1 .data         00000000  00000000  00000000  0000008a  2**2
                  CONTENTS, ALLOC, LOAD, DATA
  2 .bss          00000000  00000000  00000000  0000008a  2**2
                  ALLOC
  3 .comment      0000001e  00000000  00000000  0000008a  2**0
                  CONTENTS, READONLY
  4 .note.GNU-stack 00000000 00000000 00000000 000000a8  2**0
                  CONTENTS, READONLY
```
