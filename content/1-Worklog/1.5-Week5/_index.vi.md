---
title: "Tuần 5"
date: 2026-07-29
weight: 5
chapter: false
pre: " <b> 1.5 </b> "
---

#### Tuần 5 — Triển khai lớp API

**Thời gian:** 29/06 - 05/07/2026

#### Mục tiêu

- Tạo IAM role cho Lambda theo nguyên tắc quyền tối thiểu
- Triển khai mã nguồn API của bạn backend lên Lambda
- Cấu hình API Gateway với 22 route
- Bật CORS cho giao diện gọi được API

#### Công việc đã thực hiện

Tạo IAM role riêng cho Lambda, chỉ cấp quyền đọc ghi trên 8 bảng DynamoDB và gọi
`personalize:GetRecommendations` trên đúng một campaign. Không dùng policy quản
lý sẵn có phạm vi rộng.

Đóng gói mã nguồn của bạn phụ trách backend cùng thư viện phụ thuộc thành file
zip và tải lên Lambda. Điều chỉnh timeout lên 30 giây và bộ nhớ lên 512 MB vì mặc
định 3 giây không đủ khi gọi dịch vụ ngoài.

Tạo HTTP API với route bắt tất cả `/{proxy+}`, để mã nguồn tự định tuyến bên
trong. Cách này giữ cấu hình API Gateway đơn giản với 22 route.

Cấu hình CORS để giao diện chạy trên tên miền CloudFront gọi được API ở tên miền
khác.

#### Kết quả đạt được

- API hoạt động, gọi được từ Internet, trả về dữ liệu thật từ DynamoDB
- IAM role tuân thủ nguyên tắc quyền tối thiểu
- Toàn bộ 22 route được kiểm tra bằng dòng lệnh

#### Khó khăn và cách xử lý

Giao diện báo không kết nối được máy chủ trong khi thử bằng `curl` vẫn chạy bình
thường. Sau khi mở Developer Tools mới thấy lỗi CORS. Em học được rằng lỗi CORS
chỉ xuất hiện ở trình duyệt, nên khi gỡ lỗi phải kiểm tra ở đúng môi trường mà
người dùng thật sử dụng.
