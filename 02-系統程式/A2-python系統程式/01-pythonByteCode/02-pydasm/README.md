

```
(base) cccimac@cccimacdeiMac 02-pycompile % python pycompile1.py
(base) cccimac@cccimacdeiMac 02-pycompile % python __pycache__/example.cpython-312.pyc
add(2,3)= 5
(base) cccimac@cccimacdeiMac 02-pycompile % python compile.py
(base) cccimac@cccimacdeiMac 02-pycompile % python dasm.py   
  0           0 RESUME                   0

  1           2 LOAD_CONST               0 (<code object add at 0x105283910, file "example.py", line 1>)
              4 MAKE_FUNCTION            0
              6 STORE_NAME               0 (add)

  4           8 PUSH_NULL
             10 LOAD_NAME                1 (print)
             12 LOAD_CONST               1 ('add(2,3)=')
             14 PUSH_NULL
             16 LOAD_NAME                0 (add)
             18 LOAD_CONST               2 (2)
             20 LOAD_CONST               3 (3)
             22 CALL                     2
             30 CALL                     2
             38 POP_TOP
             40 RETURN_CONST             4 (None)

Disassembly of <code object add at 0x105283910, file "example.py", line 1>:
  1           0 RESUME                   0

  2           2 LOAD_FAST                0 (a)
              4 LOAD_FAST                1 (b)
              6 BINARY_OP                0 (+)
             10 RETURN_VALUE
(base) cccimac@cccimacdeiMac 02-pycompile % python dasm1by1.py
        0       RESUME
1       2       LOAD_CONST
        4       MAKE_FUNCTION
        6       STORE_NAME
4       8       PUSH_NULL
        10      LOAD_NAME       1
        12      LOAD_CONST      1
        14      PUSH_NULL
        16      LOAD_NAME
        18      LOAD_CONST      2
        20      LOAD_CONST      3
        22      CALL    2
        30      CALL    2
        38      POP_TOP
        40      RETURN_CONST    4
```