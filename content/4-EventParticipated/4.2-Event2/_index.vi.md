---
title: "Sự kiện 2"
date: 2026-07-09
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Báo cáo sự kiện: "AWS First Cloud Journey: Từ Virtualization, Serverless đến AI trong An toàn thông tin"

### Thông tin sự kiện

| Thông tin | Chi tiết |
| :--- | :--- |
| **Tên sự kiện** | AWS First Cloud Journey: From Virtualization and Serverless to AI in Security |
| **Thời gian** | 09/07/2026 |
| **Địa điểm** | Workshop First Cloud AI Journey |
| **Vai trò** | Người tham dự |

### Mục tiêu sự kiện

- Tìm hiểu hành trình chuyển đổi lên nền tảng điện toán đám mây với AWS.
- Tìm hiểu kiến trúc hệ thống hiện đại thông qua việc so sánh Virtualization (Virtual Machine) và Containerization (Docker).
- Phân tích những thách thức thực tế khi triển khai kiến trúc Serverless với AWS Lambda và DynamoDB.
- Tìm hiểu cách ứng dụng Machine Learning kết hợp AWS WAF để xây dựng hệ thống phát hiện xâm nhập mạng (NIDS).
- Định hướng nghề nghiệp và chia sẻ kinh nghiệm phát triển từ Helpdesk/Sysadmin đến DevOps Engineer.

### Diễn giả

- **09:20 - 10:00 | Nguyễn Quốc Bảo**
- **10:00 - 10:35 | Nguyễn Huỳnh Quốc Bảo**
- **10:35 - 10:50 | Việt Phát**
- **10:50 - 11:10 | Lê Hoàng Gia Đại** – Chủ đề: **AWS WAF kết hợp Machine Learning trong phát hiện tấn công mạng**
- **11:10 - 12:00 | Trần Trung Vinh** – Chủ đề: **Hành trình từ Sysadmin đến DevOps và kinh nghiệm phỏng vấn tại Central Retail Group**

> *Các nội dung về Containers và Serverless được trình bày xuyên suốt trong các phiên chia sẻ của anh Nguyễn Quốc Bảo, anh Nguyễn Huỳnh Quốc Bảo và anh Việt Phát.*

---

### Nội dung chính

#### 1. Cuộc chiến kiến trúc: Virtual Machines và Containers

- **Sự khác biệt cốt lõi:** Máy ảo (Virtual Machine) là mô hình "Heavyweight" vì mỗi máy ảo đều cần một Guest Operating System chạy trên Hypervisor, dẫn đến thời gian khởi động lâu và tiêu tốn nhiều tài nguyên. Trong khi đó, Containers (Docker) hoạt động theo mô hình "Lightweight", chia sẻ Host Operating System nên khởi động rất nhanh và sử dụng tài nguyên hiệu quả hơn.

- **Khả năng tối ưu:** Containers giúp đóng gói toàn bộ ứng dụng cùng thư viện phụ thuộc vào một môi trường thống nhất, mang lại hiệu năng gần như Native, giảm mức sử dụng RAM và cho phép triển khai hàng trăm đến hàng nghìn Container trên cùng một hạ tầng.

#### 2. Những thách thức khi triển khai Serverless (AWS Lambda & DynamoDB)

- **Quản lý trạng thái (Stateless Lambda):** AWS Lambda không lưu trữ trạng thái giữa các lần thực thi. Toàn bộ dữ liệu cần được lưu trữ và truy xuất từ DynamoDB, đòi hỏi kiến trúc hệ thống phải được thiết kế hợp lý nhằm giảm độ trễ.

- **Chi phí khi sử dụng DynamoDB:** Việc sử dụng `ScanCommand` để quét toàn bộ bảng dữ liệu sẽ làm tăng chi phí cũng như thời gian xử lý khi hệ thống phát triển lớn hơn. Vì vậy cần sử dụng Query và Index để tối ưu hiệu năng.

- **Kết nối không còn hiệu lực (GoneException):** Cần xử lý tốt các kết nối bị ngắt nhằm tránh gửi dữ liệu không cần thiết và đảm bảo hệ thống Matchmaking hoạt động ổn định.

#### 3. AWS WAF kết hợp Machine Learning trong hệ thống phát hiện xâm nhập mạng

**Diễn giả:** Lê Hoàng Gia Đại

- **Giới hạn của phương pháp phát hiện theo Signature:** Các luật WAF truyền thống không còn đủ hiệu quả trước các hình thức tấn công hiện đại như Zero-day hoặc các hành vi bất thường.

- **Giải pháp NIDS sử dụng Machine Learning:** Áp dụng mô hình học máy để phát hiện bất thường dựa trên hành vi. Mô hình được huấn luyện bằng bộ dữ liệu chuẩn **CSE-CIC-IDS2018**.

- **Quy trình triển khai:** Xây dựng Dashboard giám sát thời gian thực, sau đó kết hợp kết quả dự đoán của NIDS với các sự kiện từ AWS WAF nhằm nâng cao khả năng phát hiện tấn công trên môi trường Cloud.

#### 4. Hành trình từ Sysadmin đến DevOps

**Diễn giả:** Trần Trung Vinh

- **Thay đổi tư duy:** Cloud không chỉ là một công nghệ mới mà còn là một phương pháp làm việc mới, chuyển từ việc cấu hình thủ công sang tự động hóa hạ tầng bằng Infrastructure as Code.

- **Kinh nghiệm phỏng vấn:** Diễn giả chia sẻ nhiều kinh nghiệm thực tế trong quá trình phỏng vấn tại các doanh nghiệp lớn như Central Retail Group cũng như những kỹ năng cần chuẩn bị để phát triển nghề nghiệp.

---

### Những điều em học được

#### Về tư duy kiến trúc hệ thống và Cloud

- **Lựa chọn đúng công nghệ cho từng bài toán:** Không có công nghệ nào phù hợp với mọi tình huống. Việc lựa chọn Virtual Machine hay Container cần dựa trên yêu cầu về chi phí, hiệu năng và khả năng mở rộng của hệ thống.

- **Tư duy DevOps:** Hạ tầng hiện nay được quản lý như mã nguồn (Infrastructure as Code), trong đó tự động hóa và giám sát hệ thống đóng vai trò rất quan trọng.

#### Về tư duy hiện đại trong An toàn thông tin

Buổi chia sẻ giúp em hiểu rõ hơn về giới hạn của các luật bảo mật truyền thống. Trong bối cảnh các hình thức tấn công ngày càng phức tạp, việc kết hợp AI và Machine Learning vào các hệ thống bảo mật là xu hướng tất yếu nhằm phát hiện những hành vi bất thường mà các luật cố định không thể nhận biết.

---

### Kế hoạch áp dụng

- **Đóng gói các dự án cá nhân bằng Docker:** Thay vì chạy trực tiếp các ứng dụng Java (Spring Boot) hoặc Python (Flask) trên máy chủ, em sẽ xây dựng Dockerfile để đóng gói ứng dụng nhằm đơn giản hóa quá trình triển khai.

- **Nâng cao tư duy về bảo mật:** Những kiến thức về AWS WAF kết hợp Machine Learning giúp em có thêm ý tưởng để áp dụng vào hệ thống Wazuh SIEM cũng như dự án nghiên cứu về phòng chống Session Hijacking và Session Fixation.

- **Kiểm soát chi phí trên AWS:** Bài học về chi phí khi sử dụng DynamoDB Scan giúp em cẩn trọng hơn trong quá trình thiết kế cơ sở dữ liệu nhằm tối ưu chi phí và tận dụng hiệu quả AWS Free Tier.

---

### Cảm nhận sau sự kiện

Sự kiện AWS First Cloud Journey mang đến góc nhìn rất thực tế về các công nghệ Cloud hiện đại thay vì chỉ dừng lại ở lý thuyết.

#### Góc nhìn kỹ thuật

Việc được tìm hiểu các kiến trúc hệ thống đang được triển khai trong doanh nghiệp giúp em hình dung rõ hơn con đường phát triển trở thành System Engineer hoặc Security Engineer trong tương lai. Những phân tích về hạn chế của kiến trúc Serverless cũng giúp em hiểu sâu hơn về việc thiết kế hệ thống trên nền tảng AWS.

#### Định hướng nghề nghiệp

Phần chia sẻ của anh Trần Trung Vinh về hành trình phát triển từ Helpdesk đến Sysadmin và DevOps đã mang đến cho em nhiều động lực. Qua đó em hiểu rõ hơn những kỹ năng cần chuẩn bị như Hệ điều hành, Mạng máy tính, Cloud Computing và Automation để đáp ứng yêu cầu tuyển dụng của doanh nghiệp.

#### Không khí sự kiện

Buổi Workshop được tổ chức trong không khí chuyên nghiệp nhưng rất cởi mở. Những ví dụ thực tế về việc ứng dụng AI vào AWS WAF đã mở ra cho em nhiều ý tưởng mới trong quá trình nghiên cứu và học tập về An toàn thông tin.

---

### Hình ảnh sự kiện

<img src="/images/4-EventParticipated/4.2-Event2/anh1.jpg" alt="Mô tả ảnh" width="800px">
<img src="/images/4-EventParticipated/4.2-Event2/anh2.jpg" alt="Mô tả ảnh" width="800px">
<img src="/images/4-EventParticipated/4.2-Event2/anh3.jpg" alt="Mô tả ảnh" width="800px">
<img src="/images/4-EventParticipated/4.2-Event2/anh4.jpg" alt="Mô tả ảnh" width="800px">
<img src="/images/4-EventParticipated/4.2-Event2/anh5.jpg" alt="Mô tả ảnh" width="800px">
<img src="/images/4-EventParticipated/4.2-Event2/anh6.jpg" alt="Mô tả ảnh" width="800px">
> Tóm lại, sự kiện là cầu nối giữa những kiến thức về Quản trị mạng và An toàn thông tin mà em đang được học tại trường với các tiêu chuẩn Cloud hiện đại trong doanh nghiệp. Buổi chia sẻ không chỉ giúp em hiểu rõ hơn về các công nghệ như Container, Serverless, AWS WAF và Machine Learning, mà còn củng cố quyết tâm theo đuổi lĩnh vực hạ tầng mạng, điện toán đám mây và an toàn thông tin, đồng thời định hướng cho em trong việc ứng dụng AI vào các giải pháp bảo mật trong tương lai.