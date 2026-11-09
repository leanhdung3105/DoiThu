---
title: "Mục lục & Cấu trúc Dữ liệu Nghiên cứu Đối thủ Chữ ký số Bệnh viện"
description: "Danh mục báo cáo phân tích đối thủ cạnh tranh chữ ký số bệnh nhân/người nhà tại bệnh viện Việt Nam theo chuẩn khách quan."
last_updated: "2026-11-09"
author: "EasyCA Solution Team — SoftDreams"
---

# Mục lục & Cấu trúc Dữ liệu Nghiên cứu Đối thủ

Bộ tài liệu được thiết kế theo cấu trúc Markdown chuẩn (hỗ trợ Frontmatter), sẵn sàng để tích hợp và hiển thị trực tiếp lên website tài liệu (Docsify, Astro, Next.js, Nuxt Content, Docusaurus...).

Tất cả các tài liệu được chuẩn hóa theo khung phân tích chuyên môn 6 phần, gắn nhãn kiểm chứng thông tin minh bạch theo 5 cấp độ:
- `[Đã xác minh từ văn bản/nguồn chính thức]`: Có văn bản pháp luật, giấy phép, cổng chính thức hoặc hồ sơ thầu xác thực trực tiếp.
- `[Do doanh nghiệp công bố]`: Thông tin xuất phát từ thông cáo, website hoặc tài liệu của chính nhà cung cấp.
- `[Có nguồn tham khảo thứ cấp]`: Thông tin từ bài viết báo chí hoặc nguồn gián tiếp.
- `[Nhận định chuyên môn]`: Phân tích, đánh giá hoặc giả thuyết của chuyên gia nghiên cứu.
- `[Chưa xác minh]`: Chưa tìm thấy bằng chứng đủ tin cậy, cần khảo sát thực địa thêm.

---

## Danh mục Tài liệu Hoàn chỉnh

| STT | Tên File | Đơn vị / Giải pháp | Phương thức ký bệnh nhân | Nhóm theo TT 13/2025 | Tình trạng Kiểm chứng |
|:---:|---|---|---|:---:|:---:|
| 00 | [**`00-tong-quan-so-sanh.md`**](00-tong-quan-so-sanh.md) | **Báo cáo Tổng quan** | Ma trận so sánh 13 tiêu chí & phân tích chuỗi giá trị | **Tổng hợp** | Báo cáo chiến lược tổng thể |
| 01 | [**`01-easyca-softdreams.md`**](01-easyca-softdreams.md) | **EasyCA (SoftDreams)** | **Chữ ký số PKI cá nhân (Remote Signing / HSM)** | **Nhóm 1** | Giấy phép CA: `[Đã xác minh]`; Dự án BV: `[Chưa xác minh]` |
| 02 | [**`02-2id-2contract.md`**](02-2id-2contract.md) | **2ID / 2Contract** | Quét chip CCCD (NFC) + Đối soát khuôn mặt | **Nhóm 2 & 3** | Thầu HSM Từ Dũ: `[Đã xác minh]`; Quét chip BN: `[Do DN công bố]` |
| 03 | [**`03-isofh-vneid.md`**](03-isofh-vneid.md) | **ISOFH (BV Xanh Pôn)** | Chữ ký số PKI qua VNeID (hoặc xác nhận app) | **Nhóm 1 / 3** | Bắt đầu 22/05/2025, công bố 12/06/2025: `[Đã xác minh]` |
| 04 | [**`04-viettel-hms.md`**](04-viettel-hms.md) | **Viettel HMS** | Ký cảm ứng trên Tablet & Xác thực VNeID | **Nhóm 3** | Viettel-CA bác sĩ: `[Đã xác minh]`; Ký số PKI cho BN: `[Chưa xác minh]` |
| 05 | [**`05-vnpt-his.md`**](05-vnpt-his.md) | **VNPT HIS / SmartCA** | Ký qua App VNeID, Tablet & SmartCA cá nhân | **Nhóm 3 & 1** | Độ phủ HIS: `[Do DN công bố]`; Ký số PKI cho BN vãng lai: `[Chưa xác minh]` |
| 06 | [**`06-fpt-ehospital.md`**](06-fpt-ehospital.md) | **FPT eHospital** | Xác thực qua mã OTP SMS / Zalo & eSign | **Nhóm 3** | HIS tại BV lớn: `[Đã xác minh]`; Ký số PKI cho BN: `[Chưa xác minh]` |
| 07 | [**`07-ky-tay-tablet.md`**](07-ky-tay-tablet.md) | **Ký tay Tablet (DentalFlow...)** | Vẽ chữ ký cảm ứng trên màn hình thiết bị | **Nhóm 3** | Nha khoa DentalFlow: `[Đã xác minh]`; Phổ biến tại quầy tiếp đón |
| 08 | [**`08-BAO-CAO-KIEM-CHUNG.md`**](08-BAO-CAO-KIEM-CHUNG.md) | **Báo cáo Kiểm chứng Toàn diện** | Tổng hợp đối chiếu nguồn, sửa đổi & lộ trình PoC | **Kiểm chứng** | Tài liệu kiểm soát chất lượng dữ liệu |

---

## Cấu trúc Tiêu chuẩn 6 Phần áp dụng trên Từng Hồ sơ

Mỗi hồ sơ đối thủ được trình bày theo cấu trúc đồng nhất:
1. **Thông tin doanh nghiệp:** Pháp nhân, sản phẩm, phân định 3 vai trò (HIS vendor, CA công cộng, System Integrator), mức độ hiện diện thị trường.
2. **Sản phẩm và công nghệ:** Phân tách luồng cán bộ y tế vs bệnh nhân, công nghệ định danh, xác thực, ký số, lưu trữ và tích hợp HIS/EMR.
3. **Căn cứ pháp lý:** Phân nhóm theo Điều 3 Thông tư 13/2025/TT-BYT, Luật Giao dịch điện tử 2023, Nghị định 23/2025/NĐ-CP, Luật An toàn thông tin mạng (NĐ 85/2016/NĐ-CP), Luật Bảo vệ dữ liệu cá nhân 91/2025/QH15 và Luật Khám bệnh, chữa bệnh 15/2023/QH15.
4. **Khách hàng và triển khai:** Cơ sở y tế đã triển khai, quy mô, tình trạng vận hành, nguồn xác minh.
5. **Bảng đánh giá tiêu chuẩn 13 tiêu chí & Khả năng cạnh tranh vs EasyCA:** Điểm mạnh, điểm yếu, rào cản chuyển đổi, chiến lược cạnh tranh.
6. **Nguồn tham khảo & Bằng chứng xác thực:** Văn bản quy phạm pháp luật, cổng thông tin chính thức, hồ sơ đấu thầu công khai.
