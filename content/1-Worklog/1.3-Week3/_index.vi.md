---
title: "Tuần 3"
date: 2026-07-29
weight: 3
chapter: false
pre: " <b> 1.3 </b> "
---

#### Tuần 3 — Chọn đề tài và thiết kế kiến trúc

**Thời gian:** 15/06 - 21/06/2026

#### Mục tiêu

- Chốt đề tài dự án cuối kỳ cho nhóm
- Thiết kế kiến trúc tổng thể và lựa chọn dịch vụ
- Phân công nhiệm vụ giữa năm thành viên
- Ước lượng chi phí và đặt cảnh báo ngân sách

#### Công việc đã thực hiện

Nhóm thảo luận và chốt đề tài hệ gợi ý sản phẩm thương mại điện tử. Lý do chọn:
bài toán có giá trị thực tế rõ ràng, sử dụng được nhiều dịch vụ AWS liên kết với
nhau, và có phần học máy nhưng không đòi hỏi tự cài đặt thuật toán.

Thiết kế kiến trúc hai nhánh: nhánh tĩnh qua CloudFront và S3, nhánh động qua
API Gateway và Lambda. So sánh các phương án trước khi quyết định, ghi lại lập
luận cho từng lựa chọn.

Phân công: em nhận vai trò Cloud Architect, phụ trách hạ tầng và các quyết định
kiến trúc. Bốn bạn còn lại phụ trách backend, frontend, học máy và dữ liệu.

Đặt AWS Budgets với ngưỡng cảnh báo để tránh phát sinh chi phí ngoài dự kiến.

#### Kết quả đạt được

- Sơ đồ kiến trúc tổng thể hoàn chỉnh, có lập luận cho từng lựa chọn dịch vụ
- Bảng phân công nhiệm vụ rõ ràng cho năm thành viên
- Cảnh báo ngân sách đã hoạt động

#### Khó khăn và cách xử lý

Nhóm mất khá nhiều thời gian ở khâu chọn đề tài vì không biết phạm vi nào là vừa
sức trong thời gian có hạn. Ban đầu có ý tưởng làm hệ thống lớn hơn nhiều, sau
phải cắt bớt để đảm bảo hoàn thành được.
