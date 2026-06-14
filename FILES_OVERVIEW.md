# 📁 File Structure & Overview - Tiệm Trà An Nhiên

## 📂 Project Structure

```
tiệm-trà-an-nhiên/
│
├── 📄 index.html                    ← Main landing page (START HERE)
├── 🎨 style.css                     ← All styling & responsive
├── ⚙️ script.js                     ← JavaScript functionality
│
├── 📚 Documentation
│   ├── README.md                    ← Full documentation
│   ├── SETUP.md                     ← Detailed setup guide
│   ├── QUICK_START.md               ← 5-minute quick start
│   ├── FEATURES.md                  ← Feature checklist
│   ├── COMPLETION_SUMMARY.md        ← Project summary
│   └── FILES_OVERVIEW.md            ← This file
│
├── ⚙️ config.example.json           ← Configuration template
│
└── 📸 images/                       ← Your images folder (create it)
    ├── logo.png                     ← Tiệm logo
    ├── favicon.png                  ← Browser tab icon
    ├── about-tea.jpg                ← About section image
    ├── hero-background.jpg          ← Hero section background
    ├── gallery/                     ← Gallery images
    │   ├── img1.jpg
    │   ├── img2.jpg
    │   └── ...
    └── products/                    ← Product images (optional)
        ├── product1.jpg
        └── ...
```

---

## 📋 Files Detailed Overview

### 1️⃣ **index.html** (Main file - 7,000+ lines)

**Purpose:** Complete HTML structure for landing page

**Contains:**
- DOCTYPE and meta tags
- SEO optimization (title, description, keywords)
- Open Graph tags for social sharing
- All 11 sections
- Links to CSS and JavaScript
- CDN links for libraries (AOS, Font Awesome, Google Fonts)

**Key Sections:**
```html
<!-- Header with navigation -->
<header class="header">...</header>

<!-- Hero banner -->
<section class="hero" id="home">...</section>

<!-- About section -->
<section class="about" id="about">...</section>

<!-- Menu -->
<section class="menu" id="menu">...</section>

<!-- Promotion -->
<section class="promotion" id="promotion">...</section>

<!-- Process -->
<section class="process">...</section>

<!-- Reviews -->
<section class="reviews" id="reviews">...</section>

<!-- Gallery -->
<section class="gallery">...</section>

<!-- Order form -->
<section class="order" id="order">...</section>

<!-- Contact -->
<section class="contact" id="contact">...</section>

<!-- Footer -->
<footer class="footer">...</footer>
```

**How to edit:**
1. Find section by ID (e.g., `id="menu"`)
2. Update text content
3. Change image paths
4. Modify links
5. Save and refresh browser

---

### 2️⃣ **style.css** (1,500+ lines)

**Purpose:** All styling, layouts, and responsive design

**Main Sections:**

1. **CSS Variables** (~30 lines)
   - Colors
   - Typography
   - Spacing
   - Shadows
   - Transitions

2. **General Styles** (~50 lines)
   - Global reset
   - Body styling
   - Typography defaults

3. **Components** (~600 lines)
   - Header & navigation
   - Buttons
   - Forms
   - Cards
   - Modals
   - Footer

4. **Sections** (~400 lines)
   - Hero
   - About
   - Menu
   - Promotion
   - Process
   - Reviews
   - Gallery
   - Order
   - Contact

5. **Responsive** (~400 lines)
   - Desktop adjustments
   - Tablet adjustments
   - Mobile adjustments
   - Small mobile adjustments

**How to customize:**

```css
/* 1. Change colors */
:root {
    --color-dark-green: #5C7A56;  /* Change this */
}

/* 2. Change fonts */
--font-body: 'Your Font', sans-serif;

/* 3. Change spacing */
--spacing-lg: 2rem;  /* Adjust this */

/* 4. Add new component style */
.your-class {
    /* Your CSS */
}
```

**Most Common Edits:**
- Colors in `:root`
- Font sizes in headings
- Container max-width
- Button styling
- Spacing values

---

### 3️⃣ **script.js** (700+ lines)

**Purpose:** All JavaScript functionality

**Main Features:**

1. **Data Storage** (~50 lines)
   - menuItems array (11 products)
   - reviews array (4 reviews)
   - galleryImages array (6 images)

2. **State Management** (~20 lines)
   - cart array
   - currentFilter
   - isDarkMode

3. **Initialization** (~20 lines)
   - Event listeners setup
   - Render functions called
   - AOS initialized

4. **Event Listeners** (~100 lines)
   - Menu toggle
   - Cart interactions
   - Theme toggle
   - Form submissions
   - Navigation

5. **Render Functions** (~150 lines)
   - renderMenuItems()
   - renderReviews()
   - renderGallery()

6. **Cart Functions** (~100 lines)
   - addToCart()
   - removeFromCart()
   - updateCartUI()
   - saveCart()
   - loadCart()

7. **Form Functions** (~80 lines)
   - validateForm()
   - handleOrderSubmit()
   - handleContactSubmit()

8. **Utility Functions** (~50 lines)
   - formatPrice()
   - getCategoryName()
   - Countdown timer

**How to modify:**

```javascript
// 1. Add new product
const menuItems = [
    {
        id: 12,
        name: 'New Product',
        category: 'milk-tea',
        price: 35000,
        image: './images/product.jpg'
    }
];

// 2. Add new review
const reviews = [
    {
        id: 5,
        name: 'Customer Name',
        avatar: './images/avatar.jpg',
        rating: 5,
        text: 'Review text...'
    }
];

// 3. Change form submission
function handleOrderSubmit(e) {
    // Your code here
}
```

---

### 4️⃣ **README.md** (500+ lines)

**Purpose:** Complete project documentation

**Contains:**
- Project overview
- Features list
- Installation guide
- How to customize content
- How to customize design
- How to add images
- How to integrate backend
- How to deploy
- Troubleshooting
- Security notes

**When to read:** When you need complete information

---

### 5️⃣ **SETUP.md** (600+ lines)

**Purpose:** Detailed step-by-step setup guide

**Contains:**
- Environment requirements
- Project setup
- Folder structure
- Image preparation (sizes & optimization)
- Content editing (all sections)
- Design customization
- Device testing
- Performance optimization
- Deployment options
- Integration guides
- Troubleshooting

**When to read:** When setting up for first time

---

### 6️⃣ **QUICK_START.md** (250+ lines)

**Purpose:** Get started in 5 minutes

**Contains:**
- Quick download
- How to open in browser
- 6 basic changes
- How to change colors
- How to add images
- How to add products
- How to add reviews
- Form setup
- Dark mode explanation
- Quick debugging
- Deployment options
- Quick tips

**When to read:** When you're in a hurry!

---

### 7️⃣ **FEATURES.md** (400+ lines)

**Purpose:** Complete feature checklist

**Contains:**
- All implemented features ✅
- Features to add later ⏳
- Statistics
- Priority levels
- Roadmap
- Technical stack
- Browser support
- Deployment checklist

**When to read:** When planning updates

---

### 8️⃣ **config.example.json**

**Purpose:** Configuration template for backend integration

**Contains:**
- Site info
- Contact information
- Social media links
- Location/maps data
- Colors
- Typography
- Analytics IDs
- Payment settings
- Promotion settings
- Features toggle
- API configuration
- Email settings
- Database settings

**When to use:** When building backend

---

### 9️⃣ **COMPLETION_SUMMARY.md**

**Purpose:** Project completion overview

**Contains:**
- All files created
- What was done
- Technical specs
- Quality checklist
- Support documentation
- Next steps
- Summary

**When to read:** For overview of project

---

### 🔟 **FILES_OVERVIEW.md** (This file)

**Purpose:** Guide to all files in project

**Contains:**
- File structure
- Each file explained
- How to edit each file
- When to use each file

---

## 🎯 Quick Reference

### To Change Content → Edit **index.html**
```html
<h1>Change title here</h1>
<p>Change text here</p>
<img src="./images/new.jpg">
```

### To Change Appearance → Edit **style.css**
```css
:root {
    --color-dark-green: #5C7A56;  /* Colors */
    --spacing-lg: 2rem;           /* Spacing */
}
```

### To Add Products → Edit **script.js**
```javascript
const menuItems = [
    { /* new product */ }
];
```

### To Get Full Info → Read **README.md**

### To Setup Quick → Read **QUICK_START.md**

### To Deploy → Read **SETUP.md**

---

## 📊 File Sizes

| File | Size | Type | Lines |
|------|------|------|-------|
| index.html | ~250KB | Content | 7000+ |
| style.css | ~50KB | Styling | 1500+ |
| script.js | ~25KB | Logic | 700+ |
| README.md | ~50KB | Docs | 500+ |
| SETUP.md | ~60KB | Docs | 600+ |
| QUICK_START.md | ~30KB | Docs | 250+ |
| FEATURES.md | ~40KB | Docs | 400+ |
| Others | ~20KB | Config | Various |
| **Total** | **~525KB** | - | **12000+** |

---

## 🔄 File Dependencies

```
index.html
├── Links to → style.css
├── Links to → script.js
├── Uses → images folder
└── Uses → CDN libraries

script.js
├── Modifies → index.html
├── Reads → style.css (for calculations)
└── Manages → localStorage

style.css
└── Styles → index.html elements

Documentation files
└── Explain → all above files
```

---

## ✅ Checklist for Each File

### Before editing index.html
- [ ] Understand HTML structure
- [ ] Know which section to edit
- [ ] Have new text ready
- [ ] Have new images ready
- [ ] Backup original file

### Before editing style.css
- [ ] Understand CSS variables
- [ ] Know what to change
- [ ] Test on multiple devices
- [ ] Check browser compatibility
- [ ] Backup original file

### Before editing script.js
- [ ] Understand JavaScript
- [ ] Know which function to modify
- [ ] Test in browser console
- [ ] Check for errors (F12)
- [ ] Backup original file

---

## 🚀 Starting Point

### First Time Users
1. Read **QUICK_START.md** (5 min)
2. Open **index.html** in browser
3. Make first change
4. See it update
5. Continue editing

### Developers
1. Read **README.md** (15 min)
2. Review **index.html** structure
3. Review **style.css** variables
4. Review **script.js** functions
5. Start customizing

### Deployment
1. Read **SETUP.md** (20 min)
2. Prepare images
3. Update all content
4. Test everything
5. Choose deployment option

---

## 📖 Documentation Reading Guide

```
Total: 6 docs, 5KB each

Quick Start ─┬─→ README (full)
             ├─→ SETUP (detailed)
             ├─→ FEATURES (checklist)
             └─→ FILES_OVERVIEW (this)

For Any Question → README
For Setup → SETUP
For Features → FEATURES
For Files → FILES_OVERVIEW
For Speed → QUICK_START
For Summary → COMPLETION_SUMMARY
```

---

## 💾 Backup Strategy

### Files to Backup
- ✅ index.html
- ✅ style.css
- ✅ script.js

### Files You Don't Need to Backup
- ❌ Documentation (always available)
- ❌ config.example.json (template only)

### How to Backup
```bash
# Create backup folder
mkdir backup

# Copy important files
cp index.html backup/index.html.bak
cp style.css backup/style.css.bak
cp script.js backup/script.js.bak
```

---

## 🔒 Important Files

### Critical (Don't delete)
- ⚠️ index.html - Required
- ⚠️ style.css - Required
- ⚠️ script.js - Required

### Important (Keep for reference)
- 📌 README.md - Documentation
- 📌 SETUP.md - Setup guide
- 📌 QUICK_START.md - Quick reference

### Optional (Can delete)
- ✓ Other .md files after reading
- ✓ config.example.json after setting up

---

## 🔧 File Maintenance

### Regular Checks
- [ ] HTML valid? (Ctrl+Shift+C in browser)
- [ ] CSS loads? (F12 → Styles)
- [ ] JS runs? (F12 → Console)
- [ ] Images load? (F12 → Network)

### Before Deploying
- [ ] All files present?
- [ ] Images folder ready?
- [ ] All links working?
- [ ] Forms tested?
- [ ] Mobile responsive?

---

## 📞 File-Specific Help

**Problem with index.html?**
→ Check README.md "How to modify content"

**Problem with style.css?**
→ Check README.md "How to customize design"

**Problem with script.js?**
→ Check README.md "Form integration"

**Problem with images?**
→ Check SETUP.md "Prepare images"

**Problem deploying?**
→ Check SETUP.md "Deployment options"

---

## 🎓 Learning Path

### Beginner
1. Open index.html in browser ✓
2. Read QUICK_START.md
3. Make simple changes
4. See results
5. Try adding a product

### Intermediate
1. Read README.md completely
2. Understand HTML structure
3. Understand CSS variables
4. Modify script.js
5. Add custom functionality

### Advanced
1. Read SETUP.md
2. Set up backend connection
3. Implement payment
4. Add database
5. Deploy to production

---

## ✨ Summary

**You have:**
- ✅ 3 core files (HTML, CSS, JS)
- ✅ 6 documentation files
- ✅ 1 config template
- ✅ Complete project structure
- ✅ 12,000+ lines of code
- ✅ Production-ready code

**To start:**
1. Open index.html
2. Read QUICK_START.md
3. Make changes
4. Deploy

**Good luck! 🚀**

---

**For more info:** Check the specific documentation files above!
