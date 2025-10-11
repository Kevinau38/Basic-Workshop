---
title: "Giới thiệu"

weight: 1
chapter: false
pre: " <b> 1. </b> "
---

Amazon EC2 Storage cung cấp bộ nhớ khối liên tục, hiệu suất cao cho các Amazon EC2 instances thông qua Amazon Elastic Block Store (EBS). Các EBS volumes có thể được gắn vào EC2 instances và cung cấp bộ nhớ liên tục cần thiết cho hệ thống tệp, cơ sở dữ liệu và bất kỳ trường hợp sử dụng nào khác yêu cầu bộ nhớ liên tục.

Với Amazon EC2 Storage, người dùng có thể:

- Tạo EBS volumes với các loại volume khác nhau được tối ưu hóa cho hiệu suất hoặc chi phí.
- Tạo snapshots theo thời điểm của EBS volumes để sao lưu và khôi phục thảm họa.
- Tạo Amazon Machine Images (AMI) để ghi lại toàn bộ cấu hình instance.
- Khôi phục EC2 instances từ AMI để nhanh chóng triển khai các cấu hình giống hệt nhau.
- Mã hóa EBS volumes và snapshots để tăng cường bảo mật.
- Thay đổi kích thước volumes và thay đổi loại volume khi cần thiết.

Workshop này tập trung vào các tình huống quản lý bộ nhớ thực tế bao gồm tạo snapshots, xây dựng AMIs và khôi phục instances để chứng minh cách các giải pháp EC2 storage cung cấp khả năng lưu trữ dữ liệu và khôi phục cho các workloads đám mây.