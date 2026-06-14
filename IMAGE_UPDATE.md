# 🖼️ Cập nhật hình ảnh - Tiệm Trà An Nhiên

**Ngày cập nhật:** 2024  
**Status:** ✅ Hoàn thành

---

## 📸 Các thay đổi thực hiện

### 1. Banner Chìm (Parallax Effect) ✅
- **File:** `index.html` + `style.css` + `script.js`
- **Ảnh dùng:** `./img/banner.jpg`
- **Tính năng:**
  - Background image fixed (sticky)
  - Parallax scroll effect (chuyển động chậm khi scroll)
  - Overlay gradient xanh đục
  - Animation zoom nhẹ
  - Responsive trên mọi kích thước

**Code:**
```html
<div class="hero-background" style="background-image: url('./img/banner.jpg');"></div>
<div class="hero-overlay"></div>
```

---

### 2. Hình ảnh Sản phẩm ✅
- **Cập nhật:** 6 sản phẩm thực tế từ thư mục `./img/`
- **Sản phẩm đã thêm:**

| Sản phẩm | Giá | Loại | Hình ảnh |
|---------|-----|------|---------|
| Trà Đông Trùng Hạ Thảo | 55,000đ | Trà truyền thống | Trà đông trùng hạ thảo An Nhiên.jpg |
| Trà Dưỡng Nhan An Nhiên | 48,000đ | Trà trái cây | Trà Dưỡng Nhan An Nhiên.jpg |
| Trà Dưỡng Tâm | 50,000đ | Trà truyền thống | Trà Dưỡng Tâm.jpg |
| Trà Gạo Lứt Thảo Mộc | 42,000đ | Trà truyền thống | Trà Gạo Lứt Thảo Mộc.jpg |
| Trà Giải Nhiệt Chanh Dây | 45,000đ | Trà trái cây | Trà giải nhiệt CHANH DÂY KIM QUẤT.jpg |
| Trà Sáng C Tối A Đẹp Da | 52,000đ | Trà trái cây | Trà sáng C tối A đẹp da...png |

- **Placeholder:** 5 sản phẩm khác vẫn dùng placeholder (có thể thêm ảnh sau)

---

### 3. Ảnh Câu chuyện An Nhiên ✅
- **File:** `index.html` section About
- **Ảnh dùng:** `./img/anhcauchuyen.png`
- **Thay đổi:**
  ```html
  <img src="./img/anhcauchuyen.png" alt="Pha trà">
  ```

---

### 4. Cập nhật Gallery ✅
- **File:** `script.js` mảng `galleryImages`
- **6 ảnh trong gallery:**
  1. `./img/banner.jpg` - Không gian quán
  2. `./img/anhcauchuyen.png` - Quy trình pha chế
  3. `./img/Trà đông trùng hạ thảo An Nhiên.jpg` - Trà Đông Trùng Hạ Thảo
  4. `./img/Trà Dưỡng Nhan An Nhiên.jpg` - Trà Dưỡng Nhan
  5. `./img/Trà Dưỡng Tâm.jpg` - Trà Dưỡng Tâm
  6. `./img/Trà Gạo Lứt Thảo Mộc.jpg` - Trà Gạo Lứt

---

### 5. Cập nhật Logo ✅
- **File:** `index.html` (Header + Footer)
- **Ảnh dùng:** `./img/logo.png`
- **Thay đổi:**
  - Header: `<img src="./img/logo.png" alt="Tiệm Trà An Nhiên">`
  - Footer: `<img src="./img/logo.png" alt="Tiệm Trà An Nhiên">`

---

## 🎨 Tính năng mới

### Parallax Scroll Effect
```css
.hero-background {
    background-attachment: fixed;  /* Sticky effect */
}

@keyframes zoomIn {
    0% { transform: scale(1); }
    100% { transform: scale(1.05); }
}
```

```javascript
window.addEventListener('scroll', function() {
    const scrollPosition = window.pageYOffset;
    hero.style.backgroundPosition = `center ${scrollPosition * 0.5}px`;
});
```

### Overlay Gradient
```css
.hero-overlay {
    background: linear-gradient(135deg, 
        rgba(90,122,86,0.5),      /* Xanh đậm bán trong */
        rgba(168,184,157,0.5)     /* Xanh nhạt bán trong */
    );
}
```

---

## 📁 Cấu trúc file hình ảnh

```
img/
├── logo.png                           ✅ Logo tiệm
├── banner.jpg                         ✅ Banner hero (chìm)
├── anhcauchuyen.png                   ✅ Ảnh câu chuyện An Nhiên
├── Trà đông trùng hạ thảo An Nhiên.jpg    ✅ Sản phẩm 1
├── Trà Dưỡng Nhan An Nhiên.jpg            ✅ Sản phẩm 2
├── Trà Dưỡng Tâm.jpg                      ✅ Sản phẩm 3
├── Trà Gạo Lứt Thảo Mộc.jpg               ✅ Sản phẩm 4
├── Trà giải nhiệt CHANH DÂY KIM QUẤT.jpg  ✅ Sản phẩm 5
├── Trà sáng C tối A đẹp da An Nhiên...png ✅ Sản phẩm 6
└── đường nâu.jpg                      (Chưa sử dụng)
```

---

## ✅ Kiểm tra

Để xác nhận tất cả hoạt động:

1. **Mở browser:**
   ```
   Double-click index.html
   ```

2. **Kiểm tra từng phần:**
   - ✅ Banner: Có parallax khi scroll?
   - ✅ Menu: Có hình ảnh sản phẩm?
   - ✅ About: Có ảnh câu chuyện?
   - ✅ Gallery: Có 6 ảnh đầy đủ?
   - ✅ Logo: Hiển thị ở header và footer?

3. **Test responsive:**
   - Bấm F12 → Chọn device → Xem có đủ đẹp không

---

## 🔍 Chi tiết kỹ thuật

### File đã sửa:
- ✅ `index.html` - Thêm style background-image cho hero, cập nhật logo, cập nhật ảnh about
- ✅ `style.css` - Thêm parallax effect, hero-overlay, animation zoom
- ✅ `script.js` - Cập nhật menuItems (6 sản phẩm), galleryImages, thêm parallax scroll listener

### CSS Parallax Tricks:
```css
background-attachment: fixed;     /* Sticky khi scroll */
background-size: cover;           /* Che phủ toàn bộ */
background-position: center;      /* Căn giữa */
```

### JavaScript Parallax:
```javascript
const scrollPosition = window.pageYOffset;
hero.style.backgroundPosition = `center ${scrollPosition * 0.5}px`;
/* 0.5 = tốc độ chìm (càng nhỏ chìm càng chậm) */
```

---

## 💡 Nâng cấp trong tương lai

Nếu muốn thêm:

1. **Thêm sản phẩm khác:**
   - Sửa `script.js` mảng `menuItems`
   - Thêm ảnh vào thư mục `./img/`

2. **Thay đổi tốc độ parallax:**
   ```javascript
   scrollPosition * 0.5  // Chỉnh 0.5 thành số khác
   ```

3. **Thay đổi overlay color:**
   ```css
   background: linear-gradient(135deg, 
       rgba(90,122,86,0.7),    /* Thay 0.7 (độ đục) */
       rgba(168,184,157,0.7)
   );
   ```

4. **Disable parallax trên mobile:**
   ```css
   @media (max-width: 768px) {
       .hero-background {
           background-attachment: scroll;  /* Bỏ parallax */
       }
   }
   ```

---

## 📊 Kết quả

| Tính năng | Status | Ghi chú |
|----------|--------|--------|
| Banner chìm (parallax) | ✅ Hoàn thành | Fixed background + zoom animation |
| Hình ảnh sản phẩm | ✅ 6/11 hoàn thành | Còn 5 dùng placeholder |
| Ảnh câu chuyện | ✅ Hoàn thành | anhcauchuyen.png |
| Gallery | ✅ Hoàn thành | 6 ảnh thực tế |
| Logo | ✅ Hoàn thành | Header + Footer |
| Responsive | ✅ Hoàn thành | Tất cả kích thước |

---

## 🎉 Hoàn thành!

Landing page Tiệm Trà An Nhiên giờ đây có:
- ✅ Banner chìm đẹp với parallax effect
- ✅ Hình ảnh sản phẩm thực tế
- ✅ Ảnh câu chuyện An Nhiên
- ✅ Gallery với ảnh sản phẩm
- ✅ Logo trên header và footer
- ✅ Responsive trên mọi thiết bị

**Thử ngay:** Double-click `index.html` 🚀
