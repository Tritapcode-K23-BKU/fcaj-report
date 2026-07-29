---
title: "Tuần 2"
date: 2026-07-29
weight: 2
chapter: false
pre: " <b> 1.2 </b> "
---

#### Tuần 2 — Kiến trúc không máy chủ

**Thời gian:** 08/06 - 14/06/2026

#### Mục tiêu

- Hiểu mô hình tính toán không máy chủ và khi nào nên dùng
- Triển khai được hàm Lambda đầu tiên
- Nối Lambda với API Gateway để tạo endpoint gọi được từ Internet
- Làm quen với DynamoDB và mô hình dữ liệu NoSQL

#### Công việc đã thực hiện

Viết và triển khai hàm Lambda đơn giản bằng Node.js, thử nghiệm với các mức
timeout và bộ nhớ khác nhau để quan sát ảnh hưởng.

Tạo HTTP API trên API Gateway, nối với Lambda và gọi thử bằng `curl`. Tìm hiểu
cấu trúc sự kiện mà API Gateway gửi sang Lambda.

Tạo bảng DynamoDB đầu tiên, thực hành các thao tác PutItem, GetItem, Query và
Scan. So sánh chi phí và tốc độ giữa Query và Scan trên cùng một bảng.

#### Kết quả đạt được

- Triển khai được một API hoàn chỉnh chạy trên Internet, không cần máy chủ
- Hiểu được sự khác biệt căn bản giữa Query và Scan trong DynamoDB
- Nhận ra thiết kế bảng NoSQL phải đi theo mẫu truy vấn, không phải chuẩn hoá

#### Khó khăn và cách xử lý

Gặp khó khi Lambda gọi DynamoDB nhưng báo lỗi không đủ quyền. Sau khi đọc lại
tài liệu mới hiểu Lambda dùng execution role chứ không dùng credential của người
tạo. Đây là lần đầu em thấy IAM có tác dụng thực tế chứ không chỉ là lý thuyết.
