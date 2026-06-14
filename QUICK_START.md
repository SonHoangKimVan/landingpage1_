# 🚀 Quick Start - Bắt đầu nhanh trong 5 phút

## Bước 1: Tải dự án
```bash
# Cách 1: Clone từ Git
git clone https://github.com/your-repo/tiem-tra-an-nhien.git

# Cách 2: Tải ZIP
# Tải file ZIP và giải nén
```

## Bước 2: Mở trang web
```
1. Nhấp đúp vào file: index.html
   Hoặc
2. Kéo file index.html vào trình duyệt
   Hoặc
3. Chuột phải > Open with > Browser
```

✅ **Xong!** Trang web đã chạy

---

## ⚡ Những thay đổi cơ bản

### 1. Thay đổi tên tiệm
**File: index.html** - Tìm và thay đổi:
```html
<span class="logo-text">An Nhiên</span>
<h1 class="hero-title">Tiệm Trà An Nhiên</h1>
```

### 2. Thay đổi số điện thoại
**File: index.html** - Tìm:
```html
<a href="tel:+84123456789">+84 (0)123 456 789</a>
```
Thay đổi số điện thoại

### 3. Thay đổi địa chỉ
**File: index.html** - Tìm:
```html
<p>123 Đường Lê Lợi, Quận 1, TP. Hồ Chí Minh</p>
```
Thay đổi địa chỉ của bạn

### 4. Thay đổi email
**File: index.html** - Tìm:
```html
<a href="mailto:hello@annhien.com">hello@annhien.com</a>
```

### 5. Thêm sản phẩm
**File: script.js** - Tìm mảng `menuItems` và thêm:
```javascript
{
    id: 12,
    name: 'Tên sản phẩm mới',
    category: 'milk-tea', // milk-tea, fruit-tea, traditional, topping
    price: 35000,
    image: 'https://via.placeholder.com/250x200?text=Tên+sản+phẩm'
}
```

### 6. Thêm đánh giá
**File: script.js** - Tìm mảng `reviews` và thêm:
```javascript
{
    id: 5,
    name: 'Tên khách hàng',
    avatar: 'https://via.placeholder.com/60?text=Tên',
    rating: 5,
    text: 'Nhận xét của khách hàng...'
}
```

---

## 🎨 Thay đổi màu sắc

**File: style.css** - Đầu file, tìm:
```css
:root {
    --color-light-green: #A8B89D;    /* Thay đổi ở đây */
    --color-dark-green: #5C7A56;     /* Thay đổi ở đây */
    --color-cream: #F8F7F2;          /* Thay đổi ở đây */
    --color-brown: #8A6A4A;          /* Thay đổi ở đây */
}
```

**Công cụ chọn màu:** https://colorpicker.com

---

## 📱 Test responsive

**Phím tắt:**
- Chrome/Firefox: `F12` → Bấm icon điện thoại
- Safari: `Cmd+Option+I` → Bấm icon responsive
- Edge: `F12` → Bấm icon devices

**Hoặc online:** https://responsivedesignchecker.com

---

## 📸 Thêm hình ảnh

### Cách 1: Sử dụng placeholder (nhanh)
```javascript
// Trong script.js, thay đổi:
image: 'https://via.placeholder.com/250x200?text=Tên+Sản+Phẩm'
```

### Cách 2: Thêm hình ảnh thực tế

1. **Tạo thư mục:**
   ```
   images/
   ├── logo.png
   ├── about-tea.jpg
   ├── product1.jpg
   └── ...
   ```

2. **Thay đổi đường dẫn:**
   ```javascript
   image: './images/product1.jpg'  // Thay placeholder
   ```

---

## 🌙 Dark Mode

Tự động đã có sẵn! Bấm vào icon moon ở góc trên phải.

---

## 📋 Form đặt hàng

**Hiện tại:** Form chỉ hiển thị thông báo thành công

**Để thực sự lưu đơn hàng**, bạn cần:
1. Có server backend
2. Cập nhật hàm `handleOrderSubmit` trong `script.js`

Ví dụ:
```javascript
function handleOrderSubmit(e) {
    e.preventDefault();
    
    const formData = {
        name: document.getElementById('name').value,
        phone: document.getElementById('phone').value,
        product: document.getElementById('product').value,
        quantity: parseInt(document.getElementById('quantity').value),
        notes: document.getElementById('notes').value
    };

    // Gửi đến server
    fetch('https://your-api.com/orders', {
        method: 'POST',
        headers: {
            'Content-Type': 'application/json',
        },
        body: JSON.stringify(formData)
    })
    .then(response => response.json())
    .then(data => {
        showSuccessModal();
    })
    .catch(error => console.error('Error:', error));
}
```

---

## 🔗 Các link quan trọng

- **Facebook:** Tìm trong `script.js` - `social` section
- **Instagram:** Tìm trong `script.js` - `social` section
- **TikTok:** Tìm trong `script.js` - `social` section
- **Zalo:** Tìm trong footer hoặc contact section

---

## 🛠️ Chế độ phát triển

### Sử dụng Python (Khuyến khích)
```bash
# Bước 1: Mở terminal, cd vào thư mục dự án
cd /path/to/tiem-tra-an-nhien

# Bước 2: Chạy lệnh
python -m http.server 8000

# Bước 3: Truy cập
http://localhost:8000
```

### Sử dụng Node.js
```bash
npm install -g http-server
http-server
# Truy cập: http://localhost:8080
```

### Sử dụng PHP
```bash
php -S localhost:8000
# Truy cập: http://localhost:8000
```

---

## 🔍 Debug sự cố

### Mở Developer Tools
- **Chrome/Edge/Firefox:** F12
- **Safari:** Cmd+Option+I

### Console
1. Bấm F12 → Tab "Console"
2. Xem có lỗi (error) không
3. Sửa theo thông báo lỗi

### Các lỗi phổ biến

| Lỗi | Giải pháp |
|-----|----------|
| Hình ảnh không hiển thị | Kiểm tra đường dẫn file |
| CSS không áp dụng | Kiểm tra link `<link>` |
| JavaScript không chạy | Kiểm tra link `<script>` |
| Form không hoạt động | Kiểm tra console errors |

---

## 📦 Chuẩn bị triển khai

### Checklist
- [ ] Thay đổi tên tiệm
- [ ] Thêm số điện thoại & email
- [ ] Thêm sản phẩm
- [ ] Thêm đánh giá
- [ ] Thêm hình ảnh thực tế
- [ ] Test trên mobile
- [ ] Test tất cả link
- [ ] Test form
- [ ] Test dark mode

### Upload lên web

**Tùy chọn 1: Netlify (Dễ nhất)**
1. Push code lên GitHub
2. Vào https://netlify.com
3. Kết nối GitHub
4. Auto deploy

**Tùy chọn 2: GitHub Pages**
1. Push code lên GitHub
2. Settings → Pages → Deploy from branch
3. Chọn main branch
4. Xong! (https://username.github.io/repo-name)

**Tùy chọn 3: Hosting thông thường**
1. Mua hosting + domain
2. Upload file qua FTP
3. Trỏ domain

---

## 🆘 Cần trợ giúp?

### Xem tài liệu
- Đọc file: `README.md` - Tài liệu đầy đủ
- Đọc file: `SETUP.md` - Hướng dẫn chi tiết

### Tìm kiếm trực tuyến
- **Stack Overflow:** stackoverflow.com
- **MDN Web Docs:** developer.mozilla.org
- **W3Schools:** w3schools.com

### Liên hệ
- 📧 Email hỗ trợ
- 💬 Messenger
- 📞 Hotline của tiệm

---

## ✨ Tips & Tricks

### Lưu lại giỏ hàng
Tự động lưu bằng `localStorage` - không cần làm gì!

### Hiệu ứng cuộn mượt
Tự động có sẵn - sử dụng library AOS

### Responsive design
Tự động responsive - test trên F12

### SEO optimization
Đã thêm sẵn meta tags

### Dark mode
Tự động lưu preference của user

---

## 🎉 Hoàn tất!

Bạn đã có một landing page chuyên nghiệp! 

### Các bước tiếp theo:
1. ✅ Tùy chỉnh nội dung
2. ✅ Thêm hình ảnh
3. ✅ Test tất cả
4. ✅ Deploy lên web
5. ✅ Chia sẻ URL

---

**Bạn thắc mắc gì không?** Kiểm tra file `README.md` để tìm câu trả lời!

**Happy coding! 🚀**
