                                      1 ;--------------------------------------------------------
                                      2 ; File Created by SDCC : free open source ANSI-C Compiler
                                      3 ; Version 3.8.7 #11151 (MINGW64)
                                      4 ;--------------------------------------------------------
                                      5 	.module main
                                      6 	.optsdcc -mmcs51 --model-small
                                      7 	
                                      8 ;--------------------------------------------------------
                                      9 ; Public variables in this module
                                     10 ;--------------------------------------------------------
                                     11 	.globl _main
                                     12 	.globl _KeyDown
                                     13 	.globl _delay
                                     14 	.globl _TF2
                                     15 	.globl _EXF2
                                     16 	.globl _RCLK
                                     17 	.globl _TCLK
                                     18 	.globl _EXEN2
                                     19 	.globl _TR2
                                     20 	.globl _C_T2
                                     21 	.globl _CP_RL2
                                     22 	.globl _T2CON_7
                                     23 	.globl _T2CON_6
                                     24 	.globl _T2CON_5
                                     25 	.globl _T2CON_4
                                     26 	.globl _T2CON_3
                                     27 	.globl _T2CON_2
                                     28 	.globl _T2CON_1
                                     29 	.globl _T2CON_0
                                     30 	.globl _PT2
                                     31 	.globl _ET2
                                     32 	.globl _CY
                                     33 	.globl _AC
                                     34 	.globl _F0
                                     35 	.globl _RS1
                                     36 	.globl _RS0
                                     37 	.globl _OV
                                     38 	.globl _F1
                                     39 	.globl _P
                                     40 	.globl _PS
                                     41 	.globl _PT1
                                     42 	.globl _PX1
                                     43 	.globl _PT0
                                     44 	.globl _PX0
                                     45 	.globl _RD
                                     46 	.globl _WR
                                     47 	.globl _T1
                                     48 	.globl _T0
                                     49 	.globl _INT1
                                     50 	.globl _INT0
                                     51 	.globl _TXD
                                     52 	.globl _RXD
                                     53 	.globl _P3_7
                                     54 	.globl _P3_6
                                     55 	.globl _P3_5
                                     56 	.globl _P3_4
                                     57 	.globl _P3_3
                                     58 	.globl _P3_2
                                     59 	.globl _P3_1
                                     60 	.globl _P3_0
                                     61 	.globl _EA
                                     62 	.globl _ES
                                     63 	.globl _ET1
                                     64 	.globl _EX1
                                     65 	.globl _ET0
                                     66 	.globl _EX0
                                     67 	.globl _P2_7
                                     68 	.globl _P2_6
                                     69 	.globl _P2_5
                                     70 	.globl _P2_4
                                     71 	.globl _P2_3
                                     72 	.globl _P2_2
                                     73 	.globl _P2_1
                                     74 	.globl _P2_0
                                     75 	.globl _SM0
                                     76 	.globl _SM1
                                     77 	.globl _SM2
                                     78 	.globl _REN
                                     79 	.globl _TB8
                                     80 	.globl _RB8
                                     81 	.globl _TI
                                     82 	.globl _RI
                                     83 	.globl _P1_7
                                     84 	.globl _P1_6
                                     85 	.globl _P1_5
                                     86 	.globl _P1_4
                                     87 	.globl _P1_3
                                     88 	.globl _P1_2
                                     89 	.globl _P1_1
                                     90 	.globl _P1_0
                                     91 	.globl _TF1
                                     92 	.globl _TR1
                                     93 	.globl _TF0
                                     94 	.globl _TR0
                                     95 	.globl _IE1
                                     96 	.globl _IT1
                                     97 	.globl _IE0
                                     98 	.globl _IT0
                                     99 	.globl _P0_7
                                    100 	.globl _P0_6
                                    101 	.globl _P0_5
                                    102 	.globl _P0_4
                                    103 	.globl _P0_3
                                    104 	.globl _P0_2
                                    105 	.globl _P0_1
                                    106 	.globl _P0_0
                                    107 	.globl _TH2
                                    108 	.globl _TL2
                                    109 	.globl _RCAP2H
                                    110 	.globl _RCAP2L
                                    111 	.globl _T2CON
                                    112 	.globl _B
                                    113 	.globl _ACC
                                    114 	.globl _PSW
                                    115 	.globl _IP
                                    116 	.globl _P3
                                    117 	.globl _IE
                                    118 	.globl _P2
                                    119 	.globl _SBUF
                                    120 	.globl _SCON
                                    121 	.globl _P1
                                    122 	.globl _TH1
                                    123 	.globl _TH0
                                    124 	.globl _TL1
                                    125 	.globl _TL0
                                    126 	.globl _TMOD
                                    127 	.globl _TCON
                                    128 	.globl _PCON
                                    129 	.globl _DPH
                                    130 	.globl _DPL
                                    131 	.globl _SP
                                    132 	.globl _P0
                                    133 	.globl _KeyValue
                                    134 ;--------------------------------------------------------
                                    135 ; special function registers
                                    136 ;--------------------------------------------------------
                                    137 	.area RSEG    (ABS,DATA)
      000000                        138 	.org 0x0000
                           000080   139 _P0	=	0x0080
                           000081   140 _SP	=	0x0081
                           000082   141 _DPL	=	0x0082
                           000083   142 _DPH	=	0x0083
                           000087   143 _PCON	=	0x0087
                           000088   144 _TCON	=	0x0088
                           000089   145 _TMOD	=	0x0089
                           00008A   146 _TL0	=	0x008a
                           00008B   147 _TL1	=	0x008b
                           00008C   148 _TH0	=	0x008c
                           00008D   149 _TH1	=	0x008d
                           000090   150 _P1	=	0x0090
                           000098   151 _SCON	=	0x0098
                           000099   152 _SBUF	=	0x0099
                           0000A0   153 _P2	=	0x00a0
                           0000A8   154 _IE	=	0x00a8
                           0000B0   155 _P3	=	0x00b0
                           0000B8   156 _IP	=	0x00b8
                           0000D0   157 _PSW	=	0x00d0
                           0000E0   158 _ACC	=	0x00e0
                           0000F0   159 _B	=	0x00f0
                           0000C8   160 _T2CON	=	0x00c8
                           0000CA   161 _RCAP2L	=	0x00ca
                           0000CB   162 _RCAP2H	=	0x00cb
                           0000CC   163 _TL2	=	0x00cc
                           0000CD   164 _TH2	=	0x00cd
                                    165 ;--------------------------------------------------------
                                    166 ; special function bits
                                    167 ;--------------------------------------------------------
                                    168 	.area RSEG    (ABS,DATA)
      000000                        169 	.org 0x0000
                           000080   170 _P0_0	=	0x0080
                           000081   171 _P0_1	=	0x0081
                           000082   172 _P0_2	=	0x0082
                           000083   173 _P0_3	=	0x0083
                           000084   174 _P0_4	=	0x0084
                           000085   175 _P0_5	=	0x0085
                           000086   176 _P0_6	=	0x0086
                           000087   177 _P0_7	=	0x0087
                           000088   178 _IT0	=	0x0088
                           000089   179 _IE0	=	0x0089
                           00008A   180 _IT1	=	0x008a
                           00008B   181 _IE1	=	0x008b
                           00008C   182 _TR0	=	0x008c
                           00008D   183 _TF0	=	0x008d
                           00008E   184 _TR1	=	0x008e
                           00008F   185 _TF1	=	0x008f
                           000090   186 _P1_0	=	0x0090
                           000091   187 _P1_1	=	0x0091
                           000092   188 _P1_2	=	0x0092
                           000093   189 _P1_3	=	0x0093
                           000094   190 _P1_4	=	0x0094
                           000095   191 _P1_5	=	0x0095
                           000096   192 _P1_6	=	0x0096
                           000097   193 _P1_7	=	0x0097
                           000098   194 _RI	=	0x0098
                           000099   195 _TI	=	0x0099
                           00009A   196 _RB8	=	0x009a
                           00009B   197 _TB8	=	0x009b
                           00009C   198 _REN	=	0x009c
                           00009D   199 _SM2	=	0x009d
                           00009E   200 _SM1	=	0x009e
                           00009F   201 _SM0	=	0x009f
                           0000A0   202 _P2_0	=	0x00a0
                           0000A1   203 _P2_1	=	0x00a1
                           0000A2   204 _P2_2	=	0x00a2
                           0000A3   205 _P2_3	=	0x00a3
                           0000A4   206 _P2_4	=	0x00a4
                           0000A5   207 _P2_5	=	0x00a5
                           0000A6   208 _P2_6	=	0x00a6
                           0000A7   209 _P2_7	=	0x00a7
                           0000A8   210 _EX0	=	0x00a8
                           0000A9   211 _ET0	=	0x00a9
                           0000AA   212 _EX1	=	0x00aa
                           0000AB   213 _ET1	=	0x00ab
                           0000AC   214 _ES	=	0x00ac
                           0000AF   215 _EA	=	0x00af
                           0000B0   216 _P3_0	=	0x00b0
                           0000B1   217 _P3_1	=	0x00b1
                           0000B2   218 _P3_2	=	0x00b2
                           0000B3   219 _P3_3	=	0x00b3
                           0000B4   220 _P3_4	=	0x00b4
                           0000B5   221 _P3_5	=	0x00b5
                           0000B6   222 _P3_6	=	0x00b6
                           0000B7   223 _P3_7	=	0x00b7
                           0000B0   224 _RXD	=	0x00b0
                           0000B1   225 _TXD	=	0x00b1
                           0000B2   226 _INT0	=	0x00b2
                           0000B3   227 _INT1	=	0x00b3
                           0000B4   228 _T0	=	0x00b4
                           0000B5   229 _T1	=	0x00b5
                           0000B6   230 _WR	=	0x00b6
                           0000B7   231 _RD	=	0x00b7
                           0000B8   232 _PX0	=	0x00b8
                           0000B9   233 _PT0	=	0x00b9
                           0000BA   234 _PX1	=	0x00ba
                           0000BB   235 _PT1	=	0x00bb
                           0000BC   236 _PS	=	0x00bc
                           0000D0   237 _P	=	0x00d0
                           0000D1   238 _F1	=	0x00d1
                           0000D2   239 _OV	=	0x00d2
                           0000D3   240 _RS0	=	0x00d3
                           0000D4   241 _RS1	=	0x00d4
                           0000D5   242 _F0	=	0x00d5
                           0000D6   243 _AC	=	0x00d6
                           0000D7   244 _CY	=	0x00d7
                           0000AD   245 _ET2	=	0x00ad
                           0000BD   246 _PT2	=	0x00bd
                           0000C8   247 _T2CON_0	=	0x00c8
                           0000C9   248 _T2CON_1	=	0x00c9
                           0000CA   249 _T2CON_2	=	0x00ca
                           0000CB   250 _T2CON_3	=	0x00cb
                           0000CC   251 _T2CON_4	=	0x00cc
                           0000CD   252 _T2CON_5	=	0x00cd
                           0000CE   253 _T2CON_6	=	0x00ce
                           0000CF   254 _T2CON_7	=	0x00cf
                           0000C8   255 _CP_RL2	=	0x00c8
                           0000C9   256 _C_T2	=	0x00c9
                           0000CA   257 _TR2	=	0x00ca
                           0000CB   258 _EXEN2	=	0x00cb
                           0000CC   259 _TCLK	=	0x00cc
                           0000CD   260 _RCLK	=	0x00cd
                           0000CE   261 _EXF2	=	0x00ce
                           0000CF   262 _TF2	=	0x00cf
                                    263 ;--------------------------------------------------------
                                    264 ; overlayable register banks
                                    265 ;--------------------------------------------------------
                                    266 	.area REG_BANK_0	(REL,OVR,DATA)
      000000                        267 	.ds 8
                                    268 ;--------------------------------------------------------
                                    269 ; internal ram data
                                    270 ;--------------------------------------------------------
                                    271 	.area DSEG    (DATA)
      000008                        272 _KeyValue::
      000008                        273 	.ds 1
                                    274 ;--------------------------------------------------------
                                    275 ; overlayable items in internal ram 
                                    276 ;--------------------------------------------------------
                                    277 	.area	OSEG    (OVR,DATA)
                                    278 ;--------------------------------------------------------
                                    279 ; Stack segment in internal ram 
                                    280 ;--------------------------------------------------------
                                    281 	.area	SSEG
      000009                        282 __start__stack:
      000009                        283 	.ds	1
                                    284 
                                    285 ;--------------------------------------------------------
                                    286 ; indirectly addressable internal ram data
                                    287 ;--------------------------------------------------------
                                    288 	.area ISEG    (DATA)
                                    289 ;--------------------------------------------------------
                                    290 ; absolute internal ram data
                                    291 ;--------------------------------------------------------
                                    292 	.area IABS    (ABS,DATA)
                                    293 	.area IABS    (ABS,DATA)
                                    294 ;--------------------------------------------------------
                                    295 ; bit data
                                    296 ;--------------------------------------------------------
                                    297 	.area BSEG    (BIT)
                                    298 ;--------------------------------------------------------
                                    299 ; paged external ram data
                                    300 ;--------------------------------------------------------
                                    301 	.area PSEG    (PAG,XDATA)
                                    302 ;--------------------------------------------------------
                                    303 ; external ram data
                                    304 ;--------------------------------------------------------
                                    305 	.area XSEG    (XDATA)
                                    306 ;--------------------------------------------------------
                                    307 ; absolute external ram data
                                    308 ;--------------------------------------------------------
                                    309 	.area XABS    (ABS,XDATA)
                                    310 ;--------------------------------------------------------
                                    311 ; external initialized ram data
                                    312 ;--------------------------------------------------------
                                    313 	.area XISEG   (XDATA)
                                    314 	.area HOME    (CODE)
                                    315 	.area GSINIT0 (CODE)
                                    316 	.area GSINIT1 (CODE)
                                    317 	.area GSINIT2 (CODE)
                                    318 	.area GSINIT3 (CODE)
                                    319 	.area GSINIT4 (CODE)
                                    320 	.area GSINIT5 (CODE)
                                    321 	.area GSINIT  (CODE)
                                    322 	.area GSFINAL (CODE)
                                    323 	.area CSEG    (CODE)
                                    324 ;--------------------------------------------------------
                                    325 ; interrupt vector 
                                    326 ;--------------------------------------------------------
                                    327 	.area HOME    (CODE)
      000000                        328 __interrupt_vect:
      000000 02 00 06         [24]  329 	ljmp	__sdcc_gsinit_startup
                                    330 ;--------------------------------------------------------
                                    331 ; global & static initialisations
                                    332 ;--------------------------------------------------------
                                    333 	.area HOME    (CODE)
                                    334 	.area GSINIT  (CODE)
                                    335 	.area GSFINAL (CODE)
                                    336 	.area GSINIT  (CODE)
                                    337 	.globl __sdcc_gsinit_startup
                                    338 	.globl __sdcc_program_startup
                                    339 	.globl __start__stack
                                    340 	.globl __mcs51_genXINIT
                                    341 	.globl __mcs51_genXRAMCLEAR
                                    342 	.globl __mcs51_genRAMCLEAR
                                    343 	.area GSFINAL (CODE)
      00005F 02 00 03         [24]  344 	ljmp	__sdcc_program_startup
                                    345 ;--------------------------------------------------------
                                    346 ; Home
                                    347 ;--------------------------------------------------------
                                    348 	.area HOME    (CODE)
                                    349 	.area HOME    (CODE)
      000003                        350 __sdcc_program_startup:
      000003 02 01 02         [24]  351 	ljmp	_main
                                    352 ;	return from main will return to caller
                                    353 ;--------------------------------------------------------
                                    354 ; code
                                    355 ;--------------------------------------------------------
                                    356 	.area CSEG    (CODE)
                                    357 ;------------------------------------------------------------
                                    358 ;Allocation info for local variables in function 'delay'
                                    359 ;------------------------------------------------------------
                                    360 ;i                         Allocated to registers 
                                    361 ;------------------------------------------------------------
                                    362 ;	.\main.c:29: void delay(u16 i)
                                    363 ;	-----------------------------------------
                                    364 ;	 function delay
                                    365 ;	-----------------------------------------
      000062                        366 _delay:
                           000007   367 	ar7 = 0x07
                           000006   368 	ar6 = 0x06
                           000005   369 	ar5 = 0x05
                           000004   370 	ar4 = 0x04
                           000003   371 	ar3 = 0x03
                           000002   372 	ar2 = 0x02
                           000001   373 	ar1 = 0x01
                           000000   374 	ar0 = 0x00
      000062 AE 82            [24]  375 	mov	r6,dpl
      000064 AF 83            [24]  376 	mov	r7,dph
                                    377 ;	.\main.c:31: while(i--);	
      000066                        378 00101$:
      000066 8E 04            [24]  379 	mov	ar4,r6
      000068 8F 05            [24]  380 	mov	ar5,r7
      00006A 1E               [12]  381 	dec	r6
      00006B BE FF 01         [24]  382 	cjne	r6,#0xff,00111$
      00006E 1F               [12]  383 	dec	r7
      00006F                        384 00111$:
      00006F EC               [12]  385 	mov	a,r4
      000070 4D               [12]  386 	orl	a,r5
      000071 70 F3            [24]  387 	jnz	00101$
                                    388 ;	.\main.c:32: }
      000073 22               [24]  389 	ret
                                    390 ;------------------------------------------------------------
                                    391 ;Allocation info for local variables in function 'KeyDown'
                                    392 ;------------------------------------------------------------
                                    393 ;a                         Allocated to registers r7 
                                    394 ;------------------------------------------------------------
                                    395 ;	.\main.c:40: void KeyDown(void)
                                    396 ;	-----------------------------------------
                                    397 ;	 function KeyDown
                                    398 ;	-----------------------------------------
      000074                        399 _KeyDown:
                                    400 ;	.\main.c:43: GPIO_KEY=0x0f;
                                    401 ;	.\main.c:44: if(GPIO_KEY!=0x0f)//读取按键是否按下
      000074 74 0F            [12]  402 	mov	a,#0x0f
      000076 F5 90            [12]  403 	mov	_P1,a
      000078 B5 90 01         [24]  404 	cjne	a,_P1,00174$
      00007B 22               [24]  405 	ret
      00007C                        406 00174$:
                                    407 ;	.\main.c:46: delay(1000);//延时10ms进行消抖
      00007C 90 03 E8         [24]  408 	mov	dptr,#0x03e8
      00007F 12 00 62         [24]  409 	lcall	_delay
                                    410 ;	.\main.c:47: if(GPIO_KEY!=0x0f)//再次检测键盘是否按下
      000082 74 0F            [12]  411 	mov	a,#0x0f
      000084 B5 90 01         [24]  412 	cjne	a,_P1,00175$
      000087 22               [24]  413 	ret
      000088                        414 00175$:
                                    415 ;	.\main.c:50: GPIO_KEY=0X0F;
      000088 75 90 0F         [24]  416 	mov	_P1,#0x0f
                                    417 ;	.\main.c:51: switch(GPIO_KEY)
      00008B AF 90            [24]  418 	mov	r7,_P1
      00008D BF 07 02         [24]  419 	cjne	r7,#0x07,00176$
      000090 80 0F            [24]  420 	sjmp	00101$
      000092                        421 00176$:
      000092 BF 0B 02         [24]  422 	cjne	r7,#0x0b,00177$
      000095 80 0F            [24]  423 	sjmp	00102$
      000097                        424 00177$:
      000097 BF 0D 02         [24]  425 	cjne	r7,#0x0d,00178$
      00009A 80 0F            [24]  426 	sjmp	00103$
      00009C                        427 00178$:
                                    428 ;	.\main.c:53: case(0X07):	KeyValue=0;break;
      00009C BF 0E 14         [24]  429 	cjne	r7,#0x0e,00105$
      00009F 80 0F            [24]  430 	sjmp	00104$
      0000A1                        431 00101$:
      0000A1 75 08 00         [24]  432 	mov	_KeyValue,#0x00
                                    433 ;	.\main.c:54: case(0X0b):	KeyValue=1;break;
      0000A4 80 0D            [24]  434 	sjmp	00105$
      0000A6                        435 00102$:
      0000A6 75 08 01         [24]  436 	mov	_KeyValue,#0x01
                                    437 ;	.\main.c:55: case(0X0d): KeyValue=2;break;
      0000A9 80 08            [24]  438 	sjmp	00105$
      0000AB                        439 00103$:
      0000AB 75 08 02         [24]  440 	mov	_KeyValue,#0x02
                                    441 ;	.\main.c:56: case(0X0e):	KeyValue=3;break;
      0000AE 80 03            [24]  442 	sjmp	00105$
      0000B0                        443 00104$:
      0000B0 75 08 03         [24]  444 	mov	_KeyValue,#0x03
                                    445 ;	.\main.c:57: }
      0000B3                        446 00105$:
                                    447 ;	.\main.c:59: GPIO_KEY=0XF0;
      0000B3 75 90 F0         [24]  448 	mov	_P1,#0xf0
                                    449 ;	.\main.c:60: switch(GPIO_KEY)
      0000B6 AF 90            [24]  450 	mov	r7,_P1
      0000B8 BF 70 02         [24]  451 	cjne	r7,#0x70,00180$
      0000BB 80 2A            [24]  452 	sjmp	00133$
      0000BD                        453 00180$:
      0000BD BF B0 02         [24]  454 	cjne	r7,#0xb0,00181$
      0000C0 80 0C            [24]  455 	sjmp	00107$
      0000C2                        456 00181$:
      0000C2 BF D0 02         [24]  457 	cjne	r7,#0xd0,00182$
      0000C5 80 10            [24]  458 	sjmp	00108$
      0000C7                        459 00182$:
                                    460 ;	.\main.c:62: case(0X70):	KeyValue=KeyValue;break;
      0000C7 BF E0 1D         [24]  461 	cjne	r7,#0xe0,00133$
      0000CA 80 14            [24]  462 	sjmp	00109$
                                    463 ;	.\main.c:63: case(0Xb0):	KeyValue=KeyValue+4;break;
      0000CC 80 19            [24]  464 	sjmp	00133$
      0000CE                        465 00107$:
      0000CE AF 08            [24]  466 	mov	r7,_KeyValue
      0000D0 74 04            [12]  467 	mov	a,#0x04
      0000D2 2F               [12]  468 	add	a,r7
      0000D3 F5 08            [12]  469 	mov	_KeyValue,a
                                    470 ;	.\main.c:64: case(0Xd0): KeyValue=KeyValue+8;break;
      0000D5 80 10            [24]  471 	sjmp	00133$
      0000D7                        472 00108$:
      0000D7 AF 08            [24]  473 	mov	r7,_KeyValue
      0000D9 74 08            [12]  474 	mov	a,#0x08
      0000DB 2F               [12]  475 	add	a,r7
      0000DC F5 08            [12]  476 	mov	_KeyValue,a
                                    477 ;	.\main.c:65: case(0Xe0):	KeyValue=KeyValue+12;break;
      0000DE 80 07            [24]  478 	sjmp	00133$
      0000E0                        479 00109$:
      0000E0 AF 08            [24]  480 	mov	r7,_KeyValue
      0000E2 74 0C            [12]  481 	mov	a,#0x0c
      0000E4 2F               [12]  482 	add	a,r7
      0000E5 F5 08            [12]  483 	mov	_KeyValue,a
                                    484 ;	.\main.c:67: while((a<50)&&(GPIO_KEY!=0xf0))	 //检测按键松手检测
      0000E7                        485 00133$:
      0000E7 7F 00            [12]  486 	mov	r7,#0x00
      0000E9                        487 00112$:
      0000E9 BF 32 00         [24]  488 	cjne	r7,#0x32,00184$
      0000EC                        489 00184$:
      0000EC 50 13            [24]  490 	jnc	00119$
      0000EE 74 F0            [12]  491 	mov	a,#0xf0
      0000F0 B5 90 01         [24]  492 	cjne	a,_P1,00186$
      0000F3 22               [24]  493 	ret
      0000F4                        494 00186$:
                                    495 ;	.\main.c:69: delay(1000);
      0000F4 90 03 E8         [24]  496 	mov	dptr,#0x03e8
      0000F7 C0 07            [24]  497 	push	ar7
      0000F9 12 00 62         [24]  498 	lcall	_delay
      0000FC D0 07            [24]  499 	pop	ar7
                                    500 ;	.\main.c:70: a++;
      0000FE 0F               [12]  501 	inc	r7
      0000FF 80 E8            [24]  502 	sjmp	00112$
      000101                        503 00119$:
                                    504 ;	.\main.c:74: }
      000101 22               [24]  505 	ret
                                    506 ;------------------------------------------------------------
                                    507 ;Allocation info for local variables in function 'main'
                                    508 ;------------------------------------------------------------
                                    509 ;	.\main.c:83: void main()
                                    510 ;	-----------------------------------------
                                    511 ;	 function main
                                    512 ;	-----------------------------------------
      000102                        513 _main:
                                    514 ;	.\main.c:86: while(1)
      000102                        515 00102$:
                                    516 ;	.\main.c:88: KeyDown();		   //按键判断函数
      000102 12 00 74         [24]  517 	lcall	_KeyDown
                                    518 ;	.\main.c:91: }
      000105 80 FB            [24]  519 	sjmp	00102$
                                    520 	.area CSEG    (CODE)
                                    521 	.area CONST   (CODE)
                                    522 	.area XINIT   (CODE)
                                    523 	.area CABS    (ABS,CODE)
