# บันทึกการแก้โจทย์

ไฟล์นี้ต้องเขียนโดยนักศึกษาด้วยคำพูดของตนเอง

ใช้ template นี้เฉพาะกับโจทย์ OJ ที่ถูกระบุว่าต้องส่ง learning log เท่านั้น

ห้ามให้ AI เขียนไฟล์นี้แทนคุณ AI อาจช่วยตรวจ grammar, formatting หรือความชัดเจนได้ หลังจากที่คุณเขียนเนื้อหาของตนเองแล้ว

ถ้าใช้ AI กับโจทย์ learning-log-required นี้ ต้องทำไฟล์ `ai_reflection.md` ด้วย

---

## 1. ข้อมูล OJ

หมายเลข/ชื่อโจทย์ OJ:

```text
OJ3537 - [LEARNING LOGS] Impostor
```

OJ submission ID ถ้ามีการส่งแล้ว:

```text
678736
```

สถานะ OJ:

```text
Pass
```

เวลาที่ใช้คิดและทำโจทย์ด้วยตนเอง:

```text
30-60 minutes
```

เลือกหนึ่งข้อ:

```text
0-15 minutes
15-30 minutes
30-60 minutes
1-3 hours
3-6 hours
6-24 hours
1-3 days
4-7 days
1-4 weeks
More than 4 weeks
```

วิธีนับเวลา:

- นับเฉพาะเวลาที่ตั้งใจทำโจทย์นี้ด้วยตนเองจริง ๆ
- เริ่มนับตั้งแต่ตอนที่อ่านโจทย์ครั้งแรก
- ไม่นับเวลาพัก กินข้าว เรียน นอน เวลาที่ทำโจทย์อื่น หรือเวลาที่ไม่ได้ทำโจทย์นี้
- ถ้าใช้ AI ให้นับเฉพาะเวลาที่ทำด้วยตนเองก่อน prompt แรกที่ถาม AI
- ถ้าถามเพื่อน TA หรือผู้สอน ให้นับเฉพาะเวลาที่ทำด้วยตนเองก่อนขอความช่วยเหลือครั้งแรก
- ถ้าใช้ทั้ง AI และความช่วยเหลือจากคน ให้นับเฉพาะเวลาที่ทำด้วยตนเองก่อนขอความช่วยเหลือจากภายนอกครั้งแรก ไม่ว่าจะเป็น AI หรือคน
- ถ้าไม่ได้ใช้ AI และไม่ได้ขอความช่วยเหลือจากคน ให้นับเวลาถึงก่อนเขียน `submission.md`
- ประมาณเวลาได้ แต่ต้องซื่อสัตย์

---

## 2. ความเข้าใจโจทย์ของฉัน

เขียนโจทย์ด้วยคำพูดของตนเอง

ให้อธิบาย input, output และ constraints สำคัญด้วย

ถ้ายังไม่เข้าใจโจทย์ทั้งหมด ให้เขียนสิ่งที่เข้าใจในตอนนี้ ความเข้าใจอาจยังไม่ครบหรืออาจผิดได้ แต่ต้องพยายามอธิบายอย่างจริงใจ

```text
Input:
รับstringที่เขียนเป็นdict โดยkeyเป็นชื่อผู้เล่น และvalueเป็นบทบาทระหว่างCrewmate หรือ Impostor จนกว่าผู้ใช้จะกรอกStart จากนั้นรับstringเป็นชื่อผู้เล่นที่ละบรรทัดจะกว่าผู้ใช้จะกรอกEnd

Output:
บรรทัดแรกแสดงจำนวนImpostorที่เหลืออยู่ตามด้วยข้อความ Impostor Remains
บรรทัดต่อมาแสดงข้อความ***Alive***
บรรทัดต่อมาแสดงรายชื่อผู้เล่นที่ยังมีชีวิตอยู่ตามด้วยบทบาท(คั่นกลางด้วย " : ") 1บรรทัดต่อรายชื่อผู้เล่น1คน
บรรทัดต่อมาแสดงข้อความ***Dead***
บรรทัดต่อมาแสดงรายชื่อผู้เล่นที่เสียชีวิตตามด้วยบทบาท(คั่นกลางด้วย " : ") 1บรรทัดต่อรายชื่อผู้เล่น1คน

Constraints:
input ที่รับเข้ามาเป็นstringที่เขียนแบบdict ควรใช้json.loadsในการแปลงข้อมูลให้เป็นdictจริงๆก่อน
```

---

## 3. แผนแรกของฉัน

เขียนแผนแรกก่อนรับความช่วยเหลือจาก AI เพื่อน TA ผู้สอน หรือก่อนสรุป code สุดท้าย

ถ้าใช้ AI ให้เขียนแผนที่มีอยู่ก่อน prompt แรกที่ถาม AI

ถ้าถามเพื่อน TA หรือผู้สอน ให้เขียนแผนที่มีอยู่ก่อนถาม

ถ้าไม่ได้ใช้ AI และไม่ได้ขอความช่วยเหลือจากคน ให้เขียนแผนที่มีอยู่ก่อนหรือระหว่างเริ่มเขียน code

แผนนี้เขียนแบบคร่าว ๆ ได้ อาจยังไม่สมบูรณ์หรืออาจต่างจากวิธีสุดท้าย

สามารถเขียนเป็น pseudocode, flowchart idea หรือขั้นตอนความคิดได้

```text
Step 1: import json เพื่อใช้ในการแปลงstring(ที่เขียนแบบdict)ที่รับมาให้กลายเป็นdictจริงๆ
Step 2: สร้างdict playerไว้เก็บค่าinputที่แปลงโดยใช้jsonแล้ว
Step 3: ใช้while loop รับค่าstring ทีละบรรทัดจนกว่าจะเจอ'Start'
Step 4: ใช้json.loadsแปลงข้อมูลเป็นdict แล้วใช้.updateเพิ่มค่าdictที่แปลงแล้วลงในplayer 
Step 5: สร้างlist dead ไว้เก็บค่าของผู้เล่นที่ถูกกำจัด
Step 6: ใช้while loop รับค่าstringเป็นชื่อผู้เล่น ทีละบรรทัดจนกว่าจะเจอ'End'
Step 7: เพิ่มรายชื่อผู้เล่นลงในlist dead
Step 8: จากนั้นสร้างlist alive(ไว้เก็บข้อมูลผู้เล่นที่ยังมีชีวิต) และ list eliminate(ไว้เก็บข้อมูลผู้เล่นที่เสียชีวิต)
Step 9:วนลูป name ในdict player ถ้าnameอยู่ในlist deadให้เพิ่มค่าnameลงในlist eliminate ถ้าไม่ใช่ให้เพิ่มค่าnameลงในlist alive
Step 10: จากนั้นนำทั้ง2listมาเรียงลำดับตัวอักษรโดยใช้.sort()
Step 11: จากนั้งสร้างตัวแปรimpostor_leftไว้นับจำนวนimpostorที่ยังรอดอยู่
Step 12: for loopวนลูปค่า i ในlist alive
Step 13: ในลูปเช็คว่าหากในdict playerในตำแหน่งที่keyเป็น i ถ้าได้ค่าvalueเป็นimpostorจะให้impostor_left บวก1
Step 14: แสดงค่าimpostor_left ตามด้วยข้อความImpostor Remainsในบรรทัดเดียวกัน
Step 15: แสดงข้อความ***Alive*** และบรรทัดถัดไปวนนลูปค่า n ในlist alive เพื่อแสดงค่าn และ dictplayerตำแหน่งที่keyเป็นn(แสดงบทบาท)
Step 16: แสดงข้อความ***Dead*** และบรรทัดถัดไปวนนลูปค่า m ในlist elimianteเพื่อแสดงค่าm และ dictplayerตำแหน่งที่keyเป็นm
```

---

## 4. วิธีสุดท้ายที่ใช้จริง

อธิบายสั้น ๆ ว่า algorithm หรือวิธีสุดท้ายที่ใช้จริงใน code ที่ส่งคืออะไร

หัวข้อนี้ต่างจาก Section 3:

- Section 3 คือแผนแรกก่อนใช้ AI ก่อนรับความช่วยเหลือจากคน หรือก่อนเขียน code สุดท้าย
- Section 4 คือวิธีสุดท้ายที่ใช้ใน solution จริง
- ถ้าวิธีสุดท้ายเหมือนกับแผนแรก ให้เขียนว่าเหมือนกัน และอธิบายสั้น ๆ ว่าทำไม

ห้ามคัดลอกคำอธิบายจาก AI

ห้ามคัดลอกคำอธิบายจากคนอื่น

```text
วิธีสุดท้ายเหมือนกับแผนแรก มีการใช้json.loadsแปลงstringให้เป็นdictแล้วเก็บไว้ในdict playerโดยใช้.update มีการตรวจสอบผู้เล่นที่ถูกกำจัดโดยการใช้list deadเปรีบยเทียบกับplayer ถ้าชื่อในplayerมีอยู่ในlist deadด้วยจะถือว่าผู้เล่นคนนั้นโดนกำจัดและจะappendค่าลงในlist eliminate หากชื่อไม่ได้อยู่ในlist deadก็จะappendค่าลงในlist alive จากนั้นในlist aliveจะวนลูปค่า i เพื่อเช็คว่าในdict playerตำแหน่งที่keyเป็นi หากมีvalueเป็นimpostorจะให้บอก1ที่ตัวแปรimpostor_left(ใช้นับimpostorที่ยังรอด) แล้วแสดงผลตามที่โจทย์กำหนด
```

---

## 5. การทดสอบของฉัน

เขียน test cases อย่างน้อย 3 กรณีที่ลองเองหรือออกแบบเอง

พยายามเลือก test cases ที่แตกต่างกัน

แต่ละ test case ให้อธิบายว่าทำไมเลือกกรณีนั้น

ถ้า input หรือ output มีหลายบรรทัด ให้เขียนไว้ใน text blocks

### Test Case 1

ทำไมเลือก case นี้:

```text
เช็คกรณีที่inputไม่เรียงตัวอักษรมาให้
```

Input:

```text
{"Zoro" : "Crewmate"}
{"Mike" : "Impostor"}
{"Nami" : "Crewmate"}
{"Joji" : "Crewmate"}
{"Zack" : "Crewmate"}
{"Sunji" : "Impostor"}
Start
Zoro
Mike
Joji
End
```

Expected output:

```text
1 Impostor Remains
***Alive***
Nami : Crewmate
Sunji : Impostor
Zack : Crewmate
***Dead***
Joji : Crewmate
Mike : Impostor
Zoro : Crewmate
```

Actual output:

```text
1 Impostor Remains
***Alive***
Nami : Crewmate
Sunji : Impostor
Zack : Crewmate
***Dead***
Joji : Crewmate
Mike : Impostor
Zoro : Crewmate
```

Result:

```text
Pass
```

### Test Case 2

ทำไมเลือก case นี้:

```text
เช็คกรณีที่ตอนจบไม่มีimpostorเหลือ
```

Input:

```text
{"Zuzan" : "Crewmate"}
{"Victor" : "Impostor"}
{"Jean" : "Crewmate"}
{"Toby" : "Crewmate"}
{"Sitama" : "Crewmate"}
{"Thanos" : "Impostor"}
Start
Sitama
Victor
Thanos
End
```

Expected output:

```text
0 Impostor Remains
***Alive***
Jean : Crewmate
Toby : Crewmate
Zuzan : Crewmate
***Dead***
Sitama : Crewmate
Thanos : Impostor
Victor : Impostor
```

Actual output:

```text
0 Impostor Remains
***Alive***
Jean : Crewmate
Toby : Crewmate
Zuzan : Crewmate
***Dead***
Sitama : Crewmate
Thanos : Impostor
Victor : Impostor
```

Result:

```text
Pass
```

### Test Case 3

ทำไมเลือก case นี้:

```text
เช็คกรณีที่ไม่มีใครโดนกำจัด
```

Input:

```text
{"Ronaldo" : "Crewmate"}
{"Messi" : "Impostor"}
{"Haland" : "Crewmate"}
{"Naymar" : "Crewmate"}
{"Jude" : "Crewmate"}
{"Tewarakorn" : "Impostor"}
Start
End
```

Expected output:

```text
2 Impostor Remains
***Alive***
Haland : Crewmate
Jude : Crewmate
Messi : Impostor
Naymar : Crewmate
Ronaldo : Crewmate
Tewarakorn : Impostor
***Dead***
```

Actual output:

```text
2 Impostor Remains
***Alive***
Haland : Crewmate
Jude : Crewmate
Messi : Impostor
Naymar : Crewmate
Ronaldo : Crewmate
Tewarakorn : Impostor
***Dead***
```

Result:

```text
Pass
```

---

## 6. การใช้ AI

ใช้ AI กับโจทย์นี้หรือไม่

```text
No
```

ถ้าใช้ AI ต้องทำไฟล์นี้ด้วย:

```text
ai_reflection.md
```

ถ้าถามเฉพาะเพื่อน TA หรือผู้สอน และไม่ได้ใช้ AI ไม่ต้องทำ `ai_reflection.md`

---

## 7. ความช่วยเหลือจากคน / การร่วมมือ

ได้ถามเพื่อน TA ผู้สอน หรือบุคคลอื่นเพื่อขอความช่วยเหลือในโจทย์นี้หรือไม่

```text
No
```

ถ้าใช่ ให้อธิบายสั้น ๆ ว่าได้รับความช่วยเหลือแบบใด

ตัวอย่างที่อนุญาต:

- อธิบายความหมายของโจทย์
- อธิบาย concept การเขียนโปรแกรม
- ให้ hint เกี่ยวกับแนวทาง
- คุยเรื่อง debugging
- คุยเรื่อง test cases
- ช่วยอธิบาย error message

สิ่งที่ไม่อนุญาต:

- คัดลอก code ของผู้อื่น
- ส่ง solution ของผู้อื่น
- ขอให้ผู้อื่นเขียน solution ให้
- ใช้ OJ submission ของผู้อื่น
- ขอให้ผู้อื่นส่ง OJ แทน

ใครช่วยคุณ

```text

```

เขาช่วยอะไร

```text

```

คุณยังทำอะไรด้วยตนเอง

```text

```

คุณคัดลอก code จากคนอื่นหรือไม่

```text
No
```

---

## 8. คำรับรองของนักศึกษา

เขียน `Yes` ในแต่ละ statement

| Statement | Yes/No |
|---|---|
| I wrote this submission in my own words. | Yes |
| I understand my final code. | Yes |
| I recorded the real OJ status. | Yes |
| I did not copy AI-generated text directly into this file. | Yes |
| I did not copy code from another person. | Yes |
| If I received human help, I disclosed it in this file. | Yes |
| I submitted the final code to the OJ by myself. | Yes |
