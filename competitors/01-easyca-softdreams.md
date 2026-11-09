---
title: "EasyCA (SoftDreams) — Chữ ký số Chuẩn PKI cho Bệnh nhân"
vendor: "SoftDreams"
product: "EasyCA"
signing_method: "CKS chuẩn PKI (Cloud HSM / eKYC tức thì)"
tt13_category: "Hình thức 1 (Chữ ký điện tử hợp pháp — Cấp cao nhất)"
legal_standing: "Tuyệt đối (NEAC - Bộ TT&TT cấp phép)"
target_hospital: "Bệnh viện đa khoa, chuyên khoa công lập & tư nhân"
deployments: "Đang mở rộng tích hợp các hệ thống HIS/EMR"
role: "Sản phẩm của chúng ta"
---

# EasyCA (SoftDreams) — Giải pháp Chữ ký số Chuẩn PKI

EasyCA là giải pháp chữ ký số công cộng được **NEAC (Trung tâm Chứng thực điện tử quốc gia — Bộ TT&TT)** cấp phép, ứng dụng công nghệ **Ký số từ xa (Remote Signing)** và **Cloud HSM (đạt chuẩn FIPS 140-2 Level 3)** để cấp chứng thư số tức thì cho bệnh nhân/người nhà khi khám chữa bệnh.

---

## 1. Phương thức & Quy trình Bệnh nhân Ký tại Viện

Khác với bác sĩ dùng Token cố định hàng năm, bệnh nhân được **cấp Chứng thư số PKI theo sự vụ (On-demand/Ad-hoc PKI)** hoặc CTS cá nhân nhanh qua eKYC:

```
[Bệnh nhân đến quầy / tại giường]
               │
               ▼
   1. eKYC Định danh tức thì (Quét chip CCCD + Face Matching trong 30s)
               │
               ▼
   2. Cấp Chứng thư số PKI trên Cloud HSM (Bệnh nhân sở hữu Private Key riêng)
               │
               ▼
   3. Xem tài liệu & Xác nhận ký (Mã PIN / OTP / Sinh trắc khuôn mặt)
               │
               ▼
   4. Ký số PKI & Niêm phong tài liệu (Băm SHA-256 + Đóng dấu thời gian TSA)
```

- **Thời gian xử lý:** Dưới 1 phút/lượt làm thủ tục.
- **Hỗ trợ đa kênh:** Ký tại quầy tiếp đón (dùng CCCD), ký tại giường bệnh (tablet điều dưỡng), hoặc **ký từ xa** (khi người nhà ở xa viện).

---

## 2. Giá trị Pháp lý (Thông tư 13/2025/TT-BYT)

- **Phân loại TT 13:** **Hình thức 1 (Chữ ký điện tử hợp pháp)** — Cấp độ pháp lý cao nhất trong y tế.
- **Tính toàn vẹn (Integrity):** Thuật toán băm SHA-256 khóa cứng file PDF. Bất kỳ ai sửa 1 chữ số viện phí hay liều thuốc, chữ ký sẽ báo lỗi (Invalid) ngay lập tức.
- **Tính chống chối bỏ (Non-repudiation):** Khóa bí mật chỉ người bệnh kiểm soát; có CA quốc gia đứng ra bảo chứng trước Tòa án.
- **Dấu thời gian TSA:** Đóng dấu thời gian chuẩn quốc gia, chứng minh chính xác tài liệu được ký trước hay sau ca mổ.

---

## 3. Điểm mạnh Vượt trội

- ✅ **Bảo vệ tuyệt đối Bác sĩ & Bệnh viện:** Đảm bảo giá trị chứng cứ nguyên bản khi có tranh chấp kiện tụng y khoa.
- ✅ **Linh hoạt thiết bị:** Người già không có smartphone vẫn ký được tại quầy qua CCCD gắn chip; người ở xa ký được qua link eKYC.
- ✅ **Open API không phụ thuộc HIS:** Kết nối được vào mọi phần mềm HIS/EMR (VNPT, Viettel, FPT, ISOFH...).
- ✅ **Hồ sơ lưu trữ 20 năm:** Chuẩn ký số quốc tế (PAdES / LTV) đảm bảo sau 20 năm mở lại file vẫn xác minh được người ký.

---

## 4. Điểm yếu & Thách thức cần giải quyết

- ⚠️ **Rào cản nhận thức:** Nhiều bệnh viện nghĩ rằng "cho bệnh nhân ký tay trên iPad là đủ rồi", cần truyền thông mạnh về rủi ro pháp lý.
- ⚠️ **Chi phí vận hành:** Cần mô hình giá theo gói lượt ký (Transaction Pack) hợp lý để bệnh viện dễ dàng chi trả thay cho bệnh nhân.

