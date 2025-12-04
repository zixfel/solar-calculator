# 🌞 Ứng Dụng Tính Toán Tiết Kiệm Điện Năng Lượng Mặt Trời

Ứng dụng web Progressive Web App (PWA) giúp bạn tính toán, theo dõi và phân tích hiệu quả tiết kiệm chi phí từ hệ thống năng lượng mặt trời của mình một cách chi tiết và trực quan.

**📱 Version 3.4.7** - Cập nhật ngày 04/12/2025

---

## ✨ TÍNH NĂNG CHÍNH

### 📊 1. Tổng Quát Dự Án Solar Của Bạn
Hiển thị toàn bộ thông số tổng quan của dự án năng lượng mặt trời trong một dashboard đẹp mắt:

**Các chỉ số tổng cộng:**
- 💰 **Tổng Tiết Kiệm**: Tổng số tiền đã tiết kiệm được
- 🔌 **Tổng Điện Tiêu Thụ (Load)**: Tổng lượng điện tiêu thụ
- ☀️ **Tổng Điện Solar Sản Xuất**: Tổng điện năng mặt trời tạo ra
- ⚡ **Tổng Điện Lưới EVN (Grid)**: Tổng điện mua từ lưới điện
- 💵 **Chi Phí Nếu Không Có Solar**: Chi phí giả định không dùng Solar

**Các chỉ số trung bình:**
- 📈 Trung Bình Tiết Kiệm/Tháng
- 📊 Trung Bình Tổng Điện Tiêu Thụ
- 🌤️ Trung Bình Điện Solar Sản Xuất
- 🔋 Trung Bình Điện Lưới EVN
- 📉 Trung Bình Không Có Solar/Tháng

**Đặc điểm:**
- ✅ Animation viền xoay gradient đẹp mắt
- ✅ Có thể ẩn/hiện bằng nút toggle
- ✅ Responsive hoàn toàn (desktop → mobile)
- ✅ Màu sắc xanh lá cây tươi sáng

### 📈 2. Phân Tích Nhanh (Quick Stats)
10 chỉ số thông minh giúp phân tích hiệu quả Solar:

**So sánh tháng:**
- 🏆 Tháng Tiết Kiệm Nhiều Nhất
- 📉 Tháng Tiết Kiệm Ít Nhất
- 🌤️ Tháng Solar Sản Xuất Nhiều Nhất

**Tỷ lệ phần trăm:**
- ⚡ Tỷ Lệ Sử Dụng Solar (%)
- 🔌 Tỷ Lệ Sử Dụng Lưới EVN (%)
- 🔋 Tỷ Lệ Tự Cung Tự Cấp (%)
- 💡 Hiệu Suất Tiết Kiệm (%)

**Xu hướng & thống kê:**
- 📊 Xu Hướng Gần Đây (Tăng/Giảm/Ổn định)
- 💰 Trung Bình Tiết Kiệm/Ngày
- 📅 Số Tháng Có Dữ Liệu

### 💰 3. Phân Tích Đầu Tư & ROI (Return on Investment)

**Tính năng:**
- 🏦 Nhập chi phí lắp đặt ban đầu
- 📊 4 chỉ số ROI quan trọng:
  - 💵 Chi Phí Đầu Tư
  - 💰 Đã Tiết Kiệm (với % hoàn vốn)
  - 📉 Còn Thu Hồi
  - ⏱️ Thời Gian Hoàn Vốn (tháng/năm)
- 🎉 Card "Tiền Lời" hiển thị khi đã hoàn vốn
- 📈 Thanh tiến trình ROI với màu sắc thay đổi:
  - Vàng: 0-50%
  - Tím: 50-75%
  - Xanh lá: 75-100%
  - Xanh lá đậm: > 100% (có lời)
- 📱 Tối ưu hoàn toàn cho mobile với layout compact

### ☀️ 4. Đồng Bộ Lumentree Dashboard

**2 phương thức đồng bộ:**

**🔄 Tự Động:**
- Nhập Device ID (VD: `P250801055`)
- Bấm "Lấy Dữ Liệu" để tự động fetch
- Hệ thống thử nhiều CORS proxy để đảm bảo kết nối
- Preview dữ liệu trước khi import

**📋 Thủ Công:**
- Mở link API Lumentree trực tiếp
- Copy toàn bộ JSON data
- Paste vào ứng dụng
- Xử lý và import dữ liệu

**Dữ liệu được import:**
- 📅 Dữ liệu theo tháng (Load, Grid, PV, Backup)
- 💾 Tự động lưu Device ID
- 🔄 Tự động thêm tháng nếu cần
- ✅ Preview trước khi áp dụng

### ⚡ 5. Tính Tiền Điện EVN (Bậc Thang)

**Công cụ calculator độc lập:**
- 📊 6 bậc giá điện chính thức của EVN
- 💵 Tự động tính VAT 8%
- 📋 Hiển thị chi tiết từng bậc:
  - Bậc 1: 0-50 kWh = 1,984 đ/kWh
  - Bậc 2: 51-100 kWh = 2,050 đ/kWh
  - Bậc 3: 101-200 kWh = 2,380 đ/kWh
  - Bậc 4: 201-300 kWh = 2,998 đ/kWh
  - Bậc 5: 301-400 kWh = 3,350 đ/kWh
  - Bậc 6: 401+ kWh = 3,460 đ/kWh
- 🧮 Breakdown chi tiết từng bậc
- ✅ Kiểm tra khớp với hóa đơn EVN thực tế

### 📊 6. Nhập & Quản Lý Dữ Liệu Tháng

**Nhập dữ liệu linh hoạt:**
- 📅 Hỗ trợ không giới hạn số tháng (mặc định 12 tháng)
- ➕ Thêm/xóa tháng dễ dàng
- 🗑️ Xóa từng tháng cụ thể
- 📄 Phân trang 12 tháng/trang

**3 trường dữ liệu mỗi tháng:**
- 🔌 **Load (kWh)**: Tổng điện tiêu thụ chính
- ⚡ **Grid EVN (kWh)**: Điện mua từ lưới điện
- 🔋 **Backup (kWh)**: Điện tiêu thụ phụ

**Tự động tính toán:**
- ☀️ Điện Solar = Load + Backup - Grid
- 💰 Chi phí Grid (bậc thang EVN)
- 💵 Chi phí giả định không có Solar
- 🎯 Tiết kiệm thực tế

### 📈 7. Biểu Đồ Trực Quan

**2 biểu đồ cột (Bar Charts):**
- 💰 **Biểu đồ Tiết Kiệm**: Hiển thị tiền tiết kiệm từng tháng
- ☀️ **Biểu đồ Solar**: Hiển thị điện năng mặt trời sản xuất từng tháng

**Đặc điểm:**
- 🎨 Màu sắc gradient đẹp mắt
- 📱 Responsive hoàn toàn
- 🖱️ Hover để xem chi tiết
- 📊 Tự động scale theo dữ liệu

### 📋 8. Chi Tiết Từng Tháng

**Cards thông tin chi tiết:**
- 📅 Emoji theo mùa (❄️ Đông, 🌸 Xuân, ☀️ Hè, 🍂 Thu)
- 🔌 Load, Grid, Backup, Solar (kWh)
- 💰 Chi phí EVN, Solar, Thực tế, Không Solar
- 🔥 Tiết kiệm nổi bật

**Phân trang:**
- 📄 24 tháng/trang (2 năm)
- 🔄 Điều hướng dễ dàng

### 💾 9. Lưu Trữ & Xuất Dữ Liệu

**Lưu trữ tự động:**
- 💾 LocalStorage - lưu ngay trên trình duyệt
- 🔄 Tự động load khi mở lại
- 📊 Theo dõi trạng thái lưu trữ

**Xuất/Nhập dữ liệu:**
- 📤 **Xuất JSON**: Backup toàn bộ cài đặt
- 📊 **Xuất CSV**: Báo cáo Excel chi tiết
  - Dữ liệu từng tháng
  - Tổng cộng & trung bình
  - Phân tích ROI
  - Thống kê nhanh
- 📥 **Nhập JSON**: Khôi phục từ file backup

### 🎯 10. Demo Data & Reset

**Chức năng hỗ trợ:**
- 🎯 **Demo Data**: Tải dữ liệu mẫu cho tất cả tháng
  - Tự động tăng 3%/năm
  - Giúp test nhanh ứng dụng
- 🔄 **Reset**: Xóa toàn bộ dữ liệu và bắt đầu lại
- 💾 **Lưu/Tải**: Lưu cài đặt hiện tại hoặc load lại

### 📱 11. Progressive Web App (PWA)

**Cài đặt như app native:**
- 📲 Thêm vào Home Screen (iOS/Android)
- 🚀 Mở nhanh như app thật
- 📴 Hoạt động offline (Service Worker)
- 🔄 Tự động cập nhật khi có phiên bản mới
- 🎨 Full-screen experience

---

## 🎨 GIAO DIỆN & THIẾT KẾ

### 🌈 Theme & Colors
- 🌃 **Dark theme** với gradient xanh dương đẹp mắt
- 💚 **Accent color**: Xanh lá cây (#4ade80) cho Solar
- 💜 **Purple**: Tím (#8b5cf6) cho ROI
- 🌊 **Gradient backgrounds**: Hiệu ứng sống động

### ✨ Animations & Effects
- 🌀 **Rotating gradient borders** trên cards tổng quan
- 💫 **Smooth transitions** khi hover
- 🎯 **Scale & shadow effects** khi tương tác
- 📈 **Progress bar animations** cho ROI

### 📱 Responsive Design
**Desktop (> 768px):**
- 5-6 columns grid
- Full features hiển thị
- Hover effects đầy đủ

**Tablet (768px - 1024px):**
- 2-3 columns grid
- Tối ưu cho màn hình cảm ứng

**Mobile (< 768px):**
- 2 columns grid cho cards
- 3 columns grid cho month inputs (siêu compact)
- ROI section compact với mini cards
- Buttons 3x3 grid layout
- Font size & spacing tối ưu
- Prevent iOS zoom (font-size: 16px)

**Extra Small (< 400px):**
- Tối ưu tối đa cho màn hình nhỏ
- Compact spacing
- Touch-friendly buttons

---

## 🚀 CÁCH SỬ DỤNG

### Bước 1: Nhập Dữ Liệu
1. 📊 Vào section "Nhập Dữ Liệu (12 Tháng)"
2. ➕ Thêm tháng nếu cần (hoặc dùng 12 tháng mặc định)
3. 🔌 Nhập Load, Grid, Backup cho mỗi tháng
4. 🎯 Hoặc bấm "Demo" để test nhanh

**Hoặc đồng bộ từ Lumentree:**
1. ☀️ Bấm "Đồng Bộ Lumentree"
2. 🔗 Nhập Device ID (VD: P250801055)
3. 🔄 Chọn "Tự Động" hoặc "Thủ Công"
4. ✅ Import dữ liệu vào ứng dụng

### Bước 2: Nhập Chi Phí Đầu Tư (Tùy chọn)
1. 💰 Vào section "Đầu Tư & ROI"
2. 💵 Nhập chi phí lắp đặt hệ thống Solar
3. 📊 Xem phân tích ROI tự động

### Bước 3: Tính Toán
1. 🔍 Bấm nút "Tính"
2. ⏱️ Đợi vài giây xử lý
3. ✅ Xem kết quả hiển thị

### Bước 4: Phân Tích
1. 📊 Xem "Tổng Quát Dự Án Solar Của Bạn"
2. 📈 Xem "Phân Tích Nhanh" để hiểu xu hướng
3. 💰 Xem ROI để biết tiến độ hoàn vốn
4. 📋 Xem "Chi Tiết Từng Tháng" nếu cần

### Bước 5: Lưu & Xuất
1. 💾 Bấm "Lưu Cài Đặt" để lưu vào trình duyệt
2. 📤 "Xuất" để backup ra file JSON
3. 📊 "CSV" để tạo báo cáo Excel
4. 📥 "Nhập" để khôi phục từ file backup

---

## 💡 MẸO SỬ DỤNG

### ✅ Tối ưu hóa nhập liệu
- Dùng **Demo Data** để test nhanh trước
- Dùng **Lumentree Sync** nếu có thiết bị kết nối
- Nhập từng tháng theo hóa đơn EVN thực tế
- **Backup thường xuyên** bằng "Xuất" JSON

### ✅ Đọc hiểu số liệu
- **Load** = Tổng điện tiêu thụ chính (từ counter)
- **Grid** = Điện mua từ EVN (từ hóa đơn)
- **Backup** = Điện tiêu thụ phụ (nếu có)
- **Solar** = Load + Backup - Grid (tự động tính)

### ✅ Phân tích hiệu quả
- Xem **Tỷ Lệ Sử Dụng Solar** để đánh giá tự cung cấp
- Xem **Hiệu Suất Tiết Kiệm** để biết % giảm chi phí
- Xem **Xu Hướng Gần Đây** để theo dõi biến động
- So sánh **tháng tốt nhất vs tháng xấu nhất**

### ✅ ROI hiệu quả
- Nhập **chính xác chi phí đầu tư** ban đầu
- Theo dõi **% hoàn vốn** định kỳ
- Xem **thời gian hoàn vốn** ước tính
- Tính toán **tiền lời** khi đã hoàn vốn

---

## 📊 CẤU TRÚC DỮ LIỆU

### LocalStorage Keys
- `solarSettings`: Object chứa toàn bộ cài đặt
  - `solarPrice`: Giá điện solar (default: 0)
  - `vatRate`: VAT rate (default: 8%)
  - `initialCost`: Chi phí đầu tư
  - `totalMonths`: Số tháng dữ liệu
  - `startYear`: Năm bắt đầu
  - `startMonth`: Tháng bắt đầu (1-12)
  - `currentPage`: Trang hiện tại
  - `monthlyData[]`: Mảng dữ liệu từng tháng
    - `load`: Điện tiêu thụ
    - `grid`: Điện lưới EVN
    - `backup`: Điện backup
  - `savedAt`: Timestamp lưu
  - `version`: Phiên bản data schema

- `lumentreeDeviceId`: Device ID Lumentree đã lưu

### JSON Export Format
```json
{
  "solarPrice": "0",
  "vatRate": "8",
  "initialCost": "100000000",
  "totalMonths": 24,
  "startYear": 2024,
  "startMonth": 1,
  "currentPage": 1,
  "monthlyData": [
    {
      "load": "800",
      "grid": "250",
      "backup": "0"
    }
  ],
  "savedAt": "2025-12-04T10:30:00.000Z",
  "version": "3.3"
}
```

### CSV Export Format
```csv
Tháng,Load (kWh),Grid EVN (kWh),Backup (kWh),Solar (kWh),Chi Phí Grid (VNĐ),Chi Phí Solar (VNĐ),Chi Phí Thực Tế (VNĐ),Chi Phí Không Solar (VNĐ),Tiết Kiệm (VNĐ)
Tháng 1/2024,800,250,0,550,567840,0,567840,1857600,1289760
...
Tổng Cộng,9600,3000,0,6600,...
Trung Bình,800,250,0,550,...
```

---

## 🔧 KỸ THUẬT

### Frontend Stack
- **HTML5**: Semantic markup
- **CSS3**: Modern styling, Grid, Flexbox, Animations
- **JavaScript (ES6+)**: Vanilla JS, no framework
- **Chart.js**: Data visualization
- **PWA**: Service Worker, Manifest

### Features Highlights
- 📱 **Responsive**: Mobile-first design
- 💾 **LocalStorage**: Client-side persistence
- 🔄 **CORS Proxy**: Multiple fallbacks for Lumentree API
- 📊 **CSV Export**: UTF-8 BOM for Excel compatibility
- 🎨 **CSS Animations**: Smooth transitions & effects
- ♿ **Accessibility**: Semantic HTML, ARIA labels

### Browser Support
- ✅ Chrome/Edge (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Mobile browsers (iOS Safari, Chrome Android)

### File Structure
```
solar-calculator/
├── index.html           # Main app (5000+ lines)
├── README.md           # Documentation
├── manifest.json       # PWA manifest
├── service-worker.js   # PWA service worker
└── icons/             # PWA icons (if any)
```

---

## 📈 CÔNG THỨC TÍNH TOÁN

### 1. Solar Production
```
Solar = Load + Backup - Grid
```

### 2. Grid Cost (Tiered Pricing)
```javascript
// Bậc 1: 0-50 kWh
tier1 = min(grid, 50) * 1984

// Bậc 2: 51-100 kWh
tier2 = min(max(grid - 50, 0), 50) * 2050

// ... tương tự cho các bậc khác

// Tổng với VAT
totalCost = (tier1 + tier2 + ... + tier6) * 1.08
```

### 3. Savings
```
Savings = Cost Without Solar - Actual Cost
Cost Without Solar = Tiered Price(Load + Backup) * 1.08
Actual Cost = Grid Cost + Solar Cost (= 0)
```

### 4. ROI
```
Percent Recovered = (Total Savings / Initial Cost) * 100
Remaining = Initial Cost - Total Savings
Payback Months = Initial Cost / Average Monthly Savings
Profit = Total Savings - Initial Cost (when > 0)
```

### 5. Quick Stats
```
Solar % = (Total Solar / Total Load) * 100
Grid % = (Total Grid / Total Load) * 100
Self-Sufficiency % = Solar %
Savings Efficiency % = (Total Savings / Cost Without Solar) * 100
Trend = (Recent 3 months avg - Previous 3 months avg) / Previous avg * 100
```

---

## 🛠️ PHÁT TRIỂN TƯƠNG LAI

### 🎯 Tính năng đã hoàn thành
- ✅ Tính toán bậc thang EVN chính xác
- ✅ Đồng bộ Lumentree (tự động + thủ công)
- ✅ ROI analysis với progress tracking
- ✅ Quick stats với 10 chỉ số
- ✅ Mobile optimization hoàn toàn
- ✅ PWA với offline support
- ✅ CSV export với BOM UTF-8
- ✅ Section "Tổng Quát Dự Án Solar"
- ✅ Toggle cho tất cả sections
- ✅ Animation cards đẹp mắt

### 🚧 Tính năng có thể mở rộng
- ⏳ Multi-language support (EN, VI)
- ⏳ Dark/Light theme toggle
- ⏳ More chart types (Line, Pie, Stacked)
- ⏳ Yearly comparison view
- ⏳ Export to PDF report
- ⏳ Cloud sync (Firebase/Supabase)
- ⏳ Multiple solar systems comparison
- ⏳ Weather data integration
- ⏳ Solar panel degradation tracking
- ⏳ Cost projection (5, 10, 20 years)

### 💡 Ý tưởng cải tiến
- Custom color themes
- More animation options
- Advanced filtering & sorting
- Goal setting & alerts
- Social sharing features
- Community data comparison

---

## 🐛 BÁO LỖI & HỖ TRỢ

### Vấn đề thường gặp

**Q: Dữ liệu bị mất khi đóng trình duyệt?**
- A: Đảm bảo bấm "💾 Lưu Cài Đặt" trước khi đóng
- A: Kiểm tra LocalStorage không bị disable
- A: Backup thường xuyên bằng "📤 Xuất"

**Q: Không đồng bộ được Lumentree?**
- A: Thử lại 4-5 lần (proxy có thể chậm)
- A: Dùng tab "📋 Thủ Công" để copy-paste
- A: Kiểm tra Device ID có đúng không

**Q: Số tiền không khớp với hóa đơn EVN?**
- A: Kiểm tra VAT rate (default 8%)
- A: Dùng "⚡ Tính Tiền Điện EVN" để verify
- A: Đảm bảo nhập đúng Grid từ hóa đơn

**Q: App chậm khi có nhiều tháng?**
- A: Ứng dụng optimize cho ~24-36 tháng
- A: Phân trang tự động kích hoạt
- A: Xóa data cũ không cần thiết

---

## 📄 GIẤY PHÉP & CREDITS

**License:** MIT License (hoặc theo yêu cầu)

**Developed by:** [Your Name/Team]

**Libraries Used:**
- Chart.js v4.x - Data visualization
- Font Awesome icons (CDN)
- EVN tiered pricing (official rates 2024)

**API Integration:**
- Lumentree API (unofficial, community-driven)
- CORS Proxies: codetabs, corsproxy.io, allorigins, cors.sh

**Special Thanks:**
- EVN for official electricity pricing
- Lumentree for solar monitoring platform
- Community testers & contributors

---

## 📞 LIÊN HỆ

- 🌐 Website: [Your website]
- 📧 Email: [Your email]
- 💬 Facebook: [Your fanpage]
- 🐛 Issues: [GitHub Issues]

---

## 📝 CHANGELOG

### v3.4.7 (04/12/2025)
- ✨ NEW: Section "Tổng Quát Dự Án Solar Của Bạn"
- ✨ NEW: Toggle functions cho tất cả sections
- 🎨 IMPROVED: Layout tổng quan đẹp hơn với animation
- 📝 DOCS: Viết lại README.md hoàn toàn

### v3.4.6 (03/12/2025)
- ✨ NEW: Lumentree Sync (Auto + Manual)
- 🔄 IMPROVED: CORS proxy với multiple fallbacks
- 📊 IMPROVED: Preview data trước khi import

### v3.4.5 (02/12/2025)
- 📱 IMPROVED: Mobile ROI compact layout
- 🎨 IMPROVED: Mini cards 2x2 grid
- 📈 IMPROVED: Progress bar optimization

### v3.4.4 (01/12/2025)
- 📱 IMPROVED: Mobile UI consistency
- 📊 IMPROVED: 2-column layout cho mobile
- 🎨 IMPROVED: Spacing & readability

### v3.4.0-3.4.3
- ✨ NEW: Quick Stats Dashboard
- 📊 NEW: 10 chỉ số phân tích
- 🎨 NEW: Stat cards với hover effects

### v3.3.0
- 💰 NEW: ROI Analysis
- 📈 NEW: Progress tracking
- 🎯 NEW: Payback calculation

### v3.2.0
- ⚡ NEW: EVN Tiered Calculator
- 📋 NEW: Chi tiết từng bậc giá

### v3.1.0
- 📊 NEW: Chart.js integration
- 📈 NEW: Savings & Solar charts

### v3.0.0
- 🎨 REDESIGN: Dark theme UI
- ✨ NEW: Animation effects
- 📱 NEW: Responsive design

---

**🌞 Cảm ơn bạn đã sử dụng Ứng Dụng Tính Toán Solar!**

_Hãy theo dõi thường xuyên để không bỏ lỡ các tính năng mới._
