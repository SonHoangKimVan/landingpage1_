# Tiệm Trà An Nhiên - Landing Page

Một landing page chuyên nghiệp cho tiệm trà "An Nhiên" với thiết kế tối giản, thanh lịch và hướng đến trải nghiệm thư giãn cho khách hàng.

## 🌟 Tính năng chính

### 1. **Thiết kế Responsive**
- Hoàn toàn tương thích với Desktop, Tablet và Mobile
- Menu hamburger tự động trên thiết bị di động
- Layout linh hoạt tự điều chỉnh theo kích thước màn hình

### 2. **Các Section Chính**
- **Header/Navigation**: Thanh điều hướng cố định với menu và giỏ hàng
- **Hero Section**: Banner chính với hình nền gradient, tiêu đề ấn tượng
- **About**: Câu chuyện thương hiệu với hình ảnh và nội dung 2 cột
- **Menu**: Danh mục sản phẩm với bộ lọc theo danh mục
- **Promotion**: Khu vực ưu đãi với đồng hồ đếm ngược
- **Process**: Quy trình pha chế 4 bước
- **Reviews**: Slider đánh giá khách hàng
- **Gallery**: Thư viện hình ảnh Masonry
- **Order**: Form đặt hàng trực tuyến
- **Contact**: Thông tin liên hệ và Google Maps
- **Footer**: Thông tin công ty và mạng xã hội

### 3. **Chức năng Tương tác**
- ✅ Giỏ hàng mini với tính toán tổng tiền tự động
- ✅ Thêm/Xóa sản phẩm từ giỏ hàng
- ✅ Dark Mode / Light Mode
- ✅ Bộ lọc thực đơn theo danh mục
- ✅ Form đặt hàng với kiểm tra dữ liệu
- ✅ Slider đánh giá khách hàng
- ✅ Nút back to top
- ✅ Hiệu ứng cuộn trang (AOS Animation)

### 4. **Tối ưu hóa**
- SEO-friendly với meta tags
- Open Graph hỗ trợ chia sẻ xã hội
- Tốc độ tải nhanh
- Performance optimized

### 5. **Màu sắc**
- Xanh lá nhạt: `#A8B89D`
- Xanh trà đậm: `#5C7A56`
- Trắng kem: `#F8F7F2`
- Nâu đất: `#8A6A4A`

### 6. **Typography**
- Tiêu đề: Playfair Display (serif)
- Nội dung: Poppins (sans-serif)

## 📁 Cấu trúc dự án

```
tiệm-trà-an-nhiên/
├── index.html          # File HTML chính
├── style.css           # Stylesheet toàn cộng
├── script.js           # JavaScript tương tác
├── images/             # Thư mục hình ảnh
│   ├── logo.png
│   ├── favicon.png
│   └── about-tea.jpg
└── README.md           # File hướng dẫn
```

## 🚀 Hướng dẫn sử dụng

### Cài đặt cơ bản
1. Clone hoặc tải về dự án
2. Mở file `index.html` trong trình duyệt
3. Không cần cài đặt dependencies thêm

### Thay đổi dữ liệu

#### Thay đổi sản phẩm
Mở `script.js` và sửa đổi mảng `menuItems`:
```javascript
const menuItems = [
    {
        id: 1,
        name: 'Tên sản phẩm',
        category: 'milk-tea', // milk-tea, fruit-tea, traditional, topping
        price: 35000,
        image: 'url-hình-ảnh'
    },
    // ...
];
```

#### Thay đổi đánh giá
Sửa đổi mảng `reviews` trong `script.js`

#### Thay đổi hình ảnh gallery
Sửa đổi mảng `galleryImages` trong `script.js`

#### Thay đổi thông tin liên hệ
Tìm và thay đổi trong phần HTML:
- Địa chỉ: Tìm "123 Đường Lê Lợi"
- Hotline: Tìm "+84123456789"
- Email: Tìm "hello@annhien.com"

### Thêm hình ảnh thực tế
1. Tạo thư mục `images/` ngoài cùng
2. Thêm hình ảnh vào thư mục
3. Cập nhật đường dẫn hình ảnh trong:
   - HTML (logo, about image)
   - CSS (hero background)
   - JavaScript (menu items, reviews, gallery)

Ví dụ:
```html
<img src="./images/logo.png" alt="Logo">
```

## 🎨 Tùy chỉnh giao diện

### Đổi màu sắc
Mở `style.css` và cập nhật các biến CSS:
```css
:root {
    --color-light-green: #A8B89D;
    --color-dark-green: #5C7A56;
    --color-cream: #F8F7F2;
    --color-brown: #8A6A4A;
    /* ... */
}
```

### Đổi font chữ
```css
--font-display: 'Playfair Display', serif;
--font-body: 'Poppins', sans-serif;
```

### Điều chỉnh khoảng cách
```css
--spacing-xs: 0.5rem;
--spacing-sm: 1rem;
--spacing-md: 1.5rem;
/* ... */
```

## 📱 Responsive Breakpoints

- **Desktop**: > 1024px
- **Tablet**: 768px - 1024px
- **Mobile**: < 768px
- **Small Mobile**: < 480px

## 🔧 Tích hợp thêm

### Tích hợp Google Analytics
Thêm vào trong tag `<head>` của `index.html`:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'GA_ID');
</script>
```

### Tích hợp Facebook Pixel
```html
<!-- Facebook Pixel -->
<img height="1" width="1" src="https://www.facebook.com/tr?id=PIXEL_ID&ev=PageView&noscript=1" />
```

### Tích hợp Chatbot Messenger
```html
<!-- Messenger Plugin Code -->
<div id="fb-root"></div>
<script>
    window.fbAsyncInit = function() {
        FB.init({
            xfbml: true,
            version: 'v18.0'
        });
    };
</script>
```

### Tích hợp API hoặc Backend
Cập nhật hàm `handleOrderSubmit` trong `script.js`:
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
    fetch('/api/orders', {
        method: 'POST',
        headers: {
            'Content-Type': 'application/json',
        },
        body: JSON.stringify(formData)
    })
    .then(response => response.json())
    .then(data => {
        // Xử lý response
        showSuccessModal();
    })
    .catch(error => console.error('Error:', error));
}
```

## 📦 Chuyển đổi sang framework khác

### React
- Sử dụng component-based architecture
- Quản lý state với useState/useReducer
- CSS modules hoặc Styled Components
- React Router cho navigation

### Vue.js
- Sử dụng Vue components
- Vue Router cho navigation
- Pinia hoặc Vuex cho state management

### Next.js
- Hỗ trợ SSR/SSG
- API routes cho backend
- Image optimization
- SEO optimization tích hợp

### Laravel/PHP
- Backend form processing
- Database integration
- Email notifications
- Payment gateway integration

## 🌐 Triển khai

### Triển khai lên Netlify
1. Push code lên GitHub
2. Kết nối với Netlify
3. Chọn build command: (để trống)
4. Deploy

### Triển khai lên Vercel
1. Push code lên GitHub
2. Import project trên Vercel
3. Automatic deployment

### Triển khai lên Server
1. Upload files lên hosting
2. Cập nhật đường dẫn hình ảnh nếu cần
3. Test trên domain cuối cùng

## 🐛 Troubleshooting

### Hình ảnh không hiển thị
- Kiểm tra đường dẫn hình ảnh
- Đảm bảo thư mục `images/` tồn tại
- Kiểm tra quyền truy cập file

### Giỏ hàng không lưu
- Kiểm tra nếu localStorage được bật
- Kiểm tra console để tìm lỗi JavaScript
- Clear browser cache

### Hiệu ứng AOS không hoạt động
- Đảm bảo CDN AOS được tải thành công
- Kiểm tra file script.js

### Dark Mode không hoạt động
- Kiểm tra localStorage availability
- Xác nhận CSS variables được định nghĩa đúng

## 📞 Hỗ trợ

Nếu có bất kỳ vấn đề hoặc câu hỏi, vui lòng kiểm tra:
1. Console của trình duyệt (F12)
2. Tất cả CDN links có khả dụng
3. JavaScript errors

## 📄 Ghi chú

- Sử dụng placeholder images từ `via.placeholder.com` - thay thế bằng hình ảnh thực tế
- Form hiện tại chỉ hiển thị modal thành công - cần tích hợp backend để lưu đơn hàng
- Countdown timer được tính từ 1 tháng từ ngày hiện tại
- Cart data được lưu trong localStorage (phía client)

## 📊 Performance Tips

1. **Hình ảnh**: Nén hình ảnh, sử dụng WebP format
2. **CSS**: Sử dụng CSS minified trong production
3. **JavaScript**: Lazy load scripts
4. **Caching**: Cấu hình browser caching
5. **CDN**: Sử dụng CDN cho fonts và libraries

## 🔐 Security

- Input validation đã được thêm vào forms
- Không lưu thông tin nhạy cảm trên client
- HTTPS recommended cho deployment
- Sanitize user inputs trước khi gửi server

---

**Tạo bởi**: Tiệm Trà An Nhiên  
**Phiên bản**: 1.0  
**Ngày cập nhật**: 2024  
**License**: MIT
