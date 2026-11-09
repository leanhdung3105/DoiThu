---
title: "Hồ sơ Đối thủ: 2ID / 2Contract — Mô hình Doanh nghiệp Tích hợp Công nghệ Xác thực"
vendor: "Công ty Cổ phần Chuyển đổi số 2ID"
product: "2Contract (Nền tảng ký hợp đồng điện tử & xác thực định danh số)"
signing_method: "Xác thực danh tính qua thẻ CCCD gắn chip (NFC), sinh trắc khuôn mặt & niêm phong tài liệu"
tt13_category: "Nhóm 2 (Sinh trắc học) & Nhóm 3 (Xác nhận điện tử khác theo K4 Đ22 Luật GDĐT)"
role: "Doanh nghiệp cung cấp giải pháp công nghệ (ISV) & Đơn vị tích hợp hệ thống (SI)"
last_updated: "2026-11-09"
verification_status: "Đã xác minh tư cách pháp nhân và trúng thầu tại BV Từ Dũ; Chưa xác minh đầy đủ tính năng lâm sàng trên toàn viện"
---

# Hồ sơ Đối thủ: 2ID / 2Contract — Mô hình Doanh nghiệp Tích hợp Công nghệ Xác thực

---

## 1. Thông tin Doanh nghiệp & Vị thế trong Chuỗi Giá trị

### 1.1 Thông tin Pháp nhân & Vai trò
- **Tên doanh nghiệp:** Công ty Cổ phần Chuyển đổi số 2ID `[Đã xác minh]`.
- **Sản phẩm cốt lõi:** 2Contract (Nền tảng ký hợp đồng điện tử, quản trị tài liệu số), giải pháp phần cứng và phần mềm đọc thẻ Căn cước công dân gắn chip `[Đã xác minh qua website 2id.vn và 2contract.vn]`.
- **Bản chất vai trò trong chuỗi cung ứng:**
  - 2ID **không phải là Tổ chức cung cấp dịch vụ chứng thực chữ ký số công cộng (CA)** `[Đã xác minh: Không có tên trong danh bạ CA công cộng do NEAC cấp phép]`.
  - 2ID đóng vai trò là **Doanh nghiệp cung cấp giải pháp công nghệ (ISV) và Nhà tích hợp hệ thống trung gian (System Integrator)**: Kết nối Bệnh viện, phần mềm HIS/EMR, thiết bị đầu đọc thẻ, dịch vụ CA bên ngoài, thiết bị HSM và các nền tảng xác thực định danh `[Nhận định chuyên môn]`.

### 1.2 Mối quan hệ Đối tác & Nền tảng Công nghệ
- 2ID quảng bá các giải pháp ứng dụng thiết bị đọc thẻ CCCD gắn chip chuẩn ICAO Doc 9303 và kết nối tiện ích dữ liệu dân cư theo tinh thần Đề án 06 của Chính phủ `[Có nguồn tham khảo từ truyền thông của doanh nghiệp]`.

---

## 2. Sản phẩm & Cơ chế Công nghệ Thực tế

Để đánh giá chính xác giải pháp của 2ID, cần phân biệt rõ 5 cấu phần kỹ thuật độc lập trong quy trình xử lý tài liệu tại bệnh viện:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ [1. ĐỊNH DANH NGƯỜI BỆNH (IDENTITY VERIFICATION)]                                     │
│     Đọc dữ liệu từ chip thẻ CCCD qua giao tiếp không tiếp xúc (NFC). Dữ liệu đọc      │
│     thông thường gồm: Vùng dữ liệu nhân thân (DG1) và Ảnh chân dung (DG2) chuẩn ICAO. │
└───────────────────────────────────┬────────────────────────────────────────────────────┘
                                    │
                                    ▼
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ [2. XÁC THỰC NGƯỜI THỰC HIỆN (AUTHENTICATION)]                                        │
│     Camera tại quầy thu nhận ảnh chân dung trực tiếp và đối soát sinh trắc học 1:1    │
│     (Face Matching) với ảnh gốc trích xuất từ chip thẻ CCCD để bảo đảm chính chủ.      │
└───────────────────────────────────┬────────────────────────────────────────────────────┘
                                    │
                                    ▼
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ [3. GHI NHẬN SỰ ĐỒNG Ý (CONSENT RECORDING)]                                           │
│     Người bệnh/người nhà xem nội dung tài liệu (phiếu mổ, cam kết) trên màn hình phụ   │
│     tại quầy và bấm nút xác nhận chấp thuận trên giao diện phần mềm 2Contract.         │
└───────────────────────────────────┬────────────────────────────────────────────────────┘
                                    │
                                    ▼
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ [4. KÝ SỐ NIÊM PHONG TÀI LIỆU (DOCUMENT SEALING)]                                      │
│     Tài liệu PDF được ký số niêm phong bằng Chứng thư số của BỆNH VIỆN hoặc nhà        │
│     cung cấp giải pháp qua HSM. (Người bệnh KHÔNG ký bằng chữ ký số PKI cá nhân).      │
└───────────────────────────────────┬────────────────────────────────────────────────────┘
                                    │
                                    ▼
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ [5. LƯU TRỮ BẰNG CHỨNG (AUDIT TRAIL LOGGING)]                                         │
│     Hệ thống lưu trữ chuỗi dữ liệu kiểm toán gồm: mã thẻ, dấu thời gian, ảnh chụp     │
│     thời điểm bấm xác nhận, kết quả so khớp sinh trắc và liên kết vào hồ sơ bệnh án.   │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

- **Lưu ý kỹ thuật quan trọng:**
  - Việc quét chip CCCD và so khớp khuôn mặt thành công **chỉ giải quyết khâu Định danh và Xác thực người bệnh**.
  - Nó **không đồng nghĩa với việc người bệnh đã tạo ra một Chữ ký số PKI cá nhân** theo quy định của Luật Giao dịch điện tử. Chữ ký số được gắn vào tài liệu thực chất là chữ ký số của tổ chức (Bệnh viện) để niêm phong văn bản sau khi đã ghi nhận sự chấp thuận của người bệnh.

---

## 3. Căn cứ Pháp lý & Giá trị Chứng cứ

### 3.1 Căn cứ theo Thông tư 13/2025/TT-BYT & Luật Giao dịch điện tử 2023
- **Phân nhóm theo Thông tư 13/2025/TT-BYT:**
  - Phần đối soát khuôn mặt thuộc **Nhóm 2: Sử dụng kỹ thuật sinh trắc học** (khoản 2 Điều 3).
  - Phần người bệnh bấm xác nhận trên màn hình thuộc **Nhóm 3: Các hình thức xác nhận bằng phương tiện điện tử khác** theo quy định tại khoản 4 Điều 22 Luật Giao dịch điện tử số 20/2023/QH15 (khoản 3 Điều 3).
- **Phân định giá trị pháp lý theo Điều 23 Luật GDĐT 2023:**
  - Theo *Khoản 1 Điều 23:* Hình thức xác nhận điện tử của người bệnh qua 2Contract không bị phủ nhận giá trị pháp lý chỉ vì được thể hiện dưới dạng điện tử.
  - Tuy nhiên, hình thức này **không thuộc phạm vi Khoản 2 Điều 23** (chữ ký số đáp ứng điều kiện an toàn có giá trị tương đương chữ ký tay của cá nhân), do người bệnh không trực tiếp sở hữu chứng thư số và khóa bí mật cá nhân tương ứng.
- **Giá trị chứng cứ theo Điều 11 Luật GDĐT 2023:**
  - Giá trị chứng minh trước cơ quan tố tụng khi xảy ra tranh chấp phụ thuộc hoàn toàn vào **tính toàn vẹn của chuỗi nhật ký kiểm toán (Audit Trail)** do Bệnh viện và 2ID lưu trữ. Nếu Bệnh viện chứng minh được dữ liệu ảnh chụp, dấu thời gian và log hệ thống không bị can thiệp sau thời điểm ghi nhận, tài liệu có giá trị chứng cứ rất đáng tin cậy.

### 3.2 Tuân thủ Pháp luật về Bảo vệ Dữ liệu Cá nhân
- **Luật Bảo vệ dữ liệu cá nhân số 91/2025/QH15 và Nghị định số 356/2025/NĐ-CP:**
  - Ảnh chân dung trong chip CCCD và ảnh camera đối soát thuộc phạm vi **dữ liệu sinh trắc học** (Điều 31 Luật 91/2025/QH15).
  - Hồ sơ bệnh án liên kết là **dữ liệu liên quan đến sức khỏe** (Điều 26 Luật 91/2025/QH15).
  - 2ID và Bệnh viện phải bảo đảm: Chỉ thu thập dữ liệu theo đúng mục đích khám chữa bệnh đã được người bệnh đồng ý; không được phép lưu trữ dữ liệu sinh trắc học thô trên máy chủ ngoài phạm vi hợp đồng; phải thực hiện đánh giá tác động xử lý dữ liệu cá nhân theo luật định.

---

## 4. Khách hàng & Triển khai Thực tế: Phân định Bằng chứng

Để tránh nhầm lẫn giữa thông tin thương mại và hiện trạng vận hành, bảng dưới đây phân định rõ các nguồn thông tin:

| Cơ sở Y tế | Thông tin từ Hồ sơ Đấu thầu | Thông tin Doanh nghiệp / Truyền thông công bố | Đánh giá Hiện trạng Triển khai Thực tế |
|---|---|---|---|
| **Bệnh viện Từ Dũ (TP.HCM)** | `[Đã xác minh]` 2ID tham gia / trúng thầu gói thầu *"Trang bị chữ ký số HSM triển khai hồ sơ bệnh án điện tử"* tại Bệnh viện Từ Dũ (năm 2023–2024). | `[Có nguồn tham khảo]` Báo Sức khỏe & Đời sống và Cổng TTĐT Sở Y tế TP.HCM đăng bài về ứng dụng CCCD gắn chip trong quy trình khám và làm thủ tục phẫu thuật. | `[Nhận định]` Có triển khai thiết bị xác thực thẻ CCCD tại một số quầy tiếp đón/khoa điều trị; tuy nhiên phạm vi áp dụng cho 100% bệnh nhân nội trú hay chỉ một nhóm thủ tục cụ thể cần kiểm tra thực tế thêm. |
| **Bệnh viện Thanh Nhàn (Hà Nội)** | `[Chưa xác minh qua hồ sơ thầu]` | `[Có nguồn công bố từ 2ID]` Đưa tin về việc hợp tác ứng dụng giải pháp định danh xác thực. | `[Chưa xác minh bằng chứng triển khai lâm sàng]` |
| **Bệnh viện Ung Bướu Hà Nội** | `[Chưa xác minh qua hồ sơ thầu]` | `[Có nguồn công bố từ 2ID]` Giới thiệu thí điểm giải pháp xác thực CCCD. | `[Chưa xác minh bằng chứng triển khai lâm sàng]` |
| **Bệnh viện Nhi đồng Cần Thơ** | `[Chưa xác minh qua hồ sơ thầu]` | `[Chưa có nguồn xác minh độc lập]` Chỉ có thông tin tham khảo nội bộ. | `[Chưa xác minh]` |

---

## 5. Đánh giá Mô hình Kinh doanh & Khả năng Cạnh tranh vs EasyCA

### 5.1 Ưu thế & Rủi ro của Mô hình "Doanh nghiệp Tích hợp Trung gian" (Integrator Model)
- **Ưu thế cạnh tranh của 2ID:**
  - *Tính linh hoạt cao:* Không bị bó buộc vào hạ tầng CA riêng, 2ID có thể mua HSM của hãng phần cứng độc lập, tích hợp dịch vụ CA của bất kỳ nhà cung cấp nào trên thị trường để chào gói thầu trọn gói cho bệnh viện.
  - *Tập trung mạnh vào trải nghiệm tiếp đón:* Giải pháp tập trung tối ưu thao tác tại quầy (đặt thẻ CCCD, chụp mặt trong vài giây), đánh trúng nhu cầu giảm ùn tắc hành chính của các bệnh viện lớn.
- **Rủi ro cốt tử của mô hình trung gian:**
  - *Phụ thuộc đối tác thứ ba:* Phụ thuộc vào nhà cung cấp thiết bị phần cứng (đầu đọc NFC, camera), nhà cung cấp CA (để cấp chữ ký số tổ chức) và chính sách kết nối dữ liệu của cơ quan quản lý.
  - *Biên lợi nhuận và trách nhiệm pháp lý:* Đơn vị trung gian thường có biên lợi nhuận mỏng hơn các nhà cung cấp CA trực tiếp; khi xảy ra sự cố bảo mật dữ liệu hoặc lỗi chữ ký số, trách nhiệm pháp lý giữa Nhà thầu tích hợp, Bệnh viện và Nhà cấp CA rất phức tạp.

### 5.2 Điểm hạn chế trong Quy trình Ký của 2ID
1. **Không hỗ trợ ký từ xa (Remote Signing cho người nhà ở xa):** Bắt buộc người bệnh/người nhà phải có mặt trực tiếp tại quầy để áp thẻ CCCD vật lý vào đầu đọc. Trường hợp người nhà bệnh nhân ở xa cần ký bảo lãnh mổ khẩn cấp thì mô hình của 2ID không đáp ứng được.
2. **Chi phí trang bị phần cứng tại chỗ:** Bệnh viện phải đầu tư mua sắm đầu đọc thẻ NFC chuyên dụng và camera tại từng bàn làm việc/quầy tiếp đón. Khó triển khai linh hoạt tại buồng bệnh nội trú nếu không có xe tiêm/thiết bị di động gắn đầu đọc.
3. **Bản chất pháp lý không phải là Chữ ký số cá nhân:** Chữ ký số trên tài liệu là của Bệnh viện; người bệnh không sở hữu cặp khóa riêng nên mức độ độc lập chứng cứ không cao bằng mô hình chữ ký số PKI Nhóm 1.

### 5.3 So sánh Cạnh tranh Trực diện với EasyCA

| Tiêu chí Đánh giá | 2ID / 2Contract | EasyCA (SoftDreams) |
|---|---|---|
| **Vai trò doanh nghiệp** | Đơn vị tích hợp giải pháp / ISV | Nhà cung cấp dịch vụ tin cậy công cộng (CA) |
| **Nhóm phương thức TT 13** | Nhóm 2 (Sinh trắc) & Nhóm 3 (Xác nhận điện tử) | Nhóm 1 (Chữ ký điện tử hợp pháp / Chữ ký số PKI) |
| **Chủ thể sở hữu khóa ký** | Bệnh viện ký số niêm phong bằng chứng thư số tổ chức | Bệnh nhân sở hữu khóa bí mật cá nhân trong Cloud HSM |
| **Ký từ xa (người nhà ở xa)** | Không hỗ trợ (bắt buộc có mặt tại viện áp thẻ chip) | Hỗ trợ qua luồng eKYC từ xa trên thiết bị di động |
| **Đầu tư phần cứng ban đầu** | Bắt buộc mua đầu đọc NFC + Camera cho từng quầy | Tận dụng thiết bị sẵn có (Web, Tablet, Smartphone) |
| **Khả năng hợp tác** | Đối tác tích hợp tiềm năng (2ID có thể tích hợp EasyCA) | Có thể cung cấp CA/Remote Signing nền tảng cho 2ID |

---

## 6. Nguồn Tham khảo & Bằng chứng Xác thực
1. Hệ thống Mạng đấu thầu Quốc gia (`muasamcong.mpi.gov.vn`) — Thông tin gói thầu "Trang bị chữ ký số HSM triển khai hồ sơ bệnh án điện tử" tại Bệnh viện Từ Dũ.
2. Cổng thông tin điện tử Sở Y tế TP. Hồ Chí Minh — Chuyên mục chuyển đổi số bệnh viện và Đề án 06.
3. Website chính thức Công ty CP Chuyển đổi số 2ID: `2id.vn` và nền tảng `2contract.vn`.
4. Danh mục Tổ chức cung cấp dịch vụ chứng thực chữ ký số công cộng — Trung tâm Chứng thực điện tử quốc gia (NEAC).
5. Luật Giao dịch điện tử số 20/2023/QH15 và Thông tư số 13/2025/TT-BYT.
6. Luật Bảo vệ dữ liệu cá nhân số 91/2025/QH15 và Nghị định số 356/2025/NĐ-CP.
