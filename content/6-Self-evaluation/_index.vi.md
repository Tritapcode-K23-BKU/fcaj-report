---
title: "Tự đánh giá"
date: 2026-07-29
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

#### Tổng quan

Kỳ thực tập tại First Cloud AI Journey là lần đầu tiên em làm việc với hạ tầng
đám mây thật, nơi mọi thao tác sai đều để lại hậu quả thật. Phần tự đánh giá này
em viết theo hướng thẳng thắn, ghi cả những chỗ làm được lẫn những chỗ chưa tốt.

#### Kiến thức chuyên môn

Trước kỳ thực tập, hiểu biết của em về điện toán đám mây dừng ở mức khái niệm:
biết đám mây là thuê máy chủ của người khác, biết tên một vài dịch vụ, nhưng
chưa từng dựng một hệ thống hoàn chỉnh.

Sau kỳ thực tập, em đã tự triển khai được một hệ thống chạy thật trên Internet
gồm bảy dịch vụ AWS kết nối với nhau. Quan trọng hơn số lượng dịch vụ là việc em
hiểu **vì sao** chọn dịch vụ này chứ không phải dịch vụ kia. Ví dụ, em có thể
giải thích tại sao dùng DynamoDB thay vì RDS cho bài toán này, và tại sao mô
hình CLIP không đưa lên Lambda được.

Điểm em thấy mình còn yếu là phần mạng. Kiến trúc dự án là serverless nên gần
như không đụng tới VPC, subnet, security group. Đây là mảng em cần tự bổ sung.

#### Kỹ năng giải quyết vấn đề

Đây là phần em thấy mình tiến bộ rõ nhất, và cũng là phần khó đo bằng chứng chỉ.

Giai đoạn đầu, khi hệ thống báo lỗi em thường thử ngẫu nhiên cho tới khi chạy
được, xong cũng không biết vì sao nó chạy. Về sau em hình thành thói quen đọc
thông báo lỗi kỹ, xác định lỗi thuộc lớp nào, rồi kiểm tra từng lớp một từ trong
ra ngoài.

Một ví dụ cụ thể: có lần sau khi tải bản build mới lên S3 thì trang web hiển thị
trắng. Em mất khá nhiều thời gian kiểm tra lại mã nguồn trước khi nhận ra nguyên
nhân là CloudFront vẫn phục vụ bản cũ trong bộ nhớ đệm. Lần sau gặp hiện tượng
tương tự, em kiểm tra cache trước tiên.

#### Tinh thần tự học

Chương trình vận hành theo hình thức tự học, không có ai chỉ từng bước. Ban đầu
em thấy khó vì quen được hướng dẫn chi tiết. Nhưng chính điều đó buộc em phải
đọc tài liệu chính thức của AWS thay vì tìm lời giải có sẵn.

Em cũng nhận ra khác biệt giữa **làm cho hệ thống chạy được** và **hiểu vì sao
nó chạy được**. Có những phần em làm theo hướng dẫn và hệ thống chạy đúng, nhưng
khi gặp lỗi lại không biết bắt đầu từ đâu. Về sau em dành thời gian đọc lại mã
nguồn và tự dựng lại từng thành phần nhỏ, khả năng xử lý sự cố cải thiện rõ rệt.

#### Làm việc nhóm

Em đảm nhận vai trò Cloud Architect trong nhóm năm người, phụ trách hạ tầng và
các quyết định kiến trúc, đồng thời triển khai mã nguồn của các thành viên khác
lên môi trường thật.

Việc em làm tốt là phát hiện sớm chỗ lệch hợp đồng dữ liệu giữa giao diện và máy
chủ, và chọn giải pháp lớp trung gian thay vì bắt hai bên sửa chéo. Cách này giữ
được phần đã kiểm thử của cả hai người.

Việc em làm chưa tốt là **không thống nhất quy ước dữ liệu với cả nhóm ngay từ
đầu**. Hệ quả là pipeline của bạn phụ trách dữ liệu sinh ra định danh khác với
catalog thật, dẫn tới không nạp vào mô hình được. Bạn ấy phải chủ động nhắn hỏi
em mới phát hiện ra. Nếu làm lại, em sẽ dành một buổi đầu dự án để chốt bằng văn
bản định dạng dữ liệu trao đổi giữa các phần.

#### Ý thức bảo mật và chi phí

Trong quá trình bàn giao mã nguồn, nhóm đã để lọt một access key AWS vào gói
source chia sẻ qua dịch vụ lưu trữ đám mây. Mức độ ảnh hưởng thấp vì khoá đó chỉ
có quyền đọc, nhưng đây vẫn là sự cố bảo mật thật.

Em rút ra được bài học mà lý thuyết không dạy được: nguyên tắc quyền tối thiểu
không ngăn được sai sót của con người, nhưng quyết định mức độ thiệt hại khi sai
sót xảy ra. Sau sự cố, nhóm chuyển sang quản lý mã nguồn tập trung trên Git và
cấp tài khoản riêng có giới hạn cho từng người.

Về chi phí, em học được rằng không phải dịch vụ nào cũng tính phí theo mức sử
dụng. Personalize campaign tính phí theo giờ tồn tại bất kể có truy vấn hay
không. Điều này thay đổi cách em nghĩ về việc dọn dẹp tài nguyên.

#### Bảng tự chấm

| Tiêu chí | Mức độ | Ghi chú |
|---|---|---|
| Kiến thức dịch vụ AWS cốt lõi | Khá | Vững phần serverless, còn yếu phần mạng |
| Khả năng thiết kế kiến trúc | Khá | Biết cân nhắc đánh đổi, chưa có kinh nghiệm quy mô lớn |
| Kỹ năng chẩn đoán sự cố | Khá | Tiến bộ rõ so với đầu kỳ |
| Tinh thần tự học | Tốt | Chủ động đọc tài liệu gốc |
| Làm việc nhóm | Trung bình khá | Thiếu sót ở khâu thống nhất quy ước từ đầu |
| Ý thức bảo mật | Khá | Có nền tảng đúng, cần cẩn thận hơn khi chia sẻ file |

#### Kế hoạch tiếp theo

Em dự định học tiếp để thi chứng chỉ **AWS Solutions Architect Associate**,
đồng thời tự dựng lại một dự án nhỏ từ đầu để kiểm chứng những gì đã học. Về
phần còn yếu, em sẽ tập trung vào mạng trong AWS và các dịch vụ container.
