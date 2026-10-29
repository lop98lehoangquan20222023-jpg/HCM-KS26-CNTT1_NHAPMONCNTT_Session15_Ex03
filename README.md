# Bài 3: Ngăn chặn quá tải lưu trữ khi đồng bộ mã nguồn
## 1. Báo cáo phân tích I/O (Từ Ctrl+S đến tích xanh)
- Lập trình viên lưu file (Ctrl+S): Hệ điều hành ghi nhận thay đổi và lưu trực tiếp mã nguồn vào ổ SSD để đảm bảo tốc độ thực thi nhanh nhất.

- Tiến trình đồng bộ kiểm tra: Phần mềm Cloud Sync quét qua thư mục dự án nhưng tự động bỏ qua (skip) thư mục nặng node_modules dựa trên thiết lập loại trừ (.gitignore hoặc Selective Sync).

- Đẩy dữ liệu lên Cloud: Chỉ các file mã nguồn thay đổi (.js, .json,...) được mã hóa và tải lên không gian đám mây.

- Xác nhận hoàn tất (Tích xanh): Khi quá trình đồng bộ hoàn tất trên mây, hệ thống trả về trạng thái đồng bộ và hiển thị biểu tượng tích xanh trên file tại máy.
## 2. Thiết kế tổ chức thư mục Cloud chuẩn cho lập trình viên:
```text
📁 My-Cloud-Workspace/
├── 📁 Code/                  # Source code dự án
├── 📁 Docs/                  # Tài liệu kỹ thuật, báo cáo, đặc tả
└── 📁 Assets/                # Tài nguyên hình ảnh, thiết kế, logo
```
