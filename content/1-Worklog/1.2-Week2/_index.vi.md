---
title: "Worklog Tuần 2"
date: 2026-09-30
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2

Tìm hiểu Amazon S3 và Amazon CloudFront ở mức nhập môn, tập trung vào cách lưu trữ tệp và phân phối nội dung đến người dùng. Kết quả thực hành của tuần là phác thảo được luồng phân phối một tệp từ S3 qua CloudFront và giải thích vai trò của từng thành phần.

### Công việc trong tuần

| Buổi | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu chính |
| --- | --- | --- | --- | --- |
| 1 | Tìm hiểu S3, phân biệt bucket với object và đọc các ví dụ lưu trữ tệp, ảnh, tài nguyên website. | 30/09/2026 | 30/09/2026 | [Bắt đầu với Amazon S3](https://000057.awsstudygroup.com/) |
| 2 | Tìm hiểu CloudFront, khái niệm CDN và edge location; xác định vai trò của distribution trong việc phân phối nội dung. | 01/10/2026 | 01/10/2026 | [CloudFront với S3 bucket origin](https://000094.awsstudygroup.com/) |
| 3 | Đọc luồng kết nối giữa S3 và CloudFront, xác định origin và đường đi của yêu cầu từ người dùng đến nội dung lưu trong bucket. | 02/10/2026 | 02/10/2026 | [CloudFront với S3 bucket origin](https://000094.awsstudygroup.com/) |
| 4 | Tìm hiểu bộ nhớ đệm, phân biệt cache hit với cache miss và vai trò của thời gian lưu cache khi nội dung thay đổi. | 03/10/2026 | 03/10/2026 | [CloudFront với S3 bucket origin](https://000094.awsstudygroup.com/) |
| 5 | Phác thảo sơ đồ người dùng → CloudFront → S3, dùng một tệp HTML hoặc ảnh làm ví dụ và trình bày lại chức năng của từng dịch vụ. | 04/10/2026 | 04/10/2026 | [CloudFront với S3 bucket origin](https://000094.awsstudygroup.com/) |

### Kiến thức đã học và kết quả thực hành

#### Lưu trữ với Amazon S3

Hiểu bucket là nơi chứa các object; một object gồm dữ liệu tệp và thông tin mô tả đi kèm. Biết object key dùng để nhận diện object trong bucket và có thể tạo cách tổ chức tên tệp theo tiền tố.

Có thể chọn ví dụ phù hợp để lưu trên S3 như ảnh, tài liệu, tệp HTML, CSS hoặc JavaScript. Phân biệt được mục đích lưu tệp của S3 với việc chạy ứng dụng trên EC2 đã học ở tuần 1. Qua tài liệu, nhận biết việc lưu được tệp và việc cho phép người dùng truy cập tệp là hai phần cấu hình cần xem xét riêng.

#### Phân phối nội dung với Amazon CloudFront

Hiểu CloudFront là dịch vụ phân phối nội dung và origin là nơi cung cấp nội dung gốc. Biết S3 bucket có thể làm origin, còn distribution xác định cách CloudFront nhận yêu cầu và chuyển nội dung đến người dùng.

Nhận biết edge location hỗ trợ phục vụ nội dung từ vị trí gần người dùng hơn. Có thể giải thích mục đích chung của CDN đối với tài nguyên website thường được truy cập, như hình ảnh hoặc tệp giao diện.

#### Bộ nhớ đệm và đường đi của yêu cầu

Hiểu cache hit xảy ra khi nội dung phù hợp đã có trong cache; cache miss khiến CloudFront cần lấy nội dung từ origin. Biết thời gian lưu cache có liên quan đến việc người dùng nhìn thấy nội dung đã cập nhật.

Đọc được luồng yêu cầu ở mức cơ bản: người dùng truy cập qua CloudFront, CloudFront kiểm tra cache và lấy nội dung từ S3 khi cần. Có thể giải thích vì sao S3 và CloudFront có vai trò khác nhau trong cùng một luồng phân phối nội dung.

#### Kết quả thực hành

Đã phác thảo sơ đồ phân phối một tệp từ S3 qua CloudFront và mô tả lại đường đi của yêu cầu bằng ví dụ tệp HTML hoặc ảnh. Trong sơ đồ, xác định được người dùng, distribution, cache và S3 origin.

Kết quả hiện tại là hiểu và trình bày được mô hình đơn giản để chuẩn bị cho bước cấu hình thực tế. Nội dung tuần này tập trung vào đọc tài liệu và phác thảo, chưa ghi nhận việc triển khai distribution hoặc website hoàn chỉnh.

### Tài liệu bổ sung

* [Amazon S3 — Tổng quan](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html): tra cứu khái niệm bucket, object và truy cập dữ liệu.
* [CloudFront — Cách phân phối nội dung](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/HowCloudFrontWorks.html): đọc thêm về origin, edge location và cache.
