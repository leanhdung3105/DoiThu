---
title: "Viettel HMS — Giải pháp Ký Tablet & VNeID Khối Bệnh viện Công"
vendor: "Tổng công ty Giải pháp Doanh nghiệp Viettel (Viettel Solutions)"
product: "Viettel HMS (Hospital Management System)"
signing_method: "Ký tay trên Tablet cảm ứng & Xác thực qua VNeID"
tt13_category: "Hình thức 3 (Ký Tablet / VNeID) & Hình thức 2 (Sinh trắc)"
legal_standing: "Ký tablet rất yếu; VNeID khá tốt"
target_hospital: "Bệnh viện công lập tuyến tỉnh, huyện trên cả nước"
deployments: "Hàng trăm bệnh viện và trung tâm y tế công lập"
role: "Đối thủ chiếm thị phần hạ tầng lớn nhất"
---

# Viettel HMS — Giải pháp Ký Bệnh nhân trên Hệ sinh thái Viettel

Viettel sở hữu phần mềm quản lý bệnh viện **Viettel HMS** phủ rộng ở khối bệnh viện công. Mặc dù có Viettel-CA, nhưng Viettel-CA chỉ dùng cho nhân viên y tế (bác sĩ ký đơn thuốc); còn đối với **Bệnh nhân**, Viettel HMS chủ yếu dùng **Ký tay trên Tablet** hoặc đang thử nghiệm **VNeID**.

---

## 1. Phương thức & Quy trình Ký

### Cách 1: Ký tay trên Tablet cảm ứng (Phổ biến nhất)
- Điều dưỡng đưa Tablet hoặc bệnh nhân ký tại quầy.
- Bệnh nhân dùng ngón tay hoặc bút cảm ứng vẽ chữ ký lên màn hình.
- Phần mềm chụp ảnh nét vẽ (PNG) chèn vào ô người bệnh ký trên file PDF ➔ Lưu vào cơ sở dữ liệu.

### Cách 2: Ký qua App VNeID
- Hệ thống đẩy thông báo Push sang App VNeID của bệnh nhân ➔ Bệnh nhân xác thực sinh trắc và bấm "Đồng ý ký".

---

## 2. Giá trị Pháp lý & Rủi ro Kỹ thuật

| Tiêu chí | Ký tay trên Tablet | EasyCA PKI (SoftDreams) |
|---|---|---|
| **Bản chất** | Ảnh chụp nét vẽ (PNG/JPEG) | **Mã hóa khóa công khai (Private Key X.509)** |
| **Tính toàn vẹn** | Sửa file PDF chữ ký vẫn hiển thị bình thường | **Sửa 1 byte file là chữ ký báo lỗi ngay** |
| **Giám định hình sự** | **Không thể giám định** vì màn hình kính không có lực ấn | **Tự động xác thực** qua CA quốc gia NEAC |
| **Phân loại TT 13** | Hình thức 3 (Cấp thấp nhất) | **Hình thức 1 (Cấp cao nhất)** |

---

## 3. Điểm mạnh

- ✅ **Thị phần bao phủ lớn:** Nằm sẵn trong hệ thống CNTT của hàng trăm bệnh viện công.
- ✅ **Đội ngũ tại chỗ đông đảo:** Chi nhánh Viettel tại 63 tỉnh thành hỗ trợ viện nhanh.

---

## 4. Điểm yếu & Cơ hội cho EasyCA

- ❌ **Chữ ký Tablet để lại rủi ro pháp lý khổng lồ:** Khi xảy ra sự cố y khoa tranh chấp tại Tòa án hoặc BHYT thanh tra xuất toán viện phí, chữ ký tablet không đủ giá trị chứng cứ để bảo vệ Bệnh viện.
- 💡 **Chiến lược EasyCA:** Đề xuất EasyCA dưới dạng **Module Ký số PKI tích hợp (Add-on)** vào Viettel HMS thông qua API, không cần thay thế phần mềm HMS hiện tại của Viettel.

