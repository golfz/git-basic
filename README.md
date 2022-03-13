# Git Basic

## Log

```shell
git log --oneline
```

```shell
git log --oneline --stat
```

## การแก้ไข Commit

1. แก้ไข Commit Message

```shell
git commit --amend -m "new message"
```

2. เพิ่มไฟล์ใน Commit เดิม

```shell
git commit --amend --no-edit
```

## Git Reset

1. --soft : ลบ Commit ทั้งหมดที่อยู่หลัง Commit ID หนึ่ง และนำไฟล์ที่เคยอยู่ใน commit เหล่านั้นกลับมายัง Staging Area

```shell
git reset --soft 3e892f
```

2. --mixed : ลบ Commit ทั้งหมดที่อยู่หลัง Commit ID หนึ่ง และนำไฟล์ที่เคยอยู่ใน commit เหล่านั้นกลับมายัง Working
   Directory

```shell
git reset --mixed 3e892f
```

หรือ

```shell
git reset 3e892f
```

3. --hard : ลบ Commit ทั้งหมดที่อยู่หลัง Commit ID หนึ่ง และทำลายไฟล์ที่เคยอยู่ใน commit เหล่านั้นทิ้งทั้งหมด

```shell
git reset --hard 3e892f
```

## สร้าง Branch ใหม่

สร้าง Branch ใหม่

```shell
git branch test
```

สร้าง Branch ใหม่ พร้อมกับ checkout ไปที่ branch นั้น

```shell
git checkout -b test
```

## แสดงรายชื่อ Branch

```shell
git branch -a
```

ตรวจสอบ Branch บน Remote

```shell
git fetch
git branch -a
```

## การดึง Branch บน Remote ลงมา

checkout ไปที่ branch อื่นก่อน แล้วใช้คำสั่ง

```shell
git checkout --track origin/test
```

## การลบ Branch

```shell
git branch -d test
```

ลบ Branch บน Remote

```shell
git push -d origin test
```

## ดู Log แบบ Graph

```shell
git log --all --graph
```