---
title: "Tổng quan & So sánh Giải pháp Chữ ký số Bệnh nhân tại Bệnh viện"
description: "Báo cáo phân tích đối thủ cạnh tranh và so sánh các phương thức ký xác nhận của bệnh nhân/người nhà tại cơ sở y tế Việt Nam."
last_updated: "2026-11-09"
author: "EasyCA Solution Team - SoftDreams"
---

# Bảng So sánh Giải pháp Chữ ký số Bệnh nhân tại Bệnh viện

Báo cáo phân tích chuyên sâu các phương thức ký xác nhận dành cho **Bệnh nhân và Người nhà bệnh nhân** đang triển khai tại các bệnh viện Việt Nam, đối chiếu trực tiếp với giải pháp **EasyCA (SoftDreams)** sử dụng **CKS chuẩn PKI**.

---

## 1. Khung Pháp lý Tham chiếu: Thông tư 13/2025/TT-BYT (Điều 3)

Theo quy định của Bộ Y tế về hồ sơ bệnh án điện tử, chữ ký/xác nhận của người bệnh hoặc người đại diện hợp pháp được chấp nhận theo 3 hình thức:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│  HÌNH THỨC 1: Chữ ký điện tử hợp pháp (CKS chuẩn PKI do CA cấp phép) ➔ Cao nhất        │
│  HÌNH THỨC 2: Kỹ thuật sinh trắc học (Dấu vân tay, nhận diện khuôn mặt) ➔ Trung bình   │
│  HÌNH THỨC 3: Phương tiện điện tử khác (Ký tablet cảm ứng, OTP, VNeID) ➔ Cơ bản       │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

> **Lưu ý pháp lý quan trọng:** Dù Thông tư 13/2025 chấp nhận cả 3 hình thức, nhưng khi xảy ra **tranh chấp tai biến y khoa tại Tòa án**, chỉ có **Hình thức 1 (CKS chuẩn PKI)** mới có giá trị chứng cứ điện tử nguyên bản chống chối bỏ tuyệt đối theo Luật Giao dịch điện tử 2023.

---

## 2. Bảng Ma trận So sánh 7 Giải pháp trên Thị trường

| Đơn vị / Giải pháp | Phương thức ký bệnh nhân | Phân loại TT 13 | Chứng thư số PKI? | Chống chối bỏ | Bệnh nhân cần gì? | Bệnh viện đã dùng |
|---|---|:---:|:---:|:---:|---|---|
| **EasyCA (SoftDreams)** | **CKS chuẩn PKI (Cloud HSM)** | **Hình thức 1** | ✅ **Có (X.509)** | ✅✅ **Tuyệt đối** | CCCD tại quầy HOẶC Smartphone | Đang phát triển & mở rộng |
| **2ID / 2Contract** | Quét chip CCCD (NFC) + Đối soát mặt | Hình thức 2 & 3 | ❌ Không | ✅ Rất tốt | Chỉ cần thẻ CCCD gắn chip | BV Từ Dũ, Thanh Nhàn, Ung Bướu HN |
| **ISOFH (EMR)** | Đẩy thông báo ký qua App VNeID | Hình thức 3 | ❌ Không | ✅ Tốt | Smartphone + App VNeID mức 2 | BV Đa khoa Xanh Pôn |
| **Viettel HMS** | Ký tay trên Tablet + VNeID | Hình thức 3 | ❌ Không | ❌ Rất yếu (Tablet) | Tablet của viện / Smartphone | Hàng trăm BV công lập tuyến tỉnh/huyện |
| **VNPT HIS** | Ký qua VNeID + SmartCA | Hình thức 1 & 3 | ⚠️ Tiềm năng | ✅ Tốt (VNeID) | Smartphone có VNeID / SmartCA | BV ĐK Nông nghiệp, hệ thống VNPT HIS |
| **FPT eHospital** | Ký OTP SMS & VNeID | Hình thức 3 | ❌ Không | ⚠️ Trung bình | Điện thoại nhận SMS / VNeID | Một số BV tư nhân & BV tỉnh |
| **Ký tay Tablet (DentalFlow...)** | Vẽ ngón tay/stylus lên màn hình | Hình thức 3 | ❌ Không | ❌ Rất yếu | Ký trực tiếp trên tablet của viện | Phổ biến tại nha khoa, thẩm mỹ, BV tư |

---

## 3. Bản chất Kỹ thuật: Vì sao PKI là Chuẩn mực Vượt trội?

```
┌──────────────────────┬───────────────────────────────┬───────────────────────────────────┐
│ Tiêu chí kỹ thuật    │ Ký tay Tablet / Vân tay / OTP │ EasyCA Chuẩn PKI (SoftDreams)     │
├──────────────────────┼───────────────────────────────┼───────────────────────────────────┤
│ Khóa mã hóa          │ Không có cặp khóa mã hóa      │ Cặp khóa Private/Public Key X.509 │
│ Tính toàn vẹn        │ Sửa nội dung PDF không báo lỗi│ Sửa 1 byte file là chữ ký hỏng ngay│
│ Giám định pháp y     │ Không thể giám định nét vẽ    │ Tự động xác thực qua CA quốc gia │
│ Dấu thời gian (TSA)  │ Giờ máy tính viện (sửa được)  │ Dấu thời gian quốc gia chuẩn TSA  │
│ Bảo chứng nhà nước   │ Quy ước nội bộ phần mềm       │ NEAC (Bộ TT&TT) cấp phép          │
└──────────────────────┴───────────────────────────────┴───────────────────────────────────┘
```

---

## 4. Danh mục File Chi tiết Từng bên

1. [**01-easyca-softdreams.md**](01-easyca-softdreams.md) — Giải pháp EasyCA CKS chuẩn PKI (Sản phẩm của chúng ta)
2. [**02-2id-2contract.md**](02-2id-2contract.md) — 2ID / 2Contract (Quét chip CCCD gắn chip)
3. [**03-isofh-vneid.md**](03-isofh-vneid.md) — ISOFH (Ký qua ứng dụng VNeID tại BV Xanh Pôn)
4. [**04-viettel-hms.md**](04-viettel-hms.md) — Viettel HMS (Ký tay Tablet cảm ứng & VNeID)
5. [**05-vnpt-his.md**](05-vnpt-his.md) — VNPT HIS & SmartCA (VNeID và ký số y tế)
6. [**06-fpt-ehospital.md**](06-fpt-ehospital.md) — FPT eHospital (Ký OTP SMS & VNeID)
7. [**07-ky-tay-tablet.md**](07-ky-tay-tablet.md) — Giải pháp Ký tay trên Tablet (DentalFlow & HIS phòng khám)

