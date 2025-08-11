# Tài liệu SkyCS (client)

SkyCS chia thành các module chính sau:
1. [Khách hàng](https://github.com/khanh2142/tai-lieu-skycs/blob/main/1.%20Kh%C3%A1ch%20h%C3%A0ng)
2. eTicket
3. Kho tri thức
4. Chiến dịch
5. Giám sát
6. Báo cáo
7. [Quản trị](https://github.com/khanh2142/tai-lieu-skycs/blob/main/7.%20Qu%E1%BA%A3n%20tr%E1%BB%8B)
8. Dịch vụ

---

## Các thành phần quan trọng trong dự án

### Trường tĩnh, trường động

> #### Trường tĩnh
> - Là các trường có các mã code/codesys cố định trong hệ thống hoặc FlagIsColDynamic = 0, chỉ để xử lý trường cố định
> - VD: Trường mã khách hàng có ColCodeSys = CustomerCodeSys thì client luôn xử lý trường này theo yêu cầu cố định (render thành textfield), không thay đổi

> #### Trường động
> - Là các trường có các mã code/codesys không cố định trong hệ thống hoặc FlagIsColDynamic = 1, dùng để xử lý nhiều trường với nhiều kiểu dữ liệu khác nhau
> - VD: Trường mã khách hàng có ColCodeSys = TKCCFGF5N20552 thì client phải check theo ColDataType rồi xử lý tiếp

> _Trường tĩnh, trường động thường sử dụng nhiều trong hệ thống, tham khảo thêm ở module [Quản trị](https://github.com/khanh2142/tai-lieu-skycs/blob/main/7.%20Qu%E1%BA%A3n%20tr%E1%BB%8B)_

### Call
