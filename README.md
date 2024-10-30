## ESP32-ble_ancs - `ble_ancs`
## ขั้นตอนการใช้งาน
1. เริ่มต้นโดยการเลือกตัวอย่าง `ble_ancs`
# ![Screenshot 2024-10-30 212243](https://github.com/user-attachments/assets/c4b21a63-6937-417d-b783-571a04332518)

# ![Screenshot 2024-10-30 212250](https://github.com/user-attachments/assets/c4ee75c5-f7bc-408c-ada0-83d3486013c0)


2. หลังจากเลือกตัวอย่างแล้ว ให้กดปุ่ม **Create**
# ![Screenshot 2024-10-30 212255](https://github.com/user-attachments/assets/dcc0fc1a-8822-410a-9d9c-10278ba9b2ec)



3. ตรวจสอบโค้ดในไฟล์ ` ble_ancs_demo.c` สามารถแก้ไขเป็นชื่อบูลทูธของตัวเองที่ต้องการ เพราะจะได้เชื่อมต่อได้อย่างถูกต้อง
# ![Screenshot 2024-10-30 212349](https://github.com/user-attachments/assets/ba79c76f-735c-4c31-b217-ff71c0e8daee)
# ![image](https://github.com/user-attachments/assets/617d6d5a-8574-4b74-b34b-e0701688ab25)

เเก้ไขซึ่งสามารถตั้งชื่อให้กับอุปกรณ์ที่จะเชื่อมต่อได้
```
#define BLE_ANCS_TAG    "BLE_ANCS"
#define EXAMPLE_DEVICE_NAME   "ESP_BLE_ANCS_TEEPOP109"
```

ตัวอย่างการเเก้ไขดังนี้
# ![Screenshot 2024-10-30 212407](https://github.com/user-attachments/assets/621a9562-360a-4da9-9b86-e5a3e675ede4)



## กด Buildเเละรันโปรแกรม

กด Build และรันโปรแกรม จากนั้นเลือก **UART**
# ![Screenshot 2024-10-30 212602](https://github.com/user-attachments/assets/71670eef-dd3d-4170-94e4-db44e386916f)

จะเเสดงสถานะการทำงาน
# ![Screenshot 2024-10-30 212704](https://github.com/user-attachments/assets/6e31294d-060d-43fa-acee-f03a4fc4d68f)

จากนั้นจะเจอบูลทูธที่เรากำหนดไว้ ซึ่งเรากำหนดไว้ว่า " ESP_BLE_ANCS_TEEPOP109 "
ผลลัพธ์จะมีลักษณะดังนี้:
# ![image](https://github.com/user-attachments/assets/98026014-119f-4a83-818e-429c9a1cd88b)

## ทดลองโดยให้เชื่อม Bluetooth กับอุปกรณ์ของ IOS ที่มี
# ![image](https://github.com/user-attachments/assets/b621cede-5e34-4d42-8d68-7b729f7fd9f8)
# ![image](https://github.com/user-attachments/assets/950c16c8-4d4b-4cf8-b1d7-0b97fe4488e9)

จะเเสดงสถานะการทำงานใน Serail Moniter จะมีการแจ้งว่าเกิดการเชื่อมต่อโดย
# ![Screenshot 2024-10-30 212741](https://github.com/user-attachments/assets/d6d9bf11-c6a9-4d79-b646-3b1ef2032e27)

ผลการทำงานจะพบว่าจะแจ้งว่ามีการแจ้งเตือนอะไรที่เกิดขึ้นในอุปกรณ์ IOS ที่เชื่อมต่อ
# ![Screenshot 2024-10-30 212952](https://github.com/user-attachments/assets/3eb53d4f-e5af-4bcb-8965-d447eaa54722)

### สรุปการทดลอง
ble_ancs หรือ Bluetooth Low Energy Apple Notification Center Service เป็นบริการ BLE ที่ถูกออกแบบโดย Apple เพื่อให้แอปพลิเคชันบนอุปกรณ์ต่าง ๆ (เช่น ESP32) สามารถเชื่อมต่อกับ iOS เพื่อรับการแจ้งเตือนจากศูนย์แจ้งเตือนของ iPhone หรือ iPad ได้ เช่น การแจ้งเตือนข้อความ อีเมล สายโทรเข้า เป็นต้น
