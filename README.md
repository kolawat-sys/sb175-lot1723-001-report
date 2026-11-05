# SB175 · 39-shot field report

รายงานความเร็ว **Sellier & Bellot .308 Win. HPBT 175 gr (V341812), lot 1723/001** จากข้อมูล 39 รายการของผู้ใช้ ยิงจาก **Bartlein 28″ / Sharp's Rifle**

## เปิดรายงาน

**[เปิดรายงานบนเว็บ](https://kolawat-sys.github.io/sb175-lot1723-001-report/)**

เปิด `index.html` ด้วย Chrome, Edge หรือ browser ที่รองรับ JavaScript รายงานเป็นไฟล์เดียว กราฟ ภาพสินค้า และข้อมูลฝังอยู่ภายใน จึงเปิดอ่านแบบ offline ได้

- **Layer 1 — ภาพรวมสำหรับ shooter:** ค่าเฉลี่ย SD, ES, กราฟรายนัด และคำอธิบายภาษาทั่วไป
- **Layer 2 — เจาะลึกเชิงสถิติ:** confidence intervals, Histogram, Normal Q–Q, ตารางสถิติ, สมมติฐาน และข้อมูลต้นทางทุกแถว
- เลือกจุดหรือเลขลำดับเพื่อดูนัดที่สนใจ ดาวน์โหลด CSV ได้จากปุ่มในรายงาน


## รายงานทดลองตัดข้อมูล (แยกจากผลหลัก)

**[เปิดกราฟทดลองเลือกข้อมูล](https://kolawat-sys.github.io/sb175-lot1723-001-report/trim.html)**

- รายงานหลัก `index.html` ยังคงใช้ครบ 39 รายการ ส่วน `trim.html` เป็น sensitivity analysis แยกหน้า มีกราฟเดียว
- คลิก/แตะจุดเพื่อเอาออกจากการคำนวณ กดซ้ำเพื่อคืนกลับ Mean, Median, Sample SD, ES และจำนวนข้อมูลเปลี่ยนทันที จุดที่เอาออกยังมองเห็นและกดคืนได้
- ใช้ปุ่มตัดต่ำสุด 3 + สูงสุด 3 หรือกำหนดข้างละ 0–18 นัด การตัดเริ่มจากข้อมูลเดิม 39 ค่าเสมอ การเลือกเองต้องเหลืออย่างน้อย 2 ค่า
- มีปุ่มคืนครบ 39 นัด และเลือกผ่าน dropdown / ตาราง / keyboard ได้ การเลือกมีผลเฉพาะหน้าที่เปิด รีเฟรชแล้วกลับเป็น 39 ค่า ไม่เปลี่ยน raw data และไม่บันทึกสถานะในลิงก์ที่แชร์
- การตัดข้างละ 3 เหลือ 33 ค่า: Mean 2,787.95 fps, Sample SD 9.80 fps, ES 37.70 fps เทียบกับฐาน 39 ค่า: Mean 2,788.31 fps, SD 12.85 fps, ES 53.60 fps
- SD ที่ลดลงเกิดจากการคัดเลือกค่าปลายออก ไม่ได้แปลว่ากระสุนสม่ำเสมอขึ้นหรือยืนยันว่าค่าที่ตัดวัดผิด SD หลังเลือกอธิบายเฉพาะค่าที่เหลือ ไม่ใช้แทนข้อมูลเต็ม
- ป้ายวิธีแยก symmetric trimming ออกจาก manual exclusion; สเกลกราฟคงเดิม และแสดง baseline จาก 39 นัดตลอด

กราฟหน้านี้ใช้ SVG และ JavaScript ภายในไฟล์ โดยฝังข้อมูลและ Noto Sans Thai พร้อมใบอนุญาต เช่นเดียวกับรายงานหลักจึงไม่ต้องโหลด runtime จากภายนอก

## ผลหลัก

| Metric | Value |
|---|---:|
| Records | 39 |
| Mean | 2,788.31 fps / 849.88 m/s |
| Median | 2,788.90 fps |
| Sample SD (n−1) | 12.85 fps |
| Extreme spread | 53.6 fps |
| Min / max | 2,766.0 / 2,819.6 fps |
| CV | 0.461% |
| 95% CI, mean | 2,784.14–2,792.47 fps |
| 95% CI, SD under Normal assumption | 10.50–16.56 fps |

## ข้อมูลและข้อจำกัด

เครื่องวัดที่ใช้: **FX True Ballistic Chronograph** ตามที่ผู้ใช้ยืนยัน

ค่าเริ่มต้นสำหรับ **AB Quantum → Muzzle Velocity (MV): 2,788 fps** ปัดจากค่าเฉลี่ย 39 นัดที่ 2,788.31 fps โดยอิงการติดตั้งและตั้งค่าเครื่องถูกต้องตาม [คู่มือ FX](https://www.fxairguns.com/media/btaboqhq/fx-true-ballistic-chronograph.pdf#page=9) ยังไม่ได้ตรวจสอบการติดตั้งหรือการสอบเทียบในวันยิง

ผู้ใช้ยืนยันยิง 2 กล่อง กล่องละ 20 นัด รวม 40 นัด แต่ไม่ได้เปิดเครื่องบันทึกในนัดแรกที่เป็น **clean cold bore** สถิตินี้จึงไม่รวมความเร็วของนัดแรก และไม่มีการเติมค่าทดแทน

ข้อมูล 39 รายการเกิดจากไฟล์ `SB175 lot 1723.001 1st try.csv` จำนวน 9 รายการ ตามด้วย `SB175 lot 1723.001.csv` จำนวน 30 รายการ ตามลำดับที่ผู้ใช้ยืนยัน: ชุด 9 คือยิงจริง 2–10 และชุด 30 คือยิงจริง 11–40 ไม่มีการตัดรายการที่บันทึกออก

ไฟล์ `SB175-Lot1723-001_39-records.csv` เพิ่มคอลัมน์ `combined_record`, `firing_shot` และ `source_file` เพื่อเก็บที่มา โดยรักษาคอลัมน์ต้นฉบับ รวมถึงเลข `shot` ของแต่ละไฟล์

CI ใช้สมมติฐานความเป็นอิสระและ Normal โดยเฉพาะ CI ของ SD ยังไม่ทราบการสอบเทียบ ตำแหน่งวัดหรือสภาพแวดล้อม และไม่ใช้ timestamp ใน CSV เป็นเวลายิงจริง

รายงานนี้อธิบายความเร็วที่บันทึก และแสดงภาพกลุ่มตัวอย่างแยกต่างหาก ไม่ได้จัดเกรดคุณภาพทั้งล็อตหรืออนุมานความแม่นยำบนเป้าจากค่า fps

## แหล่งอ้างอิงและภาพ

- [Sellier & Bellot — .308 Win. HPBT 175 gr V341812](https://www.sellier-bellot.cz/en/products/rifle-ammunition/rifle-ammunition-target-match/detail/472/)
- [Manufacturer PDF datasheet](https://www.sellier-bellot.cz/en/products/rifle-ammunition/rifle-ammunition-target-match/pdf/472/)
- ภาพกล่องและกระสุนจากผู้ผลิตเป็นภาพรุ่นอ้างอิง ไม่ใช่ภาพกล่อง lot ที่นำมายิง
- ผู้ผลิตระบุ 800 m/s จากลำทดสอบ 600 mm ส่วนผลวัดเฉลี่ยนี้ 849.88 m/s จาก Bartlein 28″ (711.2 mm) เป็นคนละเงื่อนไขทดสอบ จึงไม่สรุปสาเหตุของความต่าง
- [NIST — Confidence limits for the mean](https://www.itl.nist.gov/div898/handbook/eda/section3/eda352.htm)
- [NIST — Standard deviation confidence limits](https://itl.nist.gov/div898/software/dataplot/refman1/auxillar/sdconfli.htm)

## การเลือก GitHub repo สำหรับกราฟ

ใช้ **[Apache ECharts 6.1.0](https://github.com/apache/echarts)** ภายใต้ Apache-2.0 รองรับกราฟโต้ตอบและ SVG ซึ่งเหมาะกับหน้ารายงานสองชั้นนี้

ตัวเลือกที่ตรวจประกอบคือ [Observable Plot](https://github.com/observablehq/plot) สำหรับ exploratory visualization และ [Evidence](https://github.com/evidence-dev/evidence) สำหรับรายงานจาก SQL/Markdown เลือก ECharts เพื่อควบคุมการนำเสนอและ interaction ในไฟล์เดียวโดยไม่เพิ่มระบบรายงานหรือฐานข้อมูล

## สถานะการตรวจ

ฉบับ **Editorial** ใช้หน้าปกภาพสินค้า หัวเรื่อง Georgia บนพื้นงาช้าง สีแดงอิฐสำหรับจุดเน้น และ Noto Sans Thai ที่ฝังไว้ในไฟล์ แถบเลือก Layer ติดด้านบนขณะเลื่อนอ่าน ตัวเลขและข้อมูลทั้ง 39 แถวยังคงเดิม

หลักประกอบการออกแบบ:

- [Web Design in 4 Minutes](https://github.com/jgthms/web-design-in-4-minutes) — ความกว้างบรรทัด ระยะห่าง และน้ำหนักสี
- [Magic of CSS](https://github.com/adamschwartz/magic-of-css) — typography, layout และตาราง
- [UI Craft — Editorial](https://github.com/educlopez/ui-craft/blob/main/skills/ui-craft-editorial/SKILL.md) — แนวทางหน้าสไตล์นิตยสาร อ่านเป็นแหล่งอ้างอิง ไม่ได้ติดตั้ง skill เพิ่ม

ออกแบบหน้ารายงานเฉพาะงานนี้ ไม่ได้คัดลอก template จาก repo อ้างอิง

ตรวจ mean และ sample SD ซ้ำกับผล NumPy / Python statistics ตรวจข้อมูล 39 แถวและ hash ต้นฉบับ ทดสอบ logic สลับ Layer, keyboard navigation, เลือกนัด และสร้าง CSV ในแบบจำลอง DOM พร้อมเรนเดอร์กราฟ SVG ด้วย ECharts จริงที่ขนาดกว้างและแคบ

ตรวจเว็บที่เผยแพร่บน GitHub Pages ใน Chrome จริงแล้ว: สลับสอง Layer, เลือกนัดและเลขนัดยิงจริง, เปิดตาราง 39 แถว, โหลดภาพผู้ผลิต และดาวน์โหลด CSV โดย SHA-256 ของไฟล์ที่ดาวน์โหลดตรงกับฉบับส่งมอบ

ตรวจ layout ที่ขนาดหน้าต่างปกติและจำลอง viewport มือถือ 390 และ 320 px แก้กราฟ Histogram / Q–Q ที่เคยล้นจอเมื่อย่อหน้าต่าง แล้วตรวจซ้ำว่าเอกสารไม่ล้นแนวนอนและกราฟย่อตามกรอบ ไม่พบ console error ในรอบที่ตรวจ การจำลอง viewport ไม่ใช่การทดสอบบนโทรศัพท์จริง และยังไม่ได้ตรวจ PDF ที่บันทึกจาก browser

ตรวจแหล่งข้อมูลวันที่ **31 ตุลาคม 2026**

ฉบับ Editorial ตรวจซ้ำบนเว็บจริงใน Chrome ทั้งขนาดหน้าต่างปกติและ viewport 390 / 320 px: ภาพผู้ผลิตโหลดได้, กราฟสี่แบบเรนเดอร์, สลับ Layer และเลือกเลขบันทึก 26 แสดงนัดยิงจริง 27 / shot 17, ตารางต้นทางมี 39 แถว, หน้าหลักไม่ล้นแนวนอนและตารางกว้างเลื่อนภายในกรอบได้ ไม่พบ console error ในรอบที่ตรวจ ส่วน logic CSV และผลคำนวณตรวจซ้ำอัตโนมัติ โดย CSV ไม่เปลี่ยนจากฉบับก่อน

## Third-party notices

Apache ECharts © The Apache Software Foundation, Apache License 2.0 และ Noto Sans Thai © The Noto Project Authors, SIL Open Font License 1.1 ดู `THIRD_PARTY_NOTICES.txt` ภาพสินค้า © Sellier & Bellot และยังคงเป็นสิทธิ์ของเจ้าของเดิม


## ภาพกลุ่มตัวอย่าง — เพิ่ม 5 พฤศจิกายน 2026

[เปิดส่วนภาพกลุ่มที่ 100 เมตร](https://kolawat-sys.github.io/sb175-lot1723-001-report/#target-groups)

- วิธียิง: Bench + Bipod + rear bag support เว้นประมาณ 3–4 วินาทีระหว่างนัด และทำ scope tracking test ร่วมด้วย
- ผู้ใช้ยืนยันว่าภาพทั้งสองเป็น SB175 lot 1723/001 จาก Bartlein 28″ / Sharp's Rifle ในการยิง 40 นัดเดียวกับที่บันทึกความเร็วได้ 39 นัด แต่ไม่ทราบเลขนัดที่ตรงกับแต่ละกลุ่ม จึงไม่จับคู่กับ fps และไม่สรุปผล scope tracking จากภาพนี้
- ตัวอย่าง A: 6 นัด ระยะ 100 m, Group 1.324 cm / 0.455 MOA, Mean Radius 0.548 cm / 0.188 MOA
- ตัวอย่าง B: 5 นัด ระยะ 100 m, Group 1.663 cm / 0.572 MOA, Mean Radius 0.601 cm / 0.207 MOA
- ค่าทั้งหมดถอดจากข้อความ Ballistic-X ในภาพ ไม่ได้วัดหรือสอบเทียบสเกลใหม่ รายละเอียด CEP, Width/Height และ SD บนเป้าอยู่ในตารางที่เปิดดูได้ และแยกจาก SD ความเร็วหน่วย fps
- แสดง A/B เพื่อระบุภาพ ไม่ใช่ลำดับยิง ไม่รวมเป็นกลุ่ม 11 นัดหรือใช้ค่าเฉลี่ยสองกลุ่มแทนผลของทั้งล็อต
- ภาพแสดงแบบซูมเฉพาะกรอบ แต่ฝัง JPEG ต้นฉบับทุก byte ไว้ใน HTML เปิดภาพเต็ม ซูม 100% และดาวน์โหลดต้นฉบับได้ รายงานยังเป็นไฟล์เดียวและไม่มี runtime dependency ภายนอก

SHA-256 ภาพต้นฉบับ:

- `S__122413069_0.jpg`: `dafdb3598bcaaa9b320c152d010fcd7b8f11742273b0ad28038662545c126625`
- `S__122413070_0.jpg`: `1ef219fd2bf127b66d580a879151c6ef47a999ed66664d279d6027c1887e86c2`

ตรวจ byte ของภาพที่ฝังกับต้นฉบับตรงกันทั้งสองภาพ ข้อมูล CSV 39 รายการคงเดิม และการตรวจคำนวณ/interaction เดิมในแบบจำลอง DOM ผ่าน ส่วนนี้ไม่ใช่หลักฐานการทดลองบนโทรศัพท์จริง
