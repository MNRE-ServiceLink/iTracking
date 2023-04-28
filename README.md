# [iTracking](https://mnre-servicelink.github.io/iTracking)
โปรแกรมติดตามสถานะคำขอของศูนย์บริการร่วม กระทรวงทรัพยากรธรรมชาติและสิ่งแวดล้อม
พัฒนาเมื่อ ปี พ.ศ. 2566
## Officers' Manual
คู่มือการดูแลระบบติดตามสถานะคำขอ (e-Tracking) สำหรับเจ้าหน้าที่
1. เจ้าหน้าที่ รับคำขอ จากประชาชน
2. เจ้าหน้าที่แต่ละหน่วยงาน ออกรหัสคำขอ ด้วยโปรแกรม [ID Gen](https://mnre-servicelink.github.io/iTracking/IDGen.html)<sup></sup> ของศูนย์บริการร่วม กระทรวงทรัพยากรธรรมชาติและสิ่งแวดล้อม
3. เจ้าหน้าที่ที่รับคำขอ แจ้งรหัสคำขอ ให้ประชาชนทราบ เพื่อใช้ติดตามผลผ่านระบบติดตามสถานะคำขอของกระทรวงทรัพยากรธรรมชาติและสิ่งแวดล้อม (e-Tracking) ทาง URL
[https://mnre-servicelink.github.io/iTracking/](https://mnre-servicelink.github.io/iTracking/)
4. เจ้าหน้าที่ที่รับคำขอ ส่งรหัสคำขอและข้อมูลความคืบหน้าให้ ทส. ทราบทางอีเมล servicelinkcenter@mnre.go.th ในวันที่รับคำขอ และแจ้งความคืบหน้าทุกครั้ง
4. เจ้าหน้าที่ ศบร.ทส. update โปรแกรม โดยคลิกที่เมนู <> Code ด้านบน เพื่อเปิดไฟล์ iTrack.js โดยคัดลอก Code ด้านล่างนี้  วางในไฟล์ iTrack.js
แล้วแก้ไขข้อความ 2 แห่ง ใน Code ดังนี้

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
6. ประชาชน ติดตามความคืบหน้าผ่าน[ระบบติดตามสถานะคำขอของกระทรวงทรัพยากรธรรมชาติและสิ่งแวดล้อม](https://mnre-servicelink.github.io/iTracking/)

## History
v1.0.0 | 28 April 2023
- Prototype
- Adapted from Kietpawpan's jTech code
