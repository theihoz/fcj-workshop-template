---
title: "Worklog Tuần 1"
date: 2026-09-23
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu tuần 1

Làm quen với môi trường thực tập First Cloud AI Journey, các nhóm dịch vụ AWS và cách quản lý tài nguyên bằng AWS Management Console, AWS CLI. Phần thực hành tập trung vào việc khởi chạy một EC2 instance, kết nối SSH và nhận biết các thành phần cần thiết cho một máy chủ cơ bản.

### Công việc trong tuần

| Buổi | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu chính |
| --- | --- | --- | --- | --- |
| 1 | Làm quen với các thành viên FCAJ, đọc nội quy và xác định cách ghi chép nội dung học tập trong thời gian thực tập. | 23/09/2026 | 23/09/2026 | [First Cloud Journey](https://cloudjourney.awsstudygroup.com/) |
| 2 | Tìm hiểu điện toán đám mây và các nhóm compute, storage, networking, database; xác định vai trò cơ bản của EC2, S3, VPC và RDS trong một ứng dụng. | 24/09/2026 | 25/09/2026 | [Khám phá các dịch vụ AWS](https://cloudjourney.awsstudygroup.com/1-explore/) |
| 3 | Tạo tài khoản AWS, làm quen với giao diện Console; cài đặt AWS CLI, cấu hình thông tin truy cập và Region, kiểm tra tài khoản đang sử dụng. | 24/09/2026 | 25/09/2026 | [Tạo tài khoản AWS](https://000001.awsstudygroup.com/) |
| 4 | Tìm hiểu instance, AMI, instance type, key pair, security group, EBS và Elastic IP; đọc quy trình khởi chạy máy chủ và kết nối SSH. | 25/09/2026 | 26/09/2026 | [Bắt đầu với Amazon EC2](https://000004.awsstudygroup.com/) |
| 5 | Khởi chạy EC2 instance theo hướng dẫn, kết nối qua SSH và gắn EBS volume; đối chiếu thông tin instance trên Console với kết quả từ CLI. | 25/09/2026 | 26/09/2026 | [Bắt đầu với Amazon EC2](https://000004.awsstudygroup.com/) |

### Kiến thức đã học và kết quả thực hành

#### Môi trường thực tập và cách học

Đã làm quen với các thành viên và nội quy của đơn vị thực tập. Biết sử dụng Cloud Journey để chọn bài học theo dịch vụ, đọc phần chuẩn bị trước khi thực hành và ghi lại các bước cấu hình để có thể xem lại khi gặp lỗi.

#### Các nhóm dịch vụ AWS

Hiểu ở mức cơ bản rằng EC2 cung cấp máy chủ ảo, S3 lưu trữ tệp dưới dạng object, VPC tổ chức mạng và RDS hỗ trợ cơ sở dữ liệu quan hệ. Có thể xác định nhóm dịch vụ phù hợp với một nhu cầu đơn giản, chẳng hạn chạy ứng dụng, lưu tệp hoặc lưu dữ liệu có cấu trúc.

Nhận biết Region là nơi lựa chọn để triển khai tài nguyên và cần kiểm tra Region khi tìm tài nguyên trên Console hoặc chạy lệnh CLI. Các khái niệm này đủ để theo dõi một bài thực hành cơ bản và đọc sơ đồ hệ thống đơn giản.

#### Tài khoản AWS và Management Console

Đã tạo tài khoản AWS và làm quen với các thao tác tìm dịch vụ, mở trang quản lý tài nguyên, chọn Region và xem thông tin cấu hình. Biết kiểm tra trạng thái tài nguyên sau khi tạo thay vì chỉ dựa vào thông báo hoàn tất thao tác.

#### AWS CLI

Đã cài đặt và cấu hình AWS CLI trên máy tính. Hiểu mục đích của thông tin xác thực, Region mặc định và profile; biết kiểm tra cấu hình đang dùng trước khi thao tác với tài nguyên.

Thực hiện được các lệnh cơ bản để xem thông tin tài khoản, danh sách Region, EC2 instances và key pairs. Có thể đối chiếu instance ID, trạng thái và địa chỉ IP giữa Console với kết quả CLI. Mức sử dụng hiện tại tập trung vào các lệnh riêng lẻ theo hướng dẫn.

#### EC2 nhập môn

Phân biệt được AMI dùng làm mẫu hệ điều hành, instance type xác định tài nguyên máy chủ, key pair phục vụ xác thực SSH và security group kiểm soát lưu lượng mạng. Biết EBS là ổ lưu trữ gắn với EC2 và Elastic IP là địa chỉ IPv4 công cộng có thể cấp phát riêng.

Đã thực hành khởi chạy instance, kết nối SSH và gắn EBS volume. Khi kiểm tra kết nối, biết xem lại địa chỉ IP, tên người dùng, key pair và quy tắc cho phép SSH. Kết quả tuần này là sử dụng được một máy chủ EC2 trong bài lab cơ bản theo tài liệu.

### Tài liệu bổ sung

* [AWS CLI — Cấu hình ban đầu](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-quickstart.html): tra cứu profile, Region và phương thức xác thực.
