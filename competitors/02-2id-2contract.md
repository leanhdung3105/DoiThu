---
title: "2ID / 2Contract — Xác thực & Ký Bệnh nhân bằng Thẻ CCCD gắn Chip"
vendor: "Công ty Cổ phần Chuyển đổi số 2ID (Hợp tác C06 - Bộ Công An)"
product: "2Contract"
signing_method: "Quét chip CCCD (NFC) + Đối soát khuôn mặt C06"
tt13_category: "Hình thức 2 (Sinh trắc) & Hình thức 3 (Phương tiện điện tử)"
legal_standing: "Khá cao (Bảo chứng qua dữ liệu C06 Bộ Công An)"
target_hospital: "Bệnh viện tuyến đầu có lưu lượng khám lớn"
deployments: "BV Từ Dũ, BV Thanh Nhàn, BV Ung Bướu Hà Nội, BV Nhi đồng Cần Thơ"
role: "Đối thủ trực tiếp lớn nhất hiện nay"
---

# 2ID / 2Contract — Giải pháp Quét chip CCCD tại Bệnh viện

2ID là đơn vị tiên phong ứng dụng **Thẻ Căn cước công dân gắn chip (NFC)** kết hợp nền tảng **2Contract** để giải quyết bài toán ký cam kết và xác nhận của bệnh nhân/thân nhân tại bệnh viện.

---

## 1. Cơ chế Hoạt động & Quy trình Lâm sàng tại Bệnh viện

```
[Bệnh nhân / Người nhà đến quầy tiếp nhận hoặc làm thủ tục phẫu thuật]
                               │
                               ▼
        ┌────────────────────────────────────────────────────────┐
        │ Bước 1: Quét thẻ CCCD gắn chip (NFC)                   │
        │ - Đặt CCCD lên đầu đọc chuyên dụng tại bàn tiếp đón    │
        │ - Đọc dữ liệu sinh trắc học & thông tin mã hóa trong chip│
        │ - Tự động điền thông tin hành chính vào phiếu khám     │
        └──────────────────────────┬─────────────────────────────┘
                                   │
                                   ▼
        ┌────────────────────────────────────────────────────────┐
        │ Bước 2: Đối soát sinh trắc học khuôn mặt 1:1           │
        │ - Camera tại quầy chụp ảnh khuôn mặt bệnh nhân         │
        │ - So khớp trực tiếp với ảnh gốc lưu trong chip CCCD/C06│
        │ - Xác minh chính chủ (chống dùng thẻ CCCD người khác)  │
        └──────────────────────────┬─────────────────────────────┘
                                   │
                                   ▼
        ┌────────────────────────────────────────────────────────┐
        │ Bước 3: Xác nhận cam kết & Ghi nhận chữ ký             │
        │ - Bệnh nhân xem tài liệu trên màn hình phụ tại quầy    │
        │ - Bệnh nhân bấm "Đồng ý cam kết"                       │
        │ - 2Contract tạo bản ghi bằng chứng định danh điện tử   │
        │   (Audit Trail: Mã thẻ, ảnh chụp, kết quả so khớp, giờ)│
        │ - Hệ thống ký số niêm phong bằng Chứng thư số BỆNH VIỆN│
        └────────────────────────────────────────────────────────┘
```

---

## 2. Phân tích Bản chất Pháp lý: 2ID vs EasyCA PKI

Đây là điểm khác biệt cốt lõi mà đội ngũ EasyCA cần nắm chắc:

| Tiêu chí pháp lý | Giải pháp 2ID / 2Contract | Giải pháp EasyCA PKI |
|---|---|---|
| **Bản chất chữ ký của người bệnh** | **Xác nhận điện tử gắn với dữ liệu CCCD** (Electronic Confirmation). Bệnh nhân không sở hữu cặp khóa Private Key riêng. | **Chữ ký số PKI cá nhân chuẩn X.509** (Digital Signature). Bệnh nhân được cấp chứng thư số và ký bằng Private Key riêng của mình. |
| **Phân loại TT 13/2025** | **Hình thức 2 & 3** (Sinh trắc học kết hợp phương tiện điện tử). | **Hình thức 1** (Chữ ký điện tử hợp pháp — Cấp độ pháp lý cao nhất). |
| **Chủ thể ký số niêm phong** | Thường là **Chữ ký số của Bệnh viện / Tổ chức** ký đóng dấu lên tài liệu sau khi có log xác nhận của bệnh nhân. | **Chính bệnh nhân ký số PKI** lên tài liệu, sau đó Bác sĩ / Bệnh viện ký số tiếp theo (Dual Signing). |
| **Tính chống chối bỏ trước Tòa** | Khá tốt nhờ dữ liệu C06, nhưng nếu luật sư tranh tụng về quyền sở hữu khóa bí mật cá nhân thì 2ID không chứng minh được bệnh nhân nắm giữ Private Key. | **Mạnh nhất tuyệt đối:** Đáp ứng trọn vẹn Luật Giao dịch điện tử 2023 và Nghị định 130/2018/NĐ-CP về chữ ký số công cộng. |

---

## 3. Điểm mạnh Thực tế của 2ID

- ✅ **Trải nghiệm tại quầy cực tốt:** Bệnh nhân không cần smartphone, không cần tải app hay nhớ mật khẩu; chỉ cần mang thẻ CCCD gắn chip (thứ bắt buộc khi khám BHYT).
- ✅ **Triển khai thành công ở nhiều BV lớn:** Bệnh viện Từ Dũ (nổi tiếng với phiếu đồng ý phẫu thuật sản khoa), BV Thanh Nhàn, BV Ung Bướu Hà Nội. Đây là rào cản tham chiếu lớn khi EasyCA đi chào hàng.
- ✅ **Tốc độ làm thủ tục nhanh:** Quét chip và so khớp khuôn mặt diễn ra trong 5 - 10 giây.

---

## 4. Điểm yếu Cốt tử của 2ID để EasyCA Khai thác

1. **Hoàn toàn không ký từ xa được:**
   - Trường hợp **Người nhà bệnh nhân ở xa** (ví dụ: con ở nước ngoài hoặc ở tỉnh khác cần ký cam kết bảo lãnh mổ khẩn cấp cho bố mẹ tại viện) thì mô hình quét thẻ CCCD của 2ID **hoàn toàn bất lực**.
2. **Phụ thuộc phần cứng đầu đọc tại quầy:**
   - 2ID bắt buộc phải có đầu đọc thẻ NFC chuyên dụng và camera tại từng bàn làm việc/quầy tiếp nhận. Chi phí trang bị phần cứng cho toàn viện (hàng chục đến hàng trăm quầy) là rất lớn.
   - Khi bác sĩ đi buồng (thăm khám tại giường bệnh nội trú), việc mang theo đầu đọc thẻ cồng kềnh rất bất tiện.
3. **Không phải Chữ ký số PKI cá nhân (Hình thức 1):**
   - 2ID không phải là CA công cộng được Bộ TT&TT cấp phép. Họ chỉ cung cấp giải pháp công nghệ xác thực danh tính.

---

## 5. Kịch bản Bán hàng Thực chiến khi Gặp Khách hàng Khen 2ID

- **Tình huống Bệnh viện nói:** *"2ID đã làm ở Bệnh viện Từ Dũ rất xịn rồi, quét CCCD gắn chip tiện lợi, bên em có làm được như họ không?"*
- **EasyCA đáp trả (3 đòn bẩy):**
  1. **Thừa nhận thế mạnh:** *"2ID là một giải pháp rất tốt ở khâu quét thẻ CCCD tại quầy tiếp đón ban đầu."*
  2. **Đòn bẩy 1 — Ký từ xa & Tại giường:** *"Tuy nhiên, Bệnh viện sẽ xử lý thế nào khi người nhà bệnh nhân đang ở tỉnh khác cần ký cam kết mổ cấp cứu gấp trong đêm? 2ID bắt buộc người nhà phải có mặt tại viện để áp thẻ vào đầu đọc. EasyCA giải quyết triệt để vấn đề này vì hỗ trợ cả quét CCCD tại quầy lẫn **Ký từ xa qua eKYC trên điện thoại** cho người nhà ở bất kỳ đâu."*
  3. **Đòn bẩy 2 — Nâng cấp lên Hình thức 1:** *"2ID chỉ là giải pháp xác thực công nghệ (Hình thức 2/3). EasyCA là CA quốc gia được Bộ TT&TT cấp phép (Hình thức 1). Chúng tôi cấp Chứng thư số PKI cá nhân chuẩn X.509 đích danh cho người bệnh, giúp bệnh viện đạt chuẩn pháp lý cao nhất và được bảo hiểm trách nhiệm pháp lý theo luật."*
