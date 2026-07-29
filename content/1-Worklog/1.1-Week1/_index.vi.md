---
title: "Tuần 1"
date: 2026-07-29
weight: 1
chapter: false
pre: " <b> 1.1 </b> "
---

#### Tuần 1 — Nền tảng AWS, IAM và S3

**Thời gian:** 01/06 - 07/06/2026

#### Mục tiêu

- Nắm được mô hình trách nhiệm chia sẻ giữa AWS và khách hàng
- Hiểu cách quản lý danh tính và phân quyền bằng IAM
- Làm quen với lưu trữ đối tượng trên S3
- Thiết lập môi trường làm việc: tài khoản AWS, AWS CLI

#### Công việc đã thực hiện

Hoàn thành các bài học nền tảng theo lộ trình của chương trình. Tự tạo tài
khoản AWS, cấu hình AWS CLI và xác minh danh tính bằng `aws sts get-caller-identity`.

Thực hành phân quyền: tạo IAM user, gán policy, thử nghiệm sự khác biệt giữa
policy quản lý sẵn và policy tự viết. Tạo bucket S3, thử các chế độ truy cập
khác nhau và quan sát tác động của Block Public Access.

Đọc tài liệu về nguyên tắc quyền tối thiểu và cách áp dụng trong thực tế.

#### Kết quả đạt được

- Môi trường làm việc sẵn sàng, thao tác được cả trên console và dòng lệnh
- Hiểu được vì sao không nên dùng tài khoản root cho công việc hằng ngày
- Nắm được cấu trúc của một IAM policy: Effect, Action, Resource

#### Khó khăn và cách xử lý

Khó khăn lớn nhất là bị ngợp vì AWS có quá nhiều dịch vụ. Khi chưa biết mình
cần giải quyết bài toán gì thì rất khó xác định nên học cái nào trước. Em quyết
định bám sát lộ trình của chương trình thay vì đọc lan man.
