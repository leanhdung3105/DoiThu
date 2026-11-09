---
title: "VNPT HIS & SmartCA — Giải pháp Ký Bệnh nhân qua VNeID & SmartCA"
vendor: "Tập đoàn Bưu chính Viễn thông Việt Nam (VNPT-IT)"
product: "VNPT HIS / SmartCA"
signing_method: "Ký xác thực qua VNeID app & Tiềm năng ký SmartCA cá nhân"
tt13_category: "Hình thức 3 (VNeID) & Hình thức 1 (SmartCA)"
legal_standing: "Cao (Sở hữu CA công cộng & kết nối Đề án 06)"
target_hospital: "Bệnh viện đa khoa công lập & trung tâm y tế toàn quốc"
deployments: "Triển khai rộng khắp hệ thống y tế cơ sở và một số BV tỉnh"
role: "Đối thủ toàn diện (Hạ tầng + CA)"
---

# VNPT HIS & SmartCA — Giải pháp Ký Bệnh nhân của VNPT

VNPT tiếp cận thị trường y tế qua 2 nền tảng: **VNPT HIS (phần mềm bệnh viện)** và **VNPT SmartCA (nhà cấp chữ ký số công cộng)**.

---

## 1. Phương thức Ký Bệnh nhân Hiện tại của VNPT

### Cách 1: Ký qua ứng dụng VNeID (Đang vận hành thực tế)
- VNPT HIS kết nối với hệ thống định danh Bộ Công An, đẩy thông báo xác nhận ký hồ sơ bệnh án sang App VNeID của bệnh nhân.
- Phân loại TT 13: **Hình thức 3** (Phương tiện điện tử khác).
- Gặp rào cản thao tác lớn với người già, trẻ nhỏ và người cấp cứu không có smartphone.

### Cách 2: Ký qua VNPT SmartCA Cá nhân (Tiềm năng lý thuyết)
- VNPT sở hữu hạ tầng SmartCA có thể cấp chứng thư số cá nhân (đạt **Hình thức 1**).
- **Rào cản thương mại hóa thực tế:** Quy trình kích hoạt SmartCA cá nhân của VNPT đòi hỏi người dân phải tải app SmartCA, xác minh định danh eKYC nhiều bước và đóng phí thường niên (vài trăm nghìn đồng/năm). Điều này **hoàn toàn không khả thi với bệnh nhân vãng lai** chỉ đến viện khám 1-2 lần trong năm.

---

## 2. So sánh Trực diện: VNPT vs EasyCA PKI

| Tiêu chí | VNPT HIS (VNeID) | VNPT SmartCA Cá nhân | **EasyCA PKI (SoftDreams)** |
|---|:---:|:---:|:---:|
| **Phân loại TT 13/2025** | Hình thức 3 | Hình thức 1 | **Hình thức 1 (Cao nhất)** |
| **Mô hình cấp CTS cho BN** | Không có CTS | Bắt buộc mua gói cá nhân theo năm | **Cấp theo sự vụ (On-demand) tức thì tại quầy** |
| **Bệnh nhân già không smartphone** | ❌ Bó tay | ❌ Bó tay | ✅ **Quét CCCD eKYC tại quầy trong 30s** |
| **Khả năng tích hợp HIS khác** | ❌ Đóng kín trong VNPT | ⚠️ Ưu tiên hệ sinh thái VNPT | ✅ **Open API tích hợp vào MỌI phần mềm** |

---

## 3. Kịch bản Bán hàng Thực chiến khi Bệnh viện đang Dùng VNPT HIS

- **Tình huống:** Bệnh viện công lập đang sử dụng phần mềm VNPT HIS.
- **EasyCA đáp trả:**
  1. **Tôn trọng hệ thống hiện có:** EasyCA không yêu cầu viện thay thế VNPT HIS.
  2. **Giải quyết bài toán bệnh nhân không smartphone:** *"VNPT làm rất tốt việc cấp SmartCA cho Bác sĩ. Nhưng với hàng nghìn lượt bệnh nhân/ngày, VNPT không thể bắt mỗi bệnh nhân mua gói SmartCA 1 năm. Nếu dùng VNeID thì 40% người già không có smartphone sẽ bị ách tắc. EasyCA bổ sung mảnh ghép còn thiếu: Module cấp chứng thư số tức thì cho bệnh nhân tích hợp vào luồng tiếp đón của VNPT HIS, giúp 100% bệnh nhân đều ký được."*
