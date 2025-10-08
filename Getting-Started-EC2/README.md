# Getting Started with EC2 Workshop

## Hướng dẫn sử dụng

### Yêu cầu
- Hugo đã được cài đặt
- Trình duyệt web

### Cách chạy workshop

1. **Mở PowerShell/Command Prompt**

2. **Di chuyển đến thư mục chứa workshop:**
   ```cmd
   cd Getting-Started-EC2
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

Workshop này hướng dẫn các bước cơ bản để làm việc với Amazon EC2:

1. **Giới thiệu** - Tổng quan về Amazon EC2.
2. **Chuẩn bị** - Tạo Security Group, EC2 instance và IAM role.
3. **Kết nối đến EC2 instance** - Kết nối qua SSH, AWS Console và truy cập HTTP.
4. **Cấu hình EC2 IAM role** - Gán IAM role để truy cập S3.
5. **Dọn dẹp tài nguyên** - Xóa các tài nguyên đã tạo.

### Dừng server

Nhấn `Ctrl+C` trong PowerShell để dừng Hugo server.