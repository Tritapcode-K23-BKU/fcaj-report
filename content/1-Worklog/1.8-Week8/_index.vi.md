---
title: "Tuần 8"
date: 2026-07-29
weight: 8
chapter: false
pre: " <b> 1.8 </b> "
---

#### Tuần 8 — Cải tiến dữ liệu và huấn luyện lại

**Thời gian:** 20/07 - 26/07/2026

#### Mục tiêu

- Phân tích nguyên nhân mô hình cho kết quả kém
- Xây dựng bộ dữ liệu mô phỏng hành vi mua sắm thật
- Huấn luyện lại và so sánh chỉ số hai phiên bản
- Xử lý sự cố bảo mật phát sinh trong quá trình bàn giao

#### Công việc đã thực hiện

Phân tích lại bộ dữ liệu đầu tiên và nhận ra nguyên nhân: thuật toán lọc cộng tác
hoạt động bằng cách tìm các nhóm người dùng có hành vi tương tự. Nếu mọi người
đều tương tác ngẫu nhiên thì không tồn tại nhóm nào để tìm. Đổi thuật toán không
giải quyết được vấn đề này.

Viết lại chương trình sinh dữ liệu, mô phỏng năm đặc điểm của hành vi thật: gom
theo phiên truy cập, phễu chuyển đổi xem rồi thêm giỏ rồi mua, phân phối
power-law, nhịp theo giờ trong ngày, và phân khúc người dùng theo sở thích. Kết
quả là 23.377 lượt tương tác của 200 người dùng.

Huấn luyện lại trên cùng recipe và so sánh chỉ số với phiên bản trước. Chuyển
campaign sang solution version mới.

Trong quá trình bàn giao mã nguồn, phát hiện một gói source chia sẻ qua dịch vụ
lưu trữ đám mây có chứa file cấu hình với access key AWS. Thu hồi khoá ngay và
thay đổi quy trình bàn giao.

#### Kết quả đạt được

Chỉ số cải thiện rõ rệt trên toàn bộ các phép đo:

| Chỉ số | Dữ liệu v1 | Dữ liệu v2 | Cải thiện |
|---|---|---|---|
| Precision@5 | 0,0889 | 0,4348 | 4,9 lần |
| NDCG@10 | 0,1799 | 0,6512 | 3,6 lần |
| MRR@25 | 0,1216 | 0,7130 | 5,9 lần |
| Coverage | 0,8218 | 0,9505 | tăng 15,7% |

Kết luận: chất lượng dữ liệu huấn luyện quyết định hiệu năng mô hình nhiều hơn
việc lựa chọn thuật toán.

#### Khó khăn và cách xử lý

Sự cố lộ access key là bài học đáng nhớ nhất. Mức độ ảnh hưởng thấp vì khoá đó
chỉ có quyền đọc, và đó chính là kết quả của việc áp dụng nguyên tắc quyền tối
thiểu từ đầu. Bài học: nguyên tắc này không ngăn được sai sót, nhưng quyết định
mức độ thiệt hại khi sai sót xảy ra. Nhóm chuyển sang quản lý mã nguồn tập trung
trên Git thay vì chia sẻ file nén.
