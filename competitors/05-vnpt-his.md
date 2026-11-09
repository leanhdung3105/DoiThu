---
title: "VNPT-IT — Hệ sinh thái Y tế VNPT HIS & Dịch vụ VNPT SmartCA"
vendor: "Công ty Công nghệ thông tin VNPT (VNPT-IT) — Tập đoàn Bưu chính Viễn thông Việt Nam"
product: "Hệ thống Quản lý Bệnh viện VNPT HIS & Dịch vụ chữ ký số từ xa VNPT SmartCA"
signing_method: "Ký qua VNeID, Ký cảm ứng Tablet & Chữ ký số từ xa SmartCA"
tt13_category: "Nhóm 1 (SmartCA) & Nhóm 3 (VNeID / Ký Tablet)"
role: "Nhà cung cấp hạ tầng viễn thông, phần mềm y tế và CA công cộng hàng đầu"
last_updated: "2026-11-09"
---

# VNPT-IT — Hệ sinh thái Y tế VNPT HIS & Dịch vụ VNPT SmartCA

---

## 1. Thông tin Doanh nghiệp & Vị thế
- **Tên pháp nhân:** Công ty Công nghệ thông tin VNPT (VNPT-IT) — Chi nhánh Tập đoàn Bưu chính Viễn thông Việt Nam `[Đã xác minh]`.
- **Sản phẩm:**
  - Phần mềm Quản lý Bệnh viện (VNPT HIS), Bệnh án điện tử (VNPT EMR), Quản lý Trạm y tế xã phường (VNPT HMIS).
  - Dịch vụ chứng thực chữ ký số công cộng VNPT-CA, Chữ ký số từ xa VNPT SmartCA `[Đã xác minh]`.
- **Vai trò trong chuỗi cung ứng Y tế:** Đơn vị sở hữu thị phần lớn nhất về số lượng cơ sở khám chữa bệnh tại Việt Nam (đặc biệt là khối y tế cơ sở và bệnh viện tuyến huyện, tỉnh) `[Đã xác minh qua số liệu công bố của Bộ Y tế và VNPT]`.

---

## 2. Sản phẩm & Cơ chế Công nghệ trong Bệnh viện

Trong hệ sinh thái y tế của VNPT, giải pháp chữ ký điện tử được cấu trúc thành các mảng rõ ràng:

### 2.1 Chữ ký số cho Nhân viên Y tế (VNPT SmartCA)
- Bác sĩ, Dược sĩ, Điều dưỡng sử dụng ứng dụng di động VNPT SmartCA hoặc tích hợp HSM ký số trực tiếp trên giao diện VNPT HIS để phê duyệt bệnh án và đơn thuốc điện tử.
- Đạt chuẩn **Nhóm 1: Chữ ký điện tử hợp pháp** theo Thông tư 13/2025/TT-BYT `[Đã xác minh]`.

### 2.2 Ký xác nhận của Bệnh nhân & Người nhà bệnh nhân
Đối với đối tượng người bệnh, VNPT HIS hỗ trợ các phương thức:
1. **Xác nhận qua tài khoản định danh VNeID:** Tích hợp với CSDL quốc gia về dân cư theo Đề án 06 để người bệnh nhận thông báo xác nhận viện phí hoặc cam kết điều trị trên điện thoại di động `[Đã triển khai thí điểm tại một số đơn vị như BV ĐK Nông nghiệp]`.
2. **Ký cảm ứng trên Tablet tại quầy:** Ghi nhận chữ ký vẽ tay trên màn hình máy tính bảng hoặc thiết bị chuyên dụng tại quầy tiếp đón.
3. **Mô hình cấp SmartCA cho Người bệnh (Tiềm năng):**
   - Về mặt công nghệ, VNPT sở hữu hạ tầng Remote Signing hoàn toàn có khả năng cấp chứng thư số cá nhân cho người dân.
   - *Rào cản triển khai thực tế:* Quy trình cấp phát chứng thư số cá nhân tiêu chuẩn đòi hỏi các bước định danh eKYC, xác nhận hợp đồng thuê bao và cơ chế quản lý phí dịch vụ. Với bệnh nhân vãng lai chỉ khám chữa bệnh 1-2 lần trong năm, việc duy trì một tài khoản thuê bao SmartCA cá nhân thường niên tạo ra rào cản về trải nghiệm và chi phí nếu bệnh viện không có chính sách bao cấp lượt ký `[Nhận định chuyên môn]`.

### 2.3 Khả năng Tích hợp với Hệ thống bên thứ ba
- VNPT cung cấp cổng API / SDK cho dịch vụ SmartCA. Tuy nhiên, trong thực tế triển khai y tế công lập, VNPT thường định hướng cung cấp trọn gói đồng bộ giữa phần mềm quản lý VNPT HIS và chữ ký số VNPT SmartCA `[Nhận định thị trường]`.

---

## 3. Căn cứ Pháp lý & Giá trị Chứng cứ

- **Phân nhóm theo Thông tư 13/2025/TT-BYT:**
  - Nếu sử dụng VNPT SmartCA: Thuộc **Nhóm 1 (Chữ ký điện tử hợp pháp)**.
  - Nếu sử dụng VNeID hoặc Ký tay Tablet: Thuộc **Nhóm 3 (Phương tiện điện tử khác theo khoản 4 Điều 22 Luật GDĐT)**.
- **Căn cứ pháp lý áp dụng:**
  - Luật Giao dịch điện tử số 20/2023/QH15.
  - Nghị định số 23/2025/NĐ-CP về chữ ký điện tử và dịch vụ tin cậy.
  - Thông tư số 13/2025/TT-BYT (Điều 3).
- **Đánh giá giá trị chứng cứ:**
  - VNPT là một trong những nhà cung cấp dịch vụ tin cậy (CA) uy tín và lâu đời nhất Việt Nam, được Bộ TT&TT cấp phép. Các chứng thư số do VNPT SmartCA phát hành có đầy đủ cơ sở pháp lý cao nhất theo luật định.

---

## 4. Khách hàng & Triển khai Thực tế
- VNPT HIS được triển khai tại hàng nghìn cơ sở y tế trên toàn quốc, chiếm thị phần áp đảo tại tuyến y tế cơ sở (trạm y tế xã phường, trung tâm y tế huyện) và nhiều bệnh viện đa khoa tuyến tỉnh `[Đã xác minh qua Cổng thông tin Bộ Y tế]`.
- Một số bệnh viện lớn như Bệnh viện Đa khoa Nông nghiệp đã công bố thí điểm mô hình liên kết dữ liệu y tế và định danh số với VNPT `[Đã xác minh qua tin tức báo chí]`.

---

## 5. Đánh giá Cạnh tranh vs EasyCA

### 5.1 Điểm mạnh của VNPT
- **Quy mô thị phần và sự gắn kết chính quyền:** VNPT thường ký thỏa thuận hợp tác chuyển đổi số toàn diện với UBND và Sở Y tế các tỉnh, tạo lợi thế tuyệt đối khi đấu thầu phần mềm bệnh viện.
- **Hạ tầng viễn thông và CA hoàn chỉnh:** Tự chủ từ đường truyền cáp quang, hạ tầng đám mây VNPT Cloud cho đến dịch vụ chứng thực chữ ký số công cộng.

### 5.2 Điểm yếu & Thách thức
- **Trải nghiệm cấp phát chứng thư số tức thì:** Hiện chưa có gói giải pháp chuyên biệt "Cấp chứng thư số theo sự vụ (Transactional PKI)" tối ưu hóa riêng cho luồng bệnh nhân tại quầy tiếp đón bệnh viện.
- **Ưu tiên hệ sinh thái nội bộ:** Khách hàng sử dụng phần mềm HIS của bên thứ ba (ISOFH, FPT, Nanosoft...) thường gặp khó khăn hơn trong việc đàm phán tích hợp sâu SmartCA nếu không có thỏa thuận chiến lược cấp cao.

### 5.3 Cơ hội cho EasyCA
- **Tập trung vào phân khúc chuyên biệt:** EasyCA định vị là giải pháp chuyên sâu phục vụ riêng bài toán ký số của bệnh nhân và thân nhân với trải nghiệm eKYC mượt mà, đóng gói chi phí theo gói lượt ký (Transaction Pack) linh hoạt.
- **Tính trung lập (Vendor-agnostic):** EasyCA sẵn sàng mở cổng API kết nối với mọi phần mềm HIS/EMR của các nhà cung cấp độc lập mà không cạnh tranh thị phần phần mềm quản lý bệnh viện với họ.

---

## 6. Nguồn Tham khảo
1. Cổng thông tin điện tử Tập đoàn Bưu chính Viễn thông Việt Nam: `vnpt.com.vn`.
2. Trang thông tin sản phẩm Dịch vụ Chữ ký số từ xa VNPT SmartCA: `smartca.vnpt.vn`.
3. Báo cáo Chuyển đổi số ngành Y tế — Bộ Y tế (moh.gov.vn).
4. Quyết định số 06/QĐ-TTg của Thủ tướng Chính phủ (Đề án 06).
