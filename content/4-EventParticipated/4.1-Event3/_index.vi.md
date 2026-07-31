---
title: "Sự kiện 3"
date: 2026-07-25
weight: 3
chapter: false
---

## Buổi Sinh Hoạt Chuyên Đề Nội Bộ — Ứng Dụng Agentic AI Trên AWS (25/07/2026)

**Hình thức:** Buổi báo cáo chia sẻ kiến thức nội bộ
**Phạm vi:** Ứng dụng Agentic AI trên nền tảng AWS (Amazon Bedrock, SageMaker, hệ thống Multi-Agent)
**Số lượng dự án:** 04
**Thời gian:** 25/07/2026
**Địa điểm:** Tầng 26, tòa nhà Bitexco, số 02 đường Hải Triều, phường Sài Gòn, thành phố Hồ Chí Minh
**Vai trò:** Người tham dự

Buổi báo cáo tập trung vào **Agentic AI** — làn sóng AI thế hệ mới có khả năng tự chủ phân tích, ra quyết định và thực thi quy trình kinh doanh. Thông qua 4 dự án tiêu biểu, buổi meeting minh họa cách kết hợp các dịch vụ hạ tầng AWS (Amazon Bedrock, SageMaker) với mô hình Đa Agent để giải quyết các bài toán từ an ninh công cộng, kỹ thuật hạ tầng đến chiến lược kinh doanh và tuân thủ tài chính.

![Ảnh tham dự](/fcaj-report/images/4-Events/events-seminar-2.jpg)

### Dự án 1 — S.H.E.P.H.E.R.D (Đội 3KA)

Quản lý và giám sát đám đông thông minh tại các sự kiện hoặc địa điểm công cộng.

**Thách thức:** Giám sát thủ công truyền thống thường chậm, khó mở rộng và dễ bỏ sót sự cố khi điều kiện môi trường thay đổi nhanh.

**Giải pháp:** Phân tích video trực tiếp để chuyển dữ liệu hình ảnh thành thông tin vận hành — đo mật độ đám đông, ước tính thời gian hàng đợi, dự báo áp lực quá tải — sử dụng YOLO + ByteTrack để theo dõi đối tượng, xử lý trên Amazon SageMaker và Amazon Bedrock AgentCore.

**Cấu trúc AI Agent:**
- *Autonomous Monitor* — tự động theo dõi và phát cảnh báo kịp thời.
- *Operator Copilot* — trợ lý hỗ trợ nhân viên truy vấn bằng ngôn ngữ tự nhiên để nhận thông tin thực tế từ hệ thống.

### Dự án 2 — SA Professional Native App (Đội Plan V)

Ứng dụng "AI-native" tự động hóa các tác vụ chuyên môn cho Kiến trúc sư Giải pháp (Solutions Architect).

**Thách thức:** SA mất nhiều thời gian thực hiện thủ công: bóc tách yêu cầu, vẽ sơ đồ, tính chi phí, viết mã hạ tầng (IaC).

**Giải pháp:**
- Nhận yêu cầu bằng ngôn ngữ tự nhiên và tự động vẽ sơ đồ kiến trúc trên Draw.io với biểu tượng AWS chuẩn.
- Tự động ước tính chi phí vận hành cho khu vực Singapore (`ap-southeast-1`).
- Tự động khởi tạo mã hạ tầng (IaC).

**Giá trị:** Rút ngắn thời gian từ ý tưởng sơ khai thành bản thảo kiến trúc hoàn chỉnh chỉ trong vài phút.

### Dự án 3 — Signal Scout (Đội Dream AI)

Hệ thống hỗ trợ ra quyết định chiến lược bằng cách tự động phát hiện và tổng hợp các "tín hiệu" biến động từ doanh nghiệp.

**Giá trị cốt lõi:** Xâu chuỗi các chỉ số rời rạc thành câu chuyện hoàn chỉnh, giúp lãnh đạo quyết định "Duy trì, Thích nghi hoặc Tăng tốc" dựa trên bằng chứng cụ thể.

**Chức năng chính:** Nhận biết sớm tín hiệu tái cấu trúc, phân tích sức khỏe tài chính/vận hành, mô phỏng kịch bản rủi ro trên bảng điều khiển trung tâm (Executive Dashboard).

**Chi phí vận hành:** Ước tính $81–$359/tháng tùy quy mô, kết hợp hạ tầng AWS với công cụ bổ trợ như Apify, Langfuse.

### Dự án 4 — Adaptive AML/KYT Workflow Engine

Tự động hóa quy trình Chống rửa tiền (AML) và Thấu hiểu giao dịch (KYT) trong lĩnh vực tài chính - ngân hàng.

**Thách thức:** Kiểm tra thủ công tốn trung bình 3 giờ/ca, tỷ lệ báo động giả (False Positives) lên đến 90–95%.

**Giải pháp Multi-Agent:** Chia tách nhiệm vụ chuyên biệt — *Profile Checking Agent* (kiểm tra hồ sơ khách hàng) và *Money Flow Agent* (phân tích dòng tiền).

**Quy trình & lợi ích:** Luồng tự động Phát hiện → Điều tra → Đề xuất → Thực thi, áp dụng mô hình Human-in-the-loop (con người giữ vai trò phê duyệt cuối). Rút ngắn thời gian xử lý xuống còn vài phút, đảm bảo minh bạch nhờ trích dẫn nguồn bằng chứng rõ ràng.

---

### Bài Học Rút Ra

1. **Multi-Agent là chìa khóa cho quy trình phức tạp** — chia nhỏ bài toán cho các Agent chuyên biệt (như AML/KYT hay S.H.E.P.H.E.R.D) giúp nâng cao độ chính xác và giảm sai sót so với dùng một LLM đơn lẻ.
2. **Nguyên tắc Human-in-the-loop** — với lĩnh vực nhạy cảm như tài chính hay bảo mật, AI Agent thu thập-phân tích-đề xuất, con người giữ quyền quyết định cuối.
3. **Tính minh bạch và trích dẫn nguồn** — ứng dụng AI doanh nghiệp cần bằng chứng rõ ràng để xây dựng niềm tin với người dùng.
4. **Tối ưu chi phí vận hành** — kết hợp linh hoạt dịch vụ AWS với công cụ bên thứ ba giúp kiểm soát chi phí hàng tháng hợp lý.

### Kế Hoạch Ứng Dụng Bản Thân

1. Tìm hiểu mẫu thiết kế Multi-Agent (chia nhỏ tác vụ, chuyên biệt hóa từng agent) để cân nhắc áp dụng vào luồng xử lý request của hệ thống recommendation nhóm em đang xây.
2. Tìm hiểu Amazon Bedrock AgentCore như một cách bổ sung giao diện vận hành bằng ngôn ngữ tự nhiên trên nền hạ tầng AWS hiện có.
3. Áp dụng nguyên tắc Human-in-the-loop khi thiết kế bất kỳ thành phần ra quyết định tự động nào ảnh hưởng trực tiếp tới người dùng thật hoặc tiền thật.
