---
title: "Viettel Solutions — Giải pháp Viettel HMS & Chữ ký số Y tế"
vendor: "Tổng công ty Giải pháp Doanh nghiệp Viettel (Viettel Solutions - Tập đoàn Viettel)"
product: "Hệ thống Quản lý Bệnh viện Viettel HMS & Dịch vụ chứng thực Viettel-CA"
signing_method: "Ký cảm ứng trên Tablet & Xác thực qua VNeID / Viettel-CA"
tt13_category: "Nhóm 3 (Phương tiện điện tử khác) & Nhóm 1 (Viettel-CA cho nhân viên y tế)"
role: "Nhà cung cấp hạ tầng CNTT y tế, phần mềm HIS/EMR và CA công cộng"
last_updated: "2026-11-09"
---

# Viettel Solutions — Giải pháp Viettel HMS & Chữ ký số Y tế

---

## 1. Thông tin Doanh nghiệp & Vị thế
- **Tên pháp nhân:** Tổng công ty Giải pháp Doanh nghiệp Viettel (Viettel Solutions) — Chi nhánh Tập đoàn Công nghiệp - Viễn thông Quân đội `[Đã xác minh]`.
- **Sản phẩm:** 
  - Phần mềm quản lý thông tin bệnh viện (Viettel HMS), bệnh án điện tử (Viettel EMR).
  - Dịch vụ chứng thực chữ ký số công cộng (Viettel-CA), chữ ký số từ xa Viettel SmartCA `[Đã xác minh]`.
- **Vai trò trong chuỗi cung ứng Y tế:** Nhà thầu tổng thể về hạ tầng viễn thông, Trung tâm dữ liệu (Cloud), phần mềm quản trị bệnh viện (HIS/EMR) và nhà cấp dịch vụ tin cậy (CA) `[Đã xác minh]`.
- **Quy mô thị phần:** Đơn vị sở hữu thị phần lớn nhất trong khối bệnh viện và trung tâm y tế công lập tuyến tỉnh, huyện tại Việt Nam thông qua các gói thầu CNTT y tế `[Đã xác minh qua Hệ thống Mạng đấu thầu Quốc gia]`.

---

## 2. Sản phẩm & Cơ chế Công nghệ trong Bệnh viện

Trong hệ sinh thái y tế của Viettel, cần phân định rõ hai đối tượng ký riêng biệt:

### 2.1 Ký số cho Cán bộ Nhân viên Y tế (Bác sĩ, Dược sĩ, Điều dưỡng)
- **Công nghệ:** Sử dụng **Viettel-CA** (USB Token hoặc Viettel SmartCA ký từ xa) để ký duyệt đơn thuốc điện tử, bệnh án điện tử, bảng kê thanh toán BHYT.
- **Phân nhóm TT 13:** Thuộc **Nhóm 1: Chữ ký điện tử hợp pháp** `[Đã xác minh]`.

### 2.2 Ký xác nhận của Bệnh nhân & Người nhà bệnh nhân
Đối với đối tượng người bệnh, Viettel HMS hiện đang áp dụng các phương thức linh hoạt tùy theo gói triển khai tại từng cơ sở y tế:
1. **Ký cảm ứng trên Tablet / Thiết bị di động (Phổ biến):**
   - Điều dưỡng đưa máy tính bảng hoặc màn hình phụ tại quầy; bệnh nhân sử dụng bút cảm ứng hoặc ngón tay để vẽ chữ ký.
   - *Cơ chế lưu trữ kỹ thuật:* Hệ thống ghi nhận nét vẽ chữ ký, lưu kèm các thông tin phiên làm việc (thời điểm ký, mã hồ sơ bệnh án, tài khoản nhân viên y tế lập phiếu).
2. **Xác nhận qua tài khoản VNeID:**
   - Tích hợp API cổng định danh Bộ Công An theo lộ trình chuyển đổi số Đề án 06 để người bệnh xác nhận một số mẫu phiếu qua ứng dụng di động `[Đang triển khai thí điểm tại một số đơn vị]`.

---

## 3. Căn cứ Pháp lý & Giá trị Chứng cứ

- **Phân nhóm theo Thông tư 13/2025/TT-BYT đối với Người bệnh:**
  - Thuộc **Nhóm 3: Sử dụng các hình thức xác nhận bằng phương tiện điện tử khác** theo khoản 4 Điều 22 Luật Giao dịch điện tử số 20/2023/QH15.
- **Căn cứ pháp lý áp dụng:**
  - Luật Giao dịch điện tử số 20/2023/QH15 (Điều 8, Điều 11, Điều 22).
  - Thông tư số 13/2025/TT-BYT (Điều 3).
- **Đánh giá giá trị chứng cứ:**
  - Phương thức ký cảm ứng trên Tablet của Viettel HMS được coi là một hình thức xác nhận điện tử hợp pháp nếu đáp ứng các điều kiện về việc thể hiện sự chấp thuận của chủ thể ký.
  - *Mức độ tin cậy chứng cứ:* Phụ thuộc vào chất lượng gói dữ liệu kiểm toán (Audit Trail) được Viettel HMS lưu trữ kèm theo (nhật ký truy cập, địa chỉ thiết bị, thời gian tạo lập, cơ chế bảo vệ chống sửa đổi file sau khi ký). 
  - Khi cơ sở y tế mong muốn nâng cao tính toàn vẹn và giá trị chứng minh pháp lý lên mức cao nhất (Nhóm 1), việc bổ sung giải pháp ký số PKI cho người bệnh là một hướng nâng cấp cần thiết `[Nhận định chuyên môn]`.

---

## 4. Khách hàng & Triển khai Thực tế
- Viettel HMS đang được vận hành tại hàng trăm cơ sở y tế công lập, bao gồm các bệnh viện đa khoa tuyến tỉnh, bệnh viện chuyên khoa và trung tâm y tế quận/huyện trên phạm vi toàn quốc `[Đã xác minh qua các thông báo trúng thầu và bài viết triển khai trên truyền thông chính thức của Viettel]`.
- Mức độ triển khai các module không giấy tờ (ký điện tử người bệnh) khác nhau tùy thuộc vào mức độ sẵn sàng hạ tầng và quyết định đầu tư của từng bệnh viện.

---

## 5. Đánh giá Cạnh tranh vs EasyCA

### 5.1 Điểm mạnh của Viettel
- **Thế mạnh độc quyền về hạ tầng:** Viettel thường cung cấp trọn gói từ đường truyền internet, hạ tầng mạng nội bộ, máy chủ đám mây (Cloud Server) cho đến phần mềm quản lý bệnh viện.
- **Mạng lưới hỗ trợ kỹ thuật phủ kín 63 tỉnh/thành:** Đội ngũ kỹ sư tại các chi nhánh Viettel tỉnh/huyện có khả năng ứng cứu và hỗ trợ vận hành trực tiếp tại chỗ rất nhanh chóng.

### 5.2 Điểm yếu & Thách thức
- **Bộ máy lớn, quy trình thay đổi chậm:** Việc bổ sung hoặc tùy biến sâu các tính năng chuyên biệt mới (như luồng cấp chứng thư số theo sự vụ cho người bệnh) đòi hỏi quy trình phê duyệt nội bộ phức tạp.
- **Chưa chuyên biệt hóa mảng CKS Bệnh nhân:** Trọng tâm của Viettel-CA vẫn là thị trường doanh nghiệp và nhân viên y tế; chưa đóng gói một sản phẩm ký số chuyên dụng cho người bệnh vãng lai.

### 5.3 Cơ hội Hợp tác & Cạnh tranh cho EasyCA
- **Không cạnh tranh trực tiếp thay thế Viettel HMS:** Đội ngũ kinh doanh EasyCA không nên định vị thay thế phần mềm bệnh viện của Viettel vì đây là hợp đồng hạ tầng tổng thể.
- **Chiến lược đối tác tích hợp (Add-on Module):** Đề xuất EasyCA dưới dạng **Module Ký số PKI Chuyên sâu** tích hợp vào hệ thống Viettel HMS qua API mở, giúp bệnh viện nâng cấp phương thức ký của người bệnh từ Nhóm 3 lên Nhóm 1 theo Thông tư 13/2025/TT-BYT.

---

## 6. Nguồn Tham khảo
1. Hệ thống Mạng đấu thầu Quốc gia (muasamcong.mpi.gov.vn) — Các gói thầu triển khai phần mềm quản lý bệnh viện Viettel HMS.
2. Website chính thức Tổng công ty Giải pháp Doanh nghiệp Viettel: `viettelsolutions.com.vn`.
3. Website dịch vụ Chữ ký số Viettel: `viettel-ca.vn`.
4. Thông tư số 13/2025/TT-BYT của Bộ Y tế hướng dẫn hồ sơ bệnh án điện tử.
