# Bài tập số 04 - Trần Thị Thu Hà - K22480106009 - Tạo csdl TKB 
# YÊU CẦU: 
## -  Tạo csdl cho hệ thống TKB (đã nghe giảng, đã xem cách làm)
## -  Nguồn dữ liệu: TMS.tnut.edu.vn
## -  Tạo các bảng tuỳ ý (3nf)
## -  Tạo được query truy vấn ra thông tin gồm 4 cột: họ tên gv, môn dạy, giờ vào lớp, giờ ra.
##  Trả lời câu hỏi: trong khoảng thời gian từ datetime1 tới datetime2 thì có những gv nào đang bận     giảng dạy.
# BÀI LÀM: 
## 1. Tạo csdl cho hệ thống TKB 
- Để tạo csdl cho hệ thống, thì đầu tiên ta phải truy cập vào tms.tnut.edu.vn để lấy dữ liệu
  ![image](https://github.com/user-attachments/assets/d0eee039-502e-4df8-8d92-19c534b7f2b9)
- Dữ liệu trong trang này vẫn là dữ liệu thô vì thế phải chuẩn hóa dữ liệu về dạng 3NF
- Dữ liệu sau khi chuẩn háo về 3NF sẽ gồm các bảng:
  + GiaoVien (#MaGV, TenGV)
  + LopHP (#MaLHP, TenLHP)
  + MonHoc (#MaMon, TenMon)
  + PhongHoc (#MaPhong, TenPhong)
  + TKB (#id_TKB, @MaGV, @MaMon, @MaLHP, @MaPhong, SoTiet, GioVao, GioRa, Thu, Ngay)
- Các bảng trên đã đạt chuẩn 3NF và không có phụ thuộc hàm dư thừa
## - Dưới đây là các bước tạo CSDL TKB của bộ môn Công nghệ thông tin 
### - Vào SQL Server 
  ![image](https://github.com/user-attachments/assets/826771c4-6b51-4383-96b1-d14095900aa9)
  Click chuột phải vào Database chọn New database
  
  ![image](https://github.com/user-attachments/assets/0c308d89-abfd-4012-92e7-3ebe15db6df7)

### - Tạo bảng dữ liệu cho csdl TKB:
- Tạo bảng GiaoVien:
  ![image](https://github.com/user-attachments/assets/9dcde210-8fa4-4b14-b513-393274ee7954)

  ![image](https://github.com/user-attachments/assets/db75c9fe-a8d1-4eee-81b5-a13d141ae8d3)
  
  ![image](https://github.com/user-attachments/assets/82391719-761c-4e8a-bb09-2bd0347f979a)


#### Các bảng còn lại tạo tương tự như bảng GiaoVien
- Tạo bảng LopHP:
  ![image](https://github.com/user-attachments/assets/f2044cb5-9720-4b39-8582-17ea0e4cd8d5)

- Tạo bảng MonHoc:
  ![image](https://github.com/user-attachments/assets/ed615bea-fa56-4f7d-9fa6-5c80b0133f23)

- tạo bảng PhongHoc:
  ![image](https://github.com/user-attachments/assets/2f8c3f78-9cc3-4848-93c4-c07552f71391)

- Tạo bảng TKB: 
  ![image](https://github.com/user-attachments/assets/9a42e7e4-befa-4d8e-bb60-47788fa7f585)

### Sau khi nhập xong các bảng ta có một diagram như sau: 
  ![image](https://github.com/user-attachments/assets/7b524c9b-15d9-4e25-9ea9-d6b6f3528002)

### Nhập dữ liệu cho bảng dựa vào dữ liệu trên tms.tnut.edu.vn
- Nhập dữ liệu cho bảng giáo viên 
  ![image](https://github.com/user-attachments/assets/93ee1c6c-8610-413e-99b3-420e53443b64)

- Nhập dữ liệu cho bảng LopHP:
  ![image](https://github.com/user-attachments/assets/2c74317d-c77a-4137-8ef9-9340ebdca203)
  
- Nhập dữ liệu cho bảng MonHoc:
  ![image](https://github.com/user-attachments/assets/d602d315-5cfb-4964-8050-3b55085e77d5)

- Nhập dữ liệu cho bảng PhongHoc:
  ![image](https://github.com/user-attachments/assets/135582cc-2fdf-4ec5-87b6-277b3189d8d8)

- Nhập dữ liệu cho bảng TKB:

## 2. Tạo Query truy vấn thông tin gồm 4 cột: tên giáo viên, môn dậy, giờ vào, giờ ra

## 3. Trả lời câu hỏi: trong khoảng thời gian từ datetime1 tới datetime2 thì có những gv nào đang bận giảng dạy.

