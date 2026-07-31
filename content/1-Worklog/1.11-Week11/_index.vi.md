---
title: "Tuần 11"
date: 2026-07-29
weight: 11
chapter: false
pre: " <b> 1.11 </b> "
---

#### Tuần 11 — Dọn dẹp tài nguyên và tổng kết

**Thời gian:** 10/08 - 16/08/2026

#### Mục tiêu

- Dọn dẹp toàn bộ tài nguyên AWS theo bảng kiểm
- Xác nhận không còn chi phí phát sinh
- Tổng kết bài học kinh nghiệm

#### Công việc đã thực hiện

Thực hiện dọn dẹp theo đúng thứ tự ưu tiên đã lập: xoá Personalize campaign
trước vì đây là thành phần tính phí theo giờ tồn tại, sau đó xoá solution và
dataset group, vô hiệu hoá rồi xoá CloudFront distribution, làm rỗng và xoá hai
bucket S3, xoá API Gateway và Lambda, xoá tám bảng DynamoDB, cuối cùng xoá IAM
role và các alarm.

Xoá các tài khoản IAM tạm thời đã cấp cho thành viên trong nhóm cùng access key
đi kèm.

Kiểm tra lại qua Billing Dashboard và Resource Groups để đảm bảo không còn tài
nguyên nào sót lại.

Tổng kết các bài học kinh nghiệm và hướng phát triển tiếp theo.

#### Kết quả đạt được

- Toàn bộ tài nguyên đã được xoá, xác nhận qua Billing Dashboard
- Không phát sinh chi phí ngoài dự kiến
- Hoàn thành kỳ thực tập với đầy đủ sản phẩm bàn giao

#### Khó khăn và cách xử lý

Khi xoá Personalize phải theo đúng thứ tự campaign, solution, dataset, dataset
group, nếu không sẽ báo lỗi phụ thuộc. Em cũng phải nhớ tắt chế độ huấn luyện tự
động của solution trước khi xoá, tránh việc nó khởi động một lần huấn luyện mới
gây phát sinh chi phí.
