# 🌸 GlowShop – Hướng Dẫn Cài Đặt & Tài Khoản Demo

> Website bán mỹ phẩm xây dựng bằng **WordPress + WooCommerce** chạy trên **XAMPP (localhost)**

---

## 📋 Yêu Cầu Hệ Thống

| Phần mềm | Phiên bản | Link tải |
|---|---|---|
| XAMPP | 8.1+ | [apachefriends.org](https://www.apachefriends.org) |
| Trình duyệt | Chrome / Firefox | — |

---

## ⚙️ Hướng Dẫn Cài Đặt

### Bước 1 — Khởi động XAMPP

1. Mở **XAMPP Control Panel**
2. Click **[Start]** cho **Apache**
3. Click **[Start]** cho **MySQL**
4. Kiểm tra: cả hai dòng chuyển sang nền **xanh lá** là thành công ✅

---

### Bước 2 — Copy Source Code

Sao chép thư mục `glowshop` vào đúng đường dẫn sau:

```
C:\xampp\htdocs\glowshop
```

---

### Bước 3 — Import Database

1. Mở trình duyệt, truy cập: [http://localhost/phpmyadmin](http://localhost/phpmyadmin)
2. Tạo database mới:
   - Click tab **"Databases"**
   - Nhập tên: `glowshop_db`
   - Collation: `utf8mb4_unicode_ci`
   - Click **[Create]**
3. Chọn database `glowshop_db` vừa tạo
4. Click tab **"Import"**
5. Chọn file: `database/glowshop_db.sql`
6. Click **[Go]** ✅

---

### Bước 4 — Kiểm Tra `wp-config.php` (nếu cần)

Mở file `htdocs/glowshop/wp-config.php` và đảm bảo các dòng sau khớp:

```php
define( 'DB_NAME',     'glowshop_db' );
define( 'DB_USER',     'root' );
define( 'DB_PASSWORD', '' );
define( 'DB_HOST',     'localhost' );
```

> ⚠️ Nếu máy bạn đặt mật khẩu MySQL riêng, hãy điền vào `DB_PASSWORD`.

---

### Bước 5 — Truy Cập Website

| Mục đích | URL |
|---|---|
| 🌐 Trang khách hàng (Frontend) | [http://localhost/glowshop](http://localhost/glowshop) |
| 🔧 Trang quản trị (Backend) | [http://localhost/glowshop/wp-admin](http://localhost/glowshop/wp-admin) |

---

## 👥 Danh Sách Tài Khoản Demo

### 🔑 Administrator — Toàn quyền quản trị

| Trường | Giá trị |
|---|---|
| URL đăng nhập | http://localhost/glowshop/wp-admin |
| Username | `admin` |
| Password | `Admin@123456` |

---

### ✏️ Editor — Quản lý nội dung

| Trường | Giá trị |
|---|---|
| Username | `editor01` |
| Password | `Editor@123` |

---

### 🛒 Customer — Khách hàng (đã có đơn hàng mẫu)

| Trường | Giá trị |
|---|---|
| Username | `customer01` |
| Password | `Customer@123` |

> 💡 Dùng tài khoản `customer01` để xem lịch sử đơn hàng mẫu.  
> Phương thức thanh toán demo: **Chuyển khoản ngân hàng (COD)**

---

## 📁 Cấu Trúc Thư Mục Nộp Bài

```
📁 GlowShop/
├── 📁 source_code/
│   └── glowshop/               ← Toàn bộ thư mục WordPress
├── 📁 database/
│   └── glowshop_db.sql         ← File export từ phpMyAdmin
├── 📁 bao_cao/
│   └── BaoCao_GlowShop.docx
├── 📁 slide/
│   └── Slide_GlowShop.pptx
├── 📄 HUONG_DAN_GLOWSHOP.md    ← File này
```

---

## 🔄 Cách Export Database (để backup hoặc nộp bài)

```
1. Mở http://localhost/phpmyadmin
2. Chọn database: glowshop_db
3. Click tab "Export"
4. Format: SQL
5. Click [Go] → Lưu file .sql
```

---

## ❓ Xử Lý Lỗi Thường Gặp

| Lỗi | Nguyên nhân | Cách xử lý |
|---|---|---|
| Trang trắng (White Screen) | Lỗi PHP hoặc plugin | Bật `WP_DEBUG` trong wp-config.php |
| Không vào được wp-admin | Sai URL hoặc database chưa import | Kiểm tra lại Bước 3 & 4 |
| Port 80 bị chiếm | Skype / IIS đang dùng port 80 | Tắt ứng dụng đó hoặc đổi port Apache trong XAMPP |
| Ảnh không hiển thị | Đường dẫn media sai | Vào Settings → Media → Lưu lại |

---

*© 2026 GlowShop – Bài tập nhóm môn Quản Trị Website. Xây dựng bằng WordPress & WooCommerce.*
