---
title: "FPT eHospital — Giải pháp Ký Bệnh nhân qua OTP SMS & eSign"
vendor: "Công ty Cổ phần Bệnh viện Thông minh FPT (FPT Healthcare / FPT IS)"
product: "FPT eHospital / FPT eSign"
signing_method: "Ký qua mã xác thực OTP SMS & Tích hợp VNeID"
tt13_category: "Hình thức 3 (Phương tiện điện tử khác)"
legal_standing: "Trung bình (OTP) đến Khá (VNeID)"
target_hospital: "Bệnh viện tư nhân quy mô lớn, Bệnh viện đa khoa tỉnh"
deployments: "Một số bệnh viện tư nhân lớn và bệnh viện tỉnh"
role: "Đối thủ mảng bệnh viện tư nhân"
---

# FPT eHospital — Giải pháp Ký Bệnh nhân qua OTP & eSign

FPT tiếp cận giải pháp ký số y tế thông qua **FPT eHospital (phần mềm bệnh viện)** kết hợp nền tảng ký điện tử **FPT eSign**.

---

## 1. Phương thức Ký Bệnh nhân

1. **Xác thực qua OTP SMS / Zalo (Phổ biến):**
   - Khi cần ký phiếu cam kết, hệ thống gửi mã xác thực OTP 6 số về số điện thoại của bệnh nhân.
   - Bệnh nhân nhập OTP trên tablet tại quầy hoặc máy tính để hoàn tất xác nhận.
2. **Ký qua ứng dụng VNeID:** Tích hợp cổng định danh của Bộ Công An tương tự các bên khác.

---

## 2. Giá trị Pháp lý (Thông tư 13/2025/TT-BYT)

- **Phân loại TT 13:** **Hình thức 3** (Phương tiện điện tử khác).
- **Rủi ro phương thức OTP:**
  + **Không chứng minh được người ký:** OTP chỉ chứng minh SIM nhận được tin nhắn, không chứng minh được người cầm máy là ai (người nhà cầm hộ, cho mượn máy).
  + **Tốn chi phí viễn thông:** Bệnh viện phải chịu phí SMS Brandname (300 - 500đ/SMS).
  + **Sóng viễn thông chập chờn:** Tại phòng phẫu thuật, phòng chụp X-quang hoặc tầng hầm, tin nhắn OTP thường xuyên bị trễ.

---

## 3. Điểm mạnh

- ✅ **Thương hiệu CNTT uy tín:** FPT có năng lực triển khai các dự án bệnh viện thông minh phức tạp.
- ✅ **Phù hợp bệnh viện tư:** Giao diện hiện đại, dễ sử dụng cho các bệnh viện quốc tế/tư nhân.

---

## 4. Điểm yếu so với EasyCA PKI

- ❌ **OTP không có tính toàn vẹn (Integrity):** Không khóa cứng nội dung file PDF; nếu dữ liệu viện phí bị sửa, OTP không phát hiện được.
- ❌ **Chưa triển khai PKI cho bệnh nhân:** Dù có FPT-CA, nhưng FPT chưa đóng gói giải pháp cấp chứng thư số tức thì tại quầy cho bệnh nhân.

