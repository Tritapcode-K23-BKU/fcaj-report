---
title: "Sự kiện 3"
date: 2026-06-06
weight: 4
---

## Buổi Sinh Hoạt Chuyên Đề Nội Bộ — 6 Chuyên Đề (06/06/2026)

**Hình thức:** Buổi báo cáo chia sẻ kiến thức nội bộ
**Phạm vi:** Hạ tầng, Cloud, AI, Game Dev, Kỹ năng mềm
**Số lượng chuyên đề:** 06
**Thời gian:** 06/06/2026

Tôi đã tham dự buổi sinh hoạt chuyên đề nội bộ gồm 6 bài báo cáo, trải dài từ hạ tầng công nghệ, ứng dụng AI/ML, kiến trúc Serverless, đóng gói ứng dụng cho đến kỹ năng làm việc nhóm. Dưới đây là tóm tắt nội dung từng chuyên đề.



### Chuyên đề 1 — AWS WAF & ML NIDS
**Báo cáo viên:** Lê Hoàng Gia Đại

WAF truyền thống phụ thuộc vào bộ quy tắc cố định, dễ bỏ sót tấn công Zero-day hoặc các biến thể hành vi bất thường. Báo cáo viên huấn luyện mô hình LightGBM trên tập dữ liệu chuẩn CSE-CIC-IDS2018, đạt độ chính xác 0.9586 trong phân loại hành vi tấn công mạng, kết hợp với AWS Lambda, Kinesis Data Firehose và Security Hub để phân tích lưu lượng và phát động phản ứng bảo mật tự động theo thời gian thực.

**Bài học:** Chuyển từ bảo mật phản ứng (rule-based) sang bảo mật chủ động bằng AI/ML giúp tăng khả năng phát hiện mối đe dọa Zero-day trên hạ tầng Cloud.

### Chuyên đề 2 — Docker & Containerization
**Báo cáo viên:** Bảo Huỳnh

Container nhẹ hơn nhiều so với VM — khởi động tính bằng miligiây, dùng chung kernel hệ điều hành host nên tối ưu tài nguyên. Quy trình chuẩn: định nghĩa môi trường trong `Dockerfile` → build thành image immutable → khởi tạo container độc lập, nhất quán. Đây là nền tảng cho kiến trúc Microservices và CI/CD, hiện thực triết lý "build once, run anywhere", xóa khoảng cách môi trường Dev/Production.

**Bài học:** Containerization là chuẩn mực bắt buộc để đóng gói, triển khai và mở rộng phần mềm hiện đại.

### Chuyên đề 3 — Từ IT Helpdesk đến Senior Sysadmin
**Báo cáo viên:** Trần Trung Vinh

Lộ trình từ Helpdesk (xử lý sự cố, giao tiếp người dùng) đến Sysadmin chuyên nghiệp rồi Cloud/DevOps Engineer. Tư duy Sysadmin chuẩn mực: tự động hóa việc lặp lại, tài liệu hóa quy trình, không bao giờ thử nghiệm trực tiếp trên Production. Khi chuyển sang Cloud/DevOps là chuyển tư duy từ quản trị server vật lý sang hạ tầng auto-scaling, pay-as-you-go và Infrastructure as Code (IaC). Lời khuyên: ưu tiên trải nghiệm thực chiến hơn là tích lũy chứng chỉ lý thuyết.

**Bài học:** Kỹ năng giao tiếp, tư duy tự động hóa và kinh nghiệm thực chiến là chìa khóa thăng tiến trong ngành hạ tầng IT.

### Chuyên đề 4 — Multiplayer với AWS WebSockets trong Godot
**Báo cáo viên:** Nguyễn Quốc Bảo

Kiến trúc Serverless cho game multiplayer, kết hợp Godot với API Gateway (WebSocket) duy trì kết nối hai chiều, AWS Lambda xử lý game logic, và DynamoDB quản lý trạng thái người chơi. So sánh UDP (game hành động tốc độ cao) với WebSocket (game theo lượt, lobby, chat nội bộ), đồng thời xử lý bài toán ngắt kết nối ngầm (stale connections) và tối ưu chi phí bằng cách giảm thao tác Scan trên DynamoDB.

**Bài học:** Serverless kết hợp WebSocket giúp phát triển game multiplayer với chi phí vận hành ban đầu thấp và khả năng tự mở rộng linh hoạt.

### Chuyên đề 5 — Nghệ Thuật Làm Việc Nhóm Hiệu Quả
**Báo cáo viên:** Trương Huy Phước

Bốn quy tắc vàng: (1) xác định mục tiêu chung rõ ràng, đo lường được; (2) đặt đúng người vào đúng vị trí phù hợp năng lực; (3) giao tiếp cởi mở, chủ động lắng nghe; (4) nâng cao trách nhiệm cá nhân với sản phẩm chung. Ngoài ra là hệ sinh thái công cụ hỗ trợ minh bạch tiến độ: Trello, Slack, Discord, ClickUp.

**Bài học:** Kỹ thuật tốt là điều kiện cần, nhưng kỹ năng hợp tác và quy tắc giao tiếp mới là yếu tố quyết định thành công của dự án phần mềm.

### Chuyên đề 6 — GraphRAG với Amazon Bedrock và Neptune
**Báo cáo viên:** Việt Phát

GraphRAG khắc phục nhược điểm của RAG truyền thống nhờ khả năng suy luận đa bước (multi-hop reasoning) và khai thác mối quan hệ ngữ nghĩa giữa các thực thể qua đồ thị tri thức (knowledge graph). Hai hướng triển khai trên AWS: (1) dùng Amazon Bedrock Knowledge Bases kết hợp Neptune Analytics để triển khai nhanh; (2) tự xây pipeline tùy biến bằng LlamaIndex kết hợp Amazon Neptune để tùy chỉnh sâu hơn.

**Bài học:** Đồ thị tri thức là bước tiến quan trọng nâng cao chất lượng và độ chính xác của ứng dụng Generative AI phức tạp trong doanh nghiệp.

---

### Kế Hoạch Ứng Dụng Bản Thân

**Ngắn hạn (1–2 tháng)**
- Thực hành đóng gói ứng dụng cá nhân/dự án hiện tại bằng Docker và Docker Compose để chuẩn hóa môi trường Dev.
- Áp dụng công cụ quản lý dự án (Trello/ClickUp) vào làm việc nhóm theo 4 quy tắc vàng đã học.

**Trung hạn (3–6 tháng)**
- Tìm hiểu chi tiết tích hợp AWS Lambda, API Gateway WebSocket cho bài toán Real-time Data.
- Nghiên cứu ứng dụng LightGBM và các mô hình ML cơ bản trong phân tích log hệ thống.

**Dài hạn (6–12 tháng)**
- Xây dựng thử nghiệm mô hình GraphRAG kết hợp LlamaIndex để quản lý tri thức nội bộ.
- Rèn luyện tư duy Infrastructure as Code (IaC) để chuẩn bị cho lộ trình thăng tiến DevOps/Cloud Engineer.

![Ảnh tham dự](/images/4-Events/events-seminar-1.jpg)