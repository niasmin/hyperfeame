# Prompt templates

Write the descriptive part in Thai or English (keep camera terms in English), dialogue always in Thai inside quotes. Paste identity and location blocks verbatim from `bible.md`.

## 1. Character reference sheet (generate first, once per character)

```
Character reference sheet, photorealistic DSLR photo, wide 16:9 layout.
Same person shown 5 times on a plain light-grey studio background, even soft light:
front view full body, front close-up of the face, 3/4 view, side profile, back view.
[IDENTITY BLOCK]
Outfit: [OUTFIT]
Neutral expression, natural skin texture with pores, no makeup filter.
[Negative: 2D, 3D render, cartoon, anime, plastic skin, airbrushed, extra fingers, text, watermark, logo]
```

Make one more sheet per new outfit, attaching the first sheet and saying "same face as the reference".

## 2. Location reference

```
Photorealistic DSLR photo, wide establishing shot, 16:9.
[LOCATION BLOCK: place, era, time of day, light direction and colour, key props, colour palette]
No people. Natural light, realistic materials.
[Negative: 2D, 3D render, cartoon, text, watermark]
```

## 3. Shot image (Nano Banana, one per shot)

```
ภาพถ่ายจากกล้อง DSLR อัตราส่วน 9:16, [SHOT SIZE] , [ANGLE]:
[IDENTITY BLOCK ของตัวละครในช็อต] (ใช้ภาพอ้างอิงที่แนบ หน้าเดิมทุกจุด)
กำลัง [ACTION หนึ่งอย่าง] ด้วยสีหน้า [EMOTION]
สถานที่: [LOCATION BLOCK]
แสง: [LIGHT], ระยะชัดตื้น พื้นหลังเบลอเล็กน้อย
[Negative: 2D, 3D render, cartoon, low quality, plastic skin, airbrushed skin, extra fingers, deformed hands, text, subtitles, watermark, logo]
```

## 4. Shot video (Flow / Veo, start from the shot image)

```
[CAMERA MOVE, e.g. Static shot / Slow push-in]:
[ACTION in one short sentence].
(พูดเป็นภาษาไทย) ([VOICE LINE จาก bible.md]) "[บทพูดหนึ่งประโยค]"
อารมณ์: [EMOTION], [ambient sound, e.g. เสียงฝนตกเบาๆ]
[ไม่มีเพลง ไม่มีข้อความ ไม่มีซับไตเติล ไม่มีเอฟเฟกต์ ไม่มีกราฟิก ไม่มีการตัดต่อ]
```

A shot with no dialogue drops the speech line and keeps the ambient sound. Keep the closing clause last.

## 5. Shot list row (`shots.md`)

| # | Sec | Size / angle | Move | Who | Action | Line (Thai) | Emotion | Refs |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | 8 | CU, eye level | slow push-in | มายด์ | น้ำตาไหลขณะอ่านข้อความในมือถือ | "เขาโกหกฉันมาตลอดเลยเหรอ…" | ช็อก เสียใจ | มายด์-sheet, ห้องนอน |

## 6. Gemini Gem: script assistant (paste as the Gem's instructions)

```
คุณคือผู้ช่วยเขียนบทซีรีส์สั้นแนวตั้งภาษาไทย ตอนละประมาณ 2 นาที (12 ช็อต ช็อตละ ~10 วินาที)
กติกา:
- ช็อตแรกต้องเปิดด้วยฮุกภายใน 2 วินาที: ช่วงเวลาที่อารมณ์แรงที่สุดของตอน
- ทุกตอนจบด้วยปมที่ยังไม่เฉลย ให้คนอยากดูตอนต่อไป
- บทพูดหนึ่งช็อตไม่เกินหนึ่งประโยคสั้น (~25–35 พยางค์)
- ทุกช็อตมีการกระทำเดียว ระบุขนาดภาพและมุมกล้อง
- ใช้ชื่อตัวละครและสถานที่จากไบเบิลที่ให้ไว้เท่านั้น ห้ามเปลี่ยนรูปลักษณ์
ส่งออกเป็นตารางช็อตลิสต์: #, วินาที, ขนาดภาพ/มุม, การเคลื่อนกล้อง, ตัวละคร, การกระทำ, บทพูด, อารมณ์
```
