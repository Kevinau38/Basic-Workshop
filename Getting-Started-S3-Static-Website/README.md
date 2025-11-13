# Getting Started with S3 Static Website Workshop

## Hướng dẫn sử dụng

### Yêu cầu
- Hugo đã được cài đặt
- Trình duyệt web

### Cách chạy workshop

1. **Mở PowerShell/Command Prompt**

2. **Di chuyển đến thư mục chứa workshop:**
   ```cmd
   cd Getting-Started-S3-Static-Website
   ```

3. **Chạy Hugo server:**
   ```cmd
   hugo server -D
   ```

4. **Mở trình duyệt và truy cập:**
   ```
   http://localhost:1313
   ```

### Nội dung workshop

Workshop này hướng dẫn các bước cơ bản để tạo static website sử dụng Amazon S3:

1. **Giới thiệu** - Tổng quan về Amazon S3 Static Website Hosting.
2. **Register domain with Route53 (Optional)** - Mua domain từ Route53.
3. **Creating a S3 bucket** - Tạo S3 bucket để host website.
4. **Enable Static Website hosting settings** - Cấu hình S3 bucket cho static website hosting.
5. **Test the website** - Kiểm tra website hoạt động.
6. **Test the website's error page** - Kiểm tra trang lỗi của website.
7. **Setting Route53 to access http://s3static.{domain} (Optional)** - Cấu hình Route53 cho custom domain.
8. **Clean up** - Dọn dẹp tài nguyên đã tạo.

### Dừng server

Nhấn `Ctrl+C` trong PowerShell để dừng Hugo server.