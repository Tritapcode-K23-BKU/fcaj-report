---
title: "Tuần 7"
date: 2026-07-29
weight: 7
chapter: false
pre: " <b> 1.7 </b> "
---

#### Tuần 7 — Thiết lập Amazon Personalize

**Thời gian:** 13/07 - 19/07/2026

#### Mục tiêu

- Tạo dataset group và nạp dữ liệu tương tác
- Huấn luyện mô hình gợi ý đầu tiên
- Triển khai campaign phục vụ suy luận thời gian thực
- Nối kết quả gợi ý vào trang chủ

#### Công việc đã thực hiện

Tạo dataset group và định nghĩa schema cho dataset Interactions. Tạo IAM role cho
phép Personalize đọc bucket dữ liệu, đồng thời thêm bucket policy tương ứng.

Sinh bộ dữ liệu tương tác đầu tiên gồm 4.491 lượt, phân bố ngẫu nhiên đều. Nạp
vào Personalize, huấn luyện solution với recipe `aws-user-personalization`.

Sau khi huấn luyện xong, xem các chỉ số đánh giá thì thấy kết quả rất kém:
Precision@5 chỉ đạt 0,0889 và MRR@25 đạt 0,1216.

Vẫn triển khai campaign và nối vào route gợi ý trong Lambda để hoàn thiện luồng
kỹ thuật, đồng thời bắt đầu phân tích nguyên nhân kết quả kém.

#### Kết quả đạt được

- Luồng kỹ thuật hoàn chỉnh: Lambda gọi được campaign và trả gợi ý về giao diện
- Khối gợi ý hiển thị trên trang chủ
- Xác định được vấn đề nằm ở dữ liệu chứ không phải cấu hình dịch vụ

#### Khó khăn và cách xử lý

Phát hiện một lỗi tinh vi không sinh ra thông báo lỗi nào: DynamoDB không đảm bảo
trả kết quả theo thứ tự khoá được truyền vào, nên thứ hạng do mô hình tính toán
bị mất. Phải sắp xếp lại theo thứ tự gốc sau khi truy vấn. Lỗi này chỉ phát hiện
được khi so sánh kỹ kết quả trả về.
