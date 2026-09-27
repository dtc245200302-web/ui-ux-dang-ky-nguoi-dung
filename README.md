# UI/UX - Thiết kế giao diện trang đăng ký người dùng

## 1. Thông tin bài tập

**Tên bài:** Thiết kế UI/UX giao diện trang đăng ký người dùng

**Mục tiêu:** Thực hành các nguyên tắc UI/UX cơ bản như tính khả dụng, dễ hiểu, phản hồi người dùng, Fitts' Law và responsive design.

## 2. Cấu trúc project

```text
ui-ux-dang-ky-nguoi-dung/
├── index.html
├── success.html
├── style.css
└── README.md
```

### Chức năng

- `index.html`: Trang đăng ký tài khoản.
- `success.html`: Trang xác nhận đăng ký thành công.
- `style.css`: Toàn bộ giao diện và responsive design.
- `README.md`: Mô tả yêu cầu, wireframe, luồng người dùng và giải thích UI/UX.

## 3. Nghiên cứu trải nghiệm người dùng

Khi thiết kế form đăng ký, các nguyên tắc được chú ý:

1. **Đơn giản:** Chỉ yêu cầu các thông tin cần thiết: họ tên, email, mật khẩu và xác nhận mật khẩu.
2. **Thứ tự trực quan:** Các trường được sắp xếp từ thông tin cá nhân đến thông tin bảo mật.
3. **Label rõ ràng:** Tên trường đặt ngay phía trên ô nhập để người dùng dễ nhận biết.
4. **Phản hồi lỗi:** Khi dữ liệu không hợp lệ, hệ thống hiển thị thông báo ngay bên dưới trường tương ứng.
5. **Hiển thị mật khẩu:** Có nút Hiện/Ẩn để người dùng kiểm tra dữ liệu đã nhập.
6. **Call-to-action rõ ràng:** Nút "Đăng ký" nổi bật và dễ nhận biết.
7. **Responsive:** Giao diện tự điều chỉnh trên máy tính, tablet và điện thoại.
8. **Khả năng tiếp cận:** Có trạng thái focus, kích thước nút đủ lớn và hỗ trợ `prefers-reduced-motion`.

## 4. Tham khảo các mẫu giao diện phổ biến

Các dịch vụ phổ biến như Google, Facebook và X/Twitter thường sử dụng form ngắn, tập trung vào mục tiêu chính và hạn chế thông tin không cần thiết.

Bài thiết kế này áp dụng các ý tưởng chung về:
- Form tối giản.
- Một hành động chính rõ ràng.
- Label và hướng dẫn dễ hiểu.
- Phản hồi lỗi.
- Khả năng sử dụng trên nhiều thiết bị.

Không sao chép giao diện hoặc nhận diện thương hiệu của các dịch vụ trên.

## 5. Wireframe

### Trang 1 - Form đăng ký

```text
┌────────────────────────────────────────┐
│                                        │
│                   [ U ]                │
│                                        │
│            TẠO TÀI KHOẢN               │
│       Đăng ký để bắt đầu sử dụng       │
│                                        │
│  Họ và tên *                           │
│  ┌──────────────────────────────────┐  │
│  │ Nguyễn Văn A                     │  │
│  └──────────────────────────────────┘  │
│                                        │
│  Email *                               │
│  ┌──────────────────────────────────┐  │
│  │ example@gmail.com                │  │
│  └──────────────────────────────────┘  │
│                                        │
│  Mật khẩu *                            │
│  ┌──────────────────────────────────┐  │
│  │ •••••••••••••              Hiện  │  │
│  └──────────────────────────────────┘  │
│  Mật khẩu nên có ít nhất 8 ký tự.      │
│                                        │
│  Xác nhận mật khẩu *                   │
│  ┌──────────────────────────────────┐  │
│  │ •••••••••••••              Hiện  │  │
│  └──────────────────────────────────┘  │
│                                        │
│  ┌──────────────────────────────────┐  │
│  │             ĐĂNG KÝ              │  │
│  └──────────────────────────────────┘  │
│                                        │
│       Đã có tài khoản? Đăng nhập       │
│                                        │
└────────────────────────────────────────┘
```

### Trang 2 - Thành công

```text
┌────────────────────────────────────────┐
│                                        │
│                  [ ✓ ]                 │
│                                        │
│          ĐĂNG KÝ THÀNH CÔNG           │
│                                        │
│  Tài khoản của bạn đã được tạo thành   │
│  công. Chào mừng bạn đến với hệ thống. │
│                                        │
│  ┌──────────────────────────────────┐  │
│  │          ĐĂNG NHẬP NGAY          │  │
│  └──────────────────────────────────┘  │
│                                        │
│          ← Quay lại trang đăng ký     │
│                                        │
└────────────────────────────────────────┘
```

## 6. Luồng người dùng

```text
Trang đăng ký
     │
     ▼
Nhập họ tên
     │
     ▼
Nhập email
     │
     ▼
Nhập mật khẩu
     │
     ▼
Xác nhận mật khẩu
     │
     ▼
Nhấn "Đăng ký"
     │
     ├── Dữ liệu sai ──► Hiển thị lỗi ──► Sửa thông tin
     │
     └── Dữ liệu đúng
              │
              ▼
      Trang đăng ký thành công
              │
              ▼
       "Đăng nhập ngay"
```

## 7. Các nguyên tắc UI/UX đã áp dụng

| Nguyên tắc | Cách áp dụng | Lý do |
|---|---|---|
| Tính đơn giản | 4 trường thông tin chính | Giảm thời gian hoàn thành form |
| Phân cấp thị giác | Tiêu đề, mô tả, label và CTA rõ ràng | Người dùng biết cần làm gì trước |
| Fitts' Law | Nút Đăng ký cao 52px, chiều rộng toàn form | Dễ nhìn và dễ thao tác bằng chuột/touch |
| Phản hồi lỗi | Thông báo ngay dưới trường sai | Giúp sửa lỗi nhanh |
| Khả năng kiểm soát | Nút Hiện/Ẩn mật khẩu | Người dùng chủ động kiểm tra mật khẩu |
| Nhất quán | Màu và kiểu nút được dùng thống nhất | Giảm tải nhận thức |
| Responsive | Media query cho màn hình nhỏ | Sử dụng tốt trên điện thoại/tablet |
| Accessibility | Focus state, label, aria-label | Hỗ trợ khả năng tiếp cận |
| Phản hồi thành công | Trang success với dấu ✓ | Xác nhận rõ ràng hành động đã hoàn tất |

## 8. Fitts' Law

Fitts' Law cho rằng thời gian tương tác phụ thuộc vào khoảng cách tới mục tiêu và kích thước mục tiêu.

Trong thiết kế này:
- Nút **Đăng ký** có kích thước lớn.
- Nút nằm ngay sau các trường nhập.
- Khoảng cách giữa các thành phần được giữ hợp lý.
- Nút Hiện/Ẩn mật khẩu đủ lớn để thao tác trên màn hình cảm ứng.

## 9. Responsive Design

Giao diện được thiết kế theo hướng responsive:

- **Desktop:** Form nằm giữa màn hình, chiều rộng tối đa 460px.
- **Tablet:** Card và khoảng cách tự thu nhỏ.
- **Mobile:** Card chiếm gần toàn bộ chiều rộng màn hình, giảm padding để dễ đọc và thao tác.
- Có `meta viewport` để hiển thị đúng trên thiết bị di động.

## 10. Kiểm tra chức năng

Các trường hợp đã xử lý:

- Bỏ trống họ tên → báo lỗi.
- Email không hợp lệ → báo lỗi.
- Mật khẩu dưới 8 ký tự → báo lỗi.
- Mật khẩu xác nhận không khớp → báo lỗi.
- Nhập đúng tất cả thông tin → chuyển sang `success.html`.
- Có thể Hiện/Ẩn mật khẩu.

## 11. Cách chạy

Không cần backend.

Cách 1:
- Mở trực tiếp `index.html` bằng trình duyệt.

Cách 2:
- Mở thư mục bằng VS Code.
- Cài extension **Live Server**.
- Chuột phải `index.html` → **Open with Live Server**.

## 12. Link GitHub

Repository:

https://github.com/dtc245200302-web/ui-ux-dang-ky-nguoi-dung

Sau khi push code lên GitHub, có thể dùng GitHub Pages để tạo link demo website.

Ví dụ:

https://dtc245200302-web.github.io/ui-ux-dang-ky-nguoi-dung/

## 13. Kết luận

Thiết kế đáp ứng các yêu cầu của bài tập:
- Có tối thiểu 2 trang.
- Có form đăng ký.
- Có trang xác nhận thành công.
- Có wireframe.
- Có luồng người dùng.
- Áp dụng Fitts' Law.
- Có validation và phản hồi lỗi.
- Có responsive design.
- Có giải thích các nguyên tắc UI/UX.
