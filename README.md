# [iTracking](https://mnre-servicelink.github.io/iTracking)
โปรแกรมติดตามสถานะคำขอของศูนย์บริการร่วม กระทรวงทรัพยากรธรรมชาติและสิ่งแวดล้อม
พัฒนาเมื่อ ปี พ.ศ. 2566
## Officers' Manual
คู่มือการดูแลระบบติดตามสถานะคำขอ (e-Tracking) สำหรับเจ้าหน้าที่
1. รับคำขอ
2. ออกรหัสคำขอ ด้วยโปรแกรม [ID Gen](https://kietpawpan.github.io/chatBot/IDGen.html)<sup>TM</sup>
3. หน่วยงานที่รับคำขอ แจ้งรหัสคำขอ และความคืบหน้าให้ ทส. ทราบทางอีเมล servicelinkcenter@mnre.go.th
4. ทส.  update โปรแกรม โดยคลิกที่เมนู <> Code ด้านบน เพื่อเปิดไฟล์ iTrack.js
5. คัดลอก Code ด้านล่างนี้  วางในไฟล์ iTrack.js
6. แก้ไขข้อความ 2 แห่ง ใน Code ที่เพิ่งวางไป

```
else if(text=="เติมรหัสคำขอตรงนี้"){ 
  window.alert(document.getElementById("iRequest").innerHTML = 
     "รหัสคำขอ " + text + " เติมรายละเอียดความคืบหน้าตรงนี้");
  document.getElementById("orgEmail").innerHTML = 
     "สอบถามเพิ่มเติม: <br>" + text3 + " <br>อีเมล "+ eMail + 
     "<br>โทร. " + orgTel + "<br>ในวันทำการ ตั้งแต่เวลา " + 
     serviceTime;
 document.getElementById("emailForCopy").innerHTML = eMail;}
```
5. บันทึกการแก้ไข
6. จัดทำ QR Code ของโปรแกรม eTracking: URL https://mnre-servicelink.github.io/iTracking/
7. แจ้ง QR Code และรหัสคำขอ ให้ผู้ยื่นคำขอทราบ

## History
v1.0.0 | 27 April 2023
- Prototype
- Adapted from Kietpawpan's jTech code
