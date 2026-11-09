---
title: "Mục lục & Cấu trúc Dữ liệu Nghiên cứu Đối thủ Chữ ký số Bệnh viện"
description: "Danh mục báo cáo phân tích đối thủ cạnh tranh chữ ký số bệnh nhân/người nhà tại bệnh viện Việt Nam theo chuẩn khách quan."
last_updated: "2026-11-09"
---

# Mục lục & Cấu trúc Dữ liệu Nghiên cứu Đối thủ

Bộ tài liệu được thiết kế theo cấu trúc Markdown chuẩn (hỗ trợ Frontmatter), sẵn sàng để tích hợp và hiển thị trực tiếp lên website tài liệu (Docsify, Astro, Next.js, Nuxt Content, Docusaurus...).

Tất cả các tài liệu được chuẩn hóa theo khung phân tích chuyên môn 6 phần, gắn nhãn kiểm chứng thông tin minh bạch (`[Đã xác minh]`, `[Có nguồn tham khảo]`, `[Nhận định]`, `[Chưa xác minh]`).

---

## Danh mục Tài liệu

| STT | Tên File | Đơn vị / Giải pháp | Phương thức ký bệnh nhân | Nhóm theo TT 13/2025 |
|:---:|---|---|---|:---:|
| 00 | [**`00-tong-quan-so-sanh.md`**](00-tong-quan-so-sanh.md) | **Báo cáo Tổng quan** | Ma trận 7 giải pháp & phân tích chuỗi giá trị | **Tổng hợp** |
| 01 | [**`01-easyca-softdreams.md`**](01-easyca-softdreams.md) | **EasyCA (SoftDreams)** | **Chữ ký số PKI (Remote Signing / Cloud HSM)** | **Nhóm 1** |
| 02 | [**`02-2id-2contract.md`**](02-2id-2contract.md) | **2ID / 2Contract** | Quét chip CCCD (NFC) + Đối soát khuôn mặt | **Nhóm 2 & 3** |
| 03 | [**`03-isofh-vneid.md`**](03-isofh-vneid.md) | **ISOFH (BV Xanh Pôn)** | Xác nhận giao dịch điện tử qua App VNeID | **Nhóm 3** |
| 04 | [**`04-viettel-hms.md`**](04-viettel-hms.md) | **Viettel HMS** | Ký cảm ứng trên Tablet & Xác thực VNeID | **Nhóm 3** |
| 05 | [**`05-vnpt-his.md`**](05-vnpt-his.md) | **VNPT HIS / SmartCA** | Ký qua App VNeID, Tablet & SmartCA cá nhân | **Nhóm 3 & 1** |
| 06 | [**`06-fpt-ehospital.md`**](06-fpt-ehospital.md) | **FPT eHospital** | Xác thực qua mã OTP SMS / Zalo & eSign | **Nhóm 3** |
| 07 | [**`07-ky-tay-tablet.md`**](07-ky-tay-tablet.md) | **Ký tay Tablet (DentalFlow...)** | Vẽ chữ ký cảm ứng trên màn hình thiết bị | **Nhóm 3** |

---

## Cấu trúc Tiêu chuẩn 6 Phần áp dụng trên Từng Đối thủ

Mỗi hồ sơ đối thủ được trình bày theo cấu trúc đồng nhất:
1. **Thông tin doanh nghiệp:** Pháp nhân, sản phẩm, vai trò trong chuỗi cung ứng y tế, đối tác liên quan.
2. **Sản phẩm và công nghệ:** Phương thức ký, công nghệ định danh, công nghệ xác thực, công nghệ ký, lưu trữ và bảo mật, tích hợp HIS/EMR.
3. **Căn cứ pháp lý:** Phân nhóm theo Điều 3 Thông tư 13/2025/TT-BYT, Luật Giao dịch điện tử 2023, điều kiện áp dụng, hạn chế pháp lý.
4. **Khách hàng và triển khai:** Cơ sở y tế đã triển khai, thời gian, quy mô, tình trạng vận hành, nguồn xác minh.
5. **Đánh giá cạnh tranh vs EasyCA:** Điểm mạnh, điểm yếu, rào cản chuyển đổi, chiến lược cạnh tranh.
6. **Nguồn tham khảo:** Văn bản pháp luật, cổng thông tin chính thức, bài viết báo chí và tài liệu kỹ thuật.
