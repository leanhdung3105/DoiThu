---
title: "FPT Healthcare — Hệ sinh thái FPT eHospital & Dịch vụ FPT eSign"
vendor: "Công ty TNHH Hệ thống Thông tin FPT (FPT IS) — Tập đoàn FPT"
product: "Hệ thống Quản lý Bệnh viện Thông minh FPT eHospital & Nền tảng FPT eSign"
signing_method: "Xác thực qua mã OTP (SMS/Zalo), VNeID & Chữ ký số FPT-CA"
tt13_category: "Nhóm 3 (Xác nhận OTP / VNeID) & Nhóm 1 (FPT-CA cho cán bộ y tế)"
role: "Nhà tích hợp hệ thống CNTT y tế hàng đầu khối bệnh viện tư nhân và tỉnh"
last_updated: "2026-11-09"
---

# FPT Healthcare — Hệ sinh thái FPT eHospital & Dịch vụ FPT eSign

---

## 1. Thông tin Doanh nghiệp & Vị thế
- **Tên pháp nhân:** Công ty TNHH Hệ thống Thông tin FPT (FPT IS) — Tập đoàn FPT `[Đã xác minh]`.
- **Sản phẩm:**
  - Hệ sinh thái Quản lý Bệnh viện Thông minh FPT eHospital, Bệnh án điện tử FPT EMR.
  - Nền tảng ký tài liệu số FPT eSign, Dịch vụ chứng thực chữ ký số công cộng FPT-CA `[Đã xác minh]`.
- **Vai trò trong chuỗi cung ứng Y tế:** Nhà tích hợp hệ thống CNTT y tế hàng đầu, có thế mạnh đặc biệt tại các bệnh viện tư nhân quy mô lớn, chuỗi bệnh viện quốc tế và một số bệnh viện đa khoa tuyến tỉnh `[Đã xác minh qua các dự án công bố của FPT IS]`.

---

## 2. Sản phẩm & Cơ chế Công nghệ trong Bệnh viện

### 2.1 Bản chất Kỹ thuật của Phương thức Xác nhận qua mã OTP
Trong hệ thống FPT eHospital, đối với các thủ tục của người bệnh, mã OTP (One-Time Password) thường được ứng dụng dưới hai vai trò:
1. **Phương thức xác thực người dùng (Authentication Factor):** Xác minh số điện thoại người bệnh đăng ký khi tiếp đón.
2. **Phương thức ghi nhận sự chấp thuận giao dịch (Consent Confirmation):**
   - Hệ thống gửi chuỗi số ngẫu nhiên qua tin nhắn SMS Brandname hoặc thông báo Zalo ZNS đến số điện thoại người bệnh.
   - Người bệnh nhập mã OTP trên màn hình tiếp đón hoặc thiết bị cầm tay để xác nhận đồng ý với nội dung cam kết điều trị hoặc bảng kê viện phí.
   - Hệ thống lưu trữ mã OTP, số điện thoại, thời gian gửi/nhận và liên kết với tài liệu điện tử.

### 2.2 Đánh giá Kỹ thuật về Phương thức OTP
- **Tính khả thi:** Người bệnh không cần thiết bị thông minh, chỉ cần điện thoại di động có khả năng nhận tin nhắn SMS.
- **Rào cản vận hành:**
  - *Chi phí viễn thông:* Bệnh viện phải duy trì hợp đồng với các nhà mạng hoặc đại lý viễn thông để chi trả phí tin nhắn SMS Brandname cho từng lượt giao dịch `[Thông tin thị trường phổ biến]`.
  - *Chất lượng sóng viễn thông:* Tại một số khu vực đặc thù trong bệnh viện (phòng chụp bức xạ X-quang/MRI, tầng hầm, khu vực phẫu thuật cách âm), sóng di động có thể suy giảm, gây trễ mã xác thực `[Đặc thù kỹ thuật viễn thông]`.

---

## 3. Căn cứ Pháp lý & Giá trị Chứng cứ

- **Phân nhóm theo Thông tư 13/2025/TT-BYT:**
  - Phương thức xác thực qua mã OTP của người bệnh thuộc **Nhóm 3: Các hình thức xác nhận bằng phương tiện điện tử khác** theo quy định tại khoản 4 Điều 22 Luật Giao dịch điện tử số 20/2023/QH15.
- **Căn cứ pháp lý áp dụng:**
  - Luật Giao dịch điện tử số 20/2023/QH15 (Điều 8, Điều 11, Điều 22 khoản 4).
  - Thông tư số 13/2025/TT-BYT (Điều 3).
- **Đánh giá giá trị chứng cứ:**
  - Mã OTP không mặc nhiên là chữ ký số PKI, nhưng **hoàn toàn có giá trị pháp lý** khi được sử dụng như một phương tiện điện tử để thể hiện sự chấp thuận của chủ thể đối với thông điệp dữ liệu theo luật định.
  - Giá trị chứng minh trước cơ quan tố tụng phụ thuộc vào việc bệnh viện có lưu trữ đầy đủ chuỗi nhật ký viễn thông (thời gian gửi, nhà mạng, log phản hồi, biên lai viễn thông) chứng minh chính chủ thể đó đã tiếp nhận và nhập mã xác nhận `[Nhận định chuyên môn]`.

---

## 4. Khách hàng & Triển khai Thực tế
- FPT eHospital đã triển khai thành công tại nhiều bệnh viện công lập và tư nhân quy mô lớn trên toàn quốc (như hệ thống bệnh viện đa khoa tỉnh tại Quảng Ninh, Đồng Nai, một số bệnh viện thuộc Tập đoàn Y khoa Hoàn Mỹ...) `[Đã xác minh qua thông cáo báo chí của FPT IS]`.
- Hệ sinh thái FPT Healthcare được đánh giá cao về giao diện người dùng hiện đại, khả năng kết nối thiết bị xét nghiệm và chẩn đoán hình ảnh.

---

## 5. Đánh giá Cạnh tranh vs EasyCA

### 5.1 Điểm mạnh của FPT
- **Năng lực công nghệ & thương hiệu mạnh:** FPT có đội ngũ kỹ sư chuyên sâu về y tế thông minh, có khả năng triển khai các dự án quy mô phức tạp.
- **Tự chủ giải pháp CA:** Sở hữu FPT-CA và nền tảng FPT eSign, có khả năng tích hợp linh hoạt giữa ký số cán bộ y tế và xác nhận người bệnh.

### 5.2 Điểm yếu & Hạn chế
- **Tập trung vào phân khúc doanh nghiệp:** Tương tự các nhà mạng viễn thông, FPT-CA chủ yếu cung cấp chữ ký số cho doanh nghiệp và nhân viên y tế; chưa tập trung phát triển gói dịch vụ cấp chứng thư số cá nhân tức thì (On-demand PKI) cho bệnh nhân vãng lai.
- **Chi phí triển khai giải pháp FPT tổng thể thường ở mức cao:** Phù hợp với các bệnh viện có ngân sách đầu tư CNTT lớn.

### 5.3 Cơ hội cho EasyCA
- Đề xuất giải pháp ký số PKI cho bệnh nhân tích hợp vào FPT eHospital để thay thế hoặc bổ sung cho phương thức OTP, giúp bệnh viện vừa tiết kiệm chi phí tin nhắn viễn thông vừa nâng chuẩn hồ sơ bệnh án lên Nhóm 1 theo Thông tư 13/2025/TT-BYT.

---

## 6. Nguồn Tham khảo
1. Cổng thông tin Công ty Hệ thống Thông tin FPT (FPT IS): `fpt-is.com`.
2. Trang thông tin Dịch vụ Chữ ký số FPT-CA: `fpt-ca.vn`.
3. Luật Giao dịch điện tử số 20/2023/QH15.
4. Thông tư số 13/2025/TT-BYT của Bộ Y tế hướng dẫn hồ sơ bệnh án điện tử.
