---
title: "ISOFH — Giải pháp Bệnh nhân Ký số qua Ứng dụng VNeID"
vendor: "Công ty Cổ phần Công nghệ ISOFH (Hợp tác C06 - Bộ Công An)"
product: "ISOFH EMR / HIS tích hợp VNeID"
signing_method: "Xác thực & Ký qua ứng dụng VNeID (Push Notification)"
tt13_category: "Hình thức 3 (Phương tiện điện tử khác)"
legal_standing: "Khá cao (Bộ Công An bảo chứng)"
target_hospital: "Bệnh viện công lập thí điểm Đề án 06"
deployments: "Bệnh viện Đa khoa Xanh Pôn (Hà Nội), BV ĐK Nông nghiệp"
role: "Đối thủ tiêu biểu mảng ký VNeID"
---

# ISOFH — Giải pháp Ký Bệnh nhân qua App VNeID tại Bệnh viện

ISOFH là nhà cung cấp phần mềm Bệnh án điện tử (EMR) hàng đầu, phối hợp cùng Cục C06 (Bộ Công An) triển khai giải pháp cho bệnh nhân ký cam kết và hồ sơ bệnh án bằng **tài khoản định danh điện tử VNeID**, tiêu biểu nhất tại **Bệnh viện Đa khoa Xanh Pôn**.

---

## 1. Cơ chế Hoạt động & Quy trình Lâm sàng tại Bệnh viện

```
[Bác sĩ tạo phiếu cam kết trên phần mềm EMR của ISOFH]
                         │
                         ▼
        ┌───────────────────────────────────────────┐
        │ Bước 1: Nhập số CCCD của bệnh nhân        │
        │ Bác sĩ / Điều dưỡng nhập CCCD vào EMR     │
        └─────────────────────┬─────────────────────┘
                              │
                              ▼
        ┌───────────────────────────────────────────┐
        │ Bước 2: Đẩy Push Notification sang VNeID  │
        │ Hệ thống gọi API gửi yêu cầu ký sang C06  │
        │ Điện thoại bệnh nhân nhận thông báo Push  │
        └─────────────────────┬─────────────────────┘
                              │
                              ▼
        ┌───────────────────────────────────────────┐
        │ Bước 3: Người bệnh mở App VNeID           │
        │ Mở app VNeID ➔ Đăng nhập FaceID/Vân tay   │
        │ Xem trước nội dung tài liệu / phiếu mổ    │
        └─────────────────────┬─────────────────────┘
                              │
                              ▼
        ┌───────────────────────────────────────────┐
        │ Bước 4: Xác nhận ký                       │
        │ Bệnh nhân bấm "Đồng ý ký"                 │
        │ Nhập Passcode 6 số của tài khoản VNeID    │
        └─────────────────────┬─────────────────────┘
                              │
                              ▼
        ┌───────────────────────────────────────────┐
        │ Bước 5: Cập nhật bệnh án EMR              │
        │ ISOFH nhận callback thành công            │
        │ Gắn trạng thái "Đã ký" vào hồ sơ bệnh án  │
        └───────────────────────────────────────────┘
```

---

## 2. Bản chất Pháp lý theo Thông tư 13/2025/TT-BYT

- **Phân loại TT 13:** Thuộc **Hình thức 3** (Phương tiện điện tử khác).
- **Tính chống chối bỏ:** Tốt nhờ định danh công dân mức 2 của Bộ Công An bảo chứng.
- **Bản chất:** Là bản ghi chấp thuận giao dịch điện tử, **chưa phải Chữ ký số PKI cá nhân (Hình thức 1)** có cặp khóa mã hóa riêng của bệnh nhân.

---

## 3. Điểm mạnh Thực tế của ISOFH

- ✅ **Chính danh Đề án 06:** Được lãnh đạo Bộ Y tế và UBND các tỉnh đánh giá rất cao về tiêu chí chuyển đổi số và ứng dụng VNeID quốc gia.
- ✅ **Bệnh viện không cần đầu tư thiết bị tại giường:** Bệnh nhân tự dùng điện thoại thông minh cá nhân.
- ✅ **Tích hợp sâu vào lâm sàng:** Do chính ISOFH làm EMR nên quy trình từ tạo phiếu đến ký rất liền mạch.
- ✅ **Hiệu ứng truyền thông mạnh:** VTV và báo chí đưa tin rầm rộ tại BV Xanh Pôn, tạo sức ép cho nhiều Giám đốc bệnh viện khác muốn làm theo.

---

## 4. Điểm yếu Cốt tử & Rào cản Lâm sàng của VNeID

1. **Rào cản thiết bị rất lớn đối với người bệnh:**
   - Bắt buộc bệnh nhân phải có: (1) Smartphone có 4G/Wifi, (2) Đã cài app VNeID, (3) Đã kích hoạt Định danh Mức 2, (4) Nhớ mật khẩu và Passcode.
   - **Thực tế tại các bệnh viện công:** 40-50% người bệnh là người cao tuổi, người lao động nghèo, trẻ em, hoặc bệnh nhân cấp cứu tai nạn giao thông hôn mê. Nhóm này **hoàn toàn không thể tự ký qua VNeID**.
2. **Phụ thuộc vào đường truyền máy chủ:**
   - Khi hệ thống VNeID hoặc mạng Internet quá tải/bảo trì, quy trình ký tại bệnh viện bị ách tắc hoàn toàn, không thể phẫu thuật hoặc xuất viện.
3. **Lock-in phần mềm:**
   - Giải pháp của ISOFH gắn chặt với phần mềm EMR của chính họ; các bệnh viện đang dùng HIS khác (VNPT, Viettel, FPT...) rất khó tích hợp.

---

## 5. Kịch bản Bán hàng Thực chiến khi Gặp Khách hàng Muốn làm Giống Xanh Pôn

- **Tình huống Bệnh viện nói:** *"Bệnh viện Đa khoa Xanh Pôn đang cho người bệnh ký qua VNeID rất nổi tiếng trên thời sự, chúng tôi muốn làm giống họ."*
- **EasyCA đáp trả (Chiến lược Kết hợp — Không đối đầu):**
  1. **Thừa nhận:** *"Mô hình của Xanh Pôn rất tốt về mặt truyền thông Đề án 06 của Chính phủ."*
  2. **Chỉ ra điểm nghẽn lâm sàng:** *"Tuy nhiên, Ban Giám đốc đã tính đến kịch bản: 40% bệnh nhân đến viện là các cụ già 70-80 tuổi dùng điện thoại đen trắng, không nhớ mật khẩu VNeID, hoặc các ca cấp cứu khẩn cấp thì bệnh viện giải quyết thế nào? Nếu lại quay về cho ký giấy rồi scan vào máy thì không còn là Bệnh án điện tử không giấy tờ nữa!"*
  3. **Đưa giải pháp EasyCA PKI Đa kênh:** *"EasyCA giải quyết triệt để vấn đề này: Chúng tôi cung cấp giải pháp Đa phương thức. Bệnh nhân nào có VNeID thì ký qua VNeID; bệnh nhân nào không có smartphone thì quét CCCD/sinh trắc tại quầy. Tất cả đều được EasyCA đóng gói thành Chứng thư số PKI hợp pháp (Hình thức 1), giúp viện vừa đạt chỉ tiêu chuyển đổi số vừa đảm bảo 100% bệnh nhân đều ký thông suốt."*
