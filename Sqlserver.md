
## Kiem tra SQL Server dang chay?
- Dich vu cua Windows: Services, kiem tra dich vu ```SQL Server```, (co the khoi dong lai, dung, chay). Dam bao dich vu ```SQL Server Browser``` cung dang cahy

- Cau hinh co ban cua SQL Server: chay chuong trinh 
**SQL Server Configuration Manager**.

## Ket noi/quan ly Database SQL Server
- Dung chuong trinh ```Azure Data Studio``` hoac ```SQL Server Management Studio (SSMS)```
- Mac dinh ban dau dung phan mem SSMS ket noi bang tai khoan Windows (khong can passwor tren chinh may cai SQL Server)
## Kich hoat tai khoan SA (Supper Admin)
- Chay SSMS, phai chuot vao SQL Server, chon Properties, chon Security, chon muc SQL Server and Windows Authentication mode.
- Doi password tai khoan sa: chay query sau:
```
ALTER LOGIN sa ENABLE;
GO
ALTER LOGIN sa WITH PASSWORD = '<enterStrongPasswordHere>';
GO
```
- Luc nay co the ket noi toi SQL Server bang tai khoan sa
- Sau cac thiet lap phai khoi dong lai SQL Server
## Kich hoat ket noi SQL Server qua mang (Network)
- Chay SQL Server Configuration Manager, chon SQL Server Network Configuration, chon Protocol for SQL...
- Nhan phai chuot vao TCP/IP chon Properties, tai tab Protocal chon Enabled -> Yes, sau do tai tab IP Address muc TCP Port chon cong mac dinh (chon 1433 hoac cong co dinh nao do mong muon)
- Sau cac thiet lap phai khoi dong lai SQL Server
- Luu y can thiet lap firewall cua Windows cho phep mo cong SQL Server (cong 1433), chi tiet cach mo cong tai: https://learn.microsoft.com/en-us/sql/database-engine/configure-windows/configure-a-windows-firewall-for-database-engine-access?view=sql-server-ver16#to-open-a-port-in-the-windows-firewall-for-tcp-access

## Su dung SSMS hoac Azure Data Studio
- Dung de quan ly Database va thuc hien cac cau truy van (query) den co so du lieu (database)