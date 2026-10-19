# 📚 BookVerse — Vũ Trụ Sách Thế Hệ Mới

> **BÀI THI GIỮA KỲ — HỌC PHẦN THIẾT KẾ WEB**  
> **Trường:** Đại học Lạc Hồng — **Khoa:** Công nghệ Thông tin  
> **Sinh viên thực hiện:** Nguyễn Minh Anh — **MSSV:** 125001893 — **Lớp:** 25AI111  
> **Live Preview (GitHub Pages):** [https://jinozgx-god.github.io/Anh_NguyenMinh_125001893/](https://jinozgx-god.github.io/Anh_NguyenMinh_125001893/)  
> **GitHub Repository:** [https://github.com/JinozGX-god/Anh_NguyenMinh_125001893](https://github.com/JinozGX-god/Anh_NguyenMinh_125001893)

---

## 🌟 Giới Thiệu Dự Án

**BookVerse** là một Landing Page nhà sách trực tuyến & thư viện số tương tác thế hệ mới, được thiết kế theo phong cách **Modern Gen Z / Dark Cyber Aesthetic** kết hợp bảng màu neon mờ ảo (Electric Violet, Rose Pink, Neon Cyan). 

Dự án áp dụng **100% hình ảnh bìa sách và độc giả thật**, giải quyết triệt để vấn đề font chữ tiếng Việt với bộ đôi font hiện đại `Be Vietnam Pro` và `Plus Jakarta Sans`, mang lại trải nghiệm đọc sách đa chiều sống động và trực quan ngay trên trình duyệt.

---

## 🎯 Bám Sát 100% Nội Dung 5 Bài Học Trong Học Kỳ

| Bài học | Trọng tâm học phần | Triển khai thực tế trên BookVerse |
|---|---|---|
| **BÀI 02 — Semantic HTML5 & Cấu Trúc Hệ Thống** | Cấu trúc DOM có thứ bậc, sử dụng đúng thẻ ngữ nghĩa theo chuẩn W3C. | ✅ Khai báo đầy đủ các phân vùng: `<header>`, `<nav>`, `<main>`, `<aside>` (thanh sidebar lọc sách), `<section>`, `<article>` (từng cuốn sách), `<figure>`, `<figcaption>`, `<blockquote>`, `<footer>`, `<address>`. Đảm bảo 100% thẻ `<img>` có thuộc tính `alt` chuẩn SEO và `loading="lazy"`. |
| **BÀI 03 — CSS Layout System (Flexbox & Grid)** | Mô hình Box Model, Flexbox 1 chiều và CSS Grid 2 chiều. | ✅ Bố cục khu vực Tủ Sách chia 2 chiều: Sidebar `<aside>` 280px + Grid sản phẩm 3 cột.<br>✅ CSS Grid 4 cột cho dịch vụ và Footer.<br>✅ Flexbox cho thanh điều hướng, ô tìm kiếm Spotlight Ctrl K, nút bấm, cụm đánh giá sao. |
| **BÀI 04 — Design System & Responsive (Mobile First)** | Quản lý Design Tokens bằng CSS Variables, tư duy Mobile First. | ✅ Khai báo toàn bộ Design Tokens trong `:root` (màu sắc, typography, spacing, border-radius, elevation shadows).<br>✅ Viết CSS căn bản cho thiết bị di động trước, sau đó mở rộng bằng `@media (min-width: 768px)` và `@media (min-width: 1024px)`. Không tràn chiều ngang. |
| **BÀI 05 — Hiệu Ứng Chuyển Động & CSS Animations** | Transition `:hover`/`:focus`, Keyframes, tối ưu hiệu năng. | ✅ Tính năng **Quick View Modal** xem nhanh sách hoạt động bằng Pure CSS `:target`.<br>✅ Hiệu ứng 3D Floating Book ở Hero, Kệ sách 3D Bestsellers rút sách ra khi hover, Lật mở 2 trang sách 3D live.<br>✅ Tích hợp Animate.css và AOS mượt mà, **Zero JavaScript tự viết**. |
| **BÀI 06 — Hoàn Thiện & Tối Ưu Hóa Sản Phẩm** | Refactor CSS, tối ưu tài nguyên, kiểm tra chuẩn và đóng gói. | ✅ 11 hình ảnh nhiếp ảnh thật chất lượng cao lưu trữ cục bộ trong thư mục `assets/images/`.<br>✅ Bộ font `Be Vietnam Pro` chuẩn 100% tiếng Việt không bao giờ bị lỗi dấu.<br>✅ Đóng gói đầy đủ mã nguồn và báo cáo nhật ký `PROMPT_LOG.md`. |

---

## ⚡ Các Tính Năng Nổi Bật Của Website

1. **Thanh Tìm Kiếm Spotlight (Ctrl K):** Giả lập giao diện tìm kiếm hiện đại, tiện lợi.
2. **Hero Section 3D Floating Book:** Mô hình sách 3D lơ lửng không trọng lực cùng các huy hiệu nổi cam kết dịch vụ.
3. **Thanh Marquee Vô Tận:** Dải thông điệp chạy chữ liên tục mượt mà bằng `@keyframes`.
4. **Cam Kết Dịch Vụ 4 Cột:** Giao hàng 2h, 100% sách thật chuẩn NXB, bọc sách bìa kiếng miễn phí, đổi trả 7 ngày.
5. **Sidebar Lọc Danh Mục Sách (`<aside>`):** Lọc theo thể loại, mức giá, định dạng bìa (Bìa mềm/Bìa cứng/Audiobook).
6. **Lưới Sản Phẩm Hot (`<article>`):** Hiệu ứng hover phóng to ảnh bìa, hiển thị giá khuyến mãi, số sao đánh giá.
7. **Trải Nghiệm Lật Sách 3D Live (Virtual Open Book Preview):** Mô phỏng 2 trang sách lượn sóng 3D chân thực, có rãnh gáy sách đổ bóng và hiệu ứng lật uốn khi rê chuột.
8. **Kệ Sách Cyber Bestsellers 3D:** 8 cuốn sách dựng đứng trên kệ gỗ neon, hover vào cuốn nào cuốn đó sẽ rút trượt ra phía trước.
9. **Tính Năng Xem Nhanh Sách (Quick View Modal bằng Pure CSS `:target`):** Click "Xem Nhanh" mở popup chi tiết sách mà không cần 1 dòng JavaScript nào.
10. **Đánh Giá Độc Giả Thật (Bookstagram Feedback):** Ảnh chân dung thật và nhận xét thực tế từ sinh viên ĐH Lạc Hồng.
11. **Form Đặt Sách & Giao Hàng COD:** Form kính mờ Cyber Glassmorphism với validation HTML5 chuẩn mực.
12. **CSS-Only Mobile Hamburger Menu:** Sử dụng kỹ thuật Checkbox Hack thông minh cho thiết bị di động.

---

## 📁 Cấu Trúc Thư Mục Dự Án

```text
Anh_NguyenMinh_125001893/
├── index.html          # Khung Semantic HTML5 chuẩn W3C, tích hợp Animate.css & AOS
├── style.css           # Toàn bộ CSS thuần: Design System, Flexbox/Grid, CSS 3D
├── assets/
│   ├── favicon.svg     # Icon vector sách mạ vàng gold chuẩn luxury
│   └── images/         # 11 tệp hình ảnh thật chất lượng cao (bìa sách & avatar độc giả)
│       ├── book1.jpg ~ book6.jpg
│       ├── book_spotlight.jpg
│       ├── hero_library.jpg
│       └── user1.jpg ~ user3.jpg
├── PROMPT_LOG.md       # Báo cáo Nhật ký Prompt Engineering (3.0 điểm)
└── README.md           # Tài liệu giới thiệu dự án và hướng dẫn sử dụng
```

---

## 🛠️ Công Nghệ Sử Dụng

- **Ngôn ngữ:** HTML5 Ngữ nghĩa (Semantic HTML) & CSS3 Thuần.
- **Thư viện Animation (CDN):**
  - [Animate.css v4.1.1](https://animate.style/)
  - [AOS (Animate On Scroll) v2.3.1](https://michalsnik.github.io/aos/)
- **Typography:** [Google Fonts](https://fonts.google.com/) (`Be Vietnam Pro` + `Plus Jakarta Sans`).
- **Icons:** SVG Vector thuần & Emoji Unicode.
- **Ràng buộc quy chế thi:** Tuyệt đối không dùng JavaScript tự viết (Zero Custom JavaScript).

---

## 🚀 Hướng Dẫn Xem Trực Tiếp & Cài Đặt Cục Bộ

### Xem Trực Tiếp Trên Web:
Truy cập đường link GitHub Pages:  
👉 **[https://jinozgx-god.github.io/Anh_NguyenMinh_125001893/](https://jinozgx-god.github.io/Anh_NguyenMinh_125001893/)**

### Chạy Cục Bộ Trên Máy Tính:
1. Clone repository về máy:
   ```bash
   git clone https://github.com/JinozGX-god/Anh_NguyenMinh_125001893.git
   ```
2. Mở thư mục dự án và nhấp đúp vào file `index.html` để mở trực tiếp trên bất kỳ trình duyệt nào (Chrome, Edge, Firefox, Safari).

---
*Bản quyền dự án thuộc về sinh viên **Nguyễn Minh Anh** (MSSV: 125001893 — Lớp: 25AI111) — Trường Đại học Lạc Hồng.*
