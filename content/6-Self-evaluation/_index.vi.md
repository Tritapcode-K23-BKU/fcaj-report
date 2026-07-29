---
title: "Tự đánh giá"
date: 2026-07-29
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

#### Bảng tự đánh giá

| Tiêu chí | Mức độ | Nhận xét |
|---|---|---|
| Kiến thức | Khá | Vững phần serverless, còn yếu mạng và container |
| Khả năng học hỏi | Tốt | Chủ động đọc tài liệu gốc thay vì tìm lời giải có sẵn |
| Tính chủ động | Tốt | Tự đề xuất cải tiến dữ liệu khi mô hình cho kết quả kém |
| Kỷ luật | Khá | Bám sát tiến độ, nhưng có giai đoạn đầu học chưa có định hướng |
| Giao tiếp | Khá | Diễn đạt được vấn đề kỹ thuật cho người không cùng chuyên môn |
| Teamwork | Trung bình khá | Thiếu sót ở khâu thống nhất quy ước dữ liệu từ đầu |
| Giải quyết vấn đề | Khá | Tiến bộ rõ rệt về khả năng chẩn đoán lỗi theo lớp |
| Đóng góp cho dự án | Tốt | Phụ trách toàn bộ hạ tầng và các quyết định kiến trúc |

#### Nhận xét chi tiết theo từng tiêu chí

**Kiến thức — Khá**

Trước kỳ thực tập, hiểu biết của em về điện toán đám mây dừng ở mức khái niệm.
Sau kỳ thực tập, em triển khai được một hệ thống hoàn chỉnh gồm bảy dịch vụ AWS
kết nối với nhau, và quan trọng hơn là giải thích được **vì sao** chọn dịch vụ
này thay vì dịch vụ kia. Ví dụ em có thể lập luận tại sao dùng DynamoDB thay vì
RDS, và tại sao mô hình CLIP không đưa lên Lambda được.

Điểm còn yếu là mạng. Kiến trúc dự án là serverless nên gần như không đụng tới
VPC, subnet, security group. Đây là mảng em cần tự bổ sung.

**Khả năng học hỏi — Tốt**

Chương trình vận hành theo hình thức tự học, không có ai chỉ từng bước. Ban đầu
em thấy khó vì quen được hướng dẫn chi tiết, nhưng chính điều đó buộc em đọc tài
liệu chính thức của AWS thay vì tìm lời giải có sẵn.

Em cũng nhận ra khác biệt giữa làm cho hệ thống chạy được và hiểu vì sao nó chạy
được. Có những phần em làm theo hướng dẫn và hệ thống chạy đúng, nhưng khi gặp
lỗi lại không biết bắt đầu từ đâu. Sau đó em dành thời gian đọc lại mã nguồn và
tự dựng lại từng thành phần nhỏ.

**Tính chủ động — Tốt**

Khi mô hình gợi ý đầu tiên cho kết quả kém, em không dừng ở việc báo cáo con số
mà tự phân tích nguyên nhân, phát hiện vấn đề nằm ở dữ liệu ngẫu nhiên đều, rồi
đề xuất và thực hiện việc sinh lại bộ dữ liệu mô phỏng hành vi thật. Kết quả cải
thiện từ 2,8 đến 5,9 lần trên các chỉ số.

Em cũng chủ động thiết lập cảnh báo ngân sách và rà soát bảo mật mà không đợi
được yêu cầu.

**Kỷ luật — Khá**

Em bám sát tiến độ đã đề ra và hoàn thành các mốc đúng hạn. Tuy nhiên giai đoạn
hai tuần đầu em học khá lan man vì chưa có đề tài cụ thể, dẫn tới lãng phí thời
gian. Nếu làm lại, em sẽ chốt đề tài sớm hơn để việc học có định hướng.

**Giao tiếp — Khá**

Vai trò Cloud Architect đòi hỏi trao đổi với các thành viên có chuyên môn khác
nhau. Em phải diễn đạt các khái niệm hạ tầng bằng ngôn ngữ đời thường cho bạn
không quen thuật ngữ AWS, và ngược lại phải hiểu yêu cầu từ phía giao diện và dữ
liệu. Đây là kỹ năng em thấy mình làm được nhưng chưa thật sự thuần thục.

**Teamwork — Trung bình khá**

Việc em làm tốt là phát hiện sớm chỗ lệch hợp đồng dữ liệu giữa giao diện và máy
chủ, và chọn giải pháp lớp trung gian thay vì bắt hai bên sửa chéo, giữ được
phần đã kiểm thử của cả hai người.

Việc em làm chưa tốt là không thống nhất quy ước dữ liệu với cả nhóm ngay từ
đầu. Hệ quả là pipeline của bạn phụ trách dữ liệu sinh ra định danh khác với
catalog thật, dẫn tới không nạp vào mô hình được, và bạn ấy phải chủ động nhắn
hỏi em mới phát hiện ra. Đây là thiếu sót của em ở vai trò kiến trúc sư, vì việc
định nghĩa giao diện dữ liệu giữa các phần thuộc trách nhiệm của em.

**Giải quyết vấn đề — Khá**

Giai đoạn đầu, khi hệ thống báo lỗi em thường thử ngẫu nhiên cho tới khi chạy
được, xong cũng không biết vì sao. Về sau em hình thành thói quen đọc thông báo
lỗi kỹ, xác định lỗi thuộc lớp nào, rồi kiểm tra từng lớp từ trong ra ngoài.

Một ví dụ: sau khi tải bản build mới lên S3 thì trang web hiển thị trắng. Em mất
nhiều thời gian kiểm tra mã nguồn trước khi nhận ra CloudFront vẫn phục vụ bản
cũ trong bộ nhớ đệm. Lần sau gặp hiện tượng tương tự, em kiểm tra cache trước.

Một ví dụ khác khó hơn: DynamoDB không đảm bảo trả kết quả theo thứ tự khoá được
truyền vào, khiến thứ hạng do mô hình tính toán bị mất. Lỗi này không sinh ra
thông báo nào, chỉ phát hiện được khi so sánh kỹ dữ liệu trả về.

**Đóng góp cho dự án — Tốt**

Em phụ trách toàn bộ hạ tầng AWS và các quyết định kiến trúc, triển khai mã
nguồn của các thành viên khác lên môi trường thật, xây dựng lớp trung gian xử lý
lệch hợp đồng dữ liệu, thiết lập và cải tiến hệ gợi ý, và quản lý bảo mật cùng
chi phí.

Đóng góp em thấy có giá trị nhất không phải số lượng dịch vụ dựng được, mà là
việc phát hiện ra vấn đề nằm ở dữ liệu chứ không phải thuật toán, và chứng minh
được bằng số liệu định lượng.

#### Hướng phát triển

Em dự định học tiếp để thi chứng chỉ **AWS Solutions Architect Associate**, đồng
thời tự dựng lại một dự án nhỏ từ đầu để kiểm chứng những gì đã học. Về phần còn
yếu, em sẽ tập trung vào mạng trong AWS và các dịch vụ container như ECS, EKS.
