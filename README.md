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
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table
<img width="1600" height="728" alt="WhatsApp Image 2026-05-14 at 10 24 58 AM" src="https://github.com/user-attachments/assets/fa986775-e2e2-4fff-ad79-78d82af62d03" />

#### Manual Calculations
<img width="1324" height="648" alt="WhatsApp Image 2026-05-14 at 10 24 59 AM" src="https://github.com/user-attachments/assets/409b77eb-566b-4e39-ad2c-c7e84f2589ff" />

---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="1600" height="1063" alt="WhatsApp Image 2026-05-14 at 10 25 05 AM" src="https://github.com/user-attachments/assets/cfcd7b83-1f0f-408b-ba6a-5aa56d5e2d79" />

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
```asm
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

<img width="1600" height="672" alt="WhatsApp Image 2026-05-14 at 10 25 05 AM (1)" src="https://github.com/user-attachments/assets/6530a2fe-4e7d-431a-9a92-df3122356e74" />


#### Manual Calculations

<img width="888" height="476" alt="WhatsApp Image 2026-05-14 at 10 25 05 AM (2)" src="https://github.com/user-attachments/assets/96d82c35-c3db-4bb6-ac18-217d6a7d03c3" />

---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="1280" height="664" alt="WhatsApp Image 2026-05-14 at 10 25 00 AM (1)" src="https://github.com/user-attachments/assets/28debe97-1c9a-4174-8d99-0e6224acc9cd" />

## 3. MULTIPLICATION
#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

## FLOWCHART
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
<img width="1280" height="570" alt="WhatsApp Image 2026-05-14 at 10 25 06 AM" src="https://github.com/user-attachments/assets/071fadc9-458b-4861-a006-f7400823d892" />

#### Manual Calculations
<img width="1248" height="784" alt="WhatsApp Image 2026-05-14 at 10 25 06 AM (1)" src="https://github.com/user-attachments/assets/867060f3-1582-4ee4-832e-474154a379c2" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1280" height="648" alt="WhatsApp Image 2026-05-14 at 10 25 06 AM (2)" src="https://github.com/user-attachments/assets/0e1562ec-f338-46f2-91da-aabfcb07d692" />


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
<img width="1280" height="487" alt="WhatsApp Image 2026-05-14 at 10 25 07 AM (1)" src="https://github.com/user-attachments/assets/705bee91-ae46-4f06-925b-07feff69bd48" />

#### Manual Calculations

<img width="1600" height="719" alt="WhatsApp Image 2026-05-14 at 10 25 07 AM (2)" src="https://github.com/user-attachments/assets/b0e1cae6-ad66-4a2a-ae43-960de87d35f7" />

---

## OUTPUT FROM MASM SOFTWARE
<img width="1280" height="685" alt="WhatsApp Image 2026-05-14 at 10 25 08 AM" src="https://github.com/user-attachments/assets/8fce6077-2fff-4c5d-8567-ee31a5d76394" />

## RESULT
Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
