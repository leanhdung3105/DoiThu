---
title: "2ID / 2Contract — Giải pháp Xác thực & Ký Xác nhận bằng Thẻ CCCD gắn Chip"
vendor: "Công ty Cổ phần Chuyển đổi số 2ID"
product: "2Contract (Nền tảng ký hợp đồng điện tử & xác thực danh tính)"
signing_method: "Quét chip CCCD (NFC) + Đối soát sinh trắc học khuôn mặt"
tt13_category: "Nhóm 2 (Sinh trắc học) & Nhóm 3 (Phương tiện điện tử khác theo K4 Đ22 Luật GDĐT)"
role: "Nhà cung cấp giải pháp công nghệ / Đơn vị tích hợp"
last_updated: "2026-11-09"
---

# 2ID / 2Contract — Giải pháp Xác thực & Ký Xác nhận qua Thẻ CCCD gắn Chip

---

## 1. Thông tin Doanh nghiệp & Vị thế
- **Tên pháp nhân:** Công ty Cổ phần Chuyển đổi số 2ID `[Đã xác minh]`.
- **Sản phẩm:** 2Contract — Nền tảng ký hợp đồng và tài liệu điện tử, giải pháp đọc và xác thực thẻ CCCD gắn chip tích hợp hệ thống y tế `[Đã xác minh]`.
- **Vai trò trong chuỗi cung ứng Y tế:** Đơn vị cung cấp giải pháp công nghệ (ISV) và nhà tích hợp thiết bị; không trực tiếp là Tổ chức cung cấp dịch vụ chứng thực chữ ký số công cộng (CA) `[Đã xác minh: 2ID không nằm trong danh mục CA công cộng do NEAC công bố]`.
- **Đối tác liên quan:** Hợp tác triển khai các giải pháp ứng dụng tiện ích từ Đề án 06 và thiết bị xác thực thẻ CCCD gắn chip chuẩn ICAO `[Có nguồn tham khảo qua truyền thông doanh nghiệp]`.

---

## 2. Sản phẩm & Cơ chế Công nghệ

Để đánh giá chính xác giải pháp 2ID/2Contract, cần phân tách bạch 5 thành phần nghiệp vụ riêng biệt:

```
[1. ĐỊNH DANH NGƯỜI BỆNH]
   Quét chip CCCD (NFC) ➔ Đọc dữ liệu nhân thân (DG1) & ảnh chân dung (DG2) chuẩn ICAO 9303.
         │
         ▼
[2. XÁC THỰC NGƯỜI THỰC HIỆN]
   Camera đối soát sinh trắc học khuôn mặt 1:1 (Face Matching) giữa người đứng trước quầy 
   và ảnh gốc trích xuất từ chip CCCD.
         │
         ▼
[3. GHI NHẬN SỰ ĐỒNG Ý (CONSENT)]
   Người bệnh/người nhà xem nội dung tài liệu trên màn hình phụ tại quầy tiếp đón 
   và bấm xác nhận chấp thuận cam kết / thủ tục.
         │
         ▼
[4. KÝ SỐ NIÊM PHONG TÀI LIỆU]
   Tài liệu PDF được ký số niêm phong bằng Chứng thư số của BỆNH VIỆN hoặc tổ chức cung cấp dịch vụ. 
   (Bệnh nhân không được cấp chứng thư số PKI cá nhân riêng biệt).
         │
         ▼
[5. LƯU TRỮ BẰNG CHỨNG (AUDIT TRAIL)]
   Hệ thống lưu trữ gói bằng chứng điện tử gồm: mã thẻ, thời gian giao dịch, log so khớp sinh trắc, 
   ảnh chụp thời điểm xác nhận, gắn liền với tài liệu đã niêm phong.
```

- **Công nghệ đọc thẻ:** Thiết bị đầu đọc thẻ chuyên dụng hỗ trợ giao tiếp không tiếp xúc (NFC) đọc dữ liệu từ chip thẻ Căn cước công dân `[Đã xác minh]`.
- **Công nghệ sinh trắc:** Thuật toán so khớp khuôn mặt 1:1 giữa khuôn mặt chụp thực tế và dữ liệu ảnh lưu trong chip `[Đã xác minh]`.
- **Khả năng tích hợp HIS/EMR:** Cung cấp API / SDK kết nối với phần mềm quản lý bệnh viện tại khâu tiếp đón và lập phiếu phẫu thuật/thủ thuật `[Có nguồn tham khảo]`.

---

## 3. Căn cứ Pháp lý & Giá trị Chứng cứ

- **Phân nhóm theo Thông tư 13/2025/TT-BYT:** 
  - Thuộc **Nhóm 2: Kỹ thuật sinh trắc học** (đối soát khuôn mặt).
  - Kết hợp **Nhóm 3: Các hình thức xác nhận bằng phương tiện điện tử khác** theo khoản 4 Điều 22 Luật Giao dịch điện tử số 20/2023/QH15.
- **Căn cứ pháp lý áp dụng:**
  - Luật Giao dịch điện tử số 20/2023/QH15 (Điều 22 khoản 4 quy định về phương tiện điện tử khác thể hiện sự chấp thuận của chủ thể ký).
  - Thông tư số 13/2025/TT-BYT (Điều 3).
  - Nghị định số 59/2022/NĐ-CP và Luật Căn cước số 26/2023/QH15 liên quan đến khai thác thông tin trên thẻ Căn cước.
- **Đánh giá giá trị chứng cứ:**
  - Việc quét thẻ chip và đối soát sinh trắc học đem lại **độ tin cậy định danh rất cao**, hạn chế tối đa tình trạng mượn thẻ BHYT hoặc mạo danh người bệnh.
  - Về mặt chứng cứ, hồ sơ được bảo vệ bằng chuỗi nhật ký kiểm toán (Audit Trail) kết hợp chữ ký số của cơ sở khám chữa bệnh. 
  - *Hạn chế pháp lý:* Do người bệnh không sử dụng chữ ký số cá nhân (PKI) với cặp khóa riêng của mình, việc chứng minh tính chấp thuận độc lập của cá nhân phụ thuộc vào tính toàn vẹn của hệ thống ghi nhận bằng chứng do bệnh viện và đơn vị giải pháp quản lý `[Nhận định chuyên môn]`.

---

## 4. Khách hàng & Triển khai Thực tế

| Cơ sở Y tế | Nội dung triển khai | Tình trạng | Nguồn xác minh |
|---|---|---|---|
| **Bệnh viện Từ Dũ (TP.HCM)** | Ứng dụng CCCD gắn chip xác thực bệnh nhân và ký cam kết phẫu thuật/thủ thuật sản khoa | Đã triển khai thực tế | Cổng thông tin Sở Y tế TP.HCM, Báo Sức khỏe & Đời sống `[Đã xác minh]` |
| **Bệnh viện Thanh Nhàn (Hà Nội)** | Ứng dụng giải pháp xác thực CCCD gắn chip trong quy trình khám chữa bệnh | Có thông tin hợp tác | Website và thông cáo của doanh nghiệp `[Có nguồn tham khảo]` |
| **Bệnh viện Ung Bướu Hà Nội** | Thí điểm tiện ích định danh xác thực điện tử | Thí điểm | Truyền thông doanh nghiệp `[Có nguồn tham khảo]` |
| **Bệnh viện Nhi đồng Cần Thơ** | Tìm hiểu / Thí điểm giải pháp xác thực | Thí điểm | Báo cáo nội bộ ngành `[Chưa xác minh độc lập]` |

---

## 5. Đánh giá Cạnh tranh vs EasyCA

### 5.1 Điểm mạnh của 2ID
- **Trải nghiệm người bệnh rất thuận tiện:** Người bệnh chỉ cần mang thẻ CCCD gắn chip — giấy tờ bắt buộc khi đi khám bệnh; không cần sở hữu smartphone, không cần cài đặt ứng dụng hay nhớ mật khẩu.
- **Tốc độ xử lý tại quầy nhanh:** Thao tác đọc thẻ và so khớp khuôn mặt diễn ra trong thời gian ngắn, phù hợp với lưu lượng bệnh nhân đông tại các bệnh viện tuyến đầu.
- **Đã có case study điển hình:** Việc triển khai thực tế tại Bệnh viện Từ Dũ là minh chứng tham chiếu có sức nặng khi tiếp cận các bệnh viện sản - nhi và ngoại khoa.

### 5.2 Điểm yếu & Rào cản Vận hành
- **Chi phí đầu tư phần cứng tại chỗ:** Bệnh viện phải trang bị đầu đọc thẻ NFC và camera nhận diện tại từng bàn tiếp đón, phòng khám, quầy viện phí (chi phí mua sắm thiết bị ban đầu đáng kể).
- **Hạn chế ký tại buồng bệnh:** Thiết bị đầu đọc kết nối máy tính để bàn khó di chuyển linh hoạt khi bác sĩ đi buồng thăm khám tại giường bệnh nội trú.
- **Không hỗ trợ ký từ xa:** Khi người bệnh cấp cứu mà thân nhân/người đại diện hợp pháp ở xa (ở tỉnh khác hoặc nước ngoài), mô hình bắt buộc áp thẻ vật lý vào đầu đọc tại viện hoàn toàn không thể thực hiện được.

### 5.3 So sánh Cạnh tranh trực diện

| Tiêu chí | 2ID / 2Contract | EasyCA PKI (SoftDreams) |
|---|---|---|
| **Phương thức ký chính** | Xác nhận qua CCCD chip + Sinh trắc học khuôn mặt | Chữ ký số công cộng PKI (Remote Signing) |
| **Phân nhóm TT 13/2025** | Nhóm 2 & Nhóm 3 | Nhóm 1 (Chữ ký điện tử hợp pháp) |
| **Chủ thể ký số tài liệu** | Chứng thư số của Bệnh viện / Tổ chức | Bệnh nhân ký bằng Private Key riêng của mình |
| **Yêu cầu đối với bệnh nhân** | Bắt buộc có thẻ CCCD gắn chip vật lý tại quầy | Linh hoạt: CCCD tại quầy hoặc Smartphone từ xa |
| **Ký từ xa (người nhà ở xa)** | Không hỗ trợ (phải có mặt tại viện) | Hỗ trợ qua luồng eKYC từ xa |
| **Đầu tư phần cứng ban đầu** | Bắt buộc mua đầu đọc NFC + Camera cho từng quầy | Tận dụng thiết bị sẵn có (Tablet, Smartphone, Web) |

---

## 6. Nguồn Tham khảo
1. Cổng thông tin điện tử Sở Y tế TP. Hồ Chí Minh — Bài viết về ứng dụng CCCD gắn chip tại BV Từ Dũ.
2. Báo Sức khỏe & Đời sống (Cơ quan ngôn luận Bộ Y tế) — Chuyên đề chuyển đổi số bệnh án điện tử.
3. Website chính thức Công ty CP Chuyển đổi số 2ID: `2id.vn` và `2contract.vn`.
4. Danh mục Tổ chức cung cấp dịch vụ chứng thực chữ ký số công cộng — Trung tâm Chứng thực điện tử quốc gia (NEAC).
5. Tiêu chuẩn ICAO Doc 9303 (Machine Readable Travel Documents) áp dụng trên thẻ Căn cước công dân gắn chip.
