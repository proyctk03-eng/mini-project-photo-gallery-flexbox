# Mini Project: Thư Viện Ảnh (Photo Gallery) Đáp Ứng Bằng Flexbox

## 1. Mục tiêu
- Xây dựng bố cục lưới ảnh đa hàng tự động co giãn bằng `display: flex` và `flex-wrap: wrap`.
- Kiểm soát khoảng cách đồng đều giữa các ảnh bằng thuộc tính `gap`.
- Tối ưu hóa kích thước item ảnh bằng thuộc tính viết tắt `flex: 1 1 300px` (flex-grow: 1, flex-shrink: 1, flex-basis: 300px).
- Đảm bảo hình ảnh không bị méo bằng `object-fit: cover`.
- Tạo giao diện đáp ứng (responsive) mượt mà mà không cần dùng đến CSS Media Queries.

---

## 2. Các bước thực hiện tóm tắt
1. **Khởi tạo cấu trúc HTML (`gallery.html` và `index.html`):**
   - Thẻ bao bọc `<div class="gallery-container">`.
   - 9 thẻ `<div class="gallery-item">` chứa các thẻ `<img>` từ Picsum Photos với tỉ lệ kích thước chuẩn.
2. **Thiết lập CSS cơ bản (`style.css`):**
   - Reset `box-sizing: border-box; margin: 0; padding: 0;`.
   - Đặt màu nền body nhã nhặn `#f0f2f5` và font chữ Arial.
3. **Định dạng container với Flexbox:**
   - `display: flex;` kích hoạt ngữ cảnh Flexbox.
   - `flex-wrap: wrap;` cho phép các ảnh tự động xuống dòng khi thiếu không gian.
   - `justify-content: center;` căn giữa toàn bộ khối ảnh.
   - `gap: 16px;` tạo khoảng trống đều giữa các hàng và cột.
4. **Định dạng item và ảnh:**
   - `.gallery-item`: sử dụng `flex: 1 1 300px;` kết hợp `height: 240px;`, bo tròn góc `border-radius: 8px` và đổ bóng `box-shadow`.
   - `img`: đặt `width: 100%; height: 100%; object-fit: cover;` để ảnh luôn lấp đầy khung mà không méo.
   - Hiệu ứng `:hover`: phóng to nhẹ `transform: scale(1.03);` kèm bóng mờ sâu hơn.
