---
title: "Hồ sơ Giải pháp: EasyCA (SoftDreams) — Ứng dụng Chữ ký số Chuẩn PKI trong Bệnh viện"
vendor: "Công ty Cổ phần Đầu tư Công nghệ và Thương mại SoftDreams"
product: "Dịch vụ chứng thực chữ ký số công cộng EasyCA & Nền tảng Ký số từ xa (Remote Signing)"
signing_method: "Chữ ký số công cộng theo chuẩn PKI (Public Key Infrastructure)"
tt13_category: "Nhóm 1: Chữ ký điện tử hợp pháp (Khoản 1 Điều 3 Thông tư 13/2025/TT-BYT)"
role: "Tổ chức cung cấp dịch vụ chứng thực chữ ký số công cộng (Public CA)"
last_updated: "2026-11-09"
verification_status: "Đã xác minh năng lực CA; Chưa xác minh triển khai thực tế tại bệnh viện"
---

# Hồ sơ Giải pháp: EasyCA (SoftDreams) — Ứng dụng Chữ ký số Chuẩn PKI trong Bệnh viện

---

## 1. Thông tin Doanh nghiệp & Năng lực Cung cấp Dịch vụ

### 1.1 Thông tin Pháp nhân & Giấy phép Hoạt động
- **Tên doanh nghiệp:** Công ty Cổ phần Đầu tư Công nghệ và Thương mại SoftDreams `[Đã xác minh]`.
- **Thương hiệu dịch vụ:** EasyCA, EasyInvoice (Hóa đơn điện tử), EasyBooks (Kế toán), EasyPIT (Khấu trừ thuế TNCN).
- **Giấy phép hoạt động dịch vụ tin cậy:**
  1. *Giấy phép số 61/GP-BTTTT* do Bộ Thông tin và Truyền thông cấp ngày 21/02/2020: Cung cấp dịch vụ chứng thực chữ ký số công cộng theo mô hình thiết bị phần cứng (USB Token), thời hạn cấp phép được công bố đến ngày 20/02/2030 `[Đã xác minh theo danh bạ NEAC]`.
  2. *Giấy phép số 82/GP-BTTTT* do Bộ Thông tin và Truyền thông cấp ngày 14/03/2023: Cung cấp dịch vụ chứng thực chữ ký số công cộng theo mô hình ký số từ xa (Remote Signing), thời hạn cấp phép được công bố đến ngày 13/03/2033 `[Đã xác minh theo danh bạ NEAC]`.

### 1.2 Phân định Năng lực Thực tế trong Ngành Y tế
Để đánh giá khách quan năng lực tiếp cận thị trường bệnh viện, cần phân tách bạch 6 cấp độ năng lực của SoftDreams:
- **Năng lực CA công cộng:** `[Đã xác minh]` Có đầy đủ cơ sở pháp lý và hạ tầng khóa công khai quốc gia do NEAC kiểm định và cấp phép.
- **Năng lực Ký số từ xa (Remote Signing):** `[Đã xác minh]` Có giấy phép số 82/GP-BTTTT và hạ tầng phần cứng HSM quản lý khóa tập trung.
- **Năng lực Định danh điện tử (eKYC):** `[Đã xác minh một phần]` Có kinh nghiệm triển khai đối soát CCCD, OCR và nhận diện khuôn mặt trong các dịch vụ số; tuy nhiên luồng eKYC tích hợp sâu vào quy trình khám chữa bệnh tại quầy đón tiếp đang trong giai đoạn chuẩn hóa.
- **Năng lực Tích hợp phần mềm Bệnh viện (HIS/EMR):** `[Chưa xác minh]` Chưa có bằng chứng về việc EasyCA đã hoàn tất tích hợp chuẩn hóa vào các hệ thống HIS/EMR lớn trên thị trường (VNPT HIS, Viettel HMS, ISOFH EMR...).
- **Năng lực Triển khai Quy trình Ký Bệnh nhân lâm sàng:** `[Chưa xác minh dự án thực tế]` Chưa có hồ sơ công khai về việc vận hành quy trình ký số cho bệnh nhân nội trú/ngoại trú tại cơ sở y tế cụ thể.
- **Năng lực Vận hành & Hỗ trợ kỹ thuật tại Bệnh viện:** `[Nhận định]` Có đội ngũ chăm sóc khách hàng doanh nghiệp quy mô lớn, nhưng chưa có kinh nghiệm xử lý các tình huống nghiệp vụ y tế đặc thù (cấp cứu khẩn cấp, bệnh nhân không có năng lực hành vi dân sự, chuyển viện).

---

## 2. Sản phẩm & Kiến trúc Kỹ thuật Đề xuất cho Bệnh viện

### 2.1 Chuẩn hóa Khái niệm & Quy trình Kỹ thuật Ký số PKI
Chữ ký số (Digital Signature) là một dạng chữ ký điện tử sử dụng thuật toán khóa không đối xứng. Quy trình ký số kỹ thuật chuẩn diễn ra theo các bước sau:

```
[Tài liệu / Bệnh án điện tử cần ký]
                 │
                 ▼
1. BĂM DỮ LIỆU (HASHING):
   Tính giá trị băm (Hash Digest) của tài liệu bằng thuật toán an toàn (SHA-256). 
   (Lưu ý: Hàm băm tạo chuỗi đại diện duy nhất, không có chức năng mã hóa bảo mật nội dung).
                 │
                 ▼
2. TẠO CHỮ KÝ SỐ (SIGNING):
   Khóa bí mật (Private Key) của người ký được sử dụng để thực hiện phép toán mật mã 
   tạo chữ ký số trên giá trị băm.
                 │
                 ▼
3. ĐÓNG GÓI CHỨNG THƯ & DẤU THỜI GIAN:
   Chữ ký số được gắn vào tài liệu cùng với Chứng thư số X.509 của người ký 
   và Dấu thời gian (Timestamp) do Tổ chức cấp dấu thời gian (TSA) chứng nhận (Chuẩn PAdES).
                 │
                 ▼
4. KIỂM TRA CHỮ KÝ SỐ (VERIFICATION):
   Người nhận sử dụng Khóa công khai (Public Key) trích xuất từ Chứng thư số X.509 
   để giải mã chữ ký, so sánh với giá trị băm độc lập của tài liệu (xác nhận tính toàn vẹn) 
   và kiểm tra trạng thái chứng thư qua giao thức OCSP hoặc danh sách thu hồi CRL.
```

- **Giải thích thuật ngữ kỹ thuật cốt lõi:**
  - **PKI (Public Key Infrastructure):** Hạ tầng khóa công khai quản lý cặp khóa và chứng thư số.
  - **Khóa bí mật (Private Key):** Dữ liệu mật mã dùng để tạo chữ ký số; người ký phải nắm quyền kiểm soát duy nhất.
  - **Khóa công khai (Public Key):** Dữ liệu mật mã công khai dùng để kiểm tra tính hợp lệ của chữ ký số.
  - **Chứng thư số X.509:** Dữ liệu điện tử do CA cấp để liên kết danh tính của người ký với khóa công khai tương ứng. Bản thân chứng thư số không phải là chữ ký số.
  - **HSM (Hardware Security Module):** Thiết bị phần cứng bảo mật chuyên dụng dùng để lưu trữ và thực thi các phép toán mật mã với khóa bí mật; bản thân HSM không tự chứng minh được ai là người thực tế ra lệnh ký nếu thiếu nhật ký xác thực.
  - **TSA (Time-Stamping Authority):** Dịch vụ cấp dấu thời gian độc lập xác thực tài liệu tồn tại trước một thời điểm cụ thể; TSA không xác nhận danh tính người ký hay nội dung đồng ý.
  - **PAdES (PDF Advanced Electronic Signatures):** Chuẩn định dạng chữ ký số nâng cao áp dụng riêng cho định dạng PDF (theo chuẩn ETSI EN 319 142). Không phải mọi dữ liệu bệnh án điện tử đều là file PDF (nhiều dữ liệu là cấu trúc XML / JSON theo chuẩn HL7 CDA / FHIR).

### 2.2 Kiến trúc Remote Signing & Cơ chế Kiểm soát Quyền ký
Trong mô hình Ký số từ xa (Remote Signing), khóa bí mật của người bệnh không nằm trên thiết bị vật lý cá nhân (USB Token hay thẻ thông minh) mà được quản lý tập trung trong hệ thống HSM của EasyCA. 

Để bảo đảm người bệnh là người duy nhất nắm quyền kiểm soát khóa bí mật tại thời điểm ký theo luật định, kiến trúc hệ thống bắt buộc phải tách bạch 4 tầng xác thực:
1. **eKYC đăng ký cấp chứng thư:** Đối soát dữ liệu CCCD gắn chip (NFC/OCR) và nhận diện khuôn mặt động (Liveness Detection) để xác minh danh tính chủ thể khi đề nghị cấp chứng thư chữ ký số.
2. **Xác thực phiên làm việc (Session Authentication):** Xác thực người dùng đăng nhập vào hệ thống bệnh viện/ứng dụng ký số.
3. **Xác thực phê duyệt giao dịch ký (Transaction Authorization):** Với từng văn bản cụ thể (phiếu mổ, đơn thuốc, cam kết viện phí), hệ thống hiển thị tóm tắt nội dung và yêu cầu người dùng xác nhận thông qua yếu tố xác thực thứ cấp (Mã PIN bảo mật, OTP qua kênh độc lập hoặc sinh trắc học trực tiếp).
4. **Kích hoạt thao tác ký tại HSM:** Sau khi nhận đầy đủ bằng chứng xác thực hợp lệ của giao dịch, phân vùng HSM mới được kích hoạt để thực hiện phép toán ký số trên giá trị băm của tài liệu và ghi nhật ký kiểm toán (Audit Log).

---

## 3. Căn cứ Pháp lý & Rà soát Quy định Chuyên ngành

### 3.1 Khung Pháp lý Giao dịch Điện tử & Chữ ký số
- **Luật Giao dịch điện tử số 20/2023/QH15:**
  - *Khoản 11, 12 Điều 3:* Định nghĩa chữ ký điện tử và chữ ký số. Chữ ký số bảo đảm tính xác thực, tính toàn vẹn và tính chống chối bỏ, nhưng không bảo đảm tính bí mật của thông điệp dữ liệu.
  - *Điều 11:* Giá trị chứng cứ của thông điệp dữ liệu được cơ quan tố tụng đánh giá căn cứ vào độ tin cậy của cách thức khởi tạo, lưu trữ, truyền gửi; cách thức bảo đảm tính toàn vẹn; cách thức xác định người ký.
  - *Điều 22 & Điều 23:* Phân định giá trị pháp lý. Khoản 2 Điều 23 quy định chữ ký số đáp ứng điều kiện an toàn luật định có giá trị pháp lý tương đương chữ ký tay của cá nhân trong văn bản giấy.
- **Nghị định số 23/2025/NĐ-CP về Chữ ký điện tử và Dịch vụ tin cậy:**
  - *Điều 7:* Thời hạn có hiệu lực của chứng thư chữ ký số công cộng tối đa là 03 năm.
  - *Điều 15:* Trách nhiệm kiểm tra tình trạng hiệu lực của chứng thư trước khi thực hiện ký.
  - *Điều 34, 35:* Quy định về hồ sơ và thủ tục tiếp nhận, xác minh thông tin cấp chứng thư số.
  - *Điều 36:* Quy định điều kiện cấp chứng thư chữ ký số công cộng bằng phương tiện điện tử: bắt buộc xác minh danh tính, thu thập văn bản đồng ý với điều khoản hợp đồng dịch vụ, áp dụng biện pháp quản lý rủi ro và lưu trữ toàn bộ dữ liệu xác minh tối thiểu 05 năm kể từ ngày chứng thư hết hiệu lực.
  - *Điều 37:* Quy định về tạo lập và quản lý khóa bí mật bảo đảm an toàn kỹ thuật.
  - *Lưu ý về thiết kế sản phẩm:* Nghị định 23/2025/NĐ-CP không quy định một loại chứng thư riêng mang tên "chứng thư theo sự vụ" (Transactional Certificate). Việc EasyCA thiết kế gói chứng thư có thời hạn sử dụng ngắn (vài giờ hoặc vài ngày cho một đợt điều trị) là một **giải pháp thiết kế kỹ thuật - thương mại**, không phải một loại chứng thư mới theo luật định `[Nhận định pháp lý chuẩn xác]`.

### 3.2 Khung Pháp lý Y tế: Thông tư 13/2025/TT-BYT
- **Phân nhóm theo Điều 3:** Chữ ký số PKI của EasyCA thuộc **Nhóm 1: Sử dụng chữ ký điện tử hợp pháp**.
- Mối liên hệ: Thông tư 13/2025/TT-BYT mở ra 3 nhóm phương thức bình đẳng cho hồ sơ bệnh án điện tử, nhưng chữ ký số Nhóm 1 là phương thức duy nhất có cơ chế xác thực danh tính gắn liền với dịch vụ chứng thực của bên thứ ba độc lập (CA) được cấp phép theo quy định của Luật GDĐT 2023.

### 3.3 Pháp luật về Bảo vệ Dữ liệu Cá nhân
- **Luật Bảo vệ dữ liệu cá nhân số 91/2025/QH15 và Nghị định số 356/2025/NĐ-CP** (có hiệu lực từ ngày 01/01/2026, thay thế Nghị định 13/2023/NĐ-CP) `[Đã xác minh căn cứ pháp lý hiện hành]`.
- **Dữ liệu nhạy cảm trong bệnh viện:**
  - *Điều 26 Luật 91/2025/QH15:* Dữ liệu về tình trạng sức khỏe, bệnh án, đời tư y tế của người bệnh là dữ liệu cá nhân nhạy cảm.
  - *Điều 31 Luật 91/2025/QH15:* Dữ liệu sinh trắc học (khuôn mặt, vân tay) thu thập trong quy trình eKYC là dữ liệu nhạy cảm.
- **Yêu cầu đối với EasyCA và Bệnh viện:**
  - Bệnh viện (Bên kiểm soát dữ liệu) và EasyCA (Bên xử lý dữ liệu) phải có thỏa thuận xử lý dữ liệu cá nhân rõ ràng.
  - Phải thu thập sự đồng ý rõ ràng (Consent) của người bệnh trước khi thu thập dữ liệu sinh trắc học và CCCD.
  - Nghiêm cấm lưu trữ trái phép hoặc sử dụng dữ liệu bệnh án, dữ liệu sinh trắc học cho mục đích thương mại ngoài phạm vi dịch vụ ký số y tế.

---

## 4. Khách hàng & Triển khai Thực tế
- **Khách hàng Doanh nghiệp:** Hàng trăm nghìn doanh nghiệp đang sử dụng USB Token và Remote Signing EasyCA trong các dịch vụ hành chính công (Thuế, Hải quan, Hóa đơn điện tử) `[Đã xác minh qua số liệu công bố của SoftDreams]`.
- **Triển khai tại Bệnh viện:** Chưa xác minh được bệnh viện nào đã vận hành chính thức giải pháp ký số bệnh nhân của EasyCA trên quy mô toàn viện `[Ghi nhận thực tế: Chưa có bằng chứng triển khai lâm sàng công khai]`.

---

## 5. Đánh giá Năng lực Cạnh tranh & Chiến lược

### 5.1 Điểm mạnh (Strengths)
1. Có đầy đủ giấy phép CA công cộng hợp pháp cho cả USB Token và Remote Signing.
2. Tự chủ hạ tầng công nghệ mật mã, không phải đi thuê lại dịch vụ CA của bên khác.
3. Tính trung lập cao: Không sở hữu phần mềm HIS/EMR nên không cạnh tranh thị phần phần mềm với các nhà thầu quản trị bệnh viện hiện hữu.

### 5.2 Điểm yếu & Thách thức (Weaknesses & Bottlenecks)
1. **Thiếu sự hiện diện trong hệ sinh thái bệnh viện:** Không có sẵn phần mềm HIS/EMR tại các cơ sở y tế; việc tiếp cận bệnh viện phụ thuộc hoàn toàn vào việc đàm phán mở cổng API với nhà thầu HIS hiện tại của viện.
2. **Quy trình định danh cấp chứng thư cho bệnh nhân vãng lai:** Việc tuân thủ đầy đủ Điều 36 Nghị định 23/2025/NĐ-CP (hợp đồng thuê bao, xác minh danh tính, lưu trữ hồ sơ) có thể làm chậm tốc độ tiếp đón tại quầy nếu thiết kế UI/UX chưa tối ưu.
3. **Mô hình tài chính chưa rõ ràng:** Cần xác định rõ cơ cấu chi phí TCO: chi phí thiết lập ban đầu, chi phí mỗi lượt ký hoặc chi phí duy trì tài khoản để bệnh viện có thể dự toán ngân sách.

### 5.3 Định vị Chiến lược Khuyến nghị
- **Không tự định vị là đối thủ thay thế HIS:** Định vị EasyCA là **Nhà cung cấp Dịch vụ Tin cậy Chuyên sâu (Trust Service Provider)** cung cấp Module Ký số PKI qua Open API cho các nhà thầu phần mềm HIS/EMR (ISOFH, Nanosoft, LinkCare, Infomed...).
- **Xây dựng giải pháp mẫu (Reference Architecture):** Cần triển khai thử nghiệm (PoC) thành công tại ít nhất 1-2 khoa điều trị nội trú của một bệnh viện cụ thể để kiểm chứng thời gian thao tác, tỷ lệ lỗi eKYC và mức độ chấp nhận của người bệnh trước khi mở rộng thương mại.

---

## 6. Nguồn Tham khảo & Bằng chứng Xác thực
1. Cổng thông tin Trung tâm Chứng thực điện tử quốc gia (NEAC) — Giấy phép số 61/GP-BTTTT và 82/GP-BTTTT của SoftDreams (`neac.gov.vn`).
2. Luật Giao dịch điện tử số 20/2023/QH15.
3. Nghị định số 23/2025/NĐ-CP quy định về chữ ký điện tử và dịch vụ tin cậy.
4. Thông tư số 13/2025/TT-BYT hướng dẫn triển khai hồ sơ bệnh án điện tử.
5. Luật Bảo vệ dữ liệu cá nhân số 91/2025/QH15 và Nghị định số 356/2025/NĐ-CP.
6. Tiêu chuẩn ETSI EN 319 142 (PAdES) và ETSI TS 119 431/432 (Policy and security requirements for trust service providers issuing certificates).
