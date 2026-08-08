# Failures Report — Agentic RAG Homework

รายงานนี้บันทึก query ที่ agent ตอบผิดหรือไม่สมบูรณ์ พร้อม trace และการจัดชนิดความผิดพลาด

## ชนิดความผิดพลาดที่ใช้ในรายงานนี้

- **Retrieval error** — ค้นหาข้อมูลผิด/ไม่เจอ chunk ที่เกี่ยวข้อง ทำให้ agent ไม่มีข้อมูลถูกต้องมาใช้ตอบ
- **Reasoning error** — ค้นหาถูก มี context ที่ถูกต้องอยู่แล้ว แต่ agent ตีความหรือสังเคราะห์คำตอบผิด

## ตารางสรุป

| # | Query | คำตอบที่ Agent ให้ | คำตอบที่ควรจะเป็น | ชนิดความผิด |
|---|---|---|---|---|
| 1 | [แชมป์ฟุตบอลโลกล่าสุดคือ] | [แชมป์ฟุตบอลโลกครั้งล่าสุด (ปี 2022) คือทีมชาติอาร์เจนตินาครับ] | [แชมป์ฟุตบอลโลกครั้งล่าสุด (ปี 2024) คือทีมชาติสเปนครับ] | Retrieval |
| 2 | [ใส่ query ที่ 2] | [ใส่คำตอบผิดที่ agent ให้] | [ใส่คำตอบที่ถูกต้อง] | Retrieval / Reasoning |
| 3 | [ใส่ query ที่ 3] | [ใส่คำตอบผิดที่ agent ให้] | [ใส่คำตอบที่ถูกต้อง] | Retrieval / Reasoning |

## รายละเอียดแต่ละกรณี

### 1. [แชมป์ฟุตบอลโลกล่าสุดคือ]

**Trace:**

[<img width="321" height="60" alt="image" src="https://github.com/user-attachments/assets/8383d6ee-335d-46af-9876-56ae112f28c7" />
]

**วิเคราะห์**: [อธิบายว่าทำไมถึงผิด — เช่น Qdrant คืน chunk ที่ไม่เกี่ยวข้องมาเป็นอันดับ 1 (retrieval) หรือ chunk ที่ได้มาถูกต้องแต่ agent สรุปความผิด (reasoning)]

**ชนิดความผิด**: [Retrieval error / Reasoning error]

---

### 2. [ใส่ query ที่ 2]

**Trace:**

[แนบ screenshot]

**วิเคราะห์**: [อธิบาย]

**ชนิดความผิด**: [Retrieval error / Reasoning error]

---

### 3. [ใส่ query ที่ 3]

**Trace:**

[แนบ screenshot]

**วิเคราะห์**: [อธิบาย]

**ชนิดความผิด**: [Retrieval error / Reasoning error]

---

