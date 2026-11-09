---
title: "ISOFH — Giải pháp Bệnh nhân Ký số qua Ứng dụng VNeID"
vendor: "Công ty Cổ phần Công nghệ ISOFH"
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

## 1. Phương thức & Quy trình Ký

```
[Bác sĩ tạo phiếu cam kết trên phần mềm EMR của ISOFH]
                         │
                         ▼
   1. Nhập số CCCD của bệnh nhân vào hệ thống EMR
                         │
                         ▼
   2. Hệ thống gọi API gửi thông báo Push sang App VNeID của bệnh nhân
                         │
                         ▼
   3. Bệnh nhân mở App VNeID trên điện thoại ➔ Đăng nhập bằng FaceID/Vân tay
                         │
                         ▼
   4. Bệnh nhân xem tài liệu và bấm "Đồng ý ký" (Nhập Passcode VNeID)
                         │
                         ▼
   5. ISOFH nhận tín hiệu callback và cập nhật trạng thái "Đã ký" vào EMR
```

---

## 2. Giá trị Pháp lý (Thông tư 13/2025/TT-BYT)

- **Phân loại TT 13:** Thuộc **Hình thức 3** (Phương tiện điện tử khác).
- **Tính chống chối bỏ:** Tốt nhờ định danh công dân mức 2 của Bộ Công An.
- **Bản chất:** Là bản ghi chấp thuận giao dịch điện tử, **chưa phải Chữ ký số PKI cá nhân (Hình thức 1)** có cặp khóa mã hóa riêng của bệnh nhân.

---

## 3. Điểm mạnh

- ✅ **Chính danh Đề án 06:** Được lãnh đạo Bộ Y tế và UBND các tỉnh đánh giá cao về tiêu chí chuyển đổi số.
- ✅ **Không cần đầu tư phần cứng:** Bệnh nhân tự dùng điện thoại thông minh cá nhân.
- ✅ **Tích hợp sâu vào lâm sàng:** Do chính ISOFH làm EMR nên quy trình từ tạo phiếu đến ký rất liền mạch.

---

## 4. Điểm yếu so với EasyCA PKI

- ❌ **Rào cản thiết bị rất lớn:** Bắt buộc bệnh nhân phải có smartphone, có mạng 4G/Wifi, đã cài và kích hoạt VNeID Mức 2 và nhớ mật khẩu. Người già, trẻ nhỏ, người vùng cao, bệnh nhân cấp cứu **hoàn toàn không thể tự ký**.
- ❌ **Phụ thuộc đường truyền máy chủ:** Nếu cổng kết nối VNeID bảo trì hoặc quá tải, quy trình ký tại viện bị nghẽn.
- ❌ **Lock-in phần mềm:** Chỉ chạy mượt trên EMR của ISOFH; các bệnh viện dùng HIS khác rất khó tích hợp.

