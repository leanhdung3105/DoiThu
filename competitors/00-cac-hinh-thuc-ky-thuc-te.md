---
title: "Báo cáo Chuyên đề: 6 Hình thức Ký Bệnh nhân Thực tế & Cơ chế Hoạt động"
description: "Tài liệu đào tạo nội bộ và trình bày lãnh đạo: Phân tích chi tiết cơ chế hoạt động, ưu nhược điểm và rủi ro pháp lý của 6 phương thức ký xác nhận bệnh nhân tại các bệnh viện Việt Nam."
last_updated: "2026-11-09"
author: "EasyCA Solution Team — SoftDreams"
---

# Báo cáo Chuyên đề: 6 Hình thức Ký Bệnh nhân Thực tế & Cơ chế Hoạt động

> **Tài liệu lưu hành nội bộ:** Dành cho Ban Lãnh đạo, Khối Phát triển Sản phẩm, Đội ngũ Giải pháp và Chuyên viên Tư vấn (Sales/Pre-sales) của SoftDreams.  
> **Mục tiêu:** Giúp Lãnh đạo và toàn thể cán bộ công ty hiểu tường tận bản chất kỹ thuật, cách thức vận hành thực tế tại bệnh viện, và vũ khí cạnh tranh của **EasyCA Chuẩn PKI** trước từng hình thức đối thủ.

---

## 🧭 PHẦN 1: BỨC TRANH TOÀN CẢNH (DÀNH CHO SẾP ĐỌC TRONG 2 PHÚT)

Khi bệnh nhân hoặc người nhà đến bệnh viện, họ phải ký rất nhiều loại giấy tờ: **Phiếu đồng ý phẫu thuật/thủ thuật, Cam kết sử dụng thuốc ngoài danh mục BHYT, Giấy từ chối điều trị, Bảng kê chi phí viện phí...**

Hiện nay, các bệnh viện tại Việt Nam đang chia thành **3 nhóm giải pháp**:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ NHÓM 1: LÀM TẠM BỢ ĐỂ BỎ GIẤY (Ký tay Tablet, Lấy dấu vân tay)                         │
│ ➔ Rất rẻ, thao tác nhanh, nhưng RỦI RO PHÁP LÝ KHỔNG LỒ (Tòa án không công nhận).     │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ NHÓM 2: ĂN THEO ĐỀ ÁN 06 (App VNeID, Thẻ CCCD gắn chip 2ID)                             │
│ ➔ Tính chính danh cao, nhưng BỊ NGHẼN VẬN HÀNH (Người già, cấp cứu, người ở xa).       │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ NHÓM 3: CHUẨN MỰC MẬT MÃ QUỐC GIA (EasyCA PKI — SoftDreams)                            │
│ ➔ Hình thức 1 TT 13/2025/TT-BYT. Đạt tính toàn vẹn và chống chối bỏ tuyệt đối.         │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### Bảng Ma trận Tóm tắt 6 Hình thức Ký trên Thị trường

| # | Hình thức Ký | Đơn vị tiêu biểu | Cách bệnh nhân thao tác | Phân loại TT 13 | Rủi ro lớn nhất |
|:---:|---|---|---|:---:|---|
| **1** | **Ký tay Tablet** | DentalFlow, Viettel HMS | Dùng bút/ngón tay vẽ lên iPad | **Hình thức 3** | Không giám định được khi có kiện tụng |
| **2** | **Lấy dấu Vân tay** | Các HIS tại quầy tiếp đón | Ấn ngón tay vào máy quét | **Hình thức 2** | Không khóa được nội dung file PDF |
| **3** | **Xác thực OTP** | FPT eHospital, BV tư | Nhập mã 6 số từ SMS gửi về | **Hình thức 3** | Tốn phí SMS; không biết ai là người bấm |
| **4** | **Ký qua App VNeID** | ISOFH (BV Xanh Pôn) | Bấm xác nhận trên app VNeID | **Hình thức 3** | Người già, trẻ nhỏ, ca cấp cứu không dùng được |
| **5** | **Quét chip CCCD** | 2ID / 2Contract (BV Từ Dũ) | Đặt CCCD chip lên đầu đọc NFC | **Hình thức 2 & 3** | Bắt buộc phải có mặt tại viện, không ký từ xa được |
| **6** | **CKS Chuẩn PKI** | **EasyCA (SoftDreams)** | eKYC quét CCCD tại viện / qua app | **HÌNH THỨC 1** ✅ | **Bảo vệ tuyệt đối Viện & Bác sĩ trước Tòa** |

---

## 🔍 PHẦN 2: CHI TIẾT CƠ CHẾ HOẠT ĐỘNG CỦA TỪNG HÌNH THỨC (HOW IT WORKS)

---

### HÌNH THỨC 1: KÝ TAY TRÊN TABLET CẢM ỨNG (STYLUS / TOUCH SIGNATURE)

> **Bên đang áp dụng:** DentalFlow (nha khoa), Viettel HMS, BambuFit, Nanosoft, LinkCare và nhiều phòng khám tư, bệnh viện thẩm mỹ.

#### 1. Quy trình thực tế tại bệnh viện:
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

#### 2. Bản chất kỹ thuật & Điểm nguy hiểm:
- **Chỉ là một bức ảnh vẽ thông thường:** Không hề có cặp khóa mã hóa (Private/Public Key). Bất kỳ ai có quyền truy cập cơ sở dữ liệu đều có thể trích xuất bức ảnh chữ ký này và dán vào bất kỳ tài liệu cam kết nào khác mà không để lại dấu vết.
- **Không phát hiện sửa đổi (Tamper-proofing):** File PDF sau khi chèn ảnh không được khóa hàm băm. Nếu ai đó sửa số tiền viện phí từ 5 triệu thành 50 triệu, ảnh chữ ký vẫn hiển thị bình thường.
- **Lỗ hổng giám định hình sự:** Theo **Viện Khoa học Hình sự (Bộ Công An)**, việc giám định chữ ký truyền thống dựa trên: *áp lực tì đè cơ học, thớ giấy xé, độ đậm nhạt mực, phản xạ cơ tay*. Nét vẽ trên màn hình kính điện dung **hoàn toàn mất đi các thuộc tính này**. Khi bệnh nhân kiện tai biến y khoa và tuyên bố *"Tôi chưa từng ký, nhân viên y tế tự vẽ lên"*, Bệnh viện hoàn toàn thua kiện vì không thể giám định được danh tính.

---

### HÌNH THỨC 2: LẤY DẤU VÂN TAY ĐIỆN TỬ (BIOMETRIC FINGERPRINT)

> **Bên đang áp dụng:** Nhiều hệ thống phần mềm quản lý bệnh viện (HIS) tại quầy tiếp đón ban đầu.

#### 1. Quy trình thực tế tại bệnh viện:
```
[Bệnh nhân đến quầy tiếp nhận] ──► [Đặt ngón tay lên máy quét vân tay]
                                                │
                                                ▼
[Máy quét trích xuất đặc trưng Minutiae] ──► [Lưu chuỗi byte vào Database hồ sơ]
```
1. Bệnh nhân đặt ngón trỏ hoặc ngón cái lên đầu đọc quang học/điện dung tại quầy.
2. Thiết bị phân tích các điểm ngã ba, điểm kết thúc của đường vân tay để tạo thành chuỗi số đặc trưng (Minutiae template).
3. Hệ thống lưu chuỗi dữ liệu này vào bảng dữ liệu bệnh nhân trong cơ sở dữ liệu HIS.

#### 2. Bản chất kỹ thuật & Điểm nguy hiểm:
- **"Nhận diện người" chứ "Không khóa được văn bản":** Dấu vân tay chỉ chứng minh bệnh nhân đã có mặt ở quầy lúc đăng ký khám. Dấu vân tay **không thể băm và niêm phong nội dung tài liệu**.
- Nếu sau đó có tranh chấp về nội dung phiếu cam kết mổ hay đơn thuốc, dấu vân tay không chứng minh được bệnh nhân đã đồng ý với phiên bản nội dung văn bản cụ thể nào.

---

### HÌNH THỨC 3: XÁC THỰC MÃ OTP (SMS / ZALO ZNS)

> **Bên đang áp dụng:** FPT eHospital, một số bệnh viện tư nhân và quốc tế.

#### 1. Quy trình thực tế tại bệnh viện:
```
[Bác sĩ tạo phiếu yêu cầu ký] ──► [Hệ thống gửi tin nhắn SMS chứa mã OTP 6 số]
                                                │
                                                ▼
[Bệnh nhân đọc SMS trên điện thoại] ──► [Nhập mã OTP vào màn hình] ──► [Xác nhận]
```

#### 2. Bản chất kỹ thuật & Điểm nguy hiểm:
- **Tốn chi phí viễn thông cho Bệnh viện:** Mỗi lượt gửi tin nhắn SMS Brandname tốn từ 300 - 500 đồng/tin. Một bệnh viện khám 2.000 lượt/ngày sẽ mất hàng chục triệu đồng tiền SMS mỗi tháng.
- **Nghẽn sóng trong bệnh viện:** Các khu vực nhạy cảm như phòng phẫu thuật, phòng hồi sức cấp cứu, tầng hầm, phòng chụp X-quang/MRI thường bị chắn sóng viễn thông rất nặng, mã OTP bị trễ 5 - 10 phút gây ách tắc thủ tục mổ.
- **Tính chống chối bỏ rất yếu:** Mã OTP chỉ chứng minh chiếc SIM đó nhận được tin nhắn. Bệnh nhân có thể chối bỏ trước Tòa: *"Tôi đang hôn mê trên cáng, con tôi cầm điện thoại bấm nhầm, tôi không hề đồng ý phẫu thuật"*.

---

### HÌNH THỨC 4: KÝ XÁC NHẬN QUA APP VNEID (BỘ CÔNG AN - ĐỀ ÁN 06)

> **Bên đang áp dụng:** **ISOFH** (triển khai tại **Bệnh viện Đa khoa Xanh Pôn**), **VNPT HIS** (BV Đa khoa Nông nghiệp), **Viettel HMS**.

#### 1. Quy trình thực tế tại bệnh viện:
```
[Bác sĩ tạo phiếu trên EMR] ──► [Hệ thống đẩy Push Notification sang App VNeID]
                                                │
                                                ▼
[Bệnh nhân mở VNeID trên Smartphone] ──► [Xác thực FaceID + Nhập Passcode VNeID]
                                                │
                                                ▼
[Bấm "Đồng ý ký"] ──► [Hệ thống EMR nhận tín hiệu và đổi trạng thái "Đã ký"]
```

#### 2. Điểm mạnh:
- Tận dụng tài khoản Định danh điện tử của Bộ Công An, có tính chính danh cao, phục vụ báo cáo thành tích Đề án 06 của Chính phủ cho Lãnh đạo tỉnh/thành phố.

#### 3. Điểm nghẽn vận hành thực tế tại Bệnh viện:
- **Rào cản thiết bị cực lớn:** Bắt buộc bệnh nhân phải: (1) Có điện thoại thông minh kết nối 4G/Wifi, (2) Đã cài app VNeID, (3) Đã kích hoạt Định danh Mức 2, (4) Nhớ mật khẩu đăng nhập và Passcode 6 số.
- **Thực tế lâm sàng:** 40-50% người đi khám tại các bệnh viện công là người cao tuổi, người lao động nghèo, trẻ em, hoặc bệnh nhân cấp cứu tai nạn giao thông. Đa phần các cụ dùng điện thoại "cục gạch", mắt mờ, không nhớ mật khẩu VNeID, dẫn đến việc **không thể thực hiện được thủ tục**.

---

### HÌNH THỨC 5: QUÉT CHIP THẺ CCCD (NFC) + ĐỐI SOÁT KHUÔN MẶT C06

> **Bên đang áp dụng:** **2ID / 2Contract** (đã triển khai thực tế tại **Bệnh viện Từ Dũ**, **BV Thanh Nhàn**, **BV Ung Bướu Hà Nội**, **BV Nhi đồng Cần Thơ**).

#### 1. Quy trình thực tế tại bệnh viện:
```
[Bệnh nhân đặt thẻ CCCD chip lên đầu đọc NFC] ──► [Camera chụp mặt so khớp 1:1 với chip CCCD]
                                                                │
                                                                ▼
[Bệnh nhân xem tài liệu trên màn hình phụ & bấm "Đồng ý"] ──► [2Contract tạo Audit Trail]
                                                                │
                                                                ▼
[Hệ thống dùng Chứng thư số của BỆNH VIỆN ký số niêm phong tài liệu]
```

#### 2. Điểm mạnh:
- Bệnh nhân không cần smartphone, không cần cài app; chỉ cần mang theo thẻ CCCD gắn chip (vốn là thứ bắt buộc khi đi khám BHYT). Tốc độ quét tại quầy rất nhanh (5-10 giây).

#### 3. Điểm yếu cốt tử so với EasyCA:
- **Không hỗ trợ ký từ xa:** Bắt buộc phải áp thẻ vật lý vào đầu đọc tại viện. Trong trường hợp bệnh nhân cấp cứu mà **người nhà ở xa (ở quê, ở nước ngoài)** cần ký cam kết bảo lãnh phẫu thuật gấp thì giải pháp của 2ID hoàn toàn bất lực.
- **2ID không phải là CA công cộng:** 2ID chỉ cung cấp giải pháp xác thực công nghệ. Văn bản ký xong thực chất là do **Bệnh viện ký số đóng dấu niêm phong**, chứ bệnh nhân không được cấp chứng thư số PKI riêng theo Luật Giao dịch điện tử 2023.

---

### HÌNH THỨC 6: CHỮ KÝ SỐ CHUẨN PKI CÁ NHÂN CẤP TỨC THÌ (EASYCA - SOFTPREAMS)

> **Bên tiên phong:** **EasyCA (SoftDreams)** — Ứng dụng công nghệ Cloud HSM và eKYC theo chuẩn quốc tế.

#### 1. Quy trình thực tế tại bệnh viện:
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

#### 2. Vì sao đây là "Chuẩn mực Tối thượng"?
1. **Đạt Hình thức 1 Thông tư 13/2025/TT-BYT:** Đây là hình thức có cấp độ pháp lý cao nhất trong ngành y tế, tương đương hợp đồng công chứng.
2. **Tính toàn vẹn tuyệt đối (Tamper-proofing):** Bất kỳ ai sửa đổi dù chỉ 1 dấu chấm, 1 chữ số viện phí hay liều thuốc trong file PDF, thuật toán băm SHA-256 sẽ lập tức báo chữ ký bị phá hủy (Invalid).
3. **Tính chống chối bỏ hoàn hảo (Non-repudiation):** Chứng thư số do NEAC (Bộ TT&TT) bảo chứng danh tính, được Tòa án mặc định thừa nhận là chứng cứ điện tử nguyên bản theo Luật Giao dịch điện tử 2023. Bệnh nhân không thể phủ nhận chữ ký.
4. **Linh hoạt đa kênh:**
   - Tại quầy: Quét CCCD gắn chip (tiện như 2ID).
   - Tại giường bệnh: Bác sĩ/điều dưỡng mang tablet đến giường cho bệnh nhân xác thực.
   - **Ký từ xa:** Gửi đường link cho người nhà ở bất kỳ tỉnh thành nào mở camera eKYC và ký số ngay trong 1 phút.

---

## 🎯 PHẦN 3: BẢNG SO SÁNH 3 TÌNH HUỐNG THỰC TẾ (SALES & SẾP CẦN NẮM RÕ)

Khi đi gặp Ban Giám đốc Bệnh viện, hãy dùng 3 tình huống lâm sàng này để chứng minh sự vượt trội của EasyCA:

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

## 🚀 PHẦN 4: THÔNG ĐIỆP BÁN HÀNG CỐT LÕI (EASYCA VALUE PROPOSITION)

> **"Ký tay trên tablet hay lấy vân tay chỉ là giải pháp tạm bợ để bỏ giấy, nhưng để lại BOM NỔ CHẬM VỀ PHÁP LÝ cho Bệnh viện. EasyCA mang đến giải pháp KÝ SỐ PKI CHUẨN — Vừa tiện lợi đa kênh (tại quầy, tại giường, từ xa), vừa bảo vệ tuyệt đối Ban Giám đốc và Bác sĩ trước Tòa án."**
