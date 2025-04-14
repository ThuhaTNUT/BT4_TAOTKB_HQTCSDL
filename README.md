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
  + LopHP (#MaLHP, @MaGV, @MaMon)
  + MonHoc (#MaMon, TenMon)
  + PhongHoc (#MaPhong, TenPhong)
  + TKB (#id_TKB, @MaLHP, @MaPhong, SoTiet, GioVao, GioRa, Thu, Ngay)
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
  ![image](https://github.com/user-attachments/assets/42cbd471-f058-45c4-b61c-7b7454ea2b29)

- Tạo bảng MonHoc:
  ![image](https://github.com/user-attachments/assets/723838c5-4fc0-483b-b9cf-b2de266901f4)

- tạo bảng PhongHoc:
  ![image](https://github.com/user-attachments/assets/4e60e6f4-886a-4526-a756-53f2e982a0f6)

- Tạo bảng TKB: 
  ![image](https://github.com/user-attachments/assets/622e3fa8-153d-424b-be91-51d34e631a8c)

### Nhập dữ liệu cho bảng dựa vào dữ liệu trên tms.tnut.edu.vn
- Nhập dữ liệu cho bảng giáo viên 
