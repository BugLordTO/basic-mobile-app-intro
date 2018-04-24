# Ionic เบื้องต้น

หลังจากที่เราได้ทำตามขั้นตอน [การติดตั้ง Ionic](installing-ionic.md) คราวนี้เราจะมาสร้าง App ตัวแรกของเรากัน :)

> โดยปรกติ Ionic ใช้ภาษา TypeScript ในการทำงาน หากคุณไม่คุ้นเคยกับภาษา TypeScript ก็ไม่ต้องกังวลเพราะมันคล้ายกับ JavaScript ปกตินั่นแหละ  แต่ถ้าคุณต้องการอ่านข้อมูลเพิ่มเติม  [ให้คลิกที่นี่](https://ionicframework.com/docs/developer-resources/what-is/#typescript)


### เริ่มต้นสร้าง Ionic App

ในการสร้าง App แรกของเราให้ทำการเปิดหน้าต่าง command และใช้คำสั่ง  
```
ionic start MyIonicProject tutorial
```

* `start` เป็นคำสั่งในการสร้าง App ขึ้นมาใหม่
* `MyIonicProject` เป็นชื่อของ App ใหม่ที่จะสร้าง โดยโปรแกรมจะสร้างโฟลเดอร์ชื่อเดียวกันขึ้นมา
* `tutorial` คือ template ที่ Ionic เตรียมไว้ให้ (ในตัวอย่างนี้เลือกเป็น tutorial template)

ในการสร้าง App ใหม่นี้ มันจะทำการติดตั้ง [node modules](https://ionicframework.com/docs/developer-resources/what-is/#npm) แล้วจะถามให้ตั้งค่าการติดตั้ง [Cordova](https://ionicframework.com/docs/developer-resources/what-is/#cordova) อีกด้วย

Ionic ได้มี template ที่เตรียมไว้ให้ดังนี้

* `tabs` : App ที่มีแท็บอยู่ทั้งหมด 3 แท็บ
* `sidemenu` : App ที่มีเมนูด้านข้าง ที่สามารถเลื่อนดูได้
* `blank` : App มาตรฐานที่ไม่มีอะไรเลย
* `super` : App ที่มีหน้าต่างๆที่เตรียมไว้แล้ว 14 หน้า
* `tutorial` : App สำหรับแนะนำผู้ใช้ใหม่เพื่อให้เข้าใจการเริ่มต้นส้ราง App

หากคุณไม่ได้เลือก template ไว้โปรแกรมจะแจ้งเตือนให้เลือก template อย่างใดอย่างหนึ่งก่อนถึงจะทำขั้นตอนต่อไปได้

### การเรียกดู App ของเราผ่าน Browser

ในตอนนี้เราจะใช้คำสั่งด้านล่างเพื่อเข้าไปยังโฟเดอร์ที่ถูกสร้างขึ้นมาใหม่
```
cd MyIonicProject
```

หลังจากนั้นเราจะเรียก app ของเราขึ้นมาดูบน browser ด้วยคำสั่งด้านล่างนี้
```
ionic serve
```

![alt](https://ionicframework.com/img/docs/tutorial-screen.png)