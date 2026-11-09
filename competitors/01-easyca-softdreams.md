---
title: "EasyCA (SoftDreams) — Giải pháp Chữ ký số Chuẩn PKI cho Bệnh nhân"
vendor: "SoftDreams"
product: "EasyCA"
signing_method: "CKS chuẩn PKI (Cloud HSM / eKYC tức thì)"
tt13_category: "Hình thức 1 (Chữ ký điện tử hợp pháp — Cấp cao nhất)"
legal_standing: "Tuyệt đối (NEAC - Bộ TT&TT cấp phép bảo chứng)"
target_hospital: "Bệnh viện đa khoa, chuyên khoa công lập & tư nhân"
deployments: "Đang mở rộng tích hợp các hệ thống HIS/EMR toàn quốc"
role: "Sản phẩm của chúng ta"
---

# EasyCA (SoftDreams) — Giải pháp Chữ ký số Chuẩn PKI cho Bệnh nhân

EasyCA là giải pháp chữ ký số công cộng được **NEAC (Trung tâm Chứng thực điện tử quốc gia — Bộ TT&TT)** cấp phép, ứng dụng công nghệ **Ký số từ xa (Remote Signing)** kết hợp **Cloud HSM (đạt chuẩn an mật FIPS 140-2 Level 3)** để giải quyết trọn vẹn bài toán ký xác nhận của bệnh nhân và người nhà tại cơ sở y tế.

---

## 1. Cơ chế Hoạt động & Quy trình Lâm sàng tại Bệnh viện

Khác với bác sĩ dùng USB Token cố định 1-3 năm, bệnh nhân đến viện không có sẵn chứng thư số. EasyCA giải quyết bằng mô hình **Cấp Chứng thư số PKI cá nhân theo sự vụ (On-demand/Ad-hoc PKI)** hoặc cấp nhanh qua eKYC:

```
[Bệnh nhân đến quầy / tại giường bệnh / hoặc ở xa]
                          │
                          ▼
        ┌───────────────────────────────────────────┐
        │ Bước 1: eKYC Định danh tức thì            │
        │ - Quét chip CCCD (NFC tại quầy/Camera app)│
        │ - Đối soát khuôn mặt (Face Matching 1:1)  │
        │ - Thời gian xử lý: < 30 giây              │
        └─────────────────────┬─────────────────────┘
                              │
                              ▼
        ┌───────────────────────────────────────────┐
        │ Bước 2: Cấp Chứng thư số PKI cá nhân      │
        │ - Sinh cặp khóa Private/Public Key X.509  │
        │ - Lưu trữ an mật trên EasyCA Cloud HSM    │
        │   (Chuẩn an toàn quốc tế FIPS 140-2 L3)   │
        └─────────────────────┬─────────────────────┘
                              │
                              ▼
        ┌───────────────────────────────────────────┐
        │ Bước 3: Xem tài liệu & Xác thực lệnh ký   │
        │ - Xem phiếu cam kết trên màn hình quầy /  │
        │   tablet điều dưỡng / smartphone cá nhân   │
        │ - Xác thực lệnh ký bằng FaceID / PIN / OTP│
        └─────────────────────┬─────────────────────┘
                              │
                              ▼
        ┌───────────────────────────────────────────┐
        │ Bước 4: Ký số PKI & Niêm phong hồ sơ      │
        │ - Cloud HSM dùng Private Key ký số PAdES  │
        │ - Băm SHA-256 khóa cứng nội dung file PDF │
        │ - Đóng dấu thời gian TSA quốc gia         │
        │ - Đẩy trực tiếp vào hệ thống HIS/EMR viện │
        └───────────────────────────────────────────┘
```

---

## 2. Vì sao EasyCA PKI là "Chuẩn mực Vượt trội" theo Thông tư 13/2025/TT-BYT?

### 2.1 Đạt cấp độ pháp lý cao nhất (Hình thức 1)
- Theo **Điều 3 Thông tư 13/2025/TT-BYT**, chữ ký số PKI của EasyCA được xếp vào **Hình thức 1 (Chữ ký điện tử hợp pháp)**.
- Theo **Luật Giao dịch điện tử 2023**, chữ ký số công cộng được pháp luật suy đoán tính hợp lệ và có **giá trị chứng cứ nguyên bản trước Tòa án** tương đương hợp đồng công chứng truyền thống.

### 2.2 Tính toàn vẹn tuyệt đối (Tamper-proofing)
- Thuật toán băm **SHA-256** khóa cứng toàn bộ nội dung tài liệu PDF ngay tại thời điểm ký.
- Nếu bất kỳ ai (kể cả nhân viên IT bệnh viện) can thiệp sửa đổi dù chỉ 1 dấu chấm, 1 chữ số viện phí hay phác đồ điều trị, chữ ký trên file PDF sẽ lập tức báo lỗi đỏ (**Signature Invalid / Document Tampered**).

### 2.3 Tính chống chối bỏ hoàn hảo (Non-repudiation)
- Cặp khóa Private Key nằm trong vùng bảo mật Cloud HSM mà chỉ chủ thể ký mới có quyền kích hoạt.
- Khi xảy ra sự cố tai biến y khoa, bệnh nhân/thân nhân **không thể chối bỏ** chữ ký vì danh tính đã được CA quốc gia bảo chứng.

### 2.4 Dấu thời gian TSA (Timestamp Authority) chuẩn Bộ TT&TT
- Đóng dấu thời gian chuẩn quốc gia độc lập với giờ máy tính viện, chứng minh chính xác tài liệu được ký **TRƯỚC KHI** phẫu thuật hay điều trị, dập tắt mọi nghi ngờ về việc *"bệnh viện tự ý lập biên bản sau khi bệnh nhân tử vong"*.

### 2.5 Chuẩn lưu trữ bệnh án 20 năm (LTV / PAdES)
- Luật Khám bệnh, chữa bệnh 2023 yêu cầu hồ sơ bệnh án phải lưu trữ tối thiểu **20 năm** (tử vong là 50 năm). Chuẩn ký số quốc tế LTV (Long Term Validation) đảm bảo sau 20 năm mở lại file vẫn xác minh được tính toàn vẹn và hợp lệ của người ký.

---

## 3. Khả năng Vận hành Đa kênh (Multi-channel)

Khác với các đối thủ bị trói buộc vào một phương tiện duy nhất, EasyCA hỗ trợ linh hoạt 3 kênh vận hành:
1. **Tại quầy tiếp đón ban đầu:** Bệnh nhân chỉ cần mang thẻ CCCD gắn chip (tiện lợi và nhanh như 2ID).
2. **Tại giường bệnh nội trú:** Điều dưỡng mang máy tính bảng đến giường, bệnh nhân xác thực khuôn mặt để ký cam kết thủ thuật.
3. **Ký từ xa (Remote Signing):** Gửi đường link qua Zalo/SMS cho người nhà ở bất kỳ tỉnh thành nào mở camera eKYC và ký số bảo lãnh phẫu thuật khẩn cấp trong 1 phút.

---

## 4. Ma trận So sánh: EasyCA PKI vs 5 Phương thức Đối thủ

| Tiêu chí | Ký Tablet | Vân tay | OTP SMS | VNeID App | 2ID (CCCD) | **EasyCA PKI** |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| **Phân loại TT 13/2025** | Hình thức 3 | Hình thức 2 | Hình thức 3 | Hình thức 3 | Hình thức 2 & 3 | **Hình thức 1** ✅ |
| **Bảo chứng Nhà nước** | ❌ Không | ❌ Không | ⚠️ Viễn thông | ✅ Bộ Công An | ✅ Bộ Công An | ✅ **Bộ TT&TT (NEAC)** |
| **Chứng thư số cá nhân** | ❌ Không | ❌ Không | ❌ Không | ❌ Không | ❌ Không | ✅ **Có (X.509)** |
| **Khóa toàn vẹn nội dung PDF** | ❌ Không | ❌ Không | ❌ Không | ⚠️ Tùy HIS | ⚠️ Ký sau | ✅✅ **Tuyệt đối (SHA-256)** |
| **Giám định khi kiện tụng** | ❌ Bó tay | ⚠️ Yếu | ❌ Rất yếu | ✅ Tốt | ✅ Rất tốt | ✅✅ **Chứng cứ nguyên bản** |
| **Người già không smartphone** | ✅ Ký được | ✅ Ấn được | ⚠️ Khó | ❌ **Bó tay** | ✅ Rất tốt | ✅ **Rất tốt (eKYC quầy)** |
| **Ký từ xa (người nhà ở xa)** | ❌ Bó tay | ❌ Bó tay | ⚠️ Rủi ro | ⚠️ Cần VNeID | ❌ **Bó tay** | ✅ **Xuất sắc (Link eKYC)** |

---

## 5. Kịch bản Bán hàng Thực chiến (Sales Battlecard cho Đội ngũ EasyCA)

### 5.1 Bộ 3 câu hỏi khai thác nỗi sợ (Discovery Questions)
1. *"Thưa Ban Giám đốc, nếu xảy ra một ca sốc phản vệ hoặc tử vong phẫu thuật, người nhà thuê luật sư kiện và nói rằng 'Bản cam kết này là do bệnh viện tự vẽ lên sau khi người nhà tôi mất' — Bệnh viện có bằng chứng khoa học nào được Viện Khoa học Hình sự giám định để chứng minh không?"*
2. *"Với chữ ký tablet hay vân tay hiện tại, nếu một nhân viên kỹ thuật mở file PDF ra sửa đổi liều lượng thuốc hoặc viện phí, hệ thống có tự động báo file bị phá hủy tính toàn vẹn không?"*
3. *"Khi bảo hiểm xã hội (BHYT) thanh tra bệnh án điện tử, nếu hồ sơ chỉ lưu ảnh chụp chữ ký hoặc OTP không gắn chứng thư số hợp pháp (Hình thức 1), Bệnh viện đã lường trước nguy cơ bị xuất toán hàng tỷ đồng viện phí chưa?"*

### 5.2 Thông điệp cốt lõi (Core Message)
> **"Ký tay trên tablet hay lấy vân tay chỉ là giải pháp tạm bợ để bỏ giấy, nhưng để lại BOM NỔ CHẬM VỀ PHÁP LÝ cho Bệnh viện. EasyCA mang đến giải pháp KÝ SỐ PKI CHUẨN — Vừa tiện lợi đa kênh (tại quầy, tại giường, từ xa), vừa bảo vệ tuyệt đối Ban Giám đốc và Bác sĩ trước Tòa án."**
