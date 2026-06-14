# Hướng dẫn thiết lập Tiệm Trà An Nhiên Landing Page

## 1️⃣ Chuẩn bị môi trường

### Yêu cầu tối thiểu
- Trình duyệt web hiện đại (Chrome, Firefox, Safari, Edge)
- Trình soạn thảo code (VS Code, Sublime, Atom, etc.)
- Kết nối Internet (để tải CDN libraries)

### Không cần cài đặt
- ❌ Node.js
- ❌ npm / yarn
- ❌ Build tools
- ❌ Database

## 2️⃣ Cài đặt dự án

### Cách 1: Tải từ GitHub
```bash
git clone https://github.com/yourusername/tiem-tra-an-nhien.git
cd tiem-tra-an-nhien
```

### Cách 2: Tải file ZIP
1. Download file ZIP
2. Giải nén vào thư mục bạn muốn
3. Mở file `index.html` trong trình duyệt

### Cách 3: Tạo từ đầu
```bash
mkdir tiem-tra-an-nhien
cd tiem-tra-an-nhien
# Copy 3 files: index.html, style.css, script.js
# Tạo thư mục: mkdir images
```

## 3️⃣ Cấu trúc thư mục

```
tiem-tra-an-nhien/
├── index.html              # File HTML chính (bắt buộc)
├── style.css               # Stylesheet (bắt buộc)
├── script.js               # JavaScript (bắt buộc)
├── README.md               # Tài liệu
├── SETUP.md               # File này
├── images/                 # Thư mục hình ảnh (khuyến khích)
│   ├── logo.png
│   ├── logo-white.png
│   ├── favicon.ico
│   ├── about-tea.jpg
│   ├── hero-background.jpg
│   └── gallery/
│       ├── img1.jpg
│       ├── img2.jpg
│       └── ...
└── vendor/                # Tùy chọn - lưu CDN libraries locally
    ├── aos.js
    ├── fontawesome/
    └── ...
```

## 4️⃣ Chuẩn bị hình ảnh

### Kích thước khuyến nghị

| Vị trí | Kích thước | Format | Ghi chú |
|--------|-----------|--------|---------|
| Logo | 200x200px | PNG | Transparent background |
| Logo trắng | 200x200px | PNG | Cho dark mode |
| Favicon | 32x32px | ICO | Browser tab icon |
| Hero Background | 1920x1080px | JPG | Large, use WebP too |
| About Section | 400x500px | JPG | 2:2.5 aspect ratio |
| Menu Items | 250x200px | JPG | Card images |
| Gallery | 300-400px | JPG | Varied sizes |
| Reviews Avatar | 60x60px | PNG | Circular, transparent |
| Social Icons | SVG | - | Vector format |

### Tối ưu hóa hình ảnh

```bash
# Sử dụng ImageMagick (nếu có)
convert original.jpg -resize 250x200 optimized.jpg

# Sử dụng TinyPNG (online)
# https://tinypng.com

# Sử dụng ImageOptim (macOS)
# Hoặc online tools như: https://imagecompressor.com
```

### Tạo placeholder tạm thời
- Sử dụng `https://via.placeholder.com/WIDTH×HEIGHT`
- Ví dụ: `https://via.placeholder.com/250x200?text=Trà+Sữa`
- Thay thế bằng hình ảnh thực tế sau

## 5️⃣ Chỉnh sửa nội dung

### 5.1 Cập nhật thông tin cơ bản

**File: index.html**

```html
<!-- Tiêu đề trang -->
<title>Tiệm Trà An Nhiên | Nơi Lắng Nghe Tâm Hồn</title>

<!-- Meta description -->
<meta name="description" content="Tiệm Trà An Nhiên - Một tách trà, một khoảng lặng cho tâm hồn...">

<!-- Meta keywords -->
<meta name="keywords" content="trà sữa, trà trái cây, tiệm trà, An Nhiên...">

<!-- Logo -->
<img src="./images/logo.png" alt="Tiệm Trà An Nhiên">
```

### 5.2 Thay đổi sản phẩm

**File: script.js**

```javascript
const menuItems = [
    {
        id: 1,
        name: 'Tên sản phẩm của bạn',
        category: 'milk-tea', // Thay đổi category
        price: 35000,         // Thay đổi giá
        image: './images/product1.jpg' // Thay đổi ảnh
    },
    // Thêm hoặc xóa sản phẩm...
];
```

**Categories có sẵn:**
- `milk-tea` - Trà sữa
- `fruit-tea` - Trà trái cây
- `traditional` - Trà truyền thống
- `topping` - Topping

### 5.3 Thay đổi đánh giá

```javascript
const reviews = [
    {
        id: 1,
        name: 'Tên khách hàng',
        avatar: './images/avatar1.jpg',
        rating: 5,
        text: 'Nhận xét của khách hàng...'
    },
    // Thêm hoặc xóa đánh giá...
];
```

### 5.4 Thay đổi thư viện ảnh

```javascript
const galleryImages = [
    { 
        id: 1, 
        image: './images/gallery1.jpg', 
        title: 'Tiêu đề ảnh' 
    },
    // Thêm hoặc xóa ảnh...
];
```

### 5.5 Cập nhật thông tin liên hệ

**Tìm và thay đổi các phần sau:**

```html
<!-- Địa chỉ -->
<p>123 Đường Lê Lợi, Quận 1, TP. Hồ Chí Minh</p>

<!-- Hotline -->
<p><a href="tel:+84123456789">+84 (0)123 456 789</a></p>

<!-- Email -->
<p><a href="mailto:hello@annhien.com">hello@annhien.com</a></p>

<!-- Giờ mở cửa -->
<p>Thứ 2 - Chủ nhật: 08:00 - 21:00<br>Thứ 2: Đóng cửa</p>
```

## 6️⃣ Tùy chỉnh giao diện

### 6.1 Đổi màu sắc

**File: style.css - Root variables**

```css
:root {
    --color-light-green: #A8B89D;      /* Xanh lá nhạt */
    --color-dark-green: #5C7A56;       /* Xanh trà đậm */
    --color-cream: #F8F7F2;            /* Trắng kem */
    --color-brown: #8A6A4A;            /* Nâu đất */
}
```

**Công cụ chọn màu:**
- https://coolors.co
- https://color.adobe.com
- https://colorpicker.com

### 6.2 Đổi font chữ

**Cập nhật Google Fonts link** (index.html):
```html
<link href="https://fonts.googleapis.com/css2?family=YourFont:wght@400;500;600;700&display=swap" rel="stylesheet">
```

**Cập nhật CSS** (style.css):
```css
:root {
    --font-display: 'Your Display Font', serif;
    --font-body: 'Your Body Font', sans-serif;
}
```

### 6.3 Điều chỉnh khoảng cách (spacing)

```css
:root {
    --spacing-xs: 0.5rem;   /* 8px */
    --spacing-sm: 1rem;     /* 16px */
    --spacing-md: 1.5rem;   /* 24px */
    --spacing-lg: 2rem;     /* 32px */
    --spacing-xl: 3rem;     /* 48px */
    --spacing-2xl: 4rem;    /* 64px */
}
```

### 6.4 Độ rộng container

```css
.container {
    max-width: 1200px;  /* Thay đổi độ rộng tối đa */
    padding: 0 var(--spacing-md);
}
```

## 7️⃣ Kiểm tra trên các thiết bị

### Desktop
- Chrome: DevTools → F12
- Firefox: DevTools → F12
- Safari: Develop Menu

### Tablet & Mobile
- iPhone/iPad: Preview trên thiết bị thực
- Android: Chrome DevTools
- Sử dụng: https://responsivedesignchecker.com

### Screen sizes để test
- 1920px (Desktop)
- 1366px (Laptop)
- 1024px (Tablet horizontal)
- 768px (Tablet)
- 480px (Mobile)
- 375px (Small phone)

## 8️⃣ Tối ưu hóa hiệu suất

### Tối ưu hình ảnh
```
Trước: 5MB
Sau (WebP + compression): 800KB - 1.5MB
```

### Minify CSS & JS
```bash
# Sử dụng online tools
https://minifier.org
https://cssnano.co
```

### Lazy loading ảnh (Optional)
```html
<img src="./images/logo.png" alt="Logo" loading="lazy">
```

### Cache optimization
Thêm vào `.htaccess` nếu hosting Apache:
```apache
<FilesMatch "\.(jpg|jpeg|png|gif|ico)$">
    Header set Cache-Control "max-age=31536000, public"
</FilesMatch>
```

## 9️⃣ Triển khai

### Option 1: Netlify (Khuyến khích)
1. Push code lên GitHub
2. Vào https://netlify.com
3. Kết nối GitHub repo
4. Automatic deployment mỗi khi push

### Option 2: Vercel
1. Push code lên GitHub
2. Import project trên https://vercel.com
3. Auto deploy

### Option 3: Hosting truyền thống
1. Mua hosting + domain
2. Upload files qua FTP
3. Cấu hình domain

### Option 4: GitHub Pages (Miễn phí)
```bash
git push origin main
# Bật GitHub Pages trong Settings
```

## 🔟 Tích hợp add-ons

### Tích hợp Google Analytics

```html
<!-- Thêm vào <head> -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'G-XXXXXXXXXX');
</script>
```

### Tích hợp Facebook Pixel

```html
<!-- Thêm vào <head> -->
<script>
    !function(f,b,e,v,n,t,s)
    {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
    n.callMethod.apply(n,arguments):n.queue.push(arguments)};
    if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
    n.queue=[];t=b.createElement(e);t.async=!0;
    t.src=v;s=b.getElementsByTagName(e)[0];
    s.parentNode.insertBefore(t,s)}(window,document,'script',
    'https://connect.facebook.net/en_US/fbevents.js');
    fbq('init', 'YOUR_PIXEL_ID');
    fbq('track', 'PageView');
</script>
```

### Tích hợp Zalo API
```html
<!-- Thêm nút Zalo -->
<a href="https://zalo.me/your_phone_number">Nhắn tin Zalo</a>
```

### Tích hợp Messenger
```html
<!-- Facebook Page Messenger -->
<script src="https://connect.facebook.net/vi_VN/sdk/xfbml.customerchat.js"></script>
<div id="fb-root"></div>
<div id="fb-customer-chat" class="fb-customerchat"></div>
<script>
    var chatbox = document.getElementById('fb-customer-chat');
    chatbox.setAttribute("page_id", "YOUR_PAGE_ID");
    chatbox.setAttribute("attribution", "biz_inbox");
</script>
```

## 1️⃣1️⃣ Khắc phục sự cố

| Vấn đề | Nguyên nhân | Giải pháp |
|--------|-----------|----------|
| Hình ảnh không hiển thị | Đường dẫn sai | Kiểm tra lại đường dẫn file |
| CSS không áp dụng | File style.css không load | Kiểm tra link trong `<head>` |
| JavaScript không chạy | Script.js không load | Kiểm tra link trước `</body>` |
| Dark mode không hoạt động | localStorage bị vô hiệu | Kiểm tra cài đặt trình duyệt |
| Giỏ hàng không lưu | LocalStorage bị xóa | Clear cookies hoặc thay browser |
| Form không gửi được | Không có backend | Thêm API endpoint |

## 1️⃣2️⃣ Bảo mật cơ bản

- ❌ Không bao giờ commit `.env` files
- ❌ Không commit hình ảnh quá lớn
- ✅ Sử dụng HTTPS trên production
- ✅ Validate input trên server
- ✅ Rate limit API endpoints

## 1️⃣3️⃣ Chạy trên máy cục bộ

### Sử dụng Python
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

### Sử dụng Node.js
```bash
npm install -g http-server
http-server
```

### Sử dụng PHP
```bash
php -S localhost:8000
```

Sau đó truy cập: `http://localhost:8000`

## 📝 Checklist trước khi deploy

- [ ] Tất cả hình ảnh đã được thêm vào
- [ ] Thông tin liên hệ đã cập nhật
- [ ] Sản phẩm đã thêm vào danh sách
- [ ] Đánh giá khách hàng đã cập nhật
- [ ] Thử form đặt hàng
- [ ] Test responsive trên mobile
- [ ] Test dark mode
- [ ] Test tất cả link navigation
- [ ] Kiểm tra SEO meta tags
- [ ] Gọi cho nhà thầu kiểm tra finalize
- [ ] Backup code trước deploy

## 🆘 Cần giúp đỡ?

1. **Kiểm tra Console**: F12 → Console → Tìm lỗi
2. **Kiểm tra Network**: F12 → Network → Xem file load
3. **Kiểm tra Source**: F12 → Sources → Debug
4. **Stack Overflow**: https://stackoverflow.com
5. **MDN Docs**: https://developer.mozilla.org

---

**Hỏi đáp nhanh:**
- Q: Tôi có thể thay đổi màu sắc không?
- A: Có, sửa CSS variables trong `style.css`

- Q: Tôi có thể thêm trang mới không?
- A: Có, tạo HTML file mới và link từ header

- Q: Tôi có thể chuyển sang React không?
- A: Có, nhưng cần refactor code

- Q: Tôi có thể bán với dự án này không?
- A: Có, code có license MIT

---

**Ngày cập nhật**: 2024
**Version**: 1.0
