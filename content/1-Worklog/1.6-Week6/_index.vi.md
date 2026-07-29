---
title: "Tuần 6"
date: 2026-07-29
weight: 6
chapter: false
pre: " <b> 1.6 </b> "
---

#### Tuần 6 — Tích hợp giao diện với API thật

**Thời gian:** 06/07 - 12/07/2026

#### Mục tiêu

- Nối toàn bộ giao diện React với API thật
- Xử lý lệch hợp đồng dữ liệu giữa giao diện và máy chủ
- Triển khai giao diện lên S3 và CloudFront
- Kiểm tra các luồng nghiệp vụ đầu cuối

#### Công việc đã thực hiện

Trong quá trình tích hợp phát hiện giao diện và máy chủ được phát triển song song
nên hợp đồng dữ liệu lệch nhau ở nhiều điểm: phương thức thanh toán, trạng thái
đơn hàng, tên trường giá và mã giảm giá đều khác nhau.

Cân nhắc ba phương án: sửa máy chủ, sửa giao diện, hoặc chèn lớp trung gian. Chọn
phương án thứ ba vì giữ nguyên được phần đã kiểm thử của cả hai bên. Toàn bộ việc
chuyển đổi được tập trung vào một file duy nhất, dịch dữ liệu theo cả hai chiều.

Build giao diện, tải lên S3 và tạo invalidation cho CloudFront. Kiểm tra các
luồng: đăng ký, đăng nhập, duyệt sản phẩm, thêm giỏ, áp mã giảm giá, đặt hàng,
xem lịch sử đơn.

#### Kết quả đạt được

- Website hoàn chỉnh chạy trên CloudFront với đầy đủ luồng nghiệp vụ
- Lớp trung gian xử lý lệch hợp đồng, ranh giới giữa hai tầng trở nên tường minh
- Máy chủ tính lại tổng tiền phía server, không tin dữ liệu từ trình duyệt

#### Khó khăn và cách xử lý

Khối lượng công việc để nối các phần do nhiều người viết lớn hơn nhiều so với dự
tính. Bài học rút ra là hợp đồng dữ liệu giữa các tầng cần được thống nhất bằng
văn bản ngay từ đầu, trước khi bất kỳ bên nào bắt đầu viết mã.
