# I. Lý thuyết

### 1. Giới thiệu SQL Injection (SQLi)

SQL Injection (SQLi) là một lỗ hổng bảo mật nghiêm trọng trong các ứng dụng web, xảy ra khi các tham số đầu vào không được kiểm tra và được nhà phát triển sử dụng trong câu lệnh SQL. Lỗ hổng này cho phép kẻ tấn công chỉnh sửa, truy xuất hoặc xóa dữ liệu.

**Mục đích tấn công:**

- Truy cập dữ liệu trái phép.

- Xóa, thay đổi dữ liệu.

- Kiểm soát cơ sở dữ liệu hoặc thực thi lệnh độc hại.

---

### 2. Các loại SQLi

2.1. Error-Based SQLi

2.2. Union-Based SQLi

2.3. Boolean-Based SQLi

2.4. Time-Based Blind SQLi

2.5. Out-of-Band SQL Injection

---

### 3. Cách lập trình an toàn để tránh SQLi

1. **Prepared Statements (PDO trong PHP):**

- Chuẩn bị câu lệnh SQL để gạn tham số thay vì ghép chuỗi.

```js
$stmt = $pdo->prepare("SELECT * FROM products WHERE id = :id");
$stmt->execute(['id' => $id]);
```

2. **Kiểm tra và lọc input:**

- Chỉ nhận input hợp lệ.

- Sử dụng hàm filter_input hoặc regex.

3. **Hạn chế quyền database:**

Chỉ cung cấp quyền cần thiết cho tài khoản database.
