---
title: "2ID / 2Contract — Xác thực & Ký Bệnh nhân bằng Thẻ CCCD gắn Chip"
vendor: "Công ty Cổ phần Chuyển đổi số 2ID"
product: "2Contract"
signing_method: "Quét chip CCCD (NFC) + Đối soát khuôn mặt C06"
tt13_category: "Hình thức 2 (Sinh trắc) & Hình thức 3 (Phương tiện điện tử)"
legal_standing: "Khá cao (Bảo chứng qua dữ liệu C06 Bộ Công An)"
target_hospital: "Bệnh viện tuyến đầu có lưu lượng khám lớn"
deployments: "BV Từ Dũ, BV Thanh Nhàn, BV Ung Bướu Hà Nội, BV Nhi đồng Cần Thơ"
role: "Đối thủ trực tiếp lớn nhất"
---

# 2ID / 2Contract — Giải pháp Quét chip CCCD tại Bệnh viện

2ID là đơn vị tiên phong ứng dụng **Thẻ Căn cước công dân gắn chip (NFC)** kết hợp nền tảng **2Contract** để giải quyết bài toán ký cam kết và xác nhận của bệnh nhân/thân nhân tại bệnh viện.

---

## 1. Phương thức & Quy trình Ký

```
[Bệnh nhân đến quầy tiếp nhận / làm thủ tục phẫu thuật]
                         │
                         ▼
   1. Đặt thẻ CCCD gắn chip lên đầu đọc chuyên dụng (NFC)
                         │
                         ▼
   2. Camera tại quầy chụp mặt & so khớp 1:1 với dữ liệu gốc trong chip CCCD
                         │
                         ▼
   3. Bệnh nhân bấm "Đồng ý" trên màn hình phụ tại quầy
                         │
                         ▼
   4. 2Contract tạo bản ghi bằng chứng định danh (Audit Trail)
      và ký số niêm phong bằng Chứng thư số của Bệnh viện
```

---

## 2. Giá trị Pháp lý (Thông tư 13/2025/TT-BYT)

- **Phân loại TT 13:** Thuộc **Hình thức 2** (Sinh trắc học) và **Hình thức 3** (Phương tiện điện tử khác).
- **Bản chất chữ ký:** Là **Xác nhận điện tử gắn với danh tính CCCD**, chứ **KHÔNG PHẢI là Chữ ký số PKI cá nhân (Hình thức 1)** của chính người bệnh theo Luật GDĐT 2023 vì 2ID không phải là CA công cộng được Bộ TT&TT cấp phép.
- **Niêm phong:** Thường dùng Chữ ký số của Bệnh viện để đóng dấu niêm phong văn bản sau khi có log xác nhận của bệnh nhân.

---

## 3. Điểm mạnh

- ✅ **Trải nghiệm tại quầy cực tốt:** Bệnh nhân không cần smartphone, không cần tải app hay nhớ mật khẩu; chỉ cần mang thẻ CCCD gắn chip.
- ✅ **Nhiều case study lớn:** Đã chạy thực tế tại BV Từ Dũ (phiếu cam kết mổ sản khoa), BV Thanh Nhàn, BV Ung Bướu HN.
- ✅ **Tốc độ nhanh:** Thao tác quét thẻ và so khớp khuôn mặt diễn ra trong 5 - 10 giây.

---

## 4. Điểm yếu so với EasyCA PKI

- ❌ **Không ký từ xa được:** Bắt buộc bệnh nhân/người nhà phải có mặt áp thẻ vào đầu đọc. Nếu người nhà ở xa cần ký bảo lãnh phẫu thuật gấp thì 2ID bất khả thi.
- ❌ **Phụ thuộc phần cứng tại quầy:** Bắt buộc BV phải đầu tư đầu đọc thẻ NFC và camera tại từng bàn làm việc/quầy tiếp đón. Khó triển khai khi bác sĩ đi buồng tại giường bệnh.
- ❌ **Chưa đạt Hình thức 1:** Không cấp Chứng thư số PKI cá nhân chuẩn X.509 cho bệnh nhân.

