# CoffeePHP - Hệ Thống Quản Lý & Đặt Lịch Quán Cà Phê

Hệ thống website quản lý và đặt bàn/gọi món cho quán cà phê được xây dựng bằng ngôn ngữ **PHP thuần** theo mô hình kiến trúc **MVC (Model-View-Controller)**, kết hợp mã nguồn mở frontend và cơ sở dữ liệu **MySQL**. Dự án áp dụng lập trình hướng đối tượng (OOP) giúp mã nguồn tường minh, dễ bảo trì và mở rộng.

---

## 🚀 Tính Năng Chính

### 🌐 Dành Cho Khách Hàng (Frontend)
*   **Trang chủ (Home):** Hiển thị không gian quán, các chương trình khuyến mãi và sản phẩm nổi bật.
*   **Thực đơn (Menu):** Danh sách đồ uống, món ăn phân loại theo danh mục (Cà phê, Trà, Bánh ngọt,...).
*   **Đặt bàn / Đặt món (Booking):** Cho phép khách hàng đặt bàn trước, chọn thời gian và số lượng người.
*   **Giới thiệu & Liên hệ (About & Contact):** Thông tin chi tiết về quán và form gửi phản hồi.

### 🔐 Hệ Thống Thành Viên
*   Đăng ký, Đăng nhập, Đăng xuất.
*   Quản lý thông tin cá nhân và lịch sử đặt đơn.

### 🛠️ Trang Quản Trị (Admin Dashboard)
*   **Quản lý sản phẩm (Products):** Thêm, sửa, xóa (CRUD) các món ăn, thức uống, giá cả và hình ảnh.
*   **Quản lý danh mục (Categories):** Phân loại nhóm đồ uống.
*   **Quản lý đơn hàng/Đặt bàn (Orders/Bookings):** Tiếp nhận, phê duyệt hoặc hủy yêu cầu từ khách hàng.
*   **Quản lý người dùng (Users):** Phân quyền và quản lý tài khoản nhân viên/khách hàng.

---

## 📐 Kiến Trúc Dự Án (Architecture)

Dự án tuân thủ nghiêm ngặt mô hình **MVC**:
*   **Model:** Xử lý logic dữ liệu, tương tác với MySQL Database thông qua PDO (nhằm chống lỗi SQL Injection).
*   **View:** Giao diện hiển thị (HTML5, CSS3, JavaScript, Bootstrap) nhận dữ liệu từ Controller để render.
*   **Controller:** Tiếp nhận request từ người dùng, điều hướng xử lý logic và gọi View tương ứng.

### Cấu trúc thư mục chính:
```text
CoffeePHP/
├── app/
│   ├── controllers/    # Xử lý logic điều hướng (HomeController, AdminController,...)
│   ├── models/         # Tương tác Database (ProductModel, UserModel,...)
│   └── views/          # Giao diện hiển thị (Trang chủ, Admin, Chi tiết sản phẩm,...)
├── core/               # Các file cấu hình cốt lõi (App, Controller, Database thiết lập Router)
├── public/             # Thư mục gốc chứa tài nguyên (CSS, JS, Images, file index.php chính)
├── config/             # Cấu hình hệ thống (Database config, Constant)
└── database/           # Chứa file backup cơ sở dữ liệu (.sql)
