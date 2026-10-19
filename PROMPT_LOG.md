# NHẬT KÝ PROMPT ENGINEERING (PROMPT_LOG.md)
**Học phần:** Thiết kế Web — **Bài thi:** Giữa kỳ (Kiểm tra Kỹ năng Vibe Coding & Prompt Engineering)  
**Trường:** Đại học Lạc Hồng — **Khoa:** Công nghệ Thông tin  

---

## 📌 THÔNG TIN SINH VIÊN & ĐỀ TÀI

- **Họ và tên:** Nguyễn Minh Anh
- **Mã số sinh viên (MSSV):** 125001893
- **Lớp:** 25AI111
- **Tên đề tài Website:** **BookVerse — Thế Giới Sách Của Bạn** (Landing Page Nhà Sách Trực Tuyến & Thư Viện Sách 3D Tương Tác)
- **Công cụ AI sử dụng:** Antigravity IDE (Powered by Gemini & Claude)
- **Quy chuẩn tên Repository:** `Anh_NguyenMinh_125001893`
- **Link GitHub Repository:** `https://github.com/[username]/Anh_NguyenMinh_125001893` *(Thay [username] bằng tài khoản GitHub của bạn)*
- **Link Live Preview (GitHub Pages):** `https://[username].github.io/Anh_NguyenMinh_125001893/` *(Link xem trực tiếp sau khi bật GitHub Pages)*

---

## §1. SYSTEM / INITIAL PROMPT (Khởi Tạo Ban Đầu)

### Bối cảnh & Mục tiêu
Xây dựng một website Landing Page chủ đề **Nhà sách trực tuyến & Thư viện sách tương tác 3D (BookVerse)** đáp ứng 100% các tiêu chí khắt khe của đề thi: chuẩn Semantic HTML5, CSS Variables, Layout Flexbox/Grid, hiệu ứng chuyển động mượt mà bằng Animate.css và AOS, **tuyệt đối không sử dụng JavaScript thuần ngoài script khởi tạo AOS**, và giao diện chuẩn thẩm mỹ hiện đại (Luxury Emerald Green & Gold).

### Prompt tổng quan ban đầu đã nhập:
```text
Hãy đóng vai trò là một Chuyên gia Thiết kế Website, Chuyên gia UX/UI cấp cao và Master về HTML/CSS.
Tôi đang thực hiện bài thi Thiết kế Web với các quy định nghiêm ngặt:
1. Công nghệ: Chỉ dùng HTML5 ngữ nghĩa và CSS thuần. Tuyệt đối không dùng JavaScript tự viết (chỉ được dùng 2 thư viện CDN: Animate.css và AOS để khởi tạo hiệu ứng cuộn trang).
2. Semantic HTML5: Bắt buộc đủ tối thiểu 5 thành phần: <header>, <nav>, <main>, <section> hoặc <article>, <footer>. Sử dụng thêm các thẻ <figure>, <figcaption>, <blockquote>, <address>. Không lạm dụng thẻ <div> vô nghĩa.
3. Kỹ thuật CSS: 
   - Sử dụng CSS Variables (:root) quản lý đồng bộ toàn bộ bảng màu (Emerald Deep Green #1a3c34, Gold #c9a84c, Cream #faf6f0), typography, spacing, shadows, border-radius.
   - Bố cục 100% bằng Flexbox và CSS Grid.
   - Hiệu ứng CSS 3D Transforms đặc sắc: Card lật 3D (Flip Card) và kệ sách 3D (Bookshelf Pull-out) khi hover.
   - Form đăng ký ứng dụng Glassmorphism hiện đại với trạng thái :hover, :focus chỉn chu.
   - Responsive hoàn chỉnh cho máy tính bảng và điện thoại di động (Menu mobile dùng thuần CSS Checkbox Hack).
4. Thư viện tích hợp:
   - Animate.css cho Hero banner và CTA buttons.
   - AOS (Animate On Scroll) cho các khối nội dung cuộn trang mượt mà.

Chủ đề: "BookVerse - Thế Giới Sách Của Bạn". Hãy bắt đầu phân tích và dựng kiến trúc mã nguồn.
```

---

## §2. ITERATION LOGS (Nhật Ký Các Lần Tinh Chỉnh)

---

### 🔄 Lần 1: Dựng khung Semantic HTML5 & Hệ thống CSS Variables

#### 1. Prompt đã dùng:
```text
Dựng cấu trúc khung HTML5 chuẩn Semantic cho website BookVerse gồm các phần:
- <header> chứa logo BookVerse và thanh điều hướng <nav>.
- <main> bao gồm các section: Hero (#home), Sách nổi bật (#featured), Danh mục (#categories), Kệ sách Bestseller (#bestsellers), Độc giả nói gì (#reviews), và Đăng ký nhận sách (#subscribe).
- <footer> chứa thông tin bản quyền, social links và địa chỉ liên hệ chuẩn thẻ <address>.
Đồng thời, tạo file style.css khai báo hệ thống CSS Variables trong :root với hơn 25 biến quản lý màu sắc, kiểu chữ (Google Fonts: Playfair Display + Inter), spacing và bóng đổ.
```

#### 2. Kết quả AI sinh ra:
- Khởi tạo thành công file `index.html` với cấu trúc cây phân cấp chuẩn W3C, không sử dụng `<div>` bừa bãi.
- File `style.css` định nghĩa đầy đủ `:root` với bảng màu hài hòa phong cách thư viện học thuật cao cấp (`--clr-primary`, `--clr-secondary`, `--bg-cream`,...).
- Thiết lập CSS Reset chuẩn hiện đại (`box-sizing: border-box`, `margin: 0`, `scroll-behavior: smooth`).

#### 3. Nhận xét & Đánh giá của Sinh viên:
- **Ưu điểm:** Khung HTML rất chuẩn chỉnh về ngữ nghĩa SEO, accessibility (`aria-label`, `<label for="...">`). Hệ thống biến CSS Variables rất đầy đủ và trực quan.
- **Vấn đề phát hiện:** AI ban đầu đề xuất thẻ `<div>` cho các cuốn sách nổi bật và trích dẫn đánh giá của khách hàng.
- **Tinh chỉnh của sinh viên:** Yêu cầu đổi các khối sách nổi bật thành `<figure>` kèm `<figcaption>` để nâng cao ngữ nghĩa, và khối khách hàng đánh giá thành `<article>` chứa `<blockquote>`.

---

### 🔄 Lần 2: Xây dựng tính năng tương tác CSS 3D (Flip Card & Bookshelf)

#### 1. Prompt đã dùng:
```text
Hãy lập trình hiệu ứng CSS 3D mà không dùng bất kỳ dòng JavaScript nào:
1. Section "Sách Nổi Bật": Thiết kế các thẻ sách 3D Flip Card. Mặt trước hiển thị bìa sách nghệ thuật (CSS gradient + typography), khi hover sẽ xoay 180 độ quanh trục Y (perspective: 1000px, rotateY(180deg), backface-visibility: hidden) để hiển thị mặt sau gồm thông tin chi tiết, tóm tắt và giá sách.
2. Section "Kệ Sách Bestseller": Tạo kệ sách bằng gỗ 3D với 8 cuốn sách dựng đứng (thẻ <ol> và <li>). Khi rê chuột (hover) vào từng gáy sách, cuốn sách đó sẽ trượt nhô ra phía trước kèm góc nghiêng 3D và đổ bóng sâu chân thực.
```

#### 2. Kết quả AI sinh ra:
- Bộ code CSS 3D hoàn chỉnh cho cả 2 section:
  + Flip card sử dụng `.flip-card__inner` với `transform-style: preserve-3d` và `transition: transform 0.8s cubic-bezier(...)`.
  + Bookshelf sử dụng màu sắc phong phú, hiệu ứng `:hover` đẩy sách lên `translateY(-35px) translateZ(20px) rotate(-3deg)`.
  + Gỗ kệ sách được giả lập bằng CSS linear-gradient và bóng đổ đa tầng.

#### 3. Nhận xét & Đánh giá của Sinh viên:
- **Ưu điểm:** Hiệu ứng trực quan cực kỳ ấn tượng, mang lại trải nghiệm thư viện số chân thực và vượt xa các website thông thường.
- **Tinh chỉnh của sinh viên:** Thêm thuộc tính CSS `-webkit-backface-visibility: hidden` để hỗ trợ hiển thị mượt mà trên trình duyệt Safari/WebKit và bổ sung đổ bóng `box-shadow` động khi lật thẻ.

---

### 🔄 Lần 3: Tích hợp thư viện Animate.css và AOS (Animate On Scroll)

#### 1. Prompt đã dùng:
```text
Tích hợp 2 thư viện CSS Animation từ CDN theo đúng yêu cầu đề bài:
1. Thư viện Animate.css: Áp dụng hiệu ứng animate__fadeInUp và animate__fadeIn cho tiêu đề chính H1 và các nút CTA tại Hero Section, có chỉnh animate__delay hợp lý để các thành phần xuất hiện tuần tự mượt mà.
2. Thư viện AOS: Áp dụng data-aos="fade-up", data-aos="zoom-in", data-aos-delay cho các section bên dưới để khi người dùng cuộn chuột, từng khối nội dung sẽ trồi lên tự nhiên.
Lưu ý: Hiệu ứng phải tinh tế, trang nhã, không lạm dụng gây rối mắt người xem.
```

#### 2. Kết quả AI sinh ra:
- Thêm link CDN của Animate.css v4.1.1 và AOS v2.3.1 vào thẻ `<head>`.
- Gắn các thuộc tính `data-aos="fade-up"`, `data-aos="zoom-in"` và `data-aos-delay` (100ms - 400ms) vào các card sách, category và review.
- Thêm script khởi tạo AOS ở cuối thẻ `<body>`: `AOS.init({ duration: 800, once: true, offset: 100 });`.

#### 3. Nhận xét & Đánh giá của Sinh viên:
- **Ưu điểm:** Hiệu ứng xuất hiện nhịp nhàng khi cuộn chuột, không làm nặng trang.
- **Tinh chỉnh của sinh viên:** Thiết lập `once: true` trong cấu hình AOS để animation chỉ chạy một lần khi cuộn tới, tránh tình trạng giật lag hoặc lặp đi lặp lại khi người dùng cuộn lên cuộn xuống.

---

### 🔄 Lần 4: Responsive Design, CSS-Only Mobile Menu & Form Glassmorphism

#### 1. Prompt đã dùng:
```text
Hoàn thiện tính thẩm mỹ và khả năng hiển thị đa thiết bị:
1. Thiết kế Mobile Navigation hoàn toàn bằng CSS (Checkbox Hack: <input type="checkbox" id="nav-toggle"> kết hợp label hamburger 3 gạch và selector :checked ~ .nav__menu) để mở/đóng menu trên mobile mà KHÔNG dùng JavaScript.
2. Thiết kế Form đăng ký nhận sách (#subscribe) theo phong cách Glassmorphism (nền kính mờ backdrop-filter: blur, viền mờ phản chiếu ánh sáng).
3. Viết Media Queries hoàn chỉnh cho Tablet (<= 768px) và Mobile (<= 480px), đảm bảo không bị vỡ layout hoặc tràn chiều ngang (overflow-x).
```

#### 2. Kết quả AI sinh ra:
- Hệ thống Media Queries cho 3 mốc: Desktop (> 1024px), Tablet (<= 768px), Mobile (<= 480px).
- Hamburger menu CSS-only với hiệu ứng chuyển đổi mượt 3 vạch thành dấu X khi click.
- Form đăng ký kính mờ sang trọng với `:focus-visible` viền vàng gold tinh tế.
- Tùy chỉnh thanh cuộn trình duyệt (Custom Scrollbar) đồng bộ màu sắc.

#### 3. Nhận xét & Đánh giá của Sinh viên:
- **Ưu điểm:** Giao diện co giãn chuẩn responsive từ màn hình máy tính đến màn hình điện thoại 375px mà không bị thanh cuộn ngang khó chịu.
- **Nhận xét & Tinh chỉnh của sinh viên:** Trên thiết bị di động, chuyển kệ sách Bestseller thành dạng cuộn ngang (`overflow-x: auto` với `-webkit-overflow-scrolling: touch`) để người dùng vuốt chạm tiện lợi.

---

### 🔄 Lần 5: Đột phá UI/UX theo phong cách Gen Z Trendy & Trải Nghiệm Tương Tác Đa Chiều

#### 1. Prompt đã dùng:
```text
Website phiên bản đầu tiên còn đơn giản và hơi ít nội dung, font chữ có chân kiểu vintage chưa đủ thu hút giới trẻ. Hãy nâng cấp toàn diện:
1. Phong cách thiết kế: Chuyển sang Dark Mode thời thượng (#090d16) kết hợp các quả cầu ánh sáng mờ Ambient Glow đa sắc (Electric Violet #8b5cf6, Cyan #06b6d4, Rose Pink #ec4899).
2. Typography: Đổi toàn bộ font chữ sang bộ đôi hiện đại, cực kỳ nịnh mắt: 'Outfit' (tiêu đề tròn trịa, hiện đại) và 'Plus Jakarta Sans' (nội dung thanh thoát, chuẩn công nghệ).
3. Làm giàu nội dung & Tính năng:
   - Thêm Bento Grid đa tầng giới thiệu đặc quyền: Audiobook AI, Hộp mù Blind Box, Cày Streak 28 ngày.
   - Thêm tính năng 3D Virtual Open Book Preview: Lật mở 2 trang sách 3D thực tế bằng Pure CSS.
   - Nâng cấp 3D Flip Card thành Holographic Foil phản quang shimmer lấp lánh chủ đề BookTok Trending.
   - Thêm Flash Deal giờ vàng với đồng hồ countdown boxes, thanh Marquee chạy chữ vô tận và Reviews phong cách Bookstagram mạng xã hội.
4. Ràng buộc: Giữ trọn vẹn 100% chuẩn Semantic HTML5, không phát sinh lỗi layout và tuyệt đối KHÔNG dùng JavaScript tự viết.
```

#### 2. Kết quả AI sinh ra:
- Khung giao diện lột xác hoàn toàn, mang đậm hơi thở hiện đại, nịnh mắt và tràn đầy năng lượng của giới trẻ.
- Tích hợp thành công hiệu ứng lật mở 2 trang sách 3D (`.book-3d` với `.book-page--left` và `.book-page--right` có hiệu ứng đổ bóng ở gáy sách).
- Hệ thống Bento Grid với hiệu ứng sóng âm nhạc động (`.audio-wave`) và ngọn lửa streak (`.streak-flame`) tạo ấn tượng thị giác mạnh mẽ.

#### 3. Nhận xét & Đánh giá của Sinh viên:
- **Ưu điểm:** Giao diện cuốn hút vượt bậc, tạo ấn tượng "WOW" ngay từ giây đầu tiên. Các chi tiết mô phỏng mạng xã hội và BookTok đánh trúng tâm lý người trẻ.
- **Tinh chỉnh của sinh viên:** Cân chỉnh lại kích thước trang sách 3D trên màn hình điện thoại dưới 768px (`flex-direction: column`) để tránh vỡ chữ, đồng thời tăng độ tương phản của text trên nền kính mờ để đảm bảo khả năng đọc chuẩn Accessibility.

---

### 🔄 Lần 6: Tối Ưu Hóa Bám Sát 100% 5 Bài Học Học Phần Thiết Kế Web & Sử Dụng Nhiếp Ảnh Sách Thật

#### 1. Prompt đã dùng:
```text
Dựa theo nội dung 5 bài học cốt lõi đã học trong học phần Thiết Kế Web (ĐH Lạc Hồng):
- Bài 02 (Semantic HTML5): Sử dụng đúng cấu trúc DOM với <header>, <nav>, <main>, <aside> (sidebar lọc sách), <section>, <article> (sản phẩm), <figure>, <figcaption>, <blockquote>, <footer>, <address>. Không lạm dụng <div>. Đảm bảo 100% thẻ <img> có thuộc tính alt chuẩn SEO và loading="lazy".
- Bài 03 (Layout System): Kết hợp Flexbox (căn chỉnh menu, nút, header) và CSS Grid 2 chiều (Catalog layout gồm Sidebar <aside> 280px + Grid sản phẩm 3 cột; Services grid 4 cột; Footer grid 4 cột).
- Bài 04 (Design System & Mobile First): Dùng CSS Variables trong :root quản lý Design Tokens. Thiết kế theo tư duy Mobile First (viết CSS cơ bản cho mobile trước, mở rộng bằng @media (min-width: 768px) và @media (min-width: 1024px)). Sửa triệt để lỗi hiển thị dấu tiếng Việt bằng font 'Be Vietnam Pro' kết hợp 'Plus Jakarta Sans'.
- Bài 05 (Hiệu Ứng): Tối ưu transitions trên :hover, :focus. Xây dựng tính năng Xem Nhanh Sách (Quick View Modal) hoạt động 100% bằng CSS :target thuần mà KHÔNG dùng JavaScript.
- Bài 06 (Hoàn Thiện): Loại bỏ các tính năng không thiết thực (blindbox, streak game); thay thế toàn bộ emoji icon bằng hình ảnh bìa sách thật và ảnh độc giả chân dung thật lưu cục bộ trong thư mục assets/images/. Bổ sung form đặt sách và tư vấn chi tiết, thực tế.
```

#### 2. Kết quả AI sinh ra:
- Khởi tạo thành công thư mục `assets/images/` chứa 11 tệp hình ảnh nhiếp ảnh sách thật và chân dung người đọc thực tế, loại bỏ hoàn toàn cảm giác icon AI sơ sài.
- Toàn bộ typography được chuyển sang font chuyên dụng `Be Vietnam Pro` (tối ưu hóa 100% tiếng Việt, hiển thị mượt mà không lỗi bất kỳ ký tự có dấu nào).
- Bổ sung thanh Sidebar `<aside>` lọc sách chuyên nghiệp bên cạnh lưới sản phẩm `<article>`, bám sát chuẩn kiến trúc DOM được giảng dạy trong Bài 02 & Bài 03.
- Tính năng Quick View Modal mở chi tiết sách khi click bằng CSS `:target` mượt mà, tiện dụng và tuyệt đối tuân thủ quy chế thi (Zero JavaScript).

#### 3. Nhận xét & Đánh giá của Sinh viên:
- **Ưu điểm:** Website đã trở thành một nhà sách trực tuyến thực thụ, đáng tin cậy và thẩm mỹ cao. Bố cục trang mạch lạc, cân đối, đáp ứng hoàn hảo tiêu chí chấm thi của cả 5 bài học trên lớp.
- **Tinh chỉnh của sinh viên:** Thêm thanh thông báo miễn phí vận chuyển trên đầu trang, tích hợp hotline hỗ trợ, phân trang pagination và bổ sung chính sách đổi trả minh bạch để tăng độ tin cậy thực tế cho trang web.

---

### ⚠️ THÁCH THỨC KỸ THUẬT & DEBUG PROMPT

Trong quá trình thực hiện bài thi, tôi đã gặp phải 3 vấn đề kỹ thuật lớn và đã tiến hành viết prompt debug để giải quyết triệt để:

#### Thách thức 1: Xử lý Menu Mobile khi đề bài cấm dùng JavaScript
- **Hiện tượng:** Thông thường nút hamburger menu cần JS để toggle class `active`. Đề bài nghiêm cấm viết JS.
- **Debug Prompt:**
  ```text
  "Đề bài cấm dùng JavaScript hoàn toàn cho logic trang. Hãy viết kỹ thuật CSS Checkbox Hack chuẩn UX để khi người dùng nhấn vào biểu tượng 3 gạch trên mobile, menu sẽ trượt xuống mượt mà và 3 vạch chuyển thành dấu X, không dùng 1 dòng JS nào."
  ```
- **Giải pháp xử lý:** Sử dụng `<input type="checkbox" id="nav-toggle" hidden>` đặt trước `<label>` và `<ul class="nav__menu">`. Trong CSS dùng bộ chọn `#nav-toggle:checked ~ .nav__menu { display: flex; transform: translateY(0); }` và transform cho các thẻ `span` bên trong hamburger.

#### Thách thức 2: Lỗi lật thẻ 3D Flip Card bị nhấp nháy hoặc lộ mặt sau trên Safari/iOS
- **Hiện tượng:** Khi hover trên một số trình duyệt nền WebKit, mặt sau của sách bị lộ xuyên qua mặt trước trước khi xoay xong.
- **Debug Prompt:**
  ```text
  "Hiệu ứng CSS 3D card flip bị hiện tượng xuyên thấu và flickering trên WebKit/Safari. Hãy tối ưu lại các thuộc tính 3D gồm transform-style, perspective, backface-visibility và hardware acceleration."
  ```
- **Giải pháp xử lý:** Bổ sung `-webkit-backface-visibility: hidden;`, gán `transform: translateZ(0);` để ép GPU render mượt mà, và thiết lập `transform-style: preserve-3d;` chính xác trên container xoay.

#### Thách thức 3: Tràn layout ngang (Horizontal Overflow) khi xoay 3D trên màn hình nhỏ
- **Hiện tượng:** Khi các cuốn sách trên kệ hoặc card 3D phóng to/xoay, độ sâu Z khiến trình duyệt xuất hiện thanh cuộn ngang đáy màn hình.
- **Debug Prompt:**
  ```text
  "Tìm và triệt tiêu nguyên nhân gây tràn chiều ngang (horizontal scrollbar) khi render các hiệu ứng CSS 3D trên màn hình điện thoại dưới 768px."
  ```
- **Giải pháp xử lý:** Bổ sung `overflow-x: hidden` trên `body` và `html`, đồng thời giới hạn chiều rộng `.flip-card` trên mobile thành `width: 240px; height: 360px;` với padding an toàn.

---

## §3. ĐÁNH GIÁ CÁ NHÂN & BÀI HỌC KINH NGHIỆM

### 1. AI đã giúp tiết kiệm thời gian ở những phần nào?
- **Khởi tạo mã nguồn và cấu trúc chuẩn (Boilerplate):** Tiết kiệm đến **80% thời gian** gõ các thẻ Semantic HTML5 lặp đi lặp lại và khai báo hàng chục biến CSS Variables.
- **Tính toán toán học & CSS 3D Transforms:** Thay vì mất hàng giờ tự căn chỉnh góc quay `rotateY`, độ nghiêng trục Z và đổ bóng ánh sáng, AI giúp tạo công thức ma trận transform chuẩn xác ngay trong lần thử đầu tiên.
- **Tạo nội dung mẫu thực tế (Mock Data):** AI hỗ trợ tạo tên sách, tác giả, trích dẫn văn học và nhận xét độc giả bằng tiếng Việt rất tự nhiên, loại bỏ hoàn toàn việc dùng chữ `Lorem Ipsum` thô cứng.

### 2. Những khó khăn và hạn chế khi tương tác với AI
- **Nguy cơ hallucination về công nghệ:** Nếu không chỉ định chặt chẽ, AI rất dễ tự động thêm các đoạn mã JavaScript phức tạp (như script click event, slider JS library), vi phạm trực tiếp quy chế đề thi.
- **Cần sự can thiệp thẩm mỹ của con người:** AI có thể tạo ra code hoạt động tốt, nhưng tỷ lệ bố cục, sắc thái màu vàng kim hay độ mờ kính Glassmorphism cần sinh viên trực tiếp quan sát, điều chỉnh độ tương phản để đạt chuẩn Accessibility (WCAG).

### 3. Bài học rút ra về kỹ năng Prompt Engineering
1. **Thiết lập Persona & Ràng buộc ngay từ đầu (System Prompting):** Đặt vai trò chuyên gia và nêu rõ các điều cấm kỵ (ví dụ: *Zero JavaScript*, *Strict Semantic HTML*) giúp AI không đi lệch hướng.
2. **Kỹ thuật chia nhỏ vấn đề (Modular Iteration):** Không bao giờ yêu cầu AI "viết toàn bộ trang web trong 1 prompt duy nhất". Cách tiếp cận tối ưu nhất là đi theo từng tầng: Khung HTML & Variables → Bố cục CSS → Hiệu ứng nâng cao 3D → Responsive & Debug.
3. **Kỹ năng Prompt Kỹ thuật & Tinh thần Phản biện (Critical Review):** Lập trình viên không phải là người sao chép mã AI mà là "kiến trúc sư" chỉ đạo và kiểm tra chất lượng mã nguồn. Việc phát hiện lỗi và đưa ra Debug Prompt chính xác là kỹ năng cốt lõi nhất của một kỹ sư Vibe Coding hiện đại.

---
*Báo cáo được hoàn thiện và kiểm thử kỹ lưỡng, sẵn sàng cho công tác nộp bài và chấm thi.*
