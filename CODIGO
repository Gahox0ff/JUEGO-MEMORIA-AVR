RJMP INICIO
INICIO:
    LDI     R20, 0xFF   ; Configurar PORTA como salida para el display;
    OUT     DDRA, R20   
    LDI     R25, 0x00   ; Configurar PORTC como entrada (Pulsadores);
    OUT     DDRC, R25
    LDI     R26, 0x00   ; No activar pull-ups;
    OUT     PORTC, R26
    LDI     R27, 0xFF   ; Configurar PORTD como salida (LEDs);
    OUT     DDRD, R27
    LDI     R27, 0x00   ; Apagar LEDs al inicio;
    OUT     PORTD, R27
    LDI     R21, 0      ; Contador de secuencias completadas;

; Primera secuencia;
Secuencia1:
    LDI     R20, 0xA4   ; Mostrar '2';
    OUT     PORTA, R20
    CALL    Retardo_1s
    
    LDI     R20, 0xB0   ; Mostrar '3';
    OUT     PORTA, R20
    CALL    Retardo_1s
    
    LDI     R20, 0xF9   ; Mostrar '1';
    OUT     PORTA, R20
    CALL    Retardo_1s
    
    LDI     R20, 0x99   ; Mostrar '4';
    OUT     PORTA, R20
    CALL    Retardo_1s
    
    LDI     R20, 0xA4   ; Mostrar '2';
    OUT     PORTA, R20
    CALL    Retardo_1s
PULSAR_SECUENCIA1:
    LDI     R20, 0xC0   ; Mostrar '0' durante la lectura;
    OUT     PORTA, R20
    CALL    Leer_Pulsador_PC1  ; 2;
    CALL    Leer_Pulsador_PC2  ; 3;
    CALL    Leer_Pulsador_PC0  ; 1;
    CALL    Leer_Pulsador_PC3  ; 4;
    CALL    Leer_Pulsador_PC1  ; 2;
    INC     R21                ; Incrementar contador de secuencias;
    SBI     PORTD, 0          ; Encender LED permanentemente;
	Call Retardo_3s
    RJMP    Secuencia2

; Segunda secuencia;
Secuencia2:
    LDI     R20, 0xF9   ; Mostrar '1';
    OUT     PORTA, R20
    CALL    Retardo_1s
    
    LDI     R20, 0x99   ; Mostrar '4';
    OUT     PORTA, R20
    CALL    Retardo_1s
    
    LDI     R20, 0xB0   ; Mostrar '3';
    OUT     PORTA, R20
    CALL    Retardo_1s
    
    LDI     R20, 0xA4   ; Mostrar '2';
    OUT     PORTA, R20
    CALL    Retardo_1s
    
    LDI     R20, 0xF9   ; Mostrar '1';
    OUT     PORTA, R20
    CALL    Retardo_1s

	LDI     R20, 0x92   ; Mostrar '5';
    OUT     PORTA, R20
    CALL    Retardo_1s

PULSAR_SECUENCIA2:
    LDI     R20, 0xC0   ; Mostrar '0' durante la lectura
    OUT     PORTA, R20
    CALL    Leer_Pulsador_PC0  ; 1
    CALL    Leer_Pulsador_PC3  ; 4
    CALL    Leer_Pulsador_PC2  ; 3
    CALL    Leer_Pulsador_PC1  ; 2
    CALL    Leer_Pulsador_PC0  ; 1
    CALL    Leer_Pulsador_PC4  ; 5
    INC     R21                ; Incrementar contador de secuencias
    SBI     PORTD, 1           ; Encender segundo LED permanentemente
	CALL	Retardo_3s
    RJMP    Secuencia3          ; Encender segundo LED permanentemente;


; Tercera secuencia;
Secuencia3:
    LDI     R20, 0x99   ; Mostrar '4';
    OUT     PORTA, R20
    CALL    Retardo_1s
    
    LDI     R20, 0xB0   ; Mostrar '3';
    OUT     PORTA, R20
    CALL    Retardo_1s
    
    LDI     R20, 0xA4   ; Mostrar '2';
    OUT     PORTA, R20
    CALL    Retardo_1s
    
    LDI     R20, 0xF9   ; Mostrar '1';
    OUT     PORTA, R20
    CALL    Retardo_1s
    
    LDI     R20, 0x99   ; Mostrar '4';
    OUT     PORTA, R20
    CALL    Retardo_1s
	
	LDI     R20, 0x92   ; Mostrar '5';
    OUT     PORTA, R20
    CALL    Retardo_1s

	LDI     R20, 0xF9   ; Mostrar '1';
    OUT     PORTA, R20
    CALL    Retardo_1s

PULSAR_SECUENCIA3:
    LDI     R20, 0xC0   ; Mostrar '0' durante la lectura
    OUT     PORTA, R20
    CALL    Leer_Pulsador_PC3  ; 4
    CALL    Leer_Pulsador_PC2  ; 3
    CALL    Leer_Pulsador_PC1  ; 2
    CALL    Leer_Pulsador_PC0  ; 1
    CALL    Leer_Pulsador_PC3  ; 4
    CALL    Leer_Pulsador_PC4  ; 5
    CALL    Leer_Pulsador_PC0  ; 1
    INC     R21                ; Incrementar contador de secuencias
    SBI     PORTD, 2           ; Encender tercer LED permanentemente
	CALL	Retardo_3s
    RJMP    Secuencia4


; Cuarta secuencia;
Secuencia4:
    LDI     R20, 0xB0   ; Mostrar '3';
    OUT     PORTA, R20
    CALL    Retardo_1s
    
    LDI     R20, 0xF9   ; Mostrar '1';
    OUT     PORTA, R20
    CALL    Retardo_1s
    
    LDI     R20, 0x99   ; Mostrar '4';
    OUT     PORTA, R20
    CALL    Retardo_1s
    
    LDI     R20, 0xA4   ; Mostrar '2';
    OUT     PORTA, R20
    CALL    Retardo_1s
    
    LDI     R20, 0xB0   ; Mostrar '3';
    OUT     PORTA, R20
    CALL    Retardo_1s

	LDI     R20, 0xA4   ; Mostrar '2';
    OUT     PORTA, R20
    CALL    Retardo_1s
	
	LDI     R20, 0x92   ; Mostrar '5';
    OUT     PORTA, R20
    CALL    Retardo_1s

	LDI     R20, 0x92   ; Mostrar '5';
    OUT     PORTA, R20
    CALL    Retardo_1s

PULSAR_SECUENCIA4:
    LDI     R20, 0xC0   ; Mostrar '0' durante la lectura
    OUT     PORTA, R20
    CALL    Leer_Pulsador_PC2  ; 3
    CALL    Leer_Pulsador_PC0  ; 1
    CALL    Leer_Pulsador_PC3  ; 4
    CALL    Leer_Pulsador_PC1  ; 2
    CALL    Leer_Pulsador_PC2  ; 3
    CALL    Leer_Pulsador_PC1  ; 2
    CALL    Leer_Pulsador_PC4  ; 5
    CALL    Leer_Pulsador_PC4  ; 5
    INC     R21                ; Incrementar contador de secuencias
    SBI     PORTD, 3           ; Encender cuarto LED permanentemente        ; Encender cuarto LED permanentemente;
   //////////// 
    ; Verificar si se completaron las 4 secuencias;
    CALL	Retardo_3s
	CPI     R21, 4
    BREQ    MOSTRAR_G
    RJMP    INICIO

MOSTRAR_G:
    LDI     R20, 0x02   ; Código para mostrar 'G' en el display;
    OUT     PORTA, R20
    CALL    Retardo_1s
	LDI     R20, 0xFF   ; Código para mostrar 'G' en el display;
    OUT     PORTA, R20
	CALL    Retardo_1s
	LDI     R20, 0x02   ; Código para mostrar 'G' en el display;
    OUT     PORTA, R20
    CALL    Retardo_1s
	LDI     R20, 0xFF   ; Código para mostrar 'G' en el display;
    OUT     PORTA, R20
    RJMP    INICIO

INCORRECTO:
    LDI     R16, 0xFF   ; Encender todos los LEDs (parpadeo 1);
    OUT     PORTD, R16 
    CALL    Retardo_100ms
    LDI     R17, 0x00   ; Apagar todos los LEDs;
    OUT     PORTD, R17
    CALL    Retardo_100ms
    LDI     R16, 0xFF   ; Segundo parpadeo - Encender;
    OUT     PORTD, R16 
    CALL    Retardo_100ms
    LDI     R17, 0x00   ; Segundo parpadeo - Apagar;
    OUT     PORTD, R17
    CALL    Retardo_100ms
    LDI     R16, 0xFF   ; Tercer parpadeo - Encender;
    OUT     PORTD, R16 
    CALL    Retardo_100ms
    LDI     R17, 0x00   ; Tercer parpadeo - Apagar;
    OUT     PORTD, R17
    CALL    Retardo_100ms
    LDI     R16, 0xFF   ; Cuarto parpadeo - Encender;
    OUT     PORTD, R16 
    CALL    Retardo_100ms
    LDI     R17, 0x00   ; Cuarto parpadeo - Apagar;
    OUT     PORTD, R17
    CALL    Retardo_100ms
	RJMP    INICIO


Leer_Pulsador_PC0:
    CALL    Esperar_Presionar
    IN      R25, PINC
    ANDI    R25, 0x01   ; Leer PC0
    CPI     R25, 0x01    
    BREQ    Fin_PC0
    RJMP    INCORRECTO
Fin_PC0:
    CALL    Esperar_Soltar
    RET

Leer_Pulsador_PC1:
    CALL    Esperar_Presionar
    IN      R25, PINC
    ANDI    R25, 0x02   ; Leer PC1
    CPI     R25, 0x02    
    BREQ    Fin_PC1
    RJMP    INCORRECTO
Fin_PC1:
    CALL    Esperar_Soltar
    RET

Leer_Pulsador_PC2:
    CALL    Esperar_Presionar
    IN      R25, PINC
    ANDI    R25, 0x04   ; Leer PC2
    CPI     R25, 0x04    
    BREQ    Fin_PC2
    RJMP    INCORRECTO
Fin_PC2:
    CALL    Esperar_Soltar
    RET

Leer_Pulsador_PC3:
    CALL    Esperar_Presionar
    IN      R25, PINC
    ANDI    R25, 0x08   ; Leer PC3
    CPI     R25, 0x08    
    BREQ    Fin_PC3
    RJMP    INCORRECTO
Fin_PC3:
    CALL    Esperar_Soltar
    RET

Leer_Pulsador_PC4:
    CALL    Esperar_Presionar
    IN      R25, PINC
    ANDI    R25, 0x10   ; Leer PC4
    CPI     R25, 0x10    
    BREQ    Fin_PC4
    RJMP    INCORRECTO
Fin_PC4:
    CALL    Esperar_Soltar
    RET


Retardo_1s:
    LDI     R18, 82
    LDI     R19, 43
    LDI     R20, 0
L1: DEC     R20
    BRNE    L1
    DEC     R19
    BRNE    L1
    DEC     R18
    BRNE    L1
    RET

Esperar_Presionar:
    IN      R25, PINC
    CPI     R25, 0x00   
    BREQ    Esperar_Presionar
    CALL    Retardo_50ms   
    RET

Esperar_Soltar:
    IN      R25, PINC
    CPI     R25, 0x00   
    BREQ    Fin_Esperar_Soltar  
    RJMP    Esperar_Soltar   
Fin_Esperar_Soltar:
    CALL    Retardo_50ms   
    RET

Retardo_50ms:
    LDI     R18, 2
    LDI     R19, 50
    LDI     R20, 255
L2: DEC     R20
    BRNE    L2
    DEC     R19
    BRNE    L2
    DEC     R18
    BRNE    L2
    RET

Retardo_100ms:
	ldi  r18, 9
    ldi  r19, 30
    ldi  r20, 229
L3: dec  r20
    brne L3
    dec  r19
    brne L3
    dec  r18
    brne L3
    nop
	RET
Retardo_3s:
    ldi  r18, 244
    ldi  r19, 130
    ldi  r20, 6
L4: dec  r20
    brne L4
    dec  r19
    brne L4
    dec  r18
    brne L4
	RET
