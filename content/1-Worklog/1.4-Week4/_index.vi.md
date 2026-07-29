---
title: "Tuần 4"
date: 2026-07-29
weight: 4
chapter: false
pre: " <b> 1.4 </b> "
---

#### Tuần 4 — Dựng lớp lưu trữ và cơ sở dữ liệu

**Thời gian:** 22/06 - 28/06/2026

#### Mục tiêu

- Tạo bucket S3 cho giao diện và cho dữ liệu huấn luyện
- Cấu hình CloudFront với Origin Access Control
- Tạo 8 bảng DynamoDB theo thiết kế
- Nạp dữ liệu mẫu 100 sản phẩm

#### Công việc đã thực hiện

Tạo hai bucket S3 với vai trò tách biệt. Bucket giao diện được giữ riêng tư hoàn
toàn, chỉ CloudFront truy cập được thông qua Origin Access Control thay vì mở
public như nhiều hướng dẫn cũ.

Cấu hình CloudFront: bật chuyển hướng HTTP sang HTTPS, đặt `index.html` làm
default root object, và thêm custom error response chuyển lỗi 403 và 404 về
`index.html` để ứng dụng một trang hoạt động đúng khi mở thẳng đường dẫn con.

Tạo 8 bảng DynamoDB ở chế độ on-demand. Hai bảng Reviews và Orders dùng khoá tổ
hợp để có thể truy vấn bằng Query thay vì Scan toàn bảng.

Viết script nạp dữ liệu mẫu cho 100 sản phẩm thuộc 8 danh mục.

#### Kết quả đạt được

- Giao diện tĩnh phục vụ được qua CloudFront với HTTPS
- Bucket S3 không truy cập trực tiếp được từ Internet, xác nhận bằng thử nghiệm
- 8 bảng DynamoDB sẵn sàng với dữ liệu mẫu

#### Khó khăn và cách xử lý

Sau khi tải bản build mới lên S3, trang web hiển thị trắng. Em mất khá nhiều thời
gian kiểm tra lại mã nguồn trước khi phát hiện nguyên nhân là CloudFront vẫn phục
vụ bản cũ trong bộ nhớ đệm. Từ đó em ghi nhớ quy tắc: mỗi lần tải file mới lên S3
bắt buộc phải tạo invalidation.
