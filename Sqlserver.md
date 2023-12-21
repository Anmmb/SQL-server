
## Kiểm Tra SQL Server Đang Chạy ?
- Dịch Vụ Của Windows: Services, Kiểm Tra Dịch Vụ ```SQL Server```, (Có Thể Khởi Động Lại, Dừng , Chạy ). Đảm Bảo Dịch Vụ ```SQL Server Browser``` Cũng Đang Chạy

- Cấu Hình Cơ Bản SQL Server: Chạy Chương Trình 
**SQL Server Configuration Manager**.

## Kết Nối/Quản Lý Database SQL Server
- Dùng Chương Trình ```Azure Data Studio``` Hoặc ```SQL Server Management Studio (SSMS)```
- Mặc Định Ban Đầu Sử Dụng Phần Mềm SSMS Kết Nối Bằng Tài KHoản Windows (Không Cần Pass Trên Chính Máy Cài SQL Server)
## Kich hoat tai khoan SA (Supper Admin)
- Chạy SSMS, Nhấp Phải Chuột vào SQL Server 
- Chọn Properties, Chọn Security, Chọn Mục SQL Server and Windows Authentication mode.
- Đổi Password Và Tài Khoản sa(**super-admin**)
- Chạy query sau:
```
ALTER LOGIN sa ENABLE;
GO
ALTER LOGIN sa WITH PASSWORD = '<enterStrongPasswordHere>';
GO
```
- Lúc Này Có Thể Kết Nối Tới SQL Server Bằng Tài Khoản sa (**SuperAdmin**)
- Sau cac thiet lap phai khoi dong lai SQL Server
## Kich hoat ket noi SQL Server qua mang (Network)
- Chạy SQL Server Configuration Manager, Chọn SQL Server Network Configuration, chon Protocol for SQL...
- Nhấn Phải Chuột Vào TCP/IP chon Properties, Tại tab Protocal Chọn Enabled -> Yes, Sau Đó Tại tab IP Address MỤc TCP Port Chọn Cổng Mặc Định (CHọn 1433 Hoặc Cổng Cố Định Nào Đó Mong Muốn)
- Sau Các THiết Lập Phải Khởi Động Lại SQL Server
- Lưu Ý Cần Thiết firewall Của Windows Cho Phép Mở Cổng SQL Server (cong 1433), 
Chi Tiết Cách Mở Cổng Tại: https://learn.microsoft.com/en-us/sql/database-engine/configure-windows/configure-a-windows-firewall-for-database-engine-access?view=sql-server-ver16#to-open-a-port-in-the-windows-firewall-for-tcp-access

## Sử Dụng SSMS Hoặc Azure Data Studio
- Dùng Để Quản Lý Database Và Thực Hiện Các Câu Lệnh Truy Vấn (query) Đến Cơ Sở Dữ Liệu (database)