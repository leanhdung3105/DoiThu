---
title: "Mô hình Chữ ký Cảm ứng trên Tablet (DentalFlow & Các Phần mềm Phòng khám)"
vendor: "DentalFlow, BambuFit, Nanosoft, LinkCare và nhiều đơn vị phát triển HIS nội bộ"
product: "Tính năng ký cảm ứng trên màn hình máy tính bảng (Tablet / iPad / Wacom)"
signing_method: "Vẽ chữ ký bằng tay hoặc bút cảm ứng trên màn hình thiết bị số"
tt13_category: "Nhóm 3: Phương tiện điện tử khác theo Khoản 4 Điều 22 Luật GDĐT"
role: "Phương thức xác nhận điện tử trực tiếp phổ biến nhất tại cơ sở khám chữa bệnh"
last_updated: "2026-11-09"
---

# Mô hình Chữ ký Cảm ứng trên Tablet tại Cơ sở Y tế

---

## 1. Thông tin Giải pháp & Phân khúc Thị trường
- **Đại diện giải pháp tiêu biểu:**
  - Phần mềm Quản lý Nha khoa DentalFlow, BambuFit `[Đã xác minh]`.
  - Phân hệ tiếp đón bệnh nhân của các phần mềm quản lý phòng khám như Nanosoft, LinkCare `[Đã xác minh]`.
  - Các module ký phiếu cam kết điện tử tự phát triển trên iPad/Android tablet tại nhiều bệnh viện tư nhân và công lập `[Có nguồn tham khảo]`.
- **Phân khúc khách hàng phổ biến:** Hệ thống phòng khám chuyên khoa (nha khoa, thẩm mỹ, mắt, da liễu) và các khoa khám bệnh ngoại trú tại bệnh viện.

---

## 2. Sản phẩm & Cơ chế Công nghệ

### 2.1 Bản chất Kỹ thuật của Chữ ký Cảm ứng trên Tablet
Trong thực tế kỹ thuật, một giải pháp chữ ký cảm ứng trên Tablet không đơn thuần chỉ là một bức ảnh vẽ bitmap; mức độ tin cậy công nghệ phụ thuộc hoàn toàn vào kiến trúc triển khai của nhà phát triển phần mềm:

1. **Gói dữ liệu cơ bản (Mô hình tối giản):**
   - Người bệnh vẽ chữ ký lên vùng Canvas màn hình cảm ứng.
   - Phần mềm xuất dữ liệu nét vẽ thành ảnh (PNG/JPEG) chèn vào ô người bệnh ký trên file PDF mẫu.
2. **Gói dữ liệu nâng cao (Mô hình hoàn chỉnh có Audit Trail):**
   - Ghi nhận chuỗi tọa độ (X, Y) và dấu thời gian (Timestamp) của từng nét bút.
   - Thu thập thông tin định danh thiết bị (Device ID, địa chỉ IP/MAC, hệ điều hành).
   - Ghi nhận thông tin tài khoản nhân viên y tế giám sát phiên ký.
   - Ghi nhận dữ liệu sinh trắc học động tác ký (tốc độ vẽ, áp lực tì đè cơ học nếu sử dụng bút cảm ứng chuyên dụng như Apple Pencil hoặc bảng vẽ Wacom).
   - Tạo mã băm (Hash) nội dung tài liệu tại thời điểm ký và ký số niêm phong bằng chứng thư số của cơ sở khám chữa bệnh.

---

## 3. Căn cứ Pháp lý & Giá trị Chứng cứ

- **Phân nhóm theo Thông tư 13/2025/TT-BYT:** 
  - Thuộc **Nhóm 3: Sử dụng các hình thức xác nhận bằng phương tiện điện tử khác** theo quy định tại khoản 4 Điều 22 Luật Giao dịch điện tử số 20/2023/QH15.
- **Căn cứ pháp lý áp dụng:**
  - Luật Giao dịch điện tử số 20/2023/QH15:
    - *Điều 8:* Thông điệp dữ liệu không bị phủ nhận giá trị pháp lý chỉ vì được thể hiện dưới dạng điện tử.
    - *Điều 22 khoản 4:* Trường hợp pháp luật không quy định bắt buộc dùng chữ ký điện tử thì các bên có thể thỏa thuận sử dụng phương tiện điện tử khác để thể hiện sự chấp thuận.
    - *Điều 11:* Giá trị chứng cứ của thông điệp dữ liệu được đánh giá căn cứ vào độ tin cậy của cách thức khởi tạo, lưu trữ và bảo đảm tính toàn vẹn.
  - Thông tư số 13/2025/TT-BYT (Điều 3).
- **Đánh giá giá trị chứng cứ khách quan:**
  - Chữ ký cảm ứng trên Tablet **hoàn toàn có giá trị pháp lý** khi được cơ sở y tế triển khai theo đúng quy định pháp luật về giao dịch điện tử và y tế.
  - *Mức độ tin cậy chứng minh:* Không thể mặc định rằng Tòa án chắc chắn bác bỏ chữ ký Tablet. Khi có tranh chấp, cơ quan tố tụng sẽ xem xét toàn diện: hệ thống có chứng minh được chính người bệnh đã thao tác ký hay không, tài liệu có bị sửa đổi sau thời điểm ký hay không, và chuỗi nhật ký kiểm toán có đủ độ tin cậy kỹ thuật hay không `[Nhận định pháp lý chuẩn xác]`.

---

## 4. Khách hàng & Triển khai Thực tế
- Phương thức ký trên Tablet được ứng dụng rộng rãi tại hầu hết các chuỗi nha khoa thẩm mỹ lớn và các khoa điều trị có thực hiện thủ thuật xâm lấn nhẹ `[Đã xác minh qua khảo sát thực tế phần mềm y tế]`.
- Lý do giải pháp này được ưa chuộng: Tận dụng các thiết bị máy tính bảng phổ thông sẵn có, không phát sinh chi phí chứng thư số trên từng giao dịch, giao diện trực quan và tạo cảm giác quen thuộc tương tự như ký trên giấy truyền thống đối với người bệnh.

---

## 5. Đánh giá Cạnh tranh vs EasyCA

### 5.1 Điểm mạnh của Mô hình Tablet
- **Chi phí vận hành rất thấp:** Không phải trả phí chứng thư số định danh hay phí duy trì dịch vụ tin cậy hàng năm cho từng người bệnh.
- **Quy trình tiếp đón nhanh gọn:** Điều dưỡng chỉ cần mở hồ sơ, đưa máy tính bảng cho người bệnh đọc và ký xác nhận trong vài giây; không đòi hỏi người bệnh phải có smartphone hay thực hiện các bước eKYC phức tạp.

### 5.2 Hạn chế Kỹ thuật & Rủi ro Vận hành
- **Khả năng xác thực độc lập người ký:** Nếu hệ thống chỉ lưu ảnh nét vẽ mà không thu thập đủ dữ liệu sinh trắc động tác hoặc không có nhân chứng xác thực, cơ sở khám chữa bệnh sẽ gặp khó khăn khi người bệnh phủ nhận việc mình đã từng ký vào bản cam kết.
- **Không hỗ trợ ký từ xa:** Bắt buộc người bệnh hoặc người đại diện phải có mặt trực tiếp tại cơ sở y tế để thao tác trên thiết bị của cơ sở.
- **Phụ thuộc vào mức độ bảo mật của phần mềm quản lý:** Nếu cơ sở dữ liệu của phần mềm không có cơ chế khóa mã hóa (hàm băm niêm phong), tính toàn vẹn của hồ sơ bệnh án có thể bị nghi ngờ khi xảy ra khiếu nại tranh chấp.

### 5.3 Định vị Nâng cấp của EasyCA
- Thay vì phủ nhận tính pháp lý của chữ ký Tablet, đội ngũ EasyCA nên tư vấn theo hướng **"Nâng cấp chuẩn tin cậy"**:
  - Đối với các cam kết thông thường: Bệnh viện có thể tiếp tục sử dụng ký Tablet để duy trì sự tiện lợi và tốc độ tiếp đón.
  - Đối với các thủ thuật có rủi ro pháp lý và chi phí cao (phẫu thuật lớn, cam kết từ chối điều trị, cam kết viện phí lớn ngoài danh mục BHYT): Cơ sở y tế nên áp dụng **Chữ ký số PKI của EasyCA (Nhóm 1)** để nâng mức độ an toàn thông tin và tính chống chối bỏ lên cấp độ cao nhất.

---

## 6. Nguồn Tham khảo
1. Luật Giao dịch điện tử số 20/2023/QH15.
2. Thông tư số 13/2025/TT-BYT của Bộ Y tế hướng dẫn triển khai hồ sơ bệnh án điện tử.
3. Tài liệu hướng dẫn sử dụng phần mềm quản lý nha khoa DentalFlow: `dentalflow.vn`.
4. Nghị định số 23/2025/NĐ-CP quy định chi tiết về chữ ký điện tử và dịch vụ tin cậy.
