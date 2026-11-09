# Nghiên cứu Đối thủ: Các Phương thức Ký Bệnh nhân tại Cơ sở Y tế

> **Đơn vị nghiên cứu:** Ban Giải pháp EasyCA — SoftDreams  
> **Khung pháp lý tham chiếu:** Luật Giao dịch điện tử số 20/2023/QH15, Nghị định số 23/2025/NĐ-CP, Luật Khám bệnh, chữa bệnh số 15/2023/QH15, Luật Bảo vệ dữ liệu cá nhân số 91/2025/QH15, Nghị định số 356/2025/NĐ-CP và **Thông tư số 13/2025/TT-BYT (Điều 3)**.

---

## 🧭 KHUNG PHÁP LÝ THAM CHIẾU: THÔNG TƯ 13/2025/TT-BYT (ĐIỀU 3)

Trong hồ sơ bệnh án điện tử (EMR), chữ ký hoặc xác nhận điện tử của người bệnh (hoặc người đại diện hợp pháp) được Bộ Y tế quy định thực hiện linh hoạt theo **3 nhóm phương thức**:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│  NHÓM 1: Sử dụng chữ ký điện tử hợp pháp (bao gồm chữ ký số của cá nhân người bệnh     │
│          theo quy định của pháp luật về giao dịch điện tử).                            │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  NHÓM 2: Sử dụng các kỹ thuật sinh trắc học (như dấu vân tay, nhận diện khuôn mặt...). │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  NHÓM 3: Sử dụng các hình thức xác nhận bằng phương tiện điện tử khác theo quy định tại │
│          khoản 4 Điều 22 Luật Giao dịch điện tử 2023 (như xác thực VNeID, OTP SMS,     │
│          hoặc ký trực tiếp trên thiết bị cảm ứng / bảng ký tại cơ sở y tế).            │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

> **Nguyên tắc phân tích pháp lý & giá trị chứng cứ:**
> - Thông tư 13/2025/TT-BYT quy định 3 nhóm phương thức trên cơ sở bình đẳng theo pháp luật chuyên ngành y tế; **không quy định thứ bậc hành chính** (như "Cao nhất - Trung bình - Cơ bản").
> - Tuy nhiên, khi phát sinh tranh chấp hoặc khiếu nại chuyên môn trước cơ quan tài phán, **Điều 11 Luật Giao dịch điện tử số 20/2023/QH15** quy định giá trị chứng cứ của thông điệp dữ liệu được đánh giá căn cứ vào **độ tin cậy của cách thức khởi tạo, gửi, nhận hoặc lưu trữ; cách thức bảo đảm tính toàn vẹn; và cách thức xác định chủ thể thực hiện**.
> - Chữ ký số chuẩn PKI (thuộc Nhóm 1) có ưu thế vượt trội về cơ chế mật mã học (cặp khóa bí mật/công khai, hàm băm SHA-256 chống sửa đổi, chứng thư số do CA công cộng được cấp phép phát hành), mang lại **tính chống chối bỏ kỹ thuật và giá trị chứng minh cao nhất**, mặc dù không có bất kỳ giải pháp nào được xem là "thắng kiện mặc định 100%" mà luôn phụ thuộc vào toàn bộ hồ sơ vụ việc theo pháp luật tố tụng `[Đã xác minh căn cứ pháp lý]`.

---

## 📊 BẢNG MA TRẬN SO SÁNH CÁC GIẢI PHÁP TRÊN THỊ TRƯỜNG

| Đơn vị / Giải pháp | Phương thức ký người bệnh | Phân nhóm theo TT 13/2025 | Cơ chế Chứng minh Danh tính & Toàn vẹn | Khả năng Ký từ xa | Mức độ Triển khai Thực tế tại Bệnh viện |
|---|---|:---:|---|:---:|---|
| **EasyCA (SoftDreams)** | **Chữ ký số PKI (Remote Signing / HSM)** | **Nhóm 1** | Cặp khóa cá nhân X.509 + Băm SHA-256 + Dấu thời gian TSA | ✅ Hỗ trợ eKYC từ xa | `[Chưa xác minh]` Đang nghiên cứu & phát triển, chưa có dự án vận hành chính thức |
| **ISOFH / BV Xanh Pôn** | **Chữ ký số PKI xác thực qua VNeID** | **Nhóm 1** | Cấp CTS SmartCA cá nhân + VNeID Mức 2 kích hoạt ký | ⚠️ Được (nếu có VNeID & mạng) | `[Đã xác minh]` 100% nội trú & 3 phòng khám ngoại trú tại BV Đa khoa Xanh Pôn |
| **2ID / 2Contract** | Quét chip CCCD (NFC) + Đối soát khuôn mặt | Nhóm 2 & Nhóm 3 | Đối soát sinh trắc 1:1 chip CCCD + Ký số niêm phong CTS BV | ❌ Cần quét thẻ tại quầy | `[Đã xác minh]` Trúng thầu HSM tại BV Từ Dũ; `[Có nguồn tham khảo]` Thanh Nhàn, Ung Bướu |
| **Viettel HMS** | Ký cảm ứng trên Tablet / VNeID | Nhóm 3 | Ghi nhận nét vẽ kèm Audit Log; hoặc xác nhận qua VNeID | ❌ Ký tablet phải ở viện | `[Đã xác minh]` Hiện diện tại nhiều BV công qua Hệ thống Mạng đấu thầu Quốc gia |
| **VNPT HIS** | Ký qua VNeID / Tablet / SmartCA | Nhóm 3 (hoặc Nhóm 1) | Xác thực qua VNeID; hoặc cấp SmartCA (nếu có tài khoản) | ⚠️ Phụ thuộc phương thức | `[Đã xác minh]` Hàng nghìn trạm y tế cơ sở và nhiều bệnh viện đa khoa tỉnh |
| **FPT eHospital** | Xác thực qua mã OTP SMS / Zalo | Nhóm 3 | Ghi nhận số điện thoại tiếp nhận OTP và biên lai viễn thông | ⚠️ Gửi OTP qua mạng viễn thông | `[Đã xác minh]` BV đa khoa tỉnh Quảng Ninh, Đồng Nai, hệ thống BV tư nhân Hoàn Mỹ |
| **Ký tay Tablet (DentalFlow...)** | Vẽ chữ ký trên màn hình cảm ứng | Nhóm 3 | Lưu ảnh nét vẽ; hệ thống cao cấp lưu kèm tọa độ, Device ID | ❌ Bắt buộc tại cơ sở y tế | `[Đã xác minh]` Phổ biến tại hàng trăm phòng khám chuyên khoa, nha khoa, thẩm mỹ |

---

## 🔍 TÓM TẮT 6 PHƯƠNG THỨC KÝ TRÊN THỊ TRƯỜNG

1. **Chữ ký Cảm ứng trên Tablet (Touch / Stylus Signature):** Ký bằng ngón tay hoặc bút cảm ứng trên màn hình máy tính bảng. Mức độ tin cậy chứng minh phụ thuộc vào việc hệ thống có lưu trữ đầy đủ chuỗi nhật ký kiểm toán (Audit Trail) và cơ chế khóa toàn vẹn tài liệu hay không.
2. **Kỹ thuật Sinh trắc học (Dấu vân tay điện tử tại quầy):** Tiện lợi cho người cao tuổi, nhưng chủ yếu phục vụ định danh; cần kết hợp chữ ký số của hệ thống để niêm phong nội dung tài liệu.
3. **Xác thực mã OTP (FPT eHospital):** Người bệnh không cần thiết bị thông minh; tuy nhiên phát sinh chi phí tin nhắn viễn thông và phụ thuộc vào chất lượng sóng mạng tại các khu vực đặc thù (phòng mổ, tầng hầm).
4. **Xác nhận qua App VNeID (ISOFH tại BV Xanh Pôn):** Tính xác thực danh tính rất cao từ Bộ Công An; tuy nhiên đòi hỏi người bệnh phải có smartphone kết nối mạng và tài khoản VNeID Mức 2.
5. **Quét chip CCCD qua NFC (2ID tại BV Từ Dũ):** Thao tác nhanh tại quầy không cần smartphone; tuy nhiên chưa hỗ trợ trường hợp thân nhân ở xa cần ký xác nhận từ xa.
6. **Chữ ký số Chuẩn PKI cá nhân (EasyCA - SoftDreams):** Cấp chứng thư số cá nhân theo sự vụ/thời hạn ngắn lưu trên Cloud HSM; khả năng chứng minh tính toàn vẹn và xác thực chủ thể cao nhất theo Luật Giao dịch điện tử 2023; cần hoàn thiện quy trình thuê bao theo Nghị định số 23/2025/NĐ-CP.

---

## 🔗 Danh mục Báo cáo Chi tiết Từng Giải pháp

- 📊 [00 - Báo cáo Tổng quan & Bảng Ma trận 13 Tiêu chí](competitors/00-tong-quan-so-sanh.md)
- ⭐ [01 - EasyCA (SoftDreams) - Chuẩn PKI theo Nghị định 23/2025/NĐ-CP](competitors/01-easyca-softdreams.md)
- 💳 [02 - 2ID / 2Contract (Quét chip CCCD tại BV Từ Dũ)](competitors/02-2id-2contract.md)
- 📱 [03 - ISOFH (Ký qua App VNeID tại BV Xanh Pôn)](competitors/03-isofh-vneid.md)
- 🏥 [04 - Viettel HMS (Ký tay Tablet & VNeID khối BV công)](competitors/04-viettel-hms.md)
- 🌐 [05 - VNPT HIS & Dịch vụ VNPT SmartCA](competitors/05-vnpt-his.md)
- 📩 [06 - FPT eHospital (Xác thực OTP SMS & eSign)](competitors/06-fpt-ehospital.md)
- ✍️ [07 - Mô hình Ký tay Tablet Cảm ứng](competitors/07-ky-tay-tablet.md)
- 📋 [00 - Mục lục & Cấu trúc Dữ liệu](competitors/00-INDEX.md)
