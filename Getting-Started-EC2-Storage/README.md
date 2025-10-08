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

1. **Lưu ý** - Các điều cần biết trước khi bắt đầu
2. **Create Security Group** - Tạo nhóm bảo mật
3. **Create EC2** - Tạo EC2 instance
4. **Connect to EC2 via SSH** - Kết nối qua SSH
5. **Connect to EC2 via Console** - Kết nối qua AWS Console
6. **Access HTTP** - Truy cập web server trên EC2
7. **Create and Assign IAM Role** - Tạo và gán IAM role
8. **Cleanup** - Dọn dẹp tài nguyên

### Dừng server

Nhấn `Ctrl+C` trong PowerShell để dừng Hugo server.

### Chỉnh sửa nội dung

- Nội dung workshop nằm trong thư mục `content/`
- Hình ảnh nằm trong thư mục `static/images/`
- Cấu hình trong file `config.toml`