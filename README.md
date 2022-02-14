# arm64_junk_code

arm64 junk code sample
<!-- SUBADD -->
```asm
.text:000000000005E138                 NOP                     ; SUB             X15, X15, X4
.text:000000000005E13C                 NOP                     ; ADD             X15, X15, X4

.text:000000000005E0BC                 NOP                     ; SUB             X0, X0, X1
.text:000000000005E0C0                 NOP                     ; ADD             X0, X0, X1
```

<!-- SUBSUB -->
```asm
.text:000000000005E134                 NOP                     ; SUB             X4, X15, X4
.text:000000000005E140                 NOP                     ; SUB             X4, X15, X4
```

<!-- ADDSUB -->
```asm
.text:000000000005E154                 NOP                     ; ADD             X12, X12, X0
.text:000000000005E158                 NOP                     ; SUB             X12, X12, X0

.text:000000000005E130                 NOP                     ; ADD             X15, X15, X4
.text:000000000005E144                 NOP                     ; SUB             X15, X15, X4

.text:000000000005E0B4                 NOP                     ; ADD             X0, X0, X1
.text:000000000005E0B8                 NOP                     ; SUB             X0, X0, X1
```

<!-- RBITRBIT -->
```asm
.text:000000000005E12C                 NOP                     ; RBIT            X15, X15
.text:000000000005E148                 NOP                     ; RBIT            X15, X15
```

<!-- ADD0  -->
```asm
.text:000000000005E160                 NOP                     ; ADD             X12, X12, #0
```

<!-- RBITRBIT -->
```asm
.text:000000000005E15C                 NOP                     ; RBIT            X12, X12
.text:000000000005E164                 NOP                     ; RBIT            X12, X12

.text:000000000005E0D4                 NOP                     ; RBIT            X0, X0
.text:000000000005E0D8                 NOP                     ; NOP; MOV             X0, X0
.text:000000000005E0DC                 NOP                     ; RBIT            X0, X0
```

<!-- SUBADDADD|SP|D -->
```asm
.text:000000000005E0E0                 NOP                     ; SUB             SP, SP, #0x40 ; '@'
.text:000000000005E0E4                 NOP                     ; ADD             SP, SP, #0x10
.text:000000000005E0E8                 NOP                     ; ADD             SP, SP, #0x30 ; '0'
```

<!-- SUBSUBADDSP -->
```
.text:00000000000495B8                 NOP                     ; SUB             SP, SP, #0x10
.text:00000000000495BC                 NOP                     ; SUB             SP, SP, #0x30 ; '0'
.text:00000000000495C0                 NOP                     ; ADD             SP, SP, #0x40 ; '@'
```

<!-- MOV -->
```asm
.text:000000000005E0D8                 NOP                     ; MOV             X0, X0
```

<!-- AND -->
```asm
.text:00000000000211E4                 NOP                     ; AND             X11, X11, X11
```

<!-- SUBADDNUMBER -->
```asm
.text:000000000001A764                 SUB             X16, X16, #0x7F
.text:000000000001A768                 ADD             X16, X16, #0x7F
```

<!-- SUBADDSP -->
```asm
.text:0000000000016568                 SUB             SP, SP, #0x10
.text:000000000001656C                 ADD             SP, SP, #0x10
```

<!-- ADDSUBADD_NUMBER -->
```asm
.text:00000000000165FC                 ADD             X10, X10, #0x54 ; 'T'
.text:0000000000016600                 SUB             X10, X10, #0xFE
.text:0000000000016604                 ADD             X10, X10, #0xAA
```

<!-- ADDSUB_NUMBER -->
```asm
.text:000000000007EAEC                 ADD             X0, X0, #0x5F ; '_'
.text:000000000007EAF0                 SUB             X0, X0, #0x5F ; '_'
```

<!-- SUBADDSUB_NUMBER -->
```asm
.text:000000000007EB60                 SUB             X14, X14, #0x3A ; ':'
.text:000000000007EB64                 ADD             X14, X14, #0xAE
.text:000000000007EB68                 SUB             X14, X14, #0x74
```

<!-- REVREV -->
```asm
.text:000000000007EB4C                 REV             X17, X17
.text:000000000007EB5C                 REV             X17, X17
```

<!-- ADDADDSUB|D -->
```asm
.text:000000000007FF84                 ADD             X5, X5, #0x1E
.text:000000000007FF88                 ADD             X5, X5, #0x3C ; '<'
.text:000000000007FF8C                 SUB             X5, X5, #0x5A
```

<!-- STPEORLDP| -->
```asm
.text:00000000000149A0                 STP             X4, X30, [SP,#-0x10]!
.text:00000000000149A4                 EOR             X4, X17, X14
.text:00000000000149A8                 LDP             X4, X30, [SP],#0x10
```

<!-- SUBADD|R -->
```asm
.text:000000000000929C                 SUB             X3, X3, X8
.text:00000000000092A8                 ADD             X3, X3, X8
```

<!-- STPLDP| -->
```asm
.text:0000000000067030                 STP             X6, X30, [SP,#-0x10]!
.text:0000000000067034                 LDP             X6, X30, [SP],#0x10
```
<!-- SUBSUBADD|SP|D -->
```asm
.text:0000000000066F58                 SUB             SP, SP, #0x30 ; '0'
.text:0000000000066F64                 SUB             SP, SP, #0x60 ; '`'
.text:0000000000066F70                 ADD             SP, SP, #0x90
```

<!-- SUB|0 -->
```asm
.text:0000000000066E98                 SUB             X4, X4, #0
```

<!-- STPLDRLDP|loc -->
```asm
.text:000000000007ECC0                 STP             X5, X30, [SP,#-0x10]!
.text:000000000007ECC4                 LDR             X5, loc_7ECBC
.text:000000000007ECC8                 LDP             X5, X30, [SP],#0x10
```

<!-- STPMOVLDP|-169 -->
```asm
.text:000000000005E4E8                 STP             X3, X30, [SP,#-0x10]!
.text:000000000005E4EC                 MOV             X3, #0xFFFFFFFFFFFFFF57
.text:000000000005E4F0                 LDP             X3, X30, [SP],#0x10
```

<!-- STPLDRLDP|SP -->
```asm
.text:000000000005E49C                 STP             X8, X30, [SP,#-0x10]!
.text:000000000005E4A0                 LDR             X8, [SP,#8]
.text:000000000005E4A4                 LDP             X8, X30, [SP],#0x10
```
<!-- STPANDLDP|R -->
```asm
.text:000000000003A4B8                 STP             X5, X30, [SP,#-0x10]!
.text:000000000003A4BC                 AND             X5, X2, X2
.text:000000000003A4C0                 LDP             X5, X30, [SP],#0x10
```

<!-- LDP|R -->
```asm
.text:000000000002B600                 LDR             X14, loc_2B600
.text:000000000002B604                 LDR             X14, unk_2B5FC
.text:000000000002B608                 LDR             X14, loc_2B600
.text:000000000002B60C
.text:000000000002B60C loc_2B60C                               ; DATA XREF: .text:loc_2B60C↓r
.text:000000000002B60C                 LDR             X14, loc_2B60C
.text:000000000002B610                 RBIT            X14, X1
.text:000000000002B614                 EOR             X14, X0, X7
.text:000000000002B618                 AND             X14, X4, X3
.text:000000000002B61C                 AND             X14, X13, X19
.text:000000000002B620                 LDP             X14, X30, [SP],#0x10
```

<!-- LDR -->
```asm
.text:000000000000B92C             loc_B92C                                ; DATA XREF: .text:loc_B92C↓r
.text:000000000000B92C 0B 00 00 58                 LDR             X11, loc_B92C
```


```asm
.text:0000000000043F50 E5 1F BF A9                 STP             X5, X7, [SP,#-0x10]!
.text:0000000000043F54 67 00 00 18                 LDR             W7, =0x91000084
.text:0000000000043F58 E7 7C 40 93                 SXTW            X7, W7
.text:0000000000043F5C 02 00 00 14                 B               loc_43F64
.text:0000000000043F5C             ; ---------------------------------------------------------------------------
.text:0000000000043F60 84 00 00 91 dword_43F60     DCD 0x91000084          ; DATA XREF: .text:0000000000043F54↑r
.text:0000000000043F64             ; ---------------------------------------------------------------------------
.text:0000000000043F64
.text:0000000000043F64             loc_43F64                               ; CODE XREF: .text:0000000000043F5C↑j
.text:0000000000043F64 1F 20 03 D5                 NOP
.text:0000000000043F68 84 00 07 4B                 SUB             W4, W4, W7
.text:0000000000043F6C A4 01 00 34                 CBZ             W4, loc_43FA0
.text:0000000000043F70 E0 07 BF A9                 STP             X0, X1, [SP,#-0x10]!
.text:0000000000043F74 E0 07 BF A9                 STP             X0, X1, [SP,#-0x10]!
.text:0000000000043F78 80 00 00 18                 LDR             W0, =0x1D280
.text:0000000000043F7C 00 7C 40 93                 SXTW            X0, W0
.text:0000000000043F80 41 00 00 10                 ADR             X1, dword_43F88
.text:0000000000043F84 02 00 00 14                 B               loc_43F8C
.text:0000000000043F84             ; ---------------------------------------------------------------------------
.text:0000000000043F88 80 D2 01 00 dword_43F88     DCD 0x1D280             ; DATA XREF: .text:0000000000043F78↑r
.text:0000000000043F88                                                     ; .text:0000000000043F80↑o
.text:0000000000043F8C             ; ---------------------------------------------------------------------------
.text:0000000000043F8C
.text:0000000000043F8C             loc_43F8C                               ; CODE XREF: .text:0000000000043F84↑j
.text:0000000000043F8C 00 00 01 8B                 ADD             X0, X0, X1
.text:0000000000043F90 E0 0F 00 F9                 STR             X0, [SP,#0x18]
.text:0000000000043F94 E0 07 C1 A8                 LDP             X0, X1, [SP],#0x10
.text:0000000000043F98 FE 07 40 F9                 LDR             X30, [SP,#8]
.text:0000000000043F9C FF 43 00 91                 ADD             SP, SP, #0x10
.text:0000000000043FA0
.text:0000000000043FA0             loc_43FA0                               ; CODE XREF: .text:0000000000043F6C↑j
.text:0000000000043FA0 E5 1F C1 A8                 LDP             X5, X7, [SP],#0x10
.text:0000000000043FA4 C0 03 1F D6                 BR              X30
```


```asm
.text:0000000000043788 E5 1F BF A9                 STP             X5, X7, [SP,#var_10]!
.text:000000000004378C 67 00 00 18                 LDR             W7, =0x91000084
.text:0000000000043790 E7 7C 40 93                 SXTW            X7, W7
.text:0000000000043794 02 00 00 14                 B               loc_4379C
.text:0000000000043794             ; ---------------------------------------------------------------------------
.text:0000000000043798 84 00 00 91 dword_43798     DCD 0x91000084          ; DATA XREF: sub_43788+4↑r
.text:000000000004379C             ; ---------------------------------------------------------------------------
.text:000000000004379C
.text:000000000004379C             loc_4379C                               ; CODE XREF: sub_43788+C↑j
.text:000000000004379C 1F 20 03 D5                 NOP
.text:00000000000437A0 84 00 07 4B                 SUB             W4, W4, W7
.text:00000000000437A4 A4 01 00 34                 CBZ             W4, loc_437D8
.text:00000000000437A8 E0 07 BF A9                 STP             X0, X1, [SP,#0x10+var_20]!
.text:00000000000437AC E0 07 BF A9                 STP             X0, X1, [SP,#0x20+var_30]!
.text:00000000000437B0 80 00 00 18                 LDR             W0, =0xFFFC07D0
.text:00000000000437B4 00 7C 40 93                 SXTW            X0, W0
.text:00000000000437B8 41 00 00 10                 ADR             X1, dword_437C0
.text:00000000000437BC 02 00 00 14                 B               loc_437C4
.text:00000000000437BC             ; ---------------------------------------------------------------------------
.text:00000000000437C0 D0 07 FC FF dword_437C0     DCD 0xFFFC07D0          ; DATA XREF: sub_43788+28↑r
.text:00000000000437C0                                                     ; sub_43788+30↑o
.text:00000000000437C4             ; ---------------------------------------------------------------------------
.text:00000000000437C4
.text:00000000000437C4             loc_437C4                               ; CODE XREF: sub_43788+34↑j
.text:00000000000437C4 00 00 01 8B                 ADD             X0, X0, X1
.text:00000000000437C8 E0 0F 00 F9                 STR             X0, [SP,#0x30+var_18]
.text:00000000000437CC E0 07 C1 A8                 LDP             X0, X1, [SP+0x30+var_30],#0x10
.text:00000000000437D0 FE 07 40 F9                 LDR             X30, [SP,#0x20+var_18]
.text:00000000000437D4 FF 43 00 91                 ADD             SP, SP, #0x10
.text:00000000000437D8
.text:00000000000437D8             loc_437D8                               ; CODE XREF: sub_43788+1C↑j
.text:00000000000437D8 E5 1F C1 A8                 LDP             X5, X7, [SP+0x10+var_10],#0x10
.text:00000000000437DC C0 03 1F D6                 BR              X30
```


```asm
.text:00000000000045B0 04 00 00 14                 B               loc_45C0
.text:00000000000045B0             ; ---------------------------------------------------------------------------
.text:00000000000045B4 77 01 05 00 dword_45B4      DCD 0x50177             ; DATA XREF: .text:0000000000004574↑r
.text:00000000000045B4                                                     ; .text:00000000000045A4↑o
.text:00000000000045B8             ; ---------------------------------------------------------------------------
.text:00000000000045B8 1F 20 03 D5                 NOP
.text:00000000000045BC F1 07 40 F9                 LDR             X17, [SP,#8]
.text:00000000000045C0
.text:00000000000045C0             loc_45C0                                ; CODE XREF: .text:00000000000045B0↑j
.text:00000000000045C0 00 00 01 8B                 ADD             X0, X0, X1
.text:00000000000045C4 1F 20 03 D5                 NOP
```


```asm
.text:0000000000052F68 E0 07 BF A9                 STP             X0, X1, [SP,#0x20+var_30]!
.text:0000000000052F6C 20 01 09 8B                 ADD             X0, X9, X9
.text:0000000000052F70 00 02 04 8A                 AND             X0, X16, X4
.text:0000000000052F74 00 02 00 18                 LDR             W0, qword_52FB4
.text:0000000000052F78 1F 20 03 D5                 NOP
.text:0000000000052F7C 1F 20 03 D5                 NOP
.text:0000000000052F80 1F 20 03 D5                 NOP
.text:0000000000052F84
.text:0000000000052F84             loc_52F84                               ; DATA XREF: sub_52F48:loc_52F84↓r
.text:0000000000052F84 01 00 00 58                 LDR             X1, loc_52F84
.text:0000000000052F88 00 7C 40 93                 SXTW            X0, W0
.text:0000000000052F8C 1F 20 03 D5                 NOP
.text:0000000000052F90 81 FE FF 58                 LDR             X1, loc_52F60 ; SUB             SP, SP, #0x10
.text:0000000000052F94 01 02 03 AA                 ORR             X1, X16, X3
.text:0000000000052F98
.text:0000000000052F98             loc_52F98                               ; DATA XREF: sub_52F48+58↓r
.text:0000000000052F98 41 01 0D CB                 SUB             X1, X10, X13
.text:0000000000052F9C 1F 20 03 D5                 NOP
.text:0000000000052FA0 C1 FF FF 58                 LDR             X1, loc_52F98
.text:0000000000052FA4 81 00 00 10                 ADR             X1, qword_52FB4
.text:0000000000052FA8 1F 20 03 D5                 NOP
.text:0000000000052FAC 1F 20 03 D5                 NOP
.text:0000000000052FB0 04 00 00 14                 B               loc_52FC0
.text:0000000000052FB0             ; ---------------------------------------------------------------------------
.text:0000000000052FB4 49 B8 FC FF+qword_52FB4     DCQ 0xCB080164FFFCB849  ; DATA XREF: sub_52F48+2C↑r
.text:0000000000052FB4 64 01 08 CB                                         ; sub_52F48+5C↑o ...
.text:0000000000052FBC             ; ---------------------------------------------------------------------------
.text:0000000000052FBC C4 FF FF 58                 LDR             X4, =0xCB080164FFFCB849
.text:0000000000052FC0
.text:0000000000052FC0             loc_52FC0                               ; CODE XREF: sub_52F48+68↑j
.text:0000000000052FC0 00 00 01 8B                 ADD             X0, X0, X1
.text:0000000000052FC4 1F 20 03 D5                 NOP
.text:0000000000052FC8 1F 20 03 D5                 NOP
.text:0000000000052FCC E4 07 40 F9                 LDR             X4, [SP,#0x30+var_28]
.text:0000000000052FD0 E4 03 80 D2                 MOV             X4, #0x1F
.text:0000000000052FD4 E0 0F 00 F9                 STR             X0, [SP,#0x30+var_18]
.text:0000000000052FD8
.text:0000000000052FD8             loc_52FD8                               ; DATA XREF: sub_52F48:loc_52FD8↓r
.text:0000000000052FD8 04 00 00 58                 LDR             X4, loc_52FD8
.text:0000000000052FDC
.text:0000000000052FDC             loc_52FDC                               ; DATA XREF: sub_52F48+9C↓r
.text:0000000000052FDC 44 17 80 92                 MOV             X4, #0xFFFFFFFFFFFFFF45
.text:0000000000052FE0 1F 20 03 D5                 NOP
.text:0000000000052FE4 C0 FF FF 58                 LDR             X0, loc_52FDC
.text:0000000000052FE8 E0 07 C1 A8                 LDP             X0, X1, [SP+0x30+var_30],#0x10
```


<!-- 巨坑 -->

![20220213005951](https://cdn.jsdelivr.net/gh/nzcv/picgo/20220213005951.png)

![20220213012212](https://cdn.jsdelivr.net/gh/nzcv/picgo/20220213012212.png)

![20220213013806](https://cdn.jsdelivr.net/gh/nzcv/picgo/20220213013806.png)

![20220213023559](https://cdn.jsdelivr.net/gh/nzcv/picgo/20220213023559.png)
