### Intro
![img](/imgs/ionic-view-logo.png)  

---

### Overview
- ลงโปรแกรม
- สร้าง App ถ่ายรูปอัพลง instragram
- รันจริงบน mobile !!

---

### ลงโปรแกรม
- git  
 [32-bit Git for Windows Setup.](https://github.com/git-for-windows/git/releases/download/v2.16.2.windows.1/Git-2.16.2-32-bit.exe)  
 [64-bit Git for Windows Setup.](https://github.com/git-for-windows/git/releases/download/v2.16.2.windows.1/Git-2.16.2-64-bit.exe)  
 [macOS Setup.](https://git-scm.com/download/mac)

- Visual Code  
[Visual Code](https://code.visualstudio.com/)  

---

### ลงโปรแกรม (ต่อ)
- ionic view บน play store  
[ionic view](https://play.google.com/store/apps/details?id=com.ionicframework.view)  

- ข้อจำกัด สำหรับ ionic view  
  - ปัจจุบันใช้ได้เฉพาะบน android 

---

### สร้าง app  ถ่ายรูป
- สร้าง app  
```
ionic start myapp tabs
```
- เพิ่ม plugin camera  
```
ionic cordova plugin add cordova-plugin-camera

npm install —save @ionic-native/camera
```
- run app  
```
ionic serve
```

---

### ลง Code  
![img](/imgs/day-3-code-1.png)  
```ts
import { Camera } from '@ionic-native/camera';
```
![img](/imgs/day-3-code-2.png)  

---

### ลง Code  
- file ```\src\pages\home\home.ts```  
![img](/imgs/day-3-code-5.png)  
```ts
import { Camera, CameraOptions } from '@ionic-native/camera';
```

![img](/imgs/day-3-code-3.png)  
```ts
, private camera: Camera
```

---

### ลง Code  
![img](/imgs/day-3-code-4.png)  
```ts
imgdata: string;
```

---

### ลง Code  
![img](/imgs/day-3-code-6.png)  

---

### ลง Code  
```ts
capture() {
    const options: CameraOptions = {
      quality: 100,
      destinationType: this.camera.DestinationType.DATA_URL,
      encodingType: this.camera.EncodingType.JPEG,
      mediaType: this.camera.MediaType.PICTURE,
      correctOrientation: true
    }

    this.camera.getPicture(options).then((imageData) => {
      let base64Image = 'data:image/jpeg;base64,' + imageData;
      this.imgdata = base64Image;
    }, (err) => {
      console.log(err);
    });
  }
```  

---

### ตกแต่งหน้าตา app  
- file ```\src\pages\home\home.html```  
![img](/imgs/day-3-code-7.png)  

---

### ตกแต่งหน้าตา app (ต่อ)  
```
<br/>
<button ion-button (click)="capture()">Capture</button>
<br/>
<ion-img width="200" height="200" src="{{imgdata}}"></ion-img>
```

---

### สร้าง app บน ionic pro  
[https://ionicframework.com](https://ionicframework.com)  
![img](/imgs/day-3-upload-6.png)  

---

### อัพโหลด app ขึ้น ionic pro  
![img](/imgs/day-3-upload-4.png)  
![img](/imgs/day-3-upload-5.png)  

---

### อัพโหลด app ขึ้น ionic pro (ต่อ)  
- link app ที่ local กับบน ionic pro  
- เปิด git bash  

![img](/imgs/day-3-upload-3.png)  
- พิมพ์ command เพื่อไปที่โฟลเดอร์ app  
```
cd /f/git/myapp
```  

---

### อัพโหลด app ขึ้น ionic pro (ต่อ)  
- พิมพ์ command เพื่อ link กับ ionic pro  
```
ionin link [app-id]
```
![img](/imgs/day-3-upload-1.png)  
- ตั้งค่า username และ email ของ git

---

### อัพโหลด app ขึ้น ionic pro (ต่อ)  
```
git config —global user.name "{your username}"
git config —global user.email {your email}
```
- push code เข้า ionic pro  
```
git push ionic master
```
---

### อัพโหลด app ขึ้น ionic pro (ต่อ)
![img](/imgs/day-3-upload-2.png)  

---

### รันจริงบน mobile !!
![img](/imgs/day-3-upload-7.jpg)  

---

### Share & comment
---