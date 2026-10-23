# BÀI LÀM – THI THỬ HACKATHON 01

- **Mã đề:** Thi thử
- **Họ tên:** Nguyễn Vũ Long
- **Lớp:** HN-KS26-CNTT3
- **Link repository:** [GitHub](https://github.com/vulong1712/-CNTT3_Nhap-mon-CNTT_ThiThu)
- **Hệ điều hành (Windows/macOS):** Windows

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
 pwd
 ls -r -Force
 mv .\nhap_hang.txt .\docs\
 mv .\logo_van_phong_pham.PNG .\media\
 cp .\media\logo_van_phong_pham.PNG .\backup\
 rm .\temp_131.tmp
 cd .\logs\
 ls
 cd ..
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
 Directory: D:\THITHUDAY4\starter-kit\van-phong-pham-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/23/2026   8:37 AM                backup
d-----        10/23/2026   8:38 AM                data
d-----        10/23/2026   8:37 AM                docs
d-----        10/23/2026   8:38 AM                logs
d-----        10/23/2026   8:37 AM                media
-a----        10/23/2026   8:32 AM             78 .env
-a----        10/23/2026   8:32 AM           2253 bai_lam.md
-a----        10/23/2026   8:32 AM           6053 logo_van_phong_pham.PNG
-a----        10/23/2026   8:32 AM             51 nhap_hang.txt
-a----        10/23/2026   8:32 AM             22 temp_131.tmp


Directory: D:\THITHUDAY4\starter-kit\van-phong-pham-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/23/2026   8:32 AM           6105 don_ban_thang_10.xlsx

 Directory: D:\THITHUDAY4\starter-kit\van-phong-pham-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/23/2026   8:32 AM           1053 shop.log

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
PS D:\THITHUDAY4\starter-kit\van-phong-pham-website> Get-content .\logs\shop.log | Select-String "ERROR" >logs/daily_report.txt
```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2025-10-28 08:24:28 [ERROR] Thanh toan bi tu choi
2025-10-28 08:30:28 [ERROR] Thanh toan bi tu choi
```

## 4.4. Thao tác với tài liệu Markdown (README.md)

> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [X] Heading 1: tên dự án
- [X] Mô tả ngắn có cả **in đậm** và *in nghiêng*
- [X] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
- [X] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
- [X] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
- [X] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
 D:\THITHUDAY4\starter-kit\van-phong-pham-website>Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
 D:\THITHUDAY4\starter-kit\van-phong-pham-website>.\auto_report.ps1
Dang loc log..."=== BAO CAO LOI ===
Hoan thanh!

```

### Nội dung file logs/auto_report.txt

```text
2025-10-28 08:24:28 [ERROR] Thanh toan bi tu choi
2025-10-28 08:30:28 [ERROR] Thanh toan bi tu choi
2025-10-28 08:33:28 [ERROR] Ket noi kho du lieu that bai
2025-10-28 08:39:28 [ERROR] Ket noi kho du lieu that bai
2025-10-28 08:42:28 [ERROR] Ket noi kho du lieu that bai
2025-10-28 09:12:28 [ERROR] Thanh toan bi tu choi

```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
(Get-content .\logs\shop.log | Select-String "ERROR").count

```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
6

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
.\auto_report.ps1

```

### Nội dung file logs/tong_hop.txt

```text
===Tong hop log===

2025-10-28 08:51:28 [WARNING] Thoi gian tai trang cham
2025-10-28 08:54:28 [WARNING] Anh san pham dung luong lon
2025-10-28 08:57:28 [WARNING] Thoi gian tai trang cham

6
```

## 4.8. Excel

> Phần Excel được chấm trực tiếp trên file `data/don_ban_thang_10.xlsx`, không cần ghi vào đây.
