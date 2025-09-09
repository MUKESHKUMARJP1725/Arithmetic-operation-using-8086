# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200: 12          |        1204: 24          |
|       1201: 34          |        1205: 68          |
|       1202: 12          |        1206: 00          |
|       1203: 34          |        1207: C4          |

#### Manual Calculations

![add](https://github.com/user-attachments/assets/758072f7-9ce9-46a8-bda4-68902797d981)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2025-09-09 at 18 39 33_13afb626](https://github.com/user-attachments/assets/8737ce9e-ca46-46a1-81f4-cb3ca0b846ab)
![WhatsApp Image 2025-09-09 at 18 42 54_928168d8](https://github.com/user-attachments/assets/f03606fe-20f6-4e01-aed6-3e6aa9735123)

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200: 12          |        1204: 00          |
|       1201: 34          |        1205: 00          |
|       1202: 12          |        1206: 00          |
|       1203: 34          |        1207: C4          |

#### Manual Calculations

![subt](https://github.com/user-attachments/assets/47b66f0c-d867-4b75-8c2e-5bd261430c42)



## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-09 at 18 58 26_b7ea1eb3](https://github.com/user-attachments/assets/91aba485-b07e-4d36-84c5-46c76a659569)
![WhatsApp Image 2025-09-09 at 19 00 22_c9973721](https://github.com/user-attachments/assets/b215a8dc-4263-4c5a-b1f3-cb8652352a15)


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200: 12          |        1204: 44          |
|       1201: 34          |        1205: 51          |
|       1202: 12          |        1206: 97          |
|       1203: 34          |        1207: 0A          |

#### Manual Calculations

![mult](https://github.com/user-attachments/assets/9e2116fc-9571-44d0-8d74-fe2c76692335)


## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-09 at 19 13 32_65365a03](https://github.com/user-attachments/assets/2d19bed6-3c6e-4b02-be64-0a8aa17bb925)
![WhatsApp Image 2025-09-09 at 19 15 43_fd2f5551](https://github.com/user-attachments/assets/76709422-6aac-4f52-ae86-305a9d1525d8)


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200: 12          |        1204: 01          |
|       1201: 34          |        1205: 00          |
|       1202: 12          |        1206: 00          |
|       1203: 34          |        1207: 00          |

#### Manual Calculations

![IMG-20250901-WA0003](https://github.com/user-attachments/assets/73c112cf-1d25-4a72-97b7-5e0c115910bc)

## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2025-09-09 at 19 31 45_11259c7e](https://github.com/user-attachments/assets/90cbeab9-74d6-428b-86ee-f965716502b4)
![WhatsApp Image 2025-09-09 at 19 33 27_0845cdab](https://github.com/user-attachments/assets/c2376e9c-8699-46c0-a0ba-c8f017f43004)



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
