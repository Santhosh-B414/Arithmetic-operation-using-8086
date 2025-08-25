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
|         1200:12         |          1200:24         |
|         1201:34         |          1205:68         |
|         1202:12         |          1206:00         |
|         1203:34         |                          |

#### Manual Calculations

![addition](https://github.com/user-attachments/assets/719ee99a-f1cb-4711-a32f-e34ae915a421)


---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="640" height="480" alt="Screenshot (6)" src="https://github.com/user-attachments/assets/53482313-bf40-421b-a167-744b05472187" />

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



#### Output Table


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200:12         |          1200:00         |
|         1201:34         |          1205:00         |
|         1202:12         |          1206:00         |
|         1203:34         |                          |

#### Manual Calculations

![subtraction](https://github.com/user-attachments/assets/7c20d6e4-76c6-4add-94a0-8c9c473f74f2)

---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="640" height="480" alt="Screenshot (7)" src="https://github.com/user-attachments/assets/eaf66c86-bbab-441c-b81c-4a65b8827cd2" />

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
|         1200:12         |          1200:44         |
|         1201:34         |          1205:51         |
|         1202:12         |          1206:97         |
|         1203:34         |          1207:0A         |

#### Manual Calculations

![multiplication](https://github.com/user-attachments/assets/a93f7f0a-1cbb-4932-afac-dcfda8ef884f)


---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="640" height="480" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/88cd16ed-962f-4cf8-a688-b014da44ae08" />

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
|         1200:12         |          1200:01         |
|         1201:34         |          1205:00         |
|         1202:12         |          1206:00         |
|         1203:34         |          1207:00         |


#### Manual Calculations

![divition](https://github.com/user-attachments/assets/2ca779a2-940b-45af-96e3-d34cef8d4ba8)


---
## OUTPUT FROM MASM SOFTWARE

<img width="640" height="480" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/7a3cb011-6f85-4fa0-8d8d-9e2e28432e62" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
