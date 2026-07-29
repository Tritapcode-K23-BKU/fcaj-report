---
title: "Tuần 9"
date: 2026-07-29
weight: 9
chapter: false
pre: " <b> 1.9 </b> "
---

#### Tuần 9 — Giám sát, kiểm thử và tài liệu

**Thời gian:** 27/07 - 02/08/2026

#### Mục tiêu

- Thiết lập giám sát và cảnh báo cho hệ thống
- Kiểm thử toàn luồng từ trình duyệt tới mô hình
- Lập kế hoạch dọn dẹp tài nguyên
- Hoàn thiện tài liệu và báo cáo thực tập

#### Công việc đã thực hiện

Tạo SNS topic và đăng ký email nhận cảnh báo. Thiết lập hai CloudWatch alarm cho
tỉ lệ lỗi và độ trễ của Lambda, kiểm tra bằng cách gọi thử đường dẫn không tồn
tại để sinh lỗi.

Kiểm thử toàn luồng theo từng lớp từ trong ra ngoài: DynamoDB, API, Personalize,
rồi tới giao diện. Kiểm tra riêng hai điểm quan trọng: gợi ý cho hai người dùng
khác nhau phải khác nhau, và đặt hàng với giá bị sửa phải bị máy chủ tính lại.

Lập bảng kiểm dọn dẹp tài nguyên theo thứ tự ưu tiên, đặt Personalize campaign
lên đầu vì đây là thành phần tính phí theo giờ tồn tại.

Viết tài liệu workshop dạng lab hướng dẫn từng bước, và hoàn thiện báo cáo thực
tập trên nền tảng Hugo.

#### Kết quả đạt được

- Hai alarm hoạt động, gửi email khi vượt ngưỡng
- Bảng kiểm thử toàn luồng với 8 hạng mục đều đạt
- Tài liệu workshop cho phép người khác dựng lại toàn bộ hệ thống
- Báo cáo thực tập song ngữ hoàn chỉnh

#### Khó khăn và cách xử lý

Khi viết tài liệu workshop mới phát hiện nhiều chỗ mình tưởng đã hiểu nhưng thực
ra chưa. Để hướng dẫn người khác làm lại được thì phải giải thích được từng bước,
không thể viết mơ hồ. Đây là cách kiểm tra kiến thức hiệu quả hơn nhiều so với tự
đánh giá.
