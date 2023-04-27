# [iTracking](https://mnre-servicelink.github.io/iTracking)
โปรแกรมติดตามสถานะคำขอของศูนย์บริการร่วม กระทรวงทรัพยากรธรรมชาติและสิ่งแวดล้อม
พัฒนาเมื่อ ปี พ.ศ. 2566
## คู่มือการใช้โปรแกรม eTracking สำหรับเจ้าหน้าที่
1. รับคำขอ
2. ออกรหัสคำขอ ด้วยโปรแกรม [ID Gen](https://kietpawpan.github.io/chatBot/IDGen.html)
3. แก้ไขไฟล์ iTrack.js โดยเพิ่มเติมข้อมูลความคืบหน้า

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
6. จัดทำ QR Code ของโปรแกรม eTracking: URL
7. แนบ QR Code ไว้ท้ายหนังสือขยายเวลา

## History
v1.0.0 | 27 April 2023
- Prototype
- Adapted from Kietpawpan's jTech code
