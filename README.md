# 🍳 NutriPlan - Ứng Dụng Lập Kế Hoạch Dinh Dưỡng Thông Minh

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/ericphan2545/NutriPlan)
[![License](https://img.shields.io/badge/license-ISC-green.svg)](LICENSE)
[![Deploy](https://img.shields.io/badge/deploy-GitHub%20Pages-brightgreen.svg)](https://ericphan2545.github.io/NutriPlan/)

## 📋 Giới Thiệu

**NutriPlan** là một ứng dụng web toàn diện giúp người dùng quản lý dinh dưỡng và lập kế hoạch bữa ăn hàng tuần. Ứng dụng tích hợp nhiều tính năng hữu ích như thư viện món ăn, kiểm tra BMI, lập thực đơn tuần và quản lý món ăn yêu thích.

## ✨ Tính Năng Chính

### 1. 📚 Thư Viện Món Ăn (Food Library)
- **Tìm kiếm thông minh**: Tìm kiếm món ăn theo tên với tính năng debounce
- **Lọc đa dạng**: 
  - Lọc theo danh mục (Món nước, Món quay, Món tráng miệng, Món mặn)
  - Lọc theo độ khó (Dễ, Trung bình, Khó)
  - Lọc theo thời gian nấu (Dưới 30 phút, 30-60 phút, Trên 60 phút)
- **Chi tiết công thức**: Xem đầy đủ thông tin về nguyên liệu và cách chế biến
- **Đánh dấu yêu thích**: Lưu các món ăn yêu thích để xem lại sau

### 2. 📊 Kiểm Tra BMI & Tính Toán Dinh Dưỡng
- **Tính toán BMI**: Dựa trên chiều cao, cân nặng, giới tính và tuổi
- **Tính BMR**: Tính toán tỷ lệ trao đổi chất cơ bản (Basal Metabolic Rate) theo công thức Harris-Benedict
- **Tính TDEE**: Tính toán tổng năng lượng tiêu hao hàng ngày (Total Daily Energy Expenditure) dựa trên BMR và mức độ vận động
- **Mục tiêu calo**: Đề xuất lượng calo phù hợp dựa trên BMI và mục tiêu sức khỏe
- **Phân tích dinh dưỡng**: Hiển thị chỉ số BMI trên thang đo trực quan với phân loại (Thiếu cân, Bình thường, Thừa cân, Béo phì)
- **Gợi ý dinh dưỡng**: Đưa ra lời khuyên và gợi ý món ăn phù hợp với tình trạng sức khỏe
- **Lưu trữ thông tin**: Tự động lưu thông tin cơ thể để sử dụng cho Meal Planner

### 3. 🗓️ Lập Thực Đơn Tuần (Meal Planner)
- **Lịch tuần**: Lập kế hoạch bữa ăn cho cả tuần (7 ngày, 3 bữa/ngày: Sáng, Trưa, Tối)
- **Chọn món ăn**: Chọn món ăn từ cơ sở dữ liệu phong phú với 52 món ăn Việt Nam đặc trưng
- **Tự động đề xuất**: Tính năng tự động tạo thực đơn cân bằng dinh dưỡng dựa trên mục tiêu calo
- **Theo dõi dinh dưỡng**: 
  - Hiển thị tổng lượng Carbohydrate, Protein, Chất béo, Chất xơ theo ngày
  - Cảnh báo khi thực đơn mất cân bằng dinh dưỡng (khi một nhóm > 60%)
  - Hiển thị mục tiêu calo và so sánh với thực tế
- **Quản lý tuần**: Chuyển đổi giữa các tuần, lưu trữ dữ liệu tự động
- **Giới hạn lặp lại**: Mỗi món ăn chỉ được sử dụng tối đa 2 lần/tuần để đa dạng hóa
- **Lọc món ăn**: Lọc theo nhóm dinh dưỡng (Tinh bột, Đạm, Chất béo, Chất xơ, Cân bằng)

### 4. ❤️ Trang Yêu Thích (Favorites)
- **Quản lý món yêu thích**: Xem tất cả các món ăn đã đánh dấu yêu thích
- **Xóa nhanh**: Dễ dàng bỏ yêu thích từ trang này
- **Đồng bộ dữ liệu**: Tự động cập nhật khi có thay đổi từ các trang khác

### 5. 🎨 Giao Diện & Trải Nghiệm
- **Dark/Light Mode**: Chuyển đổi giữa chế độ sáng và tối
- **Responsive Design**: Tối ưu cho mọi thiết bị (desktop, tablet, mobile)
- **UI/UX hiện đại**: Giao diện đẹp mắt, dễ sử dụng với các animation mượt mà
- **Lưu trữ cục bộ**: Tất cả dữ liệu được lưu trong localStorage, không cần đăng nhập

## 🛠️ Công Nghệ Sử Dụng

### Frontend
- **HTML5**: Cấu trúc trang web semantic
- **CSS3**: Styling với kiến trúc module hóa:
  - `base.css`: Reset CSS, biến CSS (CSS Variables), typography
  - `layout.css`: Layout system, grid system, responsive utilities
  - `components.css`: Reusable components (buttons, cards, modals, etc.)
  - `theme.css`: Dark/Light theme system với CSS Variables
  - `meal-planner.css`: Styles chuyên biệt cho Meal Planner
  - `style.css`: Main stylesheet (imported by modules)
- **JavaScript (ES6+ Modules)**: 
  - ES6 Modules với `import/export`
  - Event-driven architecture
  - Custom Events để đồng bộ giữa các trang
- **Tailwind CSS v4**: Utility-first CSS framework (PostCSS plugin)
- **Vite v7**: Build tool, development server với HMR (Hot Module Replacement)
- **PostCSS**: CSS processing với Autoprefixer

### Dữ Liệu
- **LocalStorage**: Lưu trữ dữ liệu người dùng:
  - Thông tin BMI, BMR, TDEE, mục tiêu calo
  - Thực đơn tuần (hỗ trợ nhiều tuần)
  - Danh sách món ăn yêu thích
  - Lịch sử món ăn đã sử dụng
- **JavaScript Objects**: 
  - `FOOD_DATABASE`: 52 món ăn với thông tin dinh dưỡng (calories, carbs, protein, fat, fiber)
  - `recipesDB`: Cơ sở dữ liệu công thức với hình ảnh, nguyên liệu, hướng dẫn nấu

### Build & Deploy
- **Vite**: Bundling và optimization
- **GitHub Pages**: Hosting static website

## 📁 Cấu Trúc Dự Án

```
NutriPlan-dev/
├── index.html              # Trang chủ - Thư viện món ăn
├── meal-planner.html       # Trang lập thực đơn tuần
├── favorites.html         # Trang món ăn yêu thích
│
├── css/                   # Stylesheets
│   ├── base.css           # Reset, variables, base styles
│   ├── layout.css         # Layout và grid system
│   ├── components.css     # Reusable components
│   ├── theme.css          # Dark/Light theme
│   ├── meal-planner.css   # Meal Planner specific styles
│   └── style.css          # Main stylesheet
│
├── js/                    # JavaScript modules (ES6+)
│   ├── app.js             # Main application entry point
│   ├── food-library.js    # Food Library page logic (search, filter, display)
│   ├── food-database.js   # Food database (52 dishes with nutrition data)
│   ├── bmi-checker.js     # BMI, BMR, TDEE calculation logic
│   ├── meal-planner.js    # Meal Planner core logic (weekly planning, auto-suggest)
│   ├── favorites.js       # Favorites page logic & recipe data
│   ├── recipes.js         # Recipe database & modal display logic
│   ├── theme.js           # Theme toggle functionality (Dark/Light mode)
│   └── nav-indicator.js   # Navigation active state indicator
│
├── assets/                # Static assets
│   └── images/           # Food images
│       ├── pho.jpg
│       └── banhmi.jpg
│
├── public/                # Public assets (copied to dist by Vite)
│   └── js/               # Public JS files (non-module scripts)
│
├── dist/                  # Build output (generated)
│
├── node_modules/         # Dependencies
│
├── package.json          # Project dependencies & npm scripts
├── vite.config.js        # Vite configuration (base path, build options)
├── tailwind.config.js    # Tailwind CSS v4 configuration
├── postcss.config.js     # PostCSS configuration (Tailwind, Autoprefixer)
├── github/               # GitHub Actions workflows
│   └── workflows/
│       └── static.yml    # GitHub Pages deployment workflow
└── README.md             # Project documentation
```

## 🚀 Cài Đặt & Sử Dụng

### Yêu Cầu Hệ Thống
- **Node.js**: v14 trở lên (khuyến nghị v18+)
- **npm**: v6 trở lên hoặc **yarn**
- **Trình duyệt**: Chrome, Firefox, Safari, Edge (phiên bản mới nhất)

### Cài Đặt

1. **Clone repository**
```bash
git clone https://github.com/ericphan2545/NutriPlan.git
cd NutriPlan
```

2. **Cài đặt dependencies**
```bash
npm install
```

3. **Chạy development server**
```bash
npm run dev
```

Ứng dụng sẽ chạy tại `http://localhost:5173` (hoặc port khác nếu 5173 đã được sử dụng)

**Lưu ý**: Vite sẽ tự động mở trình duyệt và có Hot Module Replacement (HMR) để reload tự động khi code thay đổi.

### Build cho Production

```bash
npm run build
```

Files được build sẽ nằm trong thư mục `dist/`

**Lưu ý**: 
- Base path được cấu hình là `/NutriPlan/` cho GitHub Pages
- Nếu deploy ở domain khác, cần chỉnh sửa `vite.config.js`

### Preview Production Build

```bash
npm run preview
```

Sẽ chạy production build tại `http://localhost:4173` để test trước khi deploy.

### Deploy lên GitHub Pages

1. Build project: `npm run build`
2. Commit và push code lên GitHub
3. GitHub Actions sẽ tự động deploy (nếu đã cấu hình workflow)
4. Hoặc manual: Settings → Pages → Source: `gh-pages` branch hoặc `dist/` folder

## 📖 Hướng Dẫn Sử Dụng

### 1. Sử Dụng Thư Viện Món Ăn
- Truy cập trang chủ (`index.html`)
- Sử dụng thanh tìm kiếm để tìm món ăn (có debounce để tối ưu)
- Click vào các nút lọc để lọc theo:
  - Danh mục: Tất cả, Món nước, Món quay, Món tráng miệng, Món mặn
  - Độ khó: Tất cả, Dễ, Trung bình, Khó
  - Thời gian nấu: Tất cả, Dưới 30 phút, 30-60 phút, Trên 60 phút
- Click vào nút ❤️ để đánh dấu món yêu thích (tự động lưu vào localStorage)
- Click "Xem Công Thức" để xem chi tiết cách nấu trong modal

### 2. Kiểm Tra BMI
- Truy cập trang Meal Planner (`meal-planner.html`)
- Click nút "⚙️ Cập nhật" ở card BMI hoặc mở modal cài đặt
- Nhập thông tin:
  - Giới tính: Nam/Nữ
  - Tuổi: 10-100 tuổi
  - Chiều cao: 100-250 cm
  - Cân nặng: 30-300 kg
  - Mức độ vận động: Ít vận động, Vận động nhẹ, Vận động vừa, Vận động nhiều
- Click "✨ Tính toán & Lưu" để xem kết quả:
  - BMI với phân loại (Thiếu cân, Bình thường, Thừa cân, Béo phì)
  - BMR (Basal Metabolic Rate)
  - TDEE (Total Daily Energy Expenditure)
  - Mục tiêu calo hàng ngày
- Dữ liệu được tự động lưu và sử dụng cho Meal Planner

### 3. Lập Thực Đơn Tuần
- Sau khi nhập thông tin BMI, quay lại trang Meal Planner
- **Chọn món thủ công:**
  - Click vào các ô trống trong lịch tuần (7 ngày × 3 bữa)
  - Modal sẽ hiển thị danh sách món ăn với các tab lọc (Tất cả, Tinh bột, Đạm, Chất béo, Chất xơ, Cân bằng)
  - Chọn món ăn phù hợp (món đã dùng 2 lần/tuần sẽ bị vô hiệu hóa)
- **Tự động đề xuất:**
  - Click nút "Tự động đề xuất" ở header lịch tuần
  - Hệ thống sẽ tự động tạo thực đơn cân bằng dinh dưỡng dựa trên mục tiêu calo
  - Cảnh báo nếu chưa có thông tin BMI
- **Theo dõi dinh dưỡng:**
  - Xem tổng dinh dưỡng ở phần tóm tắt phía trên (Carbs, Protein, Fat, Fiber)
  - Chú ý cảnh báo ⚠️ nếu thực đơn mất cân bằng
- **Quản lý tuần:**
  - Sử dụng nút ◀ ▶ để chuyển đổi giữa các tuần
  - Dữ liệu tự động lưu khi có thay đổi

### 4. Quản Lý Món Yêu Thích
- Truy cập trang Favorites (`favorites.html`)
- Xem tất cả món ăn đã đánh dấu yêu thích (hiển thị số lượng)
- Click ❤️ trên card món ăn để bỏ yêu thích
- Click "Xem Công Thức" để xem chi tiết trong modal
- Trang sẽ tự động cập nhật khi có thay đổi từ trang chủ
- Hiển thị thông báo khi chưa có món yêu thích nào

## 🎯 Tính Năng Nổi Bật

### Tự Động Đề Xuất Thực Đơn
- Phân tích mục tiêu calo và dinh dưỡng của người dùng từ BMI/TDEE
- Thuật toán thông minh:
  - Tự động chọn món ăn đa dạng, tránh lặp lại
  - Ưu tiên các món chưa được sử dụng trong tuần trước
  - Phân bổ món ăn theo bữa (sáng, trưa, tối) phù hợp
  - Đảm bảo cân bằng dinh dưỡng (tinh bột, đạm, chất béo, chất xơ)
  - Tối ưu để đạt mục tiêu calo hàng ngày
- Hiển thị cảnh báo nếu không có thông tin BMI

### Cảnh Báo Cân Bằng Dinh Dưỡng
- Theo dõi tỷ lệ các nhóm dinh dưỡng trong thực đơn tuần
- Cảnh báo khi một nhóm dinh dưỡng chiếm quá 60% tổng số món
- Hiển thị cảnh báo trực quan với icon ⚠️
- Đưa ra gợi ý cụ thể để cân bằng lại (thêm món từ nhóm thiếu)
- Tính toán và hiển thị tổng dinh dưỡng theo ngày (Carbs, Protein, Fat, Fiber)

### Lưu Trữ Dữ Liệu
- Tự động lưu thông tin BMI, BMR, TDEE, mục tiêu calo
- Lưu thực đơn cho nhiều tuần (hỗ trợ chuyển đổi giữa các tuần)
- Lưu danh sách món yêu thích
- Lưu lịch sử món ăn đã sử dụng để tránh lặp lại
- Dữ liệu được lưu trong localStorage, không mất khi refresh
- Đồng bộ dữ liệu giữa các trang thông qua Custom Events và Storage API

## 🔧 Development

### Scripts

- `npm run dev`: Chạy development server với hot reload
- `npm run build`: Build project cho production
- `npm run preview`: Preview production build

### Code Structure

- **Modular JavaScript**: 
  - Mỗi tính năng được tách thành module riêng với ES6 modules
  - Sử dụng object pattern để tổ chức code (FoodLibrary, MealPlanner, BMIChecker)
  - Separation of concerns: mỗi file xử lý một chức năng cụ thể
  
- **CSS Architecture**: 
  - Modular CSS với các file riêng biệt
  - CSS Variables cho theme system
  - BEM-like naming convention cho components
  
- **Data Management**: 
  - Centralized food database (`food-database.js`) với 52 món ăn
  - Recipe database (`recipes.js`) với đầy đủ thông tin công thức
  - LocalStorage API để persist data
  - Custom events để đồng bộ dữ liệu giữa các trang
  
- **Event-driven Architecture**: 
  - Custom Events (`favoritesUpdated`, `storage`) để giao tiếp giữa modules
  - Event listeners để cập nhật UI tự động
  - Storage Event API để đồng bộ giữa các tab

## 📝 Ghi Chú

- **Lưu trữ dữ liệu**: Dữ liệu được lưu trong localStorage, sẽ mất khi xóa cache trình duyệt
- **Offline Support**: Ứng dụng hoạt động hoàn toàn offline sau khi load lần đầu (trừ hình ảnh)
- **Hình ảnh**: Hình ảnh món ăn được lưu trữ online (CDN), cần kết nối internet để hiển thị
- **Cơ sở dữ liệu**: 
  - 52 món ăn Việt Nam đặc trưng trong `FOOD_DATABASE`
  - Mỗi món có đầy đủ thông tin dinh dưỡng (calories, carbs, protein, fat, fiber)
  - Recipe database với hình ảnh, nguyên liệu, hướng dẫn nấu chi tiết
- **Browser Support**: Hỗ trợ các trình duyệt hiện đại (Chrome, Firefox, Safari, Edge)
- **Performance**: 
  - Sử dụng debounce cho tìm kiếm để tối ưu hiệu năng
  - Lazy loading cho hình ảnh
  - Code splitting với Vite

## 🌐 Demo & Live Site

Ứng dụng được deploy tại: **[https://ericphan2545.github.io/NutriPlan/](https://ericphan2545.github.io/NutriPlan/)**

### Tính Năng Demo
- ✅ Thư viện 52 món ăn Việt Nam
- ✅ Tìm kiếm và lọc món ăn
- ✅ Tính toán BMI, BMR, TDEE
- ✅ Lập thực đơn tuần tự động
- ✅ Quản lý món yêu thích
- ✅ Dark/Light mode

## 📦 Dependencies

### Production Dependencies
- Không có (Pure JavaScript, HTML, CSS)

### Development Dependencies
- **vite**: ^7.3.0 - Build tool và dev server
- **tailwindcss**: ^4.1.18 - Utility-first CSS framework
- **@tailwindcss/postcss**: ^4.1.18 - Tailwind PostCSS plugin
- **postcss**: ^8.5.6 - CSS processor
- **autoprefixer**: ^10.4.23 - CSS vendor prefixer

Xem chi tiết trong `package.json`

## 📄 License

© 2025 NutriPlan. All rights reserved.

**License**: ISC

---

## 👥 Phân Công Thành Viên

### 1. Phan Tiến Thịnh - ID: 23090023
**Vai trò**: Project Leader, UI + Logic

**Nhiệm vụ đảm nhiệm**:
- **Project Leader**: Quản lý dự án, phân công công việc, đảm bảo tiến độ
- **UI Development**: 
  - Thiết kế và phát triển giao diện người dùng
  - Xây dựng layout và components
  - Responsive design cho mọi thiết bị
- **Logic Development**:
  - Phát triển logic tính toán BMI và TDEE
  - Xây dựng hệ thống Meal Planner
  - Xử lý lưu trữ dữ liệu với localStorage
  - Tích hợp các tính năng tự động đề xuất thực đơn
  - Xử lý cảnh báo cân bằng dinh dưỡng

### 2. Ngô Tấn Đức - ID: 23090008
**Vai trò**: UI Template + Fix Bug + Trang Yêu Thích

**Nhiệm vụ đảm nhiệm**:
- **UI Template**: 
  - Tạo các template giao diện mẫu
  - Thiết kế các component tái sử dụng
  - Xây dựng theme và styling
- **Fix Bug**: 
  - Phát hiện và sửa lỗi trong quá trình phát triển
  - Tối ưu hóa hiệu năng và trải nghiệm người dùng
  - Đảm bảo tính tương thích cross-browser
- **Trang Yêu Thích**: 
  - Phát triển trang Favorites (`favorites.html`)
  - Xây dựng logic quản lý món yêu thích
  - Tích hợp với hệ thống localStorage
  - Đồng bộ dữ liệu giữa các trang

### 3. Trần Văn Học - ID: 23090025
**Vai trò**: Thiết Kế API + UI

**Nhiệm vụ đảm nhiệm**:
- **Thiết Kế API**: 
  - Thiết kế cấu trúc dữ liệu cho Food Database
  - Xây dựng Recipe Database với đầy đủ thông tin món ăn
  - Thiết kế schema dữ liệu cho Meal Planner
  - Tối ưu hóa cách lưu trữ và truy xuất dữ liệu
- **UI Development**: 
  - Phát triển giao diện người dùng
  - Thiết kế các trang chính (Food Library, Meal Planner)
  - Xây dựng modal và các component tương tác
  - Tối ưu hóa trải nghiệm người dùng

---

**Lưu ý**: Dự án được phát triển bởi nhóm 3 thành viên với sự phân công công việc rõ ràng, đảm bảo chất lượng và tiến độ hoàn thành.

---

## 🔮 Tính Năng Tương Lai (Future Features)

- [ ] Đăng nhập/Đăng ký người dùng
- [ ] Lưu trữ dữ liệu trên cloud (Firebase/Backend API)
- [ ] Chia sẻ thực đơn với bạn bè
- [ ] Thêm món ăn tùy chỉnh của người dùng
- [ ] Xuất thực đơn ra PDF
- [ ] Thống kê dinh dưỡng theo tuần/tháng
- [ ] Nhắc nhở bữa ăn (Notifications)
- [ ] Tích hợp API món ăn từ bên thứ ba
- [ ] Hỗ trợ nhiều ngôn ngữ (i18n)
- [ ] Progressive Web App (PWA) support

---

## 🤝 Đóng Góp

Nếu bạn muốn đóng góp cho dự án, vui lòng:

1. Fork repository
2. Tạo feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Mở Pull Request

---

## 📞 Liên Hệ

- **Email**: ThinhDucHoc2005@vnuk.edu.vn
- **GitHub**: [@ericphan2545](https://github.com/ericphan2545)
- **Website**: [https://ericphan2545.github.io/NutriPlan/](https://ericphan2545.github.io/NutriPlan/)

---

## 🙏 Lời Cảm Ơn

Cảm ơn tất cả những người đã đóng góp và sử dụng NutriPlan! 🎉
