# BÀI LÀM – THI THỬ HACKATHON 02 (GAMEZONE)

- **Họ tên: TẠ ĐÌNH NAM KHÁNH** 
- **Lớp:CNTT3** 
- **Link repository:https://github.com/namkhanh2008/THI_THU** 
- **Hệ điều hành (Windows/macOS):WINDOWS** 

## 4.2. Thao tác CLI

### Các lệnh đã chạy

```shell
pwd
PS D:\de-on-tap-game\starter-kit\GameZone Website FINAL> mv .\Cap_Nhat.txt .\docs\
PS D:\de-on-tap-game\starter-kit\GameZone Website FINAL> Get-ChildItem -Recurse -Force
PS D:\de-on-tap-game\starter-kit\GameZone Website FINAL> cp .\Logo_GameZone.PNG .\backup\
PS D:\de-on-tap-game\starter-kit\GameZone Website FINAL> rm  temp_207.tmp
PS D:\de-on-tap-game\starter-kit\GameZone Website FINAL> cd .\logs\
PS D:\de-on-tap-game\starter-kit\GameZone Website FINAL\logs> ls
PS D:\de-on-tap-game\starter-kit\GameZone Website FINAL\logs> cd ..


```

### Kết quả liệt kê toàn bộ dự án

```text
   Directory: D:\de-on-tap-game\starter-kit\GameZone Website FINAL


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/26/2026   1:14 PM                backup
d-----        10/26/2026   1:16 PM                data
d-----        10/26/2026   1:19 PM                docs
d-----        10/26/2026   1:16 PM                logs
d-----        10/26/2026   1:13 PM                media
-a----        10/26/2026   1:10 PM             70 .env
-a----        10/26/2026   1:10 PM           8542 Logo_GameZone.PNG
-a----        10/26/2026   1:10 PM             22 temp_207.tmp


    Directory: D:\de-on-tap-game\starter-kit\GameZone Website FINAL\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM           5814 Giao_Dich_Thang11.xlsx


    Directory: D:\de-on-tap-game\starter-kit\GameZone Website FINAL\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM             61 Cap_Nhat.txt


    Directory: D:\de-on-tap-game\starter-kit\GameZone Website FINAL\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM            986 game.log


```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
PS D:\de-on-tap-game\starter-kit\GameZone Website FINAL> Get-Content .\logs\game.log | Select-String "ERROR" >> .\logs\daily_report.txt

```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game

```

## 4.4. README.md

> Chấm trực tiếp trên `README.md` ở gốc dự án.

- [x] Heading 1
- [x] Mô tả in đậm + in nghiêng
- [x] Bảng `Thư mục | Nội dung` (≥3 dòng)
- [x] Code block lệnh liệt kê
- [x] Task list (≥2 việc, ≥1 đã xong)
- [x] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report

### Lệnh chạy

```shell
.\auto_report.ps1
	Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

### Nội dung file logs/auto_report.txt

```text
=== BAO CAO LOI GAMEZONE ===

2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:12:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:39:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:42:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:51:15 [ERROR] Loi luu tien trinh choi



```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
 (Get-Content .\logs\game.log | Select-String "ERROR").COUNT

```

### Kết quả đếm

```text
6

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell

PS D:\de-on-tap-game\starter-kit\GameZone Website FINAL\logs> (Get-Content .\game.log | Select-String "WARNING").COUNT >> tong_hop.txt
(Get-Content .\game.log | Select-String "ERROR").COUNT >> tong_hop.txt


```

### Nội dung file logs/tong_hop.txt

```text
=== TONG HOP LOG GAMEZONE ===
1
6

```

## 4.8. Excel

> Chấm trực tiếp trên file `data/giao_dich_thang_11.xlsx`.
