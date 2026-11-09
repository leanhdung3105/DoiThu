---
title: "EasyCA (SoftDreams) — Giải pháp Chữ ký số Chuẩn PKI cho Bệnh nhân"
vendor: "Công ty Cổ phần Đầu tư Công nghệ và Thương mại SoftDreams"
product: "EasyCA (Dịch vụ chứng thực chữ ký số công cộng & Ký số từ xa)"
signing_method: "Chữ ký số công cộng theo chuẩn PKI (Remote Signing)"
tt13_category: "Nhóm 1: Chữ ký điện tử hợp pháp (Khoản 1 Điều 3 TT 13/2025/TT-BYT)"
role: "Giải pháp của SoftDreams đang nghiên cứu / phát triển"
last_updated: "2026-11-09"
---

# EasyCA (SoftDreams) — Giải pháp Chữ ký số Chuẩn PKI

---

## 1. Thông tin Doanh nghiệp & Vị thế
- **Tên pháp nhân:** Công ty Cổ phần Đầu tư Công nghệ và Thương mại SoftDreams `[Đã xác minh]`.
- **Sản phẩm:** EasyCA — Dịch vụ chứng thực chữ ký số công cộng, nền tảng ký số từ xa (Remote Signing), tích hợp phần mềm hóa đơn điện tử EasyInvoice, kế toán EasyBooks.
- **Giấy phép hoạt động:** Giấy phép cung cấp dịch vụ chứng thực chữ ký số công cộng do Bộ Thông tin và Truyền thông cấp phép, thẩm định kỹ thuật bởi Trung tâm Chứng thực điện tử quốc gia (NEAC) `[Đã xác minh]`.
- **Vai trò trong chuỗi cung ứng Y tế:** Nhà cung cấp dịch vụ tin cậy (CA công cộng) kết hợp nhà phát triển giải pháp ký số; phối hợp tích hợp với các đơn vị phát triển phần mềm bệnh viện (HIS/EMR) hoặc cung cấp trực tiếp module ký số cho cơ sở y tế `[Nhận định]`.

---

## 2. Sản phẩm & Cơ chế Công nghệ

### 2.1 Bản chất Kỹ thuật của Quy trình Ký số PKI
Quy trình ký số cho bệnh nhân/người nhà trên nền tảng EasyCA về bản chất kỹ thuật được thực hiện như sau:

```
[Hồ sơ / Bệnh án điện tử cần ký]
                 │
                 ▼
1. Tính toán giá trị băm (Hash Digest) của tài liệu (SHA-256)
                 │
                 ▼
2. Định danh & Xác thực người ký (eKYC / Sinh trắc / Mã xác thực)
                 │
                 ▼
3. Khóa bí mật (Private Key) được kích hoạt trong môi trường an toàn (HSM)
   để mã hóa giá trị băm, tạo ra Chữ ký số (Digital Signature)
                 │
                 ▼
4. Gắn Chữ ký số + Chứng thư số X.509 + Dấu thời gian (TSA) vào tài liệu (Chuẩn PAdES)
                 │
                 ▼
5. Người kiểm tra dùng Khóa công khai (Public Key) đối soát tính toàn vẹn 
   và kiểm tra trạng thái hiệu lực của Chứng thư số (qua OCSP / CRL)
```

- **Công nghệ định danh (Identity Verification):** eKYC qua đối soát thông tin Căn cước công dân và sinh trắc học khuôn mặt `[Đang nghiên cứu/phát triển]`.
- **Quản lý khóa bí mật (Key Management):** Khóa bí mật của thuê bao được lưu trữ và bảo vệ trong phân vùng bảo mật của Hệ thống Ký số từ xa (Remote Signing / HSM).
- **Chuẩn định dạng ký tài liệu:** PAdES (PDF Advanced Electronic Signatures) hỗ trợ LTV (Long Term Validation) phục vụ lưu trữ hồ sơ bệnh án dài hạn.
- **Dịch vụ dấu thời gian (TSA):** Tích hợp dịch vụ cấp dấu thời gian từ nhà cung cấp dịch vụ tin cậy được cấp phép để xác định thời điểm ký khách quan.

### 2.2 Nghiệp vụ Cấp Chứng thư số cho Bệnh nhân theo Nghị định 23/2025/NĐ-CP
Đối với mô hình cấp chứng thư số cho bệnh nhân (người dùng vãng lai, khám chữa bệnh theo sự vụ), EasyCA cần đáp ứng đầy đủ khung pháp lý tại **Nghị định số 23/2025/NĐ-CP** quy định về chữ ký điện tử và dịch vụ tin cậy:
1. **Hợp đồng thuê bao & Xác minh danh tính:** Thuê bao (người bệnh/người đại diện) phải được định danh chính xác và ký thỏa thuận sử dụng dịch vụ chứng thực trước khi sinh khóa `[Căn cứ pháp lý: Điều 14, Điều 15 NĐ 23/2025/NĐ-CP]`.
2. **Quyền kiểm soát khóa bí mật:** Hệ thống ký từ xa phải bảo đảm khóa bí mật chỉ được kích hoạt dưới sự kiểm soát duy nhất của người ký thông qua yếu tố xác thực thứ cấp (PIN/Sinh trắc).
3. **Thời hạn & Thu hồi chứng thư:** Cần xác định rõ loại chứng thư (chứng thư số cá nhân có thời hạn ngắn, chứng thư số theo sự vụ hoặc chứng thư số thuê bao cá nhân tiêu chuẩn) và cơ chế thu hồi/hết hạn tự động.
4. **Bảo vệ dữ liệu cá nhân:** Tuân thủ quy định tại Nghị định 13/2023/NĐ-CP về bảo vệ dữ liệu cá nhân khi thu thập, xử lý dữ liệu sinh trắc học và ảnh CCCD.

---

## 3. Căn cứ Pháp lý & Giá trị Chứng cứ

- **Phân nhóm theo Thông tư 13/2025/TT-BYT:** Thuộc **Nhóm 1: Sử dụng chữ ký điện tử hợp pháp** (Khoản 1 Điều 3).
- **Căn cứ pháp lý áp dụng:**
  - Luật Giao dịch điện tử số 20/2023/QH15 (Điều 8, Điều 10, Điều 11, Điều 22, Điều 23).
  - Nghị định số 23/2025/NĐ-CP quy định chi tiết về chữ ký điện tử và dịch vụ tin cậy.
  - Luật Khám bệnh, chữa bệnh số 15/2023/QH15 (Điều 69 về lưu trữ hồ sơ bệnh án).
- **Đánh giá giá trị chứng cứ (Theo Điều 11 Luật GDĐT 2023):**
  - Giá trị chứng cứ của thông điệp dữ liệu ký số PKI được đánh giá căn cứ vào **độ tin cậy của cách thức khởi tạo, lưu trữ hoặc truyền gửi; cách thức bảo đảm tính toàn vẹn; và cách thức xác định người ký**.
  - Chữ ký số công cộng PKI có ưu thế kỹ thuật vượt trội trong việc chứng minh tính toàn vẹn dữ liệu (hàm băm) và danh tính người ký (chứng thư số của CA được cấp phép). Khi đáp ứng đầy đủ điều kiện luật định, đây là cơ chế có **khả năng chứng minh cao trước cơ quan tố tụng**.
  - *Lưu ý:* Giá trị pháp lý và giá trị chứng cứ thực tế trong từng vụ việc cụ thể do Tòa án hoặc Trọng tài xem xét, đánh giá toàn diện cùng các chứng cứ khác theo quy định pháp luật tố tụng; không mặc định rằng cứ dùng PKI là đương nhiên thắng kiện trong mọi tranh chấp y khoa `[Nhận định pháp lý chuẩn xác]`.

---

## 4. Khách hàng & Triển khai Thực tế
- **Mảng Doanh nghiệp:** Hàng trăm nghìn khách hàng doanh nghiệp sử dụng chữ ký số kê khai thuế, hải quan, bảo hiểm xã hội và phát hành hóa đơn điện tử `[Đã xác minh]`.
- **Phân khúc Bệnh viện (Ký số Bệnh nhân):** Đang trong giai đoạn nghiên cứu kiến trúc giải pháp, xây dựng luồng nghiệp vụ tích hợp và đàm phán thử nghiệm với các đơn vị phát triển HIS/EMR `[Chưa triển khai thực tế trên diện rộng]`.

---

## 5. Đánh giá Cạnh tranh

### 5.1 Điểm mạnh
- Có giấy phép CA công cộng chính thức từ Bộ TT&TT, bảo đảm tính độc lập pháp lý của bên thứ ba tin cậy.
- Có năng lực công nghệ về mật mã, hạ tầng Cloud HSM và kinh nghiệm vận hành hệ thống ký số quy mô lớn.
- Khả năng kiểm tra tính toàn vẹn tài liệu và dấu thời gian độc lập theo chuẩn quốc tế (PAdES/TSA).

### 5.2 Điểm yếu & Thách thức
- **Rào cản quy trình:** Việc cấp chứng thư số cá nhân đòi hỏi quy trình định danh và thỏa thuận thuê bao chặt chẽ theo Nghị định 23/2025/NĐ-CP; nếu thiết kế luồng người dùng không tốt sẽ gây mất thời gian tại quầy tiếp đón.
- **Mô hình chi phí TCO:** Cần xác định rõ cơ cấu chi phí (phí cấp chứng thư số, phí lượt ký, chi phí bản quyền tích hợp) để bệnh viện có thể chấp nhận chi trả thay cho người bệnh.
- **Phụ thuộc đối tác HIS/EMR:** EasyCA không sở hữu phần mềm HIS/EMR lớn trong các bệnh viện công lập, bắt buộc phải hợp tác mở cổng API với các nhà cung cấp phần mềm hiện hữu (VNPT, Viettel, FPT, ISOFH...).

---

## 6. Nguồn Tham khảo
1. Luật Giao dịch điện tử số 20/2023/QH15.
2. Nghị định số 23/2025/NĐ-CP quy định chi tiết về chữ ký điện tử và dịch vụ tin cậy.
3. Thông tư số 13/2025/TT-BYT hướng dẫn triển khai hồ sơ bệnh án điện tử.
4. Cổng thông tin Trung tâm Chứng thực điện tử quốc gia (NEAC) — `neac.gov.vn`.
5. Tài liệu kỹ thuật chuẩn chữ ký số PDF (PAdES - ETSI EN 319 142).
