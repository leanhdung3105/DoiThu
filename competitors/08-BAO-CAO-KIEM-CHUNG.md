---
title: "Báo cáo Kiểm chứng Toàn diện & Đối chiếu Dữ liệu Nghiên cứu Đối thủ Chữ ký số Bệnh viện"
description: "Tổng hợp toàn bộ quá trình rà soát độc lập, phân loại lỗi, bảng đối chiếu trước/sau chỉnh sửa, căn cứ pháp lý và nguồn dữ liệu kiểm chứng."
last_updated: "2026-11-09"
author: "Ban Kiểm soát Chất lượng Dữ liệu & Pháp chế — SoftDreams"
---

# Báo cáo Kiểm chứng Toàn diện & Đối chiếu Dữ liệu Nghiên cứu Đối thủ

---

## 1. Mục đích, Phương pháp & Nguyên tắc Kiểm chứng

### 1.1 Mục đích Báo cáo
Báo cáo này được lập nhằm mục đích chuẩn hóa toàn bộ cơ sở dữ liệu nghiên cứu thị trường về giải pháp chữ ký điện tử/chữ ký số cho bệnh nhân và người nhà tại bệnh viện Việt Nam. Báo cáo đóng vai trò là tài liệu kiểm soát chất lượng dữ liệu (Data Quality Assurance), bảo đảm bộ hồ sơ nghiên cứu đạt độ tin cậy cao nhất để phục vụ Ban Lãnh đạo SoftDreams trong công tác hoạch định chiến lược sản phẩm, định giá, bán hàng và tư vấn khách hàng bệnh viện.

### 1.2 Phương pháp & Nguồn dữ liệu Kiểm chứng
1. **Văn bản quy phạm pháp luật gốc:** Tra cứu trên Cơ sở dữ liệu quốc gia về văn bản pháp luật (`vbpl.vn`), Cổng Thông tin điện tử Chính phủ (`chinhphu.vn`), Thư viện Pháp luật:
   - Luật Giao dịch điện tử số 20/2023/QH15.
   - Nghị định số 23/2025/NĐ-CP về chữ ký điện tử và dịch vụ tin cậy.
   - Thông tư số 13/2025/TT-BYT hướng dẫn triển khai hồ sơ bệnh án điện tử.
   - Luật An toàn thông tin mạng số 86/2015/QH13 và Nghị định số 85/2016/NĐ-CP về an toàn hệ thống thông tin theo cấp độ.
   - Luật Bảo vệ dữ liệu cá nhân số 91/2025/QH15 và Nghị định số 356/2025/NĐ-CP (hiệu lực 01/01/2026).
   - Luật Khám bệnh, chữa bệnh số 15/2023/QH15.
2. **Cơ quan quản lý chuyên ngành:**
   - Trung tâm Chứng thực điện tử quốc gia (NEAC) — Bộ Khoa học và Công nghệ / Bộ TT&TT (`neac.gov.vn`): Tra cứu tình trạng cấp phép của các CA công cộng.
   - Cổng dữ liệu ngành Y tế — Bộ Y tế (`moh.gov.vn`).
3. **Dữ liệu Đấu thầu & Doanh nghiệp:**
   - Hệ thống Mạng đấu thầu Quốc gia (`muasamcong.mpi.gov.vn`): Tra cứu các quyết định phê duyệt kết quả lựa chọn nhà thầu thực tế.
   - Cổng thông tin Quốc gia về Đăng ký Doanh nghiệp (`dangkykinhdoanh.gov.vn`): Kiểm tra thông tin pháp nhân, mã số thuế, đại diện pháp luật.
4. **Nguồn công bố của Bệnh viện & Doanh nghiệp:**
   - Cổng thông tin chính thức của Bệnh viện Đa khoa Xanh Pôn, Bệnh viện Từ Dũ, Bệnh viện Đa khoa Nông nghiệp...
   - Website chính thức của ISOFH, 2ID, Viettel Solutions, VNPT, FPT IS, DentalFlow.

### 1.3 Hệ thống Nhãn Kiểm chứng Thống nhất (5 Cấp độ)
- `[Đã xác minh từ văn bản/nguồn chính thức]`: Có văn bản pháp luật, giấy phép của bộ ngành, hồ sơ trúng thầu công khai hoặc thông cáo chính thức từ cơ quan nhà nước/bệnh viện.
- `[Do doanh nghiệp công bố]`: Thông tin xuất phát từ website, thông cáo báo chí hoặc tài liệu sản phẩm của chính nhà cung cấp giải pháp.
- `[Có nguồn tham khảo thứ cấp]`: Thông tin từ các bài viết báo chí, phóng sự truyền hình hoặc nguồn tin gián tiếp.
- `[Nhận định chuyên môn]`: Phân tích, đánh giá, giả thuyết kỹ thuật hoặc đề xuất chiến lược của nhóm nghiên cứu.
- `[Chưa xác minh]`: Chưa tìm thấy tài liệu chứng minh độc lập đủ tin cậy; cần tiếp tục khảo sát thực địa qua thử nghiệm (PoC).

---

## 2. Bảng Phân loại Phát hiện Kiểm chứng theo 3 Cấp độ

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│  MỨC 1: LỖI NGHIÊM TRỌNG CẦN SỬA NGAY (Pháp lý sai lệch, dữ liệu thời gian/thầu sai)   │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  MỨC 2: SAI LỆCH HOẶC THIẾU BẰNG CHỨNG CẦN HIỆU CHỈNH (Số liệu thị phần, ranh giới CA) │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  MỨC 3: VẤN ĐỀ CẦN NGHIÊN CỨU & KIỂM CHỨNG THỰC ĐỊA (Giả thuyết eKYC, hợp tác HIS)      │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 2.1 Mức 1: Lỗi Nghiêm trọng Đã Sửa Ngay

| STT | Tệp Liên quan | Nội dung Trước Chỉnh sửa | Nội dung Sau Chỉnh sửa | Căn cứ & Lý do Thay đổi |
|:---:|---|---|---|---|
| 1 | `03-isofh-vneid.md` | Ghi nhận BV Xanh Pôn triển khai ký số VNeID từ "tháng 11/2023–2024" | **Bắt đầu từ ngày 22/05/2025; công bố chính thức ngày 12/06/2025** | Thông cáo chính thức của ISOFH và báo chí (VnExpress, Báo CAND, Sức khỏe & Đời sống) xác nhận BV Xanh Pôn bắt đầu triển khai ngày 22/05/2025 và công bố 12/06/2025. |
| 2 | `01-easyca-softdreams.md` | Trích dẫn "Điều 36 NĐ 23/2025/NĐ-CP yêu cầu lưu trữ dữ liệu xác minh tối thiểu 05 năm sau khi chứng thư hết hạn" | Sửa thành: **Điều 36 quy định điều kiện cấp CTS bằng phương thức điện tử (eKYC); nghĩa vụ lưu trữ thông tin tối thiểu 05 năm quy định tại khoản 3 Điều 43** | Kiểm tra nguyên văn Nghị định số 23/2025/NĐ-CP: Điều 36 là quy định về eKYC; thời hạn lưu trữ thông tin thuê bao tối thiểu 05 năm sau khi CTS hết hiệu lực nằm tại khoản 3 Điều 43. |
| 3 | `02-2id-2contract.md` | Dùng gói thầu HSM Từ Dũ để kết luận 2ID đã triển khai hoàn tất toàn bộ giải pháp đọc chip NFC CCCD và đối soát khuôn mặt cho người bệnh | **Tách biệt: 2ID trúng thầu cung cấp chữ ký số HSM triển khai EMR; tính năng quét CCCD đối soát khuôn mặt người bệnh là giải pháp do doanh nghiệp công bố, chưa xác minh vận hành lâm sàng** | Gói thầu 128.521.600 đ tại BV Từ Dũ là "Trang bị chữ ký số HSM triển khai hồ sơ bệnh án điện tử" (ký số EMR bệnh viện), không có hạng mục đọc chip NFC hay đối soát khuôn mặt đại trà người bệnh. |
| 4 | `04-viettel-hms.md` | Khẳng định "Mọi hệ thống EMR trên Cloud bắt buộc đạt cấp độ 3 theo Luật Bảo vệ dữ liệu cá nhân" | Sửa thành: **Việc xác định cấp độ 3 của hệ thống thông tin bệnh viện căn cứ theo Luật An toàn thông tin mạng 2015 và Nghị định số 85/2016/NĐ-CP** | Luật Bảo vệ dữ liệu cá nhân 91/2025/QH15 không quy định về "cấp độ 3" của hệ thống thông tin. Cấp độ hệ thống là quy định thuộc pháp luật an toàn thông tin mạng. |
| 5 | `README.md`<br/>`00-tong-quan-so-sanh.md` | Diễn giải Điều 3 Thông tư 13/2025/TT-BYT theo thứ bậc: Nhóm 1 (Cao nhất) — Nhóm 2 (Trung bình) — Nhóm 3 (Cơ bản); khẳng định PKI "thắng kiện 100%" | **Bỏ thứ bậc hành chính; phân tích 3 nhóm bình đẳng theo Thông tư 13. Giải thích ưu thế mật mã học của PKI theo Điều 11 Luật GDĐT 2023, loại bỏ khẳng định thắng kiện tuyệt đối** | Điều 3 Thông tư 13/2025/TT-BYT không quy định thứ bậc hành chính. Theo Điều 11 Luật GDĐT 2023, giá trị chứng cứ do Tòa án đánh giá dựa trên toàn bộ chứng cứ vụ việc. |

### 2.2 Mức 2: Sai lệch hoặc Thiếu Bằng chứng Đã Hiệu chỉnh

| STT | Tệp Liên quan | Nội dung Trước Chỉnh sửa | Nội dung Sau Chỉnh sửa | Căn cứ & Lý do Thay đổi |
|:---:|---|---|---|---|
| 6 | `05-vnpt-his.md` | Trình bày con số 7.800 cơ sở y tế (7.000 trạm y tế) như số liệu thị phần độc lập đã kiểm toán | Gắn nhãn **`[Do doanh nghiệp công bố]`**, nêu rõ đây là số liệu độ phủ chung của toàn bộ sản phẩm y tế VNPT, không đồng nghĩa tất cả đều dùng EMR/ký số | Tránh nhầm lẫn giữa số liệu tiếp thị của doanh nghiệp với dữ liệu thống kê độc lập của cơ quan quản lý. |
| 7 | `06-fpt-ehospital.md` | Liệt kê các BV (Quảng Ninh, Đồng Nai, Hoàn Mỹ) và khẳng định FPT eHospital đã triển khai xác nhận OTP cho bệnh nhân | **Tách biệt: FPT IS triển khai phần mềm HIS/EMR cho cán bộ y tế tại các BV này [Đã xác minh]; việc áp dụng bắt buộc OTP/Zalo cho người bệnh [Chưa xác minh]** | Hợp đồng 100 tỷ tại Hoàn Mỹ hay dự án Đồng Nai là triển khai FPT.eHospital và EMR cho bác sĩ; chưa có văn bản xác nhận bệnh nhân bắt buộc dùng OTP. |
| 8 | `07-ky-tay-tablet.md` | Nhận định chi phí biến đổi của ký Tablet "gần như bằng 0"; khẳng định mọi tablet đều thu thập được áp lực bút | **Bổ sung phân tích TCO đầy đủ (thiết bị, rơi vỡ, bản quyền, nhân sự); làm rõ áp lực bút CHỈ có được khi dùng bút cảm ứng lực chuyên dụng trên màn hình hỗ trợ** | Ngón tay và bút điện dung thông thường không lấy được áp lực; chi phí thay màn hình vỡ và khấu hao máy tính bảng tại viện là khoản mục thực tế. |
| 9 | `01-easyca-softdreams.md` | Diễn giải "chứng thư theo sự vụ (Transactional Certificate)" như một loại chứng thư số riêng được pháp luật định danh | **Nêu rõ đây là phương án thiết kế kiến trúc sản phẩm và mô hình thương mại của SoftDreams trong khuôn khổ thời hạn chứng thư tối đa 3 năm của NĐ 23/2025/NĐ-CP** | Pháp luật Việt Nam không có định danh pháp lý riêng cho loại chứng thư mang tên "Transactional Certificate". |
| 10 | `04-viettel-hms.md` | Đưa ra nhận định chủ quan "Viettel có quy trình thay đổi tính năng chậm" | Chuyển thành: **Viettel là tập đoàn lớn với quy trình kiểm soát chất lượng tập trung, việc tùy biến tính năng riêng cần theo lộ trình phiên bản chung** | Loại bỏ ngôn từ cảm tính, hạ thấp đối thủ khi không có số liệu khảo sát độc lập. |

### 2.3 Mức 3: Vấn đề Cần Tiếp tục Nghiên cứu & Kiểm chứng Thực địa (PoC)

| STT | Hạng mục Cần Nghiên cứu | Giả thuyết Hiện tại | Phương pháp Kiểm chứng Khuyến nghị |
|:---:|---|---|---|
| 1 | **Thời gian thao tác eKYC tại quầy** | Ước tính mất 3-7 phút nếu đăng ký mới app; EasyCA thiết kế dưới 60 giây | Cần triển khai PoC thực tế tại 01 quầy tiếp đón bệnh viện để bấm giờ chính xác trên 100 lượt bệnh nhân ngẫu nhiên. |
| 2 | **Mức độ chấp nhận chi phí lượt ký PKI của Bệnh viện** | Bệnh viện sẵn sàng chi trả gói lượt ký PKI (Transaction Pack) để nâng chuẩn Nhóm 1 | Cần phỏng vấn sâu Giám đốc/Trưởng phòng KHTH của 5 bệnh viện công lập và tư nhân. |
| 3 | **Khả năng hợp tác tích hợp của các đơn vị HIS độc lập** | Các đơn vị HIS độc lập (ISOFH, Nanosoft, LinkCare...) sẽ cởi mở kết nối EasyCA vì không cạnh tranh thị phần phần mềm | Cần tổ chức các buổi tiếp xúc kỹ thuật, giới thiệu Open API và đề xuất chính sách phân chia doanh thu (Revenue Sharing) cụ thể. |
| 4 | **Quy trình ký thay của người đại diện hợp pháp** | Thiết kế luồng cho phép thân nhân ký thay người bệnh mất năng lực/cấp cứu | Cần ý kiến thẩm định của Luật sư/Chuyên gia pháp chế về hồ sơ chứng minh quan hệ đại diện hợp pháp trong giao dịch điện tử y tế. |

---

## 3. Tổng hợp Bảng Nguồn Dữ liệu Kiểm chứng Chính thức

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│  VĂN BẢN QUY PHẠM PHÁP LUẬT                                                             │
│  - Luật Giao dịch điện tử số 20/2023/QH15 (vbpl.vn)                                    │
│  - Nghị định số 23/2025/NĐ-CP ngày 21/02/2025 (chinhphu.vn)                           │
│  - Thông tư số 13/2025/TT-BYT ngày 30/06/2025 (moh.gov.vn)                             │
│  - Luật Bảo vệ dữ liệu cá nhân số 91/2025/QH15 & Nghị định 356/2025/NĐ-CP              │
│  - Luật Khám bệnh, chữa bệnh số 15/2023/QH15                                           │
│  - Luật An toàn thông tin mạng số 86/2015/QH13 & Nghị định 85/2016/NĐ-CP               │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  CƠ QUAN QUẢN LÝ NHÀ NƯỚC                                                              │
│  - Trung tâm Chứng thực điện tử quốc gia (NEAC) — neac.gov.vn (Danh bạ CA cấp phép)   │
│  - Cổng Thông tin điện tử Bộ Y tế — moh.gov.vn                                         │
│  - Hệ thống Mạng đấu thầu Quốc gia — muasamcong.mpi.gov.vn                             │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  THÔNG CÁO BỆNH VIỆN & BÁO CHÍ CHÍNH THỐNG                                             │
│  - BV Xanh Pôn & ISOFH: isofh.com (12/06/2025); Báo CAND, VnExpress, Sức khỏe & Đời sống│
│  - BV Từ Dũ: Thầu HSM EMR (2250/QĐ-BVTD, 28/09/2026, muasamcong.mpi.gov.vn)            │
│  - BV Đa khoa Nông nghiệp: Baochinhphu.vn, Thanhtra.com.vn (triển khai EMR & PACS)     │
│  - FPT & Hoàn Mỹ: SGGP (08/2020), FPT IS (Hợp đồng chuyển đổi số 100 tỷ đồng)          │
│  - DentalFlow: dentalflow.vn (tính năng ký bệnh án trên tablet nha khoa)               │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 4. Khuyến nghị Chiến lược cho Ban Lãnh đạo SoftDreams

1. **Về Định vị Pháp lý & Kỹ thuật:**
   - Không truyền thông theo hướng "chữ ký số PKI thắng kiện 100%" hay coi các hình thức khác là "vô hiệu". Hãy định vị EasyCA là **"Chuẩn bảo đảm an toàn thông tin và giá trị chứng minh cao nhất"** theo Điều 11 Luật Giao dịch điện tử 2023.
   - Tập trung vào chiến lược **"Kiến trúc Phân tầng Rủi ro (Risk-based Tiering)"**: Khuyến nghị bệnh viện áp dụng PKI EasyCA cho các biểu mẫu có rủi ro pháp lý/tài chính cao (cam kết phẫu thuật, từ chối điều trị, viện phí lớn ngoài BHYT) và duy trì Tablet cho tiếp đón thông thường.
2. **Về Mô hình Sản phẩm:**
   - Hoàn thiện bộ tài liệu kỹ thuật **Open API & SDK chuẩn hóa** để các nhà thầu HIS/EMR có thể tích hợp trong thời gian ngắn nhất (mục tiêu dưới 02 tuần).
   - Thiết kế quy trình eKYC tại quầy tiếp đón đạt mục tiêu dưới 60 giây, hỗ trợ đầy đủ các trường hợp ngoại lệ (người cao tuổi, trẻ em, người đại diện ký thay).
3. **Về Chính sách Thương mại:**
   - Đóng gói dịch vụ theo dạng **Gói lượt ký (Transaction Pack)** linh hoạt cho bệnh viện (ví dụ gói 10.000 / 50.000 / 100.000 lượt ký) thay vì mô hình thuê bao năm cá nhân, giúp bệnh viện dễ dàng lập dự toán ngân sách.
   - Xây dựng chính sách chia sẻ doanh thu hấp dẫn cho các công ty phần mềm HIS/EMR độc lập để biến họ thành đối tác phân phối chiến lược.
4. **Về Kế hoạch Triển khai Thực tế:**
   - Ưu tiên tìm kiếm 01 bệnh viện đa khoa đối tác để triển khai dự án thử nghiệm (PoC) trong vòng 03 tháng nhằm đo đếm các chỉ số vận hành lâm sàng thực tế, tạo hồ sơ năng lực thực chiến vững chắc trước khi thương mại hóa diện rộng.
