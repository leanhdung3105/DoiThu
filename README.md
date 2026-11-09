# Nghiên cứu Đối thủ: Các Phương thức Ký Bệnh nhân tại Cơ sở Y tế
> **Đơn vị nghiên cứu:** Ban Giải pháp EasyCA — SoftDreams  
> **Khung pháp lý tham chiếu:** Luật Giao dịch điện tử số 20/2023/QH15, Nghị định số 23/2025/NĐ-CP, Luật Khám bệnh, chữa bệnh số 15/2023/QH15 và **Thông tư số 13/2025/TT-BYT (Điều 3)**.

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
│          khoản 4 Điều 22 Luật Giao dịch điện tử (như xác thực VNeID, OTP SMS,          │
│          hoặc ký trực tiếp trên thiết bị cảm ứng / bảng ký tại cơ sở y tế).            │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

> **Nguyên tắc đánh giá pháp lý:** Thông tư 13/2025/TT-BYT công nhận cả 3 nhóm phương thức bình đẳng theo quy định pháp luật chuyên ngành. Tuy nhiên, theo **Điều 11 Luật Giao dịch điện tử 2023**, giá trị chứng cứ của từng phương thức khi có tranh chấp sẽ được cơ quan tố tụng đánh giá dựa trên độ tin cậy của cách thức khởi tạo, lưu trữ, khả năng bảo đảm tính toàn vẹn và xác định chủ thể thực hiện.

---

## 📊 BẢNG MA TRẬN SO SÁNH CÁC GIẢI PHÁP TRÊN THỊ TRƯỜNG

| Đơn vị / Giải pháp | Phương thức ký bệnh nhân | Nhóm theo TT 13/2025 | Cơ chế Chứng minh Danh tính & Toàn vẹn | Khả năng Ký từ xa | Bệnh viện đã triển khai |
|---|---|:---:|---|:---:|---|
| **EasyCA (SoftDreams)** | **Chữ ký số PKI (Remote Signing)** | **Nhóm 1** | Cặp khóa Private/Public Key X.509 + Băm SHA-256 + Dấu thời gian TSA | ✅ Hỗ trợ qua luồng eKYC từ xa | Đang trong giai đoạn nghiên cứu & phát triển `[Chưa triển khai rộng]` |
| **2ID / 2Contract** | Quét chip CCCD (NFC) + Đối soát khuôn mặt | Nhóm 2 & Nhóm 3 | Đối soát sinh trắc 1:1 với chip CCCD + Ký số niêm phong bằng CTS Bệnh viện | ❌ Phải có mặt áp thẻ tại quầy | BV Từ Dũ `[Đã xác minh]`, BV Thanh Nhàn, Ung Bướu HN `[Có nguồn tham khảo]` |
| **ISOFH (EMR)** | Xác nhận qua Ứng dụng VNeID | Nhóm 3 | Xác thực qua tài khoản định danh điện tử Mức 2 của Bộ Công An (C06) | ⚠️ Được (nếu có smartphone và VNeID) | BV Đa khoa Xanh Pôn `[Đã xác minh]`, BV ĐK Nông nghiệp `[Có nguồn tham khảo]` |
| **Viettel HMS** | Ký cảm ứng trên Tablet / VNeID | Nhóm 3 | Ghi nhận nét vẽ kèm nhật ký phiên làm việc; hoặc xác thực VNeID | ❌ Ký tablet phải ở viện | Khối cơ sở y tế công lập toàn quốc `[Đã xác minh qua cổng đấu thầu]` |
| **VNPT HIS** | Ký qua VNeID / Tablet / SmartCA | Nhóm 3 (hoặc Nhóm 1) | Xác thực qua VNeID; hoặc cấp SmartCA (nếu người dùng có tài khoản) | ⚠️ Phụ thuộc phương thức | Hệ thống y tế cơ sở và bệnh viện tỉnh `[Đã xác minh qua cổng đấu thầu]` |
| **FPT eHospital** | Xác thực qua mã OTP SMS / Zalo | Nhóm 3 | Ghi nhận số điện thoại tiếp nhận OTP và biên lai dịch vụ viễn thông | ⚠️ Gửi OTP qua mạng viễn thông | Bệnh viện tư nhân quy mô lớn và bệnh viện tỉnh `[Đã xác minh]` |
| **Ký tay Tablet (DentalFlow...)** | Vẽ chữ ký trên màn hình cảm ứng | Nhóm 3 | Lưu ảnh nét vẽ; một số hệ thống lưu kèm tọa độ, thời gian và Device ID | ❌ Phải có mặt tại cơ sở y tế | Chuỗi nha khoa, thẩm mỹ viện, phòng khám tư `[Đã xác minh]` |

---

## 🔍 TÓM TẮT 6 PHƯƠNG THỨC KÝ TRÊN THỊ TRƯỜNG

1. **Chữ ký Cảm ứng trên Tablet (DentalFlow, Viettel HMS, các phòng khám):** Ký bằng ngón tay hoặc bút cảm ứng trên màn hình máy tính bảng. Mức độ tin cậy chứng minh phụ thuộc vào việc hệ thống có lưu trữ đầy đủ chuỗi nhật ký kiểm toán (Audit Trail) và cơ chế khóa toàn vẹn tài liệu hay không.
2. **Kỹ thuật Sinh trắc học (Dấu vân tay điện tử tại quầy):** Tiện lợi cho người cao tuổi, nhưng chủ yếu phục vụ định danh; cần kết hợp chữ ký số của hệ thống để niêm phong nội dung tài liệu.
3. **Xác thực mã OTP (FPT eHospital):** Người bệnh không cần thiết bị thông minh; tuy nhiên phát sinh chi phí tin nhắn viễn thông và phụ thuộc vào chất lượng sóng mạng tại các khu vực đặc thù (phòng mổ, tầng hầm).
4. **Xác nhận qua App VNeID (ISOFH tại BV Xanh Pôn):** Tính xác thực danh tính rất cao từ Bộ Công An; tuy nhiên đòi hỏi người bệnh phải có smartphone kết nối mạng và tài khoản VNeID Mức 2.
5. **Quét chip CCCD qua NFC (2ID tại BV Từ Dũ):** Thao tác nhanh tại quầy không cần smartphone; tuy nhiên chưa hỗ trợ trường hợp thân nhân ở xa cần ký xác nhận từ xa.
6. **Chữ ký số Chuẩn PKI cá nhân (EasyCA - SoftDreams):** Cấp chứng thư số cá nhân theo sự vụ/thời hạn ngắn lưu trên Cloud HSM; khả năng chứng minh tính toàn vẹn và xác thực chủ thể cao nhất theo Luật Giao dịch điện tử 2023; cần hoàn thiện quy trình thuê bao theo Nghị định số 23/2025/NĐ-CP.

---

## 🔗 Danh mục Báo cáo Chi tiết Từng Giải pháp

- ⭐ [01 - EasyCA (SoftDreams) - Chuẩn PKI theo Nghị định 23/2025/NĐ-CP](competitors/01-easyca-softdreams.md)
- 💳 [02 - 2ID / 2Contract (Quét chip CCCD tại BV Từ Dũ)](competitors/02-2id-2contract.md)
- 📱 [03 - ISOFH (Ký qua App VNeID tại BV Xanh Pôn)](competitors/03-isofh-vneid.md)
- 🏥 [04 - Viettel HMS (Ký tay Tablet & VNeID khối BV công)](competitors/04-viettel-hms.md)
- 🌐 [05 - VNPT HIS & SmartCA](competitors/05-vnpt-his.md)
- 📩 [06 - FPT eHospital (Xác thực OTP SMS & eSign)](competitors/06-fpt-ehospital.md)
- ✍️ [07 - Mô hình Ký tay Tablet Cảm ứng](competitors/07-ky-tay-tablet.md)
- 📋 [00 - Mục lục & Cấu trúc Dữ liệu](competitors/00-INDEX.md)
