---
title: "Worklog Tuần 3"
date: 2026-10-05
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3

Tiếp tục sử dụng EC2 để tìm hiểu quản lý dữ liệu, phân quyền cho ứng dụng và cân bằng tải. Nội dung tập trung vào EBS snapshots, AMI, IAM roles và Application Load Balancer; vận dụng máy chủ đã làm quen ở tuần 1 để thực hiện các cấu hình phục vụ một ứng dụng web đơn giản.

### Công việc trong tuần

| Buổi | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu chính |
| --- | --- | --- | --- | --- |
| 1 | Tìm hiểu sự khác nhau giữa EBS và instance store; thực hành mount volume đã gắn, kiểm tra dữ liệu và tạo EBS snapshot để sao lưu. | 05/10/2026 | 05/10/2026 | [Amazon EC2](https://000004.awsstudygroup.com/) |
| 2 | Tìm hiểu IAM user, role, policy và nguyên tắc cấp quyền vừa đủ; đọc các thành phần Effect, Action, Resource trong policy và phân biệt trust policy với permissions policy. | 06/10/2026 | 06/10/2026 | [Quản lý truy cập với IAM](https://000002.awsstudygroup.com/) |
| 3 | Tạo IAM role cho EC2 với quyền đọc S3, gắn role vào instance và kiểm tra truy cập bằng CLI trên máy chủ mà không lưu access key riêng trên instance. | 07/10/2026 | 07/10/2026 | [Cấp quyền cho ứng dụng qua IAM role](https://000048.awsstudygroup.com/) |
| 4 | Triển khai ứng dụng web mẫu trên EC2, kiểm tra cổng dịch vụ và security group; tìm hiểu tạo AMI từ instance để lưu lại môi trường đã cấu hình. | 08/10/2026 | 08/10/2026 | [Amazon EC2](https://000004.awsstudygroup.com/) |
| 5 | Tìm hiểu ALB và NLB ở mức cơ bản; tạo ALB, listener và target group cho các máy chủ web, cấu hình health check và kiểm tra phân phối yêu cầu. | 09/10/2026 | 10/10/2026 | [Phần load balancer trong workshop FCJ](https://000006.awsstudygroup.com/) |

### Kiến thức đã học và kết quả thực hành

#### Lưu trữ EC2 và sao lưu

Hiểu EBS volume được quản lý riêng với instance, còn instance store gắn với máy chủ vật lý đang chạy instance. Biết cần kiểm tra loại lưu trữ và cấu hình xóa volume khi kết thúc instance để xác định dữ liệu nào còn được giữ lại.

Đã thực hành mount EBS volume và tạo snapshot. Phân biệt được thao tác gắn volume trên Console với thao tác làm cho hệ điều hành sử dụng được volume. Hiểu snapshot là điểm sao lưu dùng để tạo lại volume khi cần khôi phục dữ liệu.

#### IAM và phạm vi quyền

Phân biệt được IAM user với IAM role ở mức phục vụ bài thực hành. Hiểu policy mô tả hành động được phép hoặc bị từ chối trên tài nguyên; trust policy xác định đối tượng có thể nhận role, còn permissions policy xác định quyền khi dùng role.

Có thể đọc các thành phần chính của một policy mẫu và giải thích vì sao ứng dụng chỉ đọc dữ liệu không cần được cấp quyền ghi hoặc xóa. Kiến thức này đủ để chọn quyền phù hợp cho một bài lab đơn giản và kiểm tra lại quyền khi truy cập bị từ chối.

#### IAM role cho EC2

Đã tạo role có quyền đọc S3, gắn role vào EC2 instance và kiểm tra truy cập qua CLI trên máy chủ. Hiểu instance profile là thành phần dùng để liên kết role với EC2 và ứng dụng có thể sử dụng thông tin xác thực tạm thời từ role.

Biết phân biệt thông tin truy cập được cấu hình trên máy cá nhân ở tuần 1 với quyền ứng dụng nhận qua role trên EC2. Có thể kiểm tra role đang gắn và policy liên quan khi lệnh truy cập dịch vụ không hoạt động như mong đợi.

#### Ứng dụng web và AMI

Đã thực hành triển khai ứng dụng web mẫu, xem trạng thái dịch vụ và kiểm tra cổng truy cập. Biết đối chiếu cổng ứng dụng đang lắng nghe với quy tắc security group khi trình duyệt không truy cập được máy chủ.

Hiểu AMI có thể lưu lại môi trường máy chủ đã cấu hình để phục vụ lần khởi chạy sau. Phân biệt được mục đích sao lưu dữ liệu bằng EBS snapshot với mục đích tạo mẫu máy chủ bằng AMI.

#### Cân bằng tải với ALB

Hiểu ALB phục vụ lưu lượng HTTP/HTTPS, trong khi NLB phù hợp với cân bằng tải ở tầng kết nối như TCP. Xác định được listener nhận yêu cầu, target group tập hợp máy chủ đích và health check kiểm tra khả năng phục vụ của target.

Đã thực hành cấu hình ALB với các EC2 instances, kiểm tra trạng thái target và truy cập ứng dụng qua địa chỉ của load balancer. Có thể lần theo luồng người dùng → ALB → target group → EC2 và biết kiểm tra cổng, đường dẫn health check, security groups khi target không ở trạng thái healthy.

Kết quả tuần này là sử dụng được các cấu hình lưu trữ, phân quyền và cân bằng tải trong bài lab theo hướng dẫn, đồng thời hiểu vai trò của từng cấu hình đối với ứng dụng.

### Tài liệu bổ sung

* [IAM roles cho Amazon EC2](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html): tra cứu instance profile và thông tin xác thực tạm thời.
* [ALB target groups](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-target-groups.html): tra cứu target, listener và health checks.
