# Nghiên cứu Đối thủ: Chữ ký số Bệnh nhân tại Bệnh viện
> **Đơn vị nghiên cứu:** Ban Giải pháp EasyCA — SoftDreams  
> **Khung pháp lý tham chiếu:** Luật Giao dịch điện tử 2023, Luật Khám bệnh, chữa bệnh 2023, **Thông tư 13/2025/TT-BYT (Điều 3)**.

---

## 🧭 BỨC TRANH TOÀN CẢNH & KHUNG PHÁP LÝ TT 13/2025/TT-BYT

Khi bệnh nhân hoặc người nhà đến khám chữa bệnh, họ phải ký xác nhận rất nhiều loại văn bản có rủi ro pháp lý cao: **Phiếu đồng ý phẫu thuật/thủ thuật, Cam kết sử dụng thuốc ngoài danh mục BHYT, Giấy từ chối điều trị, Bảng kê chi phí viện phí...**

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

## 📊 BẢNG MA TRẬN SO SÁNH 7 GIẢI PHÁP TRÊN THỊ TRƯỜNG

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

## 🔍 CHI TIẾT CƠ CHẾ HOẠT ĐỘNG 6 PHƯƠNG THỨC KÝ

### 1. Ký tay trên Tablet cảm ứng (DentalFlow, Viettel HMS)
- **Cơ chế:** Điều dưỡng đưa Tablet ➔ Bệnh nhân dùng bút/ngón tay vẽ lên màn hình ➔ Phần mềm chụp ảnh PNG dán vào PDF ➔ Lưu Database.
- **Rủi ro:** Bản chất chỉ là file ảnh vẽ, không có mã hóa PKI, không khóa được nội dung file PDF. Viện Khoa học Hình sự không thể giám định nét vẽ trên kính cảm ứng.

### 2. Lấy dấu Vân tay điện tử (HIS quầy tiếp đón)
- **Cơ chế:** Quét ngón tay tại quầy ➔ Lưu chuỗi template đặc trưng vào Database.
- **Rủi ro:** "Nhận diện người" chứ "Không khóa được văn bản". Không niêm phong được nội dung cam kết mổ.

### 3. Xác thực mã OTP (FPT eHospital)
- **Cơ chế:** Bắn mã OTP 6 số về SMS ➔ Bệnh nhân nhập mã xác nhận.
- **Rủi ro:** Tốn phí SMS của viện; sóng chập chờn ở phòng mổ/tầng hầm; không chứng minh được ai là người bấm mã.

### 4. Ký qua App VNeID (ISOFH tại BV Xanh Pôn)
- **Cơ chế:** EMR gọi API đẩy Push Notification ➔ Bệnh nhân mở App VNeID xác thực FaceID/Passcode để ký.
- **Rào cản:** Người già 70-80 tuổi, trẻ nhỏ, bệnh nhân cấp cứu không có smartphone/không nhớ pass thì chịu chết.

### 5. Quét chip CCCD qua NFC (2ID tại BV Từ Dũ, Thanh Nhàn)
- **Cơ chế:** Đặt CCCD chip lên đầu đọc NFC ➔ Camera chụp mặt đối soát C06 ➔ Bệnh nhân bấm "Đồng ý" ➔ Chữ ký số Bệnh viện ký niêm phong.
- **Rào cản:** Không ký từ xa được khi người nhà ở xa; 2ID không phải là CA cấp chứng thư số cho bệnh nhân.

### 6. CKS Chuẩn PKI cấp tức thì (EasyCA - SoftDreams)
- **Cơ chế:** eKYC 30s ➔ Cấp Chứng thư số PKI cá nhân trên Cloud HSM FIPS 140-2 Level 3 ➔ Băm SHA-256 khóa cứng file PDF + Đóng dấu thời gian quốc gia TSA.
- **Ưu thế tuyệt đối:** Đạt Hình thức 1 TT 13/2025/TT-BYT; chống chối bỏ hoàn hảo trước Tòa án; hỗ trợ đa kênh (tại quầy, tại giường, ký từ xa).

---

## 🎯 3 TÌNH HUỐNG LÂM SÀNG THỰC TẾ

1. **Bệnh nhân 75 tuổi đi khám một mình:** VNeID bó tay ➔ EasyCA quét CCCD eKYC tại quầy trong 30s.
2. **Cấp cứu trong đêm, người nhà ở tỉnh khác:** Ký tablet và 2ID bó tay ➔ EasyCA gửi link ký từ xa qua eKYC tức thì.
3. **Kiện tụng tai biến phẫu thuật ra Tòa:** Ký tablet thua kiện ➔ EasyCA thắng kiện 100% nhờ chứng cứ điện tử nguyên bản.

---

## 🔗 Danh mục Báo cáo Chi tiết Từng Đối thủ

- ⭐ [01 - EasyCA (SoftDreams) - Chuẩn PKI](competitors/01-easyca-softdreams.md)
- 💳 [02 - 2ID / 2Contract (Quét chip CCCD)](competitors/02-2id-2contract.md)
- 📱 [03 - ISOFH (Ký qua App VNeID BV Xanh Pôn)](competitors/03-isofh-vneid.md)
- 🏥 [04 - Viettel HMS (Ký tay Tablet & VNeID)](competitors/04-viettel-hms.md)
- 🌐 [05 - VNPT HIS & SmartCA](competitors/05-vnpt-his.md)
- 📩 [06 - FPT eHospital (Ký OTP SMS & VNeID)](competitors/06-fpt-ehospital.md)
- ✍️ [07 - Mô hình Ký tay Tablet (DentalFlow...)](competitors/07-ky-tay-tablet.md)
