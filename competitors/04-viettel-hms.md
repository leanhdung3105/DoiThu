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

Viettel sở hữu phần mềm quản lý bệnh viện **Viettel HMS** phủ rộng ở khối bệnh viện công. Mặc dù có Viettel-CA, nhưng Viettel-CA chỉ dùng cho nhân viên y tế (bác sĩ ký bệnh án, đơn thuốc); còn đối với **Bệnh nhân**, Viettel HMS chủ yếu dùng **Ký tay trên Tablet** hoặc đang thử nghiệm **VNeID**.

---

## 1. Cơ chế Hoạt động 2 Phương thức của Viettel HMS

### Cách 1: Ký tay trên Tablet cảm ứng (Phổ biến nhất)
```
[Điều dưỡng mang Tablet đến giường / quầy] ──► [Bệnh nhân vẽ chữ ký lên màn hình]
                                                                │
                                                                ▼
[Viettel HMS xuất file ảnh PNG] ──► [Chèn ảnh vào ô ký trên PDF] ──► [Lưu vào Database]
```
- **Bản chất:** Chỉ là một bức ảnh vẽ bitmap (PNG), hoàn toàn không có hàm băm niêm phong tài liệu và không có cặp khóa mã hóa.
- **Rủi ro giám định:** Viện Khoa học Hình sự (Bộ Công An) không thể giám định lực nét bút trên màn hình kính cảm ứng.

### Cách 2: Ký xác thực qua App VNeID (Thí điểm Đề án 06)
- Viettel HMS đẩy thông báo Push sang App VNeID của bệnh nhân ➔ Bệnh nhân xác thực FaceID và bấm "Đồng ý ký". Tương tự ISOFH, gặp rào cản lớn với bệnh nhân cao tuổi và cấp cứu.

---

## 2. Rủi ro Pháp lý & Rủi ro Xuất toán BHYT của Viettel HMS

| Rủi ro | Giải pháp Viettel HMS (Ký Tablet) | Giải pháp EasyCA PKI (SoftDreams) |
|---|---|---|
| **Giám định khi Kiện tụng** | ❌ **Không thể giám định:** Tòa án bác bỏ chứng cứ vì nét vẽ trên kính không có thuộc tính cơ học. | ✅✅ **Chứng cứ nguyên bản:** Tòa án mặc định thừa nhận theo Luật Giao dịch điện tử 2023. |
| **Thanh tra BHYT xuất toán** | ⚠️ **Nguy cơ cao:** BHYT từ chối thanh toán các bảng kê chi phí hàng tỷ đồng nếu chữ ký bệnh nhân bị coi là không hợp lệ theo TT 13/2025. | ✅ **An toàn tuyệt đối:** Đạt chuẩn Hình thức 1 cao nhất của Bộ Y tế, không thể bị xuất toán. |
| **Tính toàn vẹn (Integrity)** | ❌ **Sửa file PDF không báo lỗi:** Chữ ký tablet vẫn hiển thị bình thường dù số tiền bị sửa. | ✅✅ **Khóa cứng SHA-256:** Sửa 1 byte file là chữ ký lập tức báo lỗi Invalid. |

---

## 3. Kịch bản Bán hàng Thực chiến khi Bệnh viện đang Dùng Viettel HMS

Khi tiếp cận các bệnh viện công lập đang sử dụng Viettel HMS, đội ngũ EasyCA cần áp dụng chiến thuật **"Cộng sinh — Không đối đầu"**:

1. **Không đối đầu thay thế Viettel HMS:**
   - Không bao giờ chào mời thay thế phần mềm Viettel HMS vì đây là hợp đồng thầu hạ tầng CNTT tổng thể rất lớn của viện.
2. **Định vị EasyCA là Module Ký số PKI Chuyên sâu (Add-on):**
   - Đề xuất giải pháp: *"EasyCA cung cấp Module Ký số PKI cho Bệnh nhân tích hợp trực tiếp vào Viettel HMS thông qua API mở. Viettel HMS tiếp tục quản lý bệnh viện, còn EasyCA đảm nhiệm việc bảo vệ pháp lý tuyệt đối cho hồ sơ bệnh án."*
3. **Đánh vào nỗi sợ của Ban Giám đốc:**
   - *"Hiện tại Bệnh viện đang cho bệnh nhân ký tay trên máy tính bảng của Viettel. Giải pháp này giúp viện bỏ giấy tờ tạm thời, nhưng khi xảy ra sự cố y khoa lớn hoặc khi đoàn Thanh tra BHYT về kiểm tra các khoản cùng chi trả, chữ ký tablet này không đủ giá trị chứng cứ để bảo vệ viện. EasyCA nâng cấp toàn bộ chữ ký tablet đó thành Chữ ký số PKI chuẩn Hình thức 1 của Bộ Y tế."*
