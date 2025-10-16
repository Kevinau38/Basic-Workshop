# Getting Started with EC2 Storage Workshop

## Hướng dẫn sử dụng

### Yêu cầu
- Hugo đã được cài đặt
- Trình duyệt web

### Cách chạy workshop

1. **Mở PowerShell/Command Prompt**

2. **Di chuyển đến thư mục chứa workshop:**
   ```cmd
   cd Getting-Started-EC2-Storage
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

Workshop này hướng dẫn các bước cơ bản để làm việc với Amazon EC2 Storage:

1. **Giới thiệu** - Tổng quan về Amazon EC2 Storage.
2. **Chuẩn bị** - Tạo Security Group, EC2 instance, EBS Snapshot và AMI.
3. **Kết nối đến EC2 instance** - Connect qua EC2 Instance Connect, kiểm tra web server và tạo file.
4. **Khôi phục EC2 từ AMI** - Khôi phục EC2 instance từ AMI đã tạo.
5. **Kiểm tra webserver và file đã tạo** - Xác minh dữ liệu đã được bảo toàn trong AMI.
6. **Dọn dẹp tài nguyên** - Xóa các tài nguyên đã tạo.

### Dừng server

Nhấn `Ctrl+C` trong PowerShell để dừng Hugo server.