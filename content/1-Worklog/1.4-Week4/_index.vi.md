---
title: "Worklog Tuần 4"
date: 2026-10-12
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4

Tìm hiểu Amazon RDS, Amazon Lightsail, Amazon EC2 Auto Scaling và Amazon CloudWatch qua các workshop của First Cloud Journey. Vận dụng phần EC2, IAM role và load balancer đã học để thực hành kết nối cơ sở dữ liệu, mở rộng ứng dụng và theo dõi hoạt động hệ thống.

### Kế hoạch học tập và thực hành

| Buổi | Công việc | Ngày bắt đầu dự kiến | Ngày hoàn thành dự kiến | Tài liệu chính |
| --- | --- | --- | --- | --- |
| 1 | Tìm hiểu RDS, database engine, DB instance và endpoint; chuẩn bị DB subnet group, cấu hình kết nối từ EC2, tạo cơ sở dữ liệu và kiểm tra sao lưu, khôi phục theo workshop. | 12/10/2026 | 12/10/2026 | [Tạo cơ sở dữ liệu với Amazon RDS](https://000005.awsstudygroup.com/) |
| 2 | Tìm hiểu gói tài nguyên và blueprint của Lightsail; chọn một ứng dụng mẫu trong workshop để triển khai, cấu hình mạng, kiểm tra truy cập, tạo snapshot và đọc cách nâng cấp instance. | 13/10/2026 | 13/10/2026 | [Tối ưu chi phí với Amazon Lightsail](https://000045.awsstudygroup.com/) |
| 3 | Tạo launch template và Auto Scaling Group; tích hợp với load balancer, đặt minimum, desired, maximum capacity; kiểm tra manual, scheduled và dynamic scaling, đọc phần predictive scaling. | 14/10/2026 | 14/10/2026 | [Mở rộng ứng dụng với EC2 Auto Scaling](https://000006.awsstudygroup.com/) |
| 4 | Xem metrics, tìm hiểu log groups và log streams; thực hành Logs Insights, metric filters, alarms và dashboard; quan sát dữ liệu khi kiểm tra hoạt động của ứng dụng và scaling. | 15/10/2026 | 15/10/2026 | [Giám sát hệ thống với CloudWatch](https://000008.awsstudygroup.com/) |
| 5 | Tổng hợp cấu hình, cách kiểm tra và kết quả quan sát của từng bài; giải thích vai trò của bốn dịch vụ, dọn tài nguyên theo hướng dẫn và kiểm tra tài nguyên còn lại. | 16/10/2026 | 16/10/2026 | [Khám phá các dịch vụ AWS](https://cloudjourney.awsstudygroup.com/1-explore/) |

### Kiến thức và kỹ năng dự kiến đạt được

#### Amazon RDS

Hiểu vai trò của dịch vụ cơ sở dữ liệu quan hệ được quản lý và phân biệt database engine, DB instance, endpoint, cổng kết nối. Biết các phần cần chuẩn bị để ứng dụng trên EC2 kết nối được với cơ sở dữ liệu, gồm mạng, security groups và thông tin đăng nhập.

Thực hành tạo DB instance theo workshop, lấy endpoint và kiểm tra kết nối từ ứng dụng. Khi kết nối không thành công, có thể kiểm tra trạng thái database, endpoint, cổng và quy tắc mạng theo trình tự. Tìm hiểu cách sao lưu, tạo snapshot và khôi phục dữ liệu trong phạm vi bài lab.

#### Amazon Lightsail

Hiểu cách Lightsail cung cấp gói tài nguyên và các blueprint để triển khai máy chủ hoặc ứng dụng. Biết xem tài nguyên của gói, phạm vi sử dụng và các thành phần có thể phát sinh chi phí trước khi lựa chọn.

Thực hành triển khai một ứng dụng mẫu, kiểm tra cấu hình mạng và truy cập từ trình duyệt. Tìm hiểu snapshot và quy trình tạo instance lớn hơn từ snapshot để nâng cấp tài nguyên. Có thể giải thích khi nào cách triển khai đơn giản của Lightsail phù hợp với một website hoặc ứng dụng nhỏ.

#### Amazon EC2 Auto Scaling

Hiểu launch template lưu các thiết lập khởi chạy, còn Auto Scaling Group quản lý số lượng instance theo minimum, desired và maximum capacity. Phân biệt việc load balancer phân phối yêu cầu với việc Auto Scaling tăng hoặc giảm số lượng máy chủ.

Thực hành tích hợp Auto Scaling Group với load balancer, thay đổi desired capacity và kiểm tra instance mới được đăng ký vào target group. Tiếp tục kiểm tra scheduled và dynamic scaling theo workshop, xem lịch sử hoạt động để xác định thời điểm tăng hoặc giảm instance. Phần predictive scaling tập trung vào đọc cơ chế và metrics được giới thiệu trong tài liệu.

#### Amazon CloudWatch

Phân biệt metrics dùng theo dõi các chỉ số, logs ghi nhận sự kiện, alarms đánh giá điều kiện cảnh báo và dashboards tổng hợp thông tin. Biết lựa chọn khoảng thời gian và tài nguyên khi xem dữ liệu để tránh đọc nhầm biểu đồ.

Thực hành truy vấn log bằng Logs Insights, tìm hiểu chuyển mẫu log thành metric bằng metric filter, cấu hình alarm và tạo dashboard. Kết hợp quan sát metrics với lịch sử scaling để giải thích thay đổi của tải và số lượng instance trong bài lab.

#### Tổng hợp và kiểm tra bài thực hành

Ghi lại các thiết lập chính, cách kiểm tra thành công và cách xử lý vấn đề gặp phải. Sau mỗi workshop, thực hiện dọn tài nguyên và kiểm tra những thành phần còn tồn tại như snapshots hoặc tài nguyên lưu trữ. Mục tiêu là thực hiện được cấu hình cơ bản theo tài liệu và giải thích được kết quả quan sát.

### Tài liệu bổ sung

* [Amazon RDS — Bắt đầu sử dụng](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_GettingStarted.html): tra cứu tạo và kết nối DB instance.
* [Amazon Lightsail — Tổng quan](https://docs.aws.amazon.com/lightsail/latest/userguide/what-is-amazon-lightsail.html): tra cứu gói dịch vụ và các thành phần.
* [EC2 Auto Scaling — Giới hạn dung lượng](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-capacity-limits.html): tra cứu minimum, desired và maximum capacity.
* [Amazon CloudWatch — Tổng quan](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html): tra cứu các chức năng giám sát cơ bản.
