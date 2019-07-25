# API For NKC MAPS

## get_category

ใช้สำหรับดึงข้อมูลประเภทสถานที่

ที่ตั้ง : https://map.numfa.com/api/get_category.php

พารามิเตอร์ : ไม่ต้องการ

รูปแบบ output : json

**ตัวอย่าง**

```json
[{"categoryid":"1",
 "name":"ที่พัก",
 "description":"แหล่งที่พัก",
 "admin_id_add":null,
 "admin_id_last_edit":"1"
}]
```

## get_grouping

ใช้สำหรับรับข้อมูลรายการหมวดหมู่ย่อยของประเภทสถานที่

ที่ตั้ง : https://map.numfa.com/api/get_grouping.php

การส่งข้อมูล : GET

พารามิเตอร์ : id

ส่งข้อมูลเป็น id ของ category

รูปแบบ output : json

**ตัวอย่าง**

```json
[{"groupingid":"1",
 "name":"หอพักชาย",
 "description":"หอพักชาย",
 "categoryid":"1",
 "admin_id_add":null,
 "admin_id_last_edit":null
 }]
```

## get_place

ใช้ดึงรายการข้อมูลสถานที่

ที่ตั้ง : https://map.numfa.com/api/get_place.php

การส่งข้อมูล : GET

พารามิเตอร์ : category,grouping,-

ส่งข้อมูลเป็น id ของ category และ id ของ grouping หากไม่เติม จะดึงรายการสถานที่ทั้งหมด

รูปแบบ output : json

**ตัวอย่าง**

```json
[{"placeid":"1",
 "name":"โรงแรม ไดซูแนล รีสอร์ท",
 "longitude":"102.744012",
 "latitude":"17.818645",
 "categoryid":"1"
}]
```

## place

ใช้ดึงรายละเอียดสถานที่

ที่ตั้ง : https://map.numfa.com/api/place.php

การส่งข้อมูล : GET

พารามิเตอร์ : id

ส่งข้อมูลเป็น id ของ place

รูปแบบ output : json

**ตัวอย่าง**

```json
[{"placeid":"1",
 "name":"โรงแรม ไดซูแนล รีสอร์ท",
  "phone":"0837044255",
  "longitude":"102.744012",
  "latitude":"17.818645",
  "description":"บริการห้องพัก<br \/>\r\nเบอร์โทร : 083-704-4255 , 087-563-9366",
  "categoryid":"1",
  "groupingid":"4",
  "image":"https:\/\/i.imgur.com\/hw5SJ3X.jpg"
 }]
```
