# AI Usage Report — Agentic RAG Homework


## จุดที่ใช้ AI ช่วย

| ส่วนที่ใช้ | ใช้ AI ช่วยอะไร | สิ่งที่แก้ไข/ปรับเองหลังจากได้คำตอบจาก AI |
|---|---|---|
| ขั้นตอนที่ 1 (Chunk+Embed+Search) | ขอโครงโค้ดสำหรับอ่านไฟล์, chunk, embed, upsert เข้า Qdrant | [ใส่ว่าคุณปรับอะไรบ้าง เช่น เปลี่ยนวิธี query, debug error ที่เกิดขึ้นจริง] |
| ขั้นตอนที่ 2 (Agent+Custom Tool) | ขอไอเดีย custom tool (เลือกใช้ตัวแปลงอุณหภูมิ) และโครง Agent ด้วย Google ADK | [ใส่การปรับแต่งของคุณ] |
| ขั้นตอนที่ 3 (RAG Agent+Judge) | ขอโครง RAG tool ที่ค้นจาก Qdrant และโค้ด LLM-as-Judge | [ใส่การปรับแต่งของคุณ] |
| Debug | แก้ปัญหา `401 UNAUTHENTICATED` (ADK พยายามใช้ Vertex AI/OAuth แทน API key) และ `429 RESOURCE_EXHAUSTED` (โมเดล gemini-3.1-pro ไม่มี free tier quota เลย ต้องเปลี่ยนไปใช้รุ่น flash) | ปรับ `GOOGLE_GENAI_USE_VERTEXAI=FALSE` และเปลี่ยนโมเดลเป็น `gemini-flash-latest` |


## สิ่งที่แก้ไขเอง / ปรับจากคำตอบของ AI

[อธิบายว่าโค้ดหรือคำอธิบายที่ AI ให้มา มีจุดไหนที่คุณต้องแก้เพิ่ม เพื่อให้ทำงานได้จริงกับ environment ของคุณ หรือให้ตรงกับผลลัพธ์ที่ได้จากรหัสนักศึกษาของคุณ]
