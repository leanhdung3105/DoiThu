---
title: "Tổng quan & Phân tích 6 Hình thức Ký Bệnh nhân tại Bệnh viện"
description: "Báo cáo phân tích toàn cảnh thị trường: Cơ chế hoạt động 6 phương thức ký xác nhận của bệnh nhân, ma trận so sánh đối thủ và ưu thế của EasyCA Chuẩn PKI."
last_updated: "2026-11-09"
author: "EasyCA Solution Team — SoftDreams"
---

# Tổng quan & Phân tích 6 Hình thức Ký Bệnh nhân tại Bệnh viện

> **Tài liệu chiến lược nội bộ:** Dành cho Ban Lãnh đạo, Khối Phát triển Sản phẩm, Đội ngũ Giải pháp và Chuyên viên Tư vấn (Sales/Pre-sales) của SoftDreams.  
> **Khung pháp lý tham chiếu:** Luật Giao dịch điện tử 2023, Luật Khám bệnh, chữa bệnh 2023, **Thông tư 13/2025/TT-BYT (Điều 3)**.

---

## 🧭 PHẦN 1: BỨC TRANH TOÀN CẢNH & KHUNG PHÁP LÝ TT 13/2025/TT-BYT

Khi bệnh nhân hoặc người nhà đến khám chữa bệnh, họ phải ký xác nhận rất nhiều loại văn bản có rủi ro pháp lý cao: **Phiếu đồng ý phẫu thuật/thủ thuật, Cam kết sử dụng thuốc/vật tư ngoài danh mục BHYT, Giấy từ chối điều trị, Bảng kê chi phí viện phí...**

Theo **Điều 3 Thông tư 13/2025/TT-BYT** của Bộ Y tế về hồ sơ bệnh án điện tử, chữ ký/xác nhận của người bệnh được chấp nhận theo 3 cấp độ:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│  HÌNH THỨC 1: Chữ ký điện tử hợp pháp (CKS chuẩn PKI do CA cấp phép) ➔ Cao nhất        │
│  HÌNH THỨC 2: Kỹ thuật sinh trắc học (Dấu vân tay, nhận diện khuôn mặt) ➔ Trung bình   │
│  HÌNH THỨC 3: Phương tiện điện tử khác (Ký tablet cảm ứng, OTP, VNeID) ➔ Cơ bản       │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

> **Lưu ý pháp lý quan trọng:** Dù Thông tư 13/2025 chấp nhận cả 3 hình thức, nhưng khi xảy ra **tranh chấp tai biến y khoa tại Tòa án**, chỉ có **Hình thức 1 (CKS chuẩn PKI)** mới có giá trị chứng cứ điện tử nguyên bản chống chối bỏ tuyệt đối theo Luật Giao dịch điện tử 2023.

---

## 📊 PHẦN 2: BẢNG MA TRẬN SO SÁNH 7 GIẢI PHÁP TRÊN THỊ TRƯỜNG

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

## 🔍 PHẦN 3: CHI TIẾT CƠ CHẾ HOẠT ĐỘNG CỦA 6 PHƯƠNG THỨC (HOW IT WORKS)

---

### 1. Ký tay trên Tablet cảm ứng (Stylus / Touch Signature)
> **Bên đang áp dụng:** DentalFlow (nha khoa), Viettel HMS, BambuFit, Nanosoft, LinkCare và hầu hết các phòng khám tư, thẩm mỹ viện.

#### Quy trình thực tế:
```
[Điều dưỡng đưa Tablet/iPad] ──► [Bệnh nhân vẽ chữ ký lên màn hình]
                                                │
                                                ▼
[Phần mềm xuất file ảnh PNG] ──► [Chèn ảnh chữ ký vào file PDF] ──► [Lưu vào Server]
```
1. Bệnh nhân hoặc người nhà xem nội dung phiếu cam kết trên màn hình máy tính bảng.
2. Dùng ngón tay hoặc bút cảm ứng vẽ ngoáy chữ ký lên ô ký tên.
3. Phần mềm bắt sự kiện nét vẽ, chụp lại thành một file ảnh bitmap (PNG/JPEG).
4. Hệ thống chèn ảnh này vào tọa độ (X, Y) trên file PDF mẫu rồi lưu vào cơ sở dữ liệu.

#### Bản chất kỹ thuật & Rủi ro:
- **Chỉ là bức ảnh vẽ thông thường:** Không hề có cặp khóa mã hóa. Bất kỳ ai có quyền truy cập cơ sở dữ liệu đều có thể trích xuất ảnh chữ ký này và dán vào bất kỳ tài liệu nào khác mà không để lại dấu vết.
- **Không phát hiện sửa đổi (Tamper-proofing):** File PDF sau khi chèn ảnh không được khóa hàm băm. Nếu ai đó sửa số tiền viện phí hay liều thuốc, ảnh chữ ký vẫn hiển thị bình thường.
- **Tòa án không công nhận:** Theo **Viện Khoa học Hình sự (Bộ Công An)**, màn hình kính không có thớ giấy, không có lực tì đè cơ học nên **không thể giám định danh tính**. Khi có tranh chấp tai biến y khoa, bệnh viện hoàn toàn mất quyền tự vệ.

---

### 2. Lấy dấu Vân tay điện tử (Biometric Fingerprint)
> **Bên đang áp dụng:** Nhiều hệ thống phần mềm quản lý bệnh viện (HIS) tại quầy tiếp đón ban đầu.

#### Quy trình thực tế:
```
[Bệnh nhân đến quầy tiếp nhận] ──► [Đặt ngón tay lên máy quét vân tay]
                                                │
                                                ▼
[Máy quét trích xuất đặc trưng Minutiae] ──► [Lưu chuỗi byte vào Database hồ sơ]
```

#### Bản chất kỹ thuật & Rủi ro:
- **"Nhận diện người" chứ "Không khóa được văn bản":** Dấu vân tay chỉ chứng minh bệnh nhân đã có mặt ở quầy lúc đăng ký khám. Dấu vân tay **không thể băm và niêm phong nội dung tài liệu**.
- Nếu sau đó có tranh chấp về nội dung phiếu cam kết mổ hay đơn thuốc, dấu vân tay không chứng minh được bệnh nhân đã đồng ý với phiên bản nội dung văn bản cụ thể nào.

---

### 3. Xác thực mã OTP (SMS / Zalo ZNS)
> **Bên đang áp dụng:** FPT eHospital, một số bệnh viện tư nhân và quốc tế.

#### Quy trình thực tế:
```
[Bác sĩ tạo phiếu yêu cầu ký] ──► [Hệ thống gửi SMS chứa mã OTP 6 số]
                                                │
                                                ▼
[Bệnh nhân đọc SMS trên điện thoại] ──► [Nhập mã OTP vào màn hình] ──► [Xác nhận]
```

#### Bản chất kỹ thuật & Rủi ro:
- **Tốn chi phí viễn thông cho Viện:** Mỗi tin nhắn SMS Brandname tốn 300 - 500 đồng/tin. Viện khám 2.000 lượt/ngày mất hàng chục triệu đồng tiền SMS mỗi tháng.
- **Nghẽn sóng trong bệnh viện:** Phòng mổ, hồi sức cấp cứu, tầng hầm, phòng chụp X-quang/MRI bị chắn sóng viễn thông rất nặng, mã OTP bị trễ 5 - 10 phút gây ách tắc ca phẫu thuật.
- **Chống chối bỏ yếu:** Mã OTP chỉ chứng minh chiếc SIM nhận được tin nhắn; bệnh nhân dễ dàng chối: *"Tôi hôn mê, con tôi cầm máy bấm nhầm, tôi không đồng ý phẫu thuật"*.

---

### 4. Ký xác nhận qua App VNeID (Bộ Công An - Đề án 06)
> **Bên đang áp dụng:** **ISOFH** (triển khai tại **BV Đa khoa Xanh Pôn**), **VNPT HIS** (BV ĐK Nông nghiệp), **Viettel HMS**.

#### Quy trình thực tế:
```
[Bác sĩ tạo phiếu trên EMR] ──► [Hệ thống đẩy Push Notification sang App VNeID]
                                                │
                                                ▼
[Bệnh nhân mở VNeID trên Smartphone] ──► [Xác thực FaceID + Nhập Passcode VNeID]
                                                │
                                                ▼
[Bấm "Đồng ý ký"] ──► [Hệ thống EMR nhận tín hiệu và đổi trạng thái "Đã ký"]
```

#### Điểm mạnh & Điểm nghẽn:
- **Điểm mạnh:** Tận dụng định danh công dân của Bộ Công An, có tính chính danh cao, đạt chỉ tiêu chuyển đổi số Đề án 06.
- **Điểm nghẽn thực tế:** Bắt buộc bệnh nhân phải có smartphone, có 4G/Wifi, đã cài app VNeID Mức 2 và nhớ mật khẩu. Thực tế tại các bệnh viện công: 40-50% người bệnh là người già, trẻ nhỏ, người cấp cứu hôn mê **hoàn toàn không thể tự thao tác**.

---

### 5. Quét thẻ CCCD gắn chip (NFC) + Đối soát khuôn mặt C06
> **Bên đang áp dụng:** **2ID / 2Contract** (đã triển khai tại **BV Từ Dũ**, **BV Thanh Nhàn**, **BV Ung Bướu Hà Nội**, **BV Nhi đồng Cần Thơ**).

#### Quy trình thực tế:
```
[Bệnh nhân đặt thẻ CCCD chip lên đầu đọc NFC] ──► [Camera chụp mặt so khớp 1:1 với chip CCCD]
                                                                │
                                                                ▼
[Bệnh nhân xem tài liệu trên màn hình phụ & bấm "Đồng ý"] ──► [2Contract tạo Audit Trail]
                                                                │
                                                                ▼
[Hệ thống dùng Chứng thư số của BỆNH VIỆN ký số niêm phong tài liệu]
```

#### Điểm mạnh & Điểm nghẽn:
- **Điểm mạnh:** Bệnh nhân không cần smartphone, không cần tải app; chỉ cần mang thẻ CCCD gắn chip. Thao tác quét tại quầy diễn ra trong 5 - 10 giây.
- **Điểm nghẽn cốt tử:** 
  + **Không ký từ xa được:** Bắt buộc phải áp thẻ vật lý vào đầu đọc tại viện; người nhà ở xa không thể ký cam kết mổ khẩn cấp.
  + **2ID không phải là CA công cộng:** Văn bản thực chất là do Bệnh viện ký số đóng dấu niêm phong sau khi có log của bệnh nhân, chứ bệnh nhân không được cấp chứng thư số PKI riêng theo Luật GDĐT 2023.

---

### 6. Chữ ký số Chuẩn PKI cá nhân cấp tức thì (EasyCA - SoftDreams)
> **Bên tiên phong:** **EasyCA (SoftDreams)** — Ứng dụng Cloud HSM và eKYC theo chuẩn quốc tế.

#### Quy trình thực tế:
```
[Bệnh nhân đến quầy / tại giường bệnh / hoặc ở xa]
                     │
                     ▼
1. eKYC Định danh tức thì (Quét CCCD chip + So khớp khuôn mặt trong 30 giây)
                     │
                     ▼
2. Cấp Chứng thư số PKI cá nhân tức thì (Lưu trên EasyCA Cloud HSM FIPS 140-2 Level 3)
                     │
                     ▼
3. Bệnh nhân xác thực lệnh ký (Mã PIN / OTP / Sinh trắc khuôn mặt)
                     │
                     ▼
4. Cloud HSM dùng Private Key của chính Bệnh nhân ký số chuẩn PAdES
   + Khóa cứng tài liệu bằng hàm băm SHA-256 + Đóng dấu thời gian quốc gia TSA
```

#### Vì sao EasyCA PKI là "Chuẩn mực Vượt trội"?
1. **Đạt Hình thức 1 TT 13/2025/TT-BYT:** Cấp độ pháp lý cao nhất trong ngành y tế, tương đương hợp đồng công chứng.
2. **Tính toàn vẹn tuyệt đối (Tamper-proofing):** Sửa đổi dù chỉ 1 chữ số viện phí hay liều thuốc trong file PDF, thuật toán băm SHA-256 sẽ lập tức báo chữ ký bị phá hủy (Invalid).
3. **Tính chống chối bỏ hoàn hảo (Non-repudiation):** Được NEAC (Bộ TT&TT) bảo chứng, Tòa án mặc định thừa nhận là chứng cứ điện tử nguyên bản theo Luật Giao dịch điện tử 2023.
4. **Linh hoạt đa kênh:**
   - Tại quầy: Quét CCCD gắn chip (tiện lợi như 2ID).
   - Tại giường bệnh: Bác sĩ mang tablet đến giường cho bệnh nhân xác thực.
   - **Ký từ xa:** Gửi đường link cho người nhà ở bất kỳ đâu mở camera eKYC và ký số ngay trong 1 phút.

---

## 🎯 PHẦN 4: 3 TÌNH HUỐNG LÂM SÀNG THỰC TẾ (SALES & SẾP CẦN NẮM RÕ)

### Tình huống 1: Bệnh nhân lớn tuổi (75 tuổi) đi khám một mình
* **VNeID (ISOFH):** ❌ Bó tay (Cụ già không có smartphone, không nhớ mật khẩu VNeID).
* **2ID (CCCD chip):** ✅ Tốt tại quầy (Nhân viên đặt thẻ chip lên đầu đọc).
* **EasyCA PKI:** ✅ Xuất sắc (Cụ chỉ cần đưa thẻ CCCD, nhân viên hỗ trợ quét chip eKYC trong 30 giây là xong).

### Tình huống 2: Bệnh nhân tai nạn cấp cứu trong đêm, người nhà ở tỉnh khác
* **Ký tablet:** ❌ Bó tay (Người nhà không có mặt ở viện để vẽ lên màn hình).
* **2ID (CCCD chip):** ❌ Bó tay (Bắt buộc phải áp thẻ vật lý vào đầu đọc tại viện).
* **EasyCA PKI:** ✅ Duy nhất xử lý được (Bệnh viện gửi link ký từ xa qua Zalo/SMS cho người nhà ở tỉnh, người nhà quét CCCD bằng camera điện thoại, xác thực khuôn mặt và ký số bảo lãnh phẫu thuật tức thì).

### Tình huống 3: Kiện tụng tai biến y khoa ra Tòa án
* **Ký tablet:** ❌ Thua kiện (Tòa án và Viện Khoa học Hình sự không thể giám định nét vẽ trên kính).
* **Vân tay:** ⚠️ Rủi ro cao (Không chứng minh được nội dung cam kết mổ có bị sửa đổi sau đó hay không).
* **EasyCA PKI:** ✅ Thắng kiện 100% (File PDF có chữ ký số PKI của người bệnh + Dấu thời gian TSA chứng minh bệnh nhân đã đồng ý trước thời điểm mổ + Toàn vẹn không bị chỉnh sửa).

---

## 📁 PHẦN 5: DANH MỤC BÁO CÁO CHI TIẾT TỪNG BÊN

1. [**01-easyca-softdreams.md**](01-easyca-softdreams.md) — Phân tích Chuyên sâu Giải pháp EasyCA CKS Chuẩn PKI (Sản phẩm của chúng ta)
2. [**02-2id-2contract.md**](02-2id-2contract.md) — 2ID / 2Contract (Quét chip thẻ CCCD tại BV Từ Dũ, Thanh Nhàn...)
3. [**03-isofh-vneid.md**](03-isofh-vneid.md) — ISOFH (Ký qua ứng dụng VNeID tại BV Đa khoa Xanh Pôn)
4. [**04-viettel-hms.md**](04-viettel-hms.md) — Viettel HMS (Ký tay Tablet cảm ứng & VNeID khối BV công)
5. [**05-vnpt-his.md**](05-vnpt-his.md) — VNPT HIS & SmartCA (VNeID và ký số y tế)
6. [**06-fpt-ehospital.md**](06-fpt-ehospital.md) — FPT eHospital (Ký OTP SMS & VNeID)
7. [**07-ky-tay-tablet.md**](07-ky-tay-tablet.md) — Phân tích Mô hình Ký tay Tablet (DentalFlow & các HIS phòng khám)
