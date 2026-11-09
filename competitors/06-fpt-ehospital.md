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

## 1. Cơ chế Hoạt động 2 Phương thức Ký Bệnh nhân của FPT

### Cách 1: Xác thực qua mã OTP SMS / Zalo ZNS (Phổ biến nhất)
```
[Bác sĩ tạo phiếu trên eHospital] ──► [Hệ thống bắn mã OTP 6 số về SMS/Zalo]
                                                    │
                                                    ▼
[Bệnh nhân đọc mã trên điện thoại] ──► [Nhập mã vào màn hình Tablet quầy] ──► [Xác nhận]
```

### 3 Lỗ hổng Cốt tử của Phương thức OTP SMS:
1. **Không chứng minh được ai là người bấm mã:** OTP chỉ chứng minh chiếc SIM đó nhận được tin nhắn. Bệnh nhân có thể chối bỏ trước Tòa: *"Tôi đang cấp cứu, người nhà hoặc điều dưỡng tự cầm máy bấm mã, tôi không đồng ý phẫu thuật"*.
2. **Tốn chi phí viễn thông cho Viện:** Bệnh viện phải chi trả 300 - 500 đồng/tin nhắn SMS Brandname. Chi phí này tích lũy hàng tháng lên đến hàng chục triệu đồng.
3. **Nghẽn sóng trong bệnh viện:** Các khu vực nhạy cảm như phòng mổ, phòng cấp cứu, tầng hầm, phòng chụp X-quang/MRI thường xuyên bị chắn sóng viễn thông, mã OTP bị trễ 5 - 10 phút gây ách tắc ca phẫu thuật.

### Cách 2: Ký qua App VNeID
- FPT eHospital tích hợp cổng định danh Bộ Công An, tương tự ISOFH và Viettel, gặp rào cản với người già và ca cấp cứu không có smartphone.

---

## 2. Kịch bản Bán hàng Thực chiến khi Bệnh viện đang Dùng FPT eHospital

Khi tiếp cận các bệnh viện tư nhân hoặc bệnh viện tỉnh đang dùng FPT eHospital:

- **Đòn bẩy 1 — Cắt giảm chi phí SMS Brandname:**
  - *"Hiện tại bệnh viện đang tốn hàng trăm triệu đồng mỗi năm chỉ để gửi tin nhắn OTP cho bệnh nhân xác nhận. EasyCA ứng dụng xác thực eKYC sinh trắc học và Private Key trên Cloud HSM, hoàn toàn không phụ thuộc vào tin nhắn SMS, giúp viện tiết kiệm toàn bộ chi phí viễn thông này."*
- **Đòn bẩy 2 — Nâng cấp từ Hình thức 3 lên Hình thức 1:**
  - *"Xác thực bằng OTP chỉ được xếp vào Hình thức 3 (thấp nhất theo Thông tư 13/2025). OTP không khóa được nội dung file PDF. EasyCA nâng cấp hồ sơ bệnh án của viện lên chuẩn Hình thức 1 (CKS PKI có mã hóa SHA-256), đảm bảo tính toàn vẹn và giá trị chứng cứ cao nhất."*
