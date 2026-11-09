---
title: "Báo cáo Tổng quan: Các Phương thức Ký Xác nhận Bệnh nhân tại Cơ sở Y tế"
description: "Phân tích khách quan các phương thức ký xác nhận của bệnh nhân/người nhà theo Thông tư 13/2025/TT-BYT, ma trận so sánh giải pháp và định vị Chữ ký số PKI của EasyCA."
last_updated: "2026-11-09"
author: "EasyCA Solution Team — SoftDreams"
---

# Báo cáo Tổng quan: Các Phương thức Ký Xác nhận Bệnh nhân tại Cơ sở Y tế

> **Tài liệu nghiên cứu chiến lược:** Phục vụ công tác hoạch định sản phẩm, định giá và tư vấn giải pháp cho khối khách hàng bệnh viện của SoftDreams.  
> **Khung pháp lý tham chiếu:** Luật Giao dịch điện tử số 20/2023/QH15, Nghị định số 23/2025/NĐ-CP, Luật Khám bệnh, chữa bệnh số 15/2023/QH15 và **Thông tư số 13/2025/TT-BYT (Điều 3)**.

---

## 1. Khung Pháp lý Tham chiếu: Điều 3 Thông tư 13/2025/TT-BYT

Trong hồ sơ bệnh án điện tử (EMR), người bệnh hoặc người đại diện hợp pháp phải ký xác nhận nhiều loại biểu mẫu: *Phiếu đồng ý phẫu thuật/thủ thuật, Cam kết sử dụng thuốc/vật tư ngoài danh mục BHYT, Giấy từ chối điều trị, Bảng kê chi phí khám chữa bệnh...*

Theo **Điều 3 Thông tư 13/2025/TT-BYT**, Bộ Y tế quy định **3 nhóm phương thức** ký hoặc xác nhận điện tử được phép áp dụng:

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

> **Lưu ý nghiệp vụ & pháp lý:** Thông tư 13/2025/TT-BYT quy định 3 nhóm phương thức bình đẳng theo quy định pháp luật chuyên ngành, không phân cấp thứ bậc hành chính. Tuy nhiên, theo **Điều 11 Luật Giao dịch điện tử 2023**, giá trị chứng cứ của từng phương thức khi có tranh chấp sẽ được cơ quan tố tụng đánh giá dựa trên **độ tin cậy của cách thức khởi tạo, lưu trữ, khả năng bảo đảm tính toàn vẹn và xác định chủ thể thực hiện** `[Căn cứ pháp lý chuẩn xác]`.

---

## 2. Bảng Ma trận So sánh Khách quan các Giải pháp trên Thị trường

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

## 3. Phân tích Kỹ thuật & Nghiệp vụ 6 Phương thức Ký Hiện nay

### 3.1 Chữ ký Cảm ứng trên Tablet (Touch / Stylus Signature)
- **Cơ chế:** Bệnh nhân vẽ chữ ký trên màn hình máy tính bảng. Phần mềm lưu trữ ảnh nét vẽ (PNG) kèm chuỗi nhật ký phiên làm việc (tọa độ, thời gian, tài khoản nhân viên y tế giám sát).
- **Ưu điểm:** Chi phí đầu tư thấp, thao tác trực quan, quy trình tiếp đón nhanh chóng.
- **Điểm cần lưu ý:** Mức độ tin cậy chứng minh phụ thuộc vào việc hệ thống có lưu trữ đầy đủ dữ liệu kiểm toán (Audit Trail) và cơ chế bảo vệ tính toàn vẹn tài liệu hay không.

### 3.2 Kỹ thuật Sinh trắc học (Dấu vân tay điện tử)
- **Cơ chế:** Quét vân tay tại quầy để trích xuất chuỗi đặc trưng (Minutiae) lưu trữ trong cơ sở dữ liệu.
- **Ưu điểm:** Thuận tiện cho người cao tuổi, người không biết chữ; không yêu cầu sở hữu thiết bị thông minh.
- **Điểm cần lưu ý:** Dấu vân tay chủ yếu phục vụ định danh người đến khám; cần kết hợp với chữ ký số của hệ thống để niêm phong nội dung tài liệu tránh việc chỉnh sửa sau thời điểm xác nhận.

### 3.3 Xác thực qua mã OTP (SMS Brandname / Zalo ZNS)
- **Cơ chế:** Gửi mã xác thực một lần về số điện thoại đăng ký; người bệnh nhập mã để xác nhận chấp thuận giao dịch.
- **Ưu điểm:** Người bệnh không cần thiết bị thông minh, sử dụng được trên điện thoại phổ thông.
- **Điểm cần lưu ý:** Bệnh viện phải chi trả chi phí tin nhắn viễn thông theo từng lượt giao dịch; chất lượng phụ thuộc vào vùng phủ sóng di động tại các khu vực đặc thù (phòng mổ, tầng hầm).

### 3.4 Xác nhận qua Ứng dụng VNeID (Đề án 06)
- **Cơ chế:** Hệ thống EMR đẩy yêu cầu xác nhận sang ứng dụng VNeID trên điện thoại bệnh nhân; bệnh nhân mở app, xác thực sinh trắc/mã khóa để xác nhận.
- **Ưu điểm:** Tính xác thực danh tính rất cao do Bộ Công An quản lý; bám sát định hướng của Đề án 06.
- **Điểm cần lưu ý:** Đòi hỏi người bệnh phải có điện thoại thông minh, có kết nối internet và đã kích hoạt tài khoản VNeID Mức 2. Quy trình có thể gặp rào cản với nhóm người bệnh cao tuổi hoặc cấp cứu.

### 3.5 Quét Thẻ CCCD gắn Chip (NFC) + Đối soát Sinh trắc (2ID / 2Contract)
- **Cơ chế:** Đọc dữ liệu từ chip thẻ CCCD qua đầu đọc NFC tại quầy tiếp đón kết hợp camera đối soát khuôn mặt 1:1; hệ thống bệnh viện ký số niêm phong tài liệu kèm hồ sơ bằng chứng.
- **Ưu điểm:** Tận dụng thẻ CCCD gắn chip vật lý sẵn có của người dân; thao tác tại quầy nhanh và chính xác.
- **Điểm cần lưu ý:** Bệnh viện cần đầu tư thiết bị đầu đọc thẻ và camera tại các quầy tiếp đón; chưa hỗ trợ được các trường hợp người nhà ở xa cần ký xác nhận từ xa.

### 3.6 Chữ ký số Chuẩn PKI cá nhân (Mô hình EasyCA đề xuất)
- **Cơ chế:** Định danh người bệnh qua eKYC (quét CCCD chip/sinh trắc khuôn mặt) ➔ Cấp chứng thư số cá nhân theo sự vụ/thời hạn ngắn lưu trên Remote Signing / Cloud HSM ➔ Bệnh nhân xác thực lệnh ký ➔ Dùng khóa bí mật ký số PAdES, tạo mã băm SHA-256 niêm phong tài liệu và đóng dấu thời gian TSA.
- **Ưu điểm vượt trội:** Đạt chuẩn Nhóm 1 theo Thông tư 13/2025/TT-BYT; khả năng chứng minh tính toàn vẹn và xác thực chủ thể cao nhất theo Luật Giao dịch điện tử 2023; hỗ trợ linh hoạt cả tại quầy, tại giường bệnh và ký từ xa.
- **Thách thức:** Cần thiết kế quy trình thỏa thuận thuê bao và cấp chứng thư số tinh gọn, tuân thủ chặt chẽ **Nghị định số 23/2025/NĐ-CP** để không làm chậm luồng tiếp đón bệnh nhân.

---

## 4. Vai trò của Nhóm Đối thủ Trung gian (HIS/EMR Vendors & System Integrators)

Trong thị trường y tế số, quyết định lựa chọn giải pháp ký số của Bệnh viện chịu ảnh hưởng quyết định bởi **Nhà cung cấp phần mềm HIS/EMR hiện hữu**:

```
┌────────────────────────────────────────────────────────────────────────┐
│                     HỆ THỐNG Y TẾ BỆNH VIỆN                            │
│  [Ban Giám đốc] ──► [Phòng CNTT] ──► [Phòng Kế hoạch Tổng hợp]         │
└───────────────────────────────────┬────────────────────────────────────┘
                                    │
       ┌────────────────────────────┴───────────────────────────┐
       ▼                                                        ▼
┌───────────────────────────────┐      ┌───────────────────────────────┐
│  NHÀ PHÁT TRIỂN HIS / EMR     │      │  NHÀ CUNG CẤP DỊCH VỤ TIN CẬY │
│  (VNPT, Viettel, FPT, ISOFH,  │◄────►│  (EasyCA, VNPT-CA, Viettel-CA,│
│   Infomed, Nanosoft, LinkCare)│ (API)│   FPT-CA, Bkav-CA, 2ID...)    │
└───────────────────────────────┘      └───────────────────────────────┘
```

1. **Khả năng chi phối của nhà thầu HIS:** Bệnh viện rất ngại can thiệp vào mã nguồn phần mềm quản lý đang vận hành ổn định. Nếu nhà cung cấp CA không phối hợp được với đơn vị HIS để mở cổng kết nối API, giải pháp ký số gần như không thể triển khai trên thực tế.
2. **Chiến lược tiếp cận đúng đắn cho EasyCA:**
   - Xây dựng tài liệu kỹ thuật tích hợp (Open API / SDK) chuẩn hóa, dễ dàng kết nối.
   - Thiết lập quan hệ đối tác chiến lược với các công ty phần mềm HIS độc lập (như Nanosoft, Infomed, LinkCare, ISOFH...) theo mô hình chia sẻ doanh thu lượt ký (Revenue Sharing), biến họ thành kênh phân phối giải pháp EasyCA.

---

## 5. Danh mục Báo cáo Chi tiết Từng Giải pháp

1. [**01-easyca-softdreams.md**](01-easyca-softdreams.md) — Phân tích Kiến trúc Giải pháp EasyCA PKI theo Nghị định 23/2025/NĐ-CP
2. [**02-2id-2contract.md**](02-2id-2contract.md) — Đánh giá Giải pháp Quét chip CCCD 2ID / 2Contract tại BV Từ Dũ
3. [**03-isofh-vneid.md**](03-isofh-vneid.md) — Phân tích Giải pháp Ký qua App VNeID của ISOFH tại BV Xanh Pôn
4. [**04-viettel-hms.md**](04-viettel-hms.md) — Đánh giá Hệ sinh thái Viettel HMS & Chữ ký số Viettel-CA
5. [**05-vnpt-his.md**](05-vnpt-his.md) — Đánh giá Hệ sinh thái VNPT HIS & Chữ ký số VNPT SmartCA
6. [**06-fpt-ehospital.md**](06-fpt-ehospital.md) — Phân tích Giải pháp Xác thực OTP & eSign trên FPT eHospital
7. [**07-ky-tay-tablet.md**](07-ky-tay-tablet.md) — Phân tích Kỹ thuật & Khung Pháp lý Mô hình Chữ ký Tablet Cảm ứng
