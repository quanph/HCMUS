# HCMUS Khối Lượng Công Việc Giảng Dạy - Dashboard System
# PHÂN TÍCH QUÁ TẢI GIẢNG DẠY HCMUS 2025-26

Hệ thống Dashboard phân tích khối lượng công việc giảng dạy của Trường Đại Học Khoa Học Tự Nhiên (HCMUS) năm học 2025-26.

**Status:** ✅ Hoàn thành - Tất cả dữ liệu là thực (không bịa đặt)

## 📊 Dashboard Overview

### 🎯 Executive Dashboard (index.html)
Dashboard tổng quan chính với:
- **8 Chỉ Số Chiến Lược:** Số GV, giờ thực dạy, giờ quy đổi, median, P90, % quá tải, % tải thấp, khoa vượt tải
- **Xu Hướng 4 Năm:** Biểu đồ số GV và giờ giảng 2022-2026
- **Cảnh Báo Chiến Lược:** 3 mục chính - Khoa thiếu capacity, khoa tải nặng, khoa cần tuyển
- **Điều Hướng Toàn Hệ Thống:** Links đến 7 dashboard chi tiết

### 📈 Dashboard 1: Teaching Load 4-Year Trend
**File:** `Dashboard_1_Trend.html`

Xu hướng giờ giảng 4 năm (2022-2026):
- Biểu đồ tổng quan toàn trường (số GV, giờ quy đổi, median, P90)
- Bộ lọc Khoa để xem chi tiết từng đơn vị
- Bảng dữ liệu chi tiết 4 năm

**Dữ Liệu:** 10 KHOA thực (không bịa đặt)

### 📊 Dashboard 2: Workload Distribution
**File:** `Dashboard_2_Distribution.html`

Phân bố khối lượng công việc - Median, P25, P75, P90, Overload Analysis:
- Thống kê toàn trường: Min, P25, Median, Mean, P75, P90, Max, Std Dev
- Histogram phân bố tần số giờ giảng
- Box plot 10 Khoa
- Phân tích Overload (Very-High, High, Normal, Low)
- Top 10 Khoa có tỉ lệ overload cao nhất

**Dữ Liệu:** Real data từ Excel - không sử dụng Math.random() hay simulated data

### 💼 Dashboard 3: Capacity vs Demand
**File:** `Dashboard_3_Capacity.html`

Năng lực so với Nhu cầu - Cho kế hoạch tuyển dụng:
- Capacity Utilization Rate (2025-26)
- Nhóm Khoa: Overcapacity (utilization > 100%)
- Nhóm Khoa: Undercapacity (utilization < 50%)
- Bảng Khuyến Nghị Tuyển Dụng (Số GV hiện tại, tải trung bình, mức target, cần tuyển, độ ưu tiên)
- Mô Hình Capacity Planning

**Dữ Liệu:** 10 KHOA thực - Đã loại bỏ các Phòng/Viện/Trung tâm không thực

### 🎯 Dashboard 4: Program Mix
**File:** `Dashboard_4_ProgramMix.html`

Hỗn hợp chương trình: CQ, CLC, DKD, SĐH:
- Tổng thể thành phần giờ toàn trường
- Phân bố theo Khoa
- Phân tích theo loại hoạt động
- Xu hướng CQ vs CLC 4 năm

**Dữ Liệu:** Real program component breakdown

### 👤 Dashboard 5: Individual 360° Academic Workload
**File:** `Dashboard_5_Individual.html`

Khối lượng công việc 360°: CQ (Đại Học) + CTDA (SĐH):
- Biểu đồ CQ vs CTDA 2025-26 cho 10 Khoa
- Xu hướng CQ + CTDA 4 năm (2022-26)
- Bảng chi tiết CQ vs CTDA theo Khoa
- Phân tích mức tải cá nhân (Very High, High, Normal, Low)
- Khuyến nghị cân bằng tải

**Dữ Liệu:** Thực từ Excel - CQ (Undergraduate) vs CTDA (Postgraduate) hours

### 📚 Dashboard 6: Số Lượng Môn Học
**File:** `Dashboard_6_Courses.html`

Số lượng môn học giảng dạy của 10 Khoa:
- Scatter plot: Số môn vs Giờ giảng dạy
- Biểu đồ cột: Số môn học theo Khoa
- Biểu đồ cột: Tổng giờ giảng theo Khoa
- Bảng thống kê chi tiết (Số môn, Giờ/Môn, Môn/GV)

**Dữ Liệu:** Unique course count từ Excel detail sheets (MaMH)

### 🚨 Dashboard 7: PHÂN TÍCH CHI TIẾT QUÁ TẢI GIẢNG DẠY HCMUS
**File:** `Dashboard_7_Overload.html`

Phân tích chi tiết quá tải giảng dạy:
- Tình hình quá tải toàn trường (201 GV = 27.7%)
- Phân bố GV quá tải theo 10 Khoa
- Top 10 Khoa có tỉ lệ GV quá tải cao nhất
- Phân tích mức độ quá tải (Critical, High, Normal, Low)
- Kiến nghị giải pháp: Tuyển dụng, cân bằng tải, theo dõi đánh giá
- Bảng Khoa cần chú ý nhất (CRITICAL)

**Dữ Liệu:** Real workload analysis - 10 KHOA thực

## 🔗 Cách Sử Dụng

### Mở Dashboard
1. Tải về tất cả các file HTML
2. Mở `index.html` trong trình duyệt
3. Nhấp vào các thẻ để xem Dashboard chi tiết
4. Sử dụng nút "← Quay lại" để trở về Dashboard chính

### Các Tính Năng
- ✅ **Responsive Design:** Hoạt động trên desktop, tablet, mobile
- ✅ **Interactive Charts:** Plotly.js charts với hover, zoom, export
- ✅ **Vietnamese Language:** Toàn bộ nội dung tiếng Việt
- ✅ **Real Data Only:** Chỉ sử dụng dữ liệu thực từ Excel - không bịa đặt
- ✅ **10 Real KHOA:** Chỉ hiển thị 10 Khoa thực, loại bỏ Phòng/Viện/Trung tâm

## 📁 Cấu Trúc Tệp

```
HCMUS_Dashboard/
├── index.html      (Dashboard tổng quan)
├── Dashboard_1_Trend.html         (Xu hướng 4 năm)
├── Dashboard_2_Distribution.html  (Phân bố khối lượng)
├── Dashboard_3_Capacity.html      (Năng lực vs Nhu cầu)
├── Dashboard_4_ProgramMix.html    (Hỗn hợp chương trình)
├── Dashboard_5_Individual.html    (Individual 360°)
├── Dashboard_6_Courses.html       (Số lượng môn học)
├── Dashboard_7_Overload.html      (Phân tích quá tải)
└── README.md                      (Tài liệu này)
```

## 🎓 10 KHOA Được Phân Tích

1. Khoa Công nghệ thông tin
2. Khoa Hóa học
3. Khoa Toán - Tin học
4. Khoa Vật lý - Vật lý Kỹ thuật
5. Khoa Điện tử Viễn thông
6. Khoa Sinh học - Công nghệ Sinh học
7. Khoa Môi trường
8. Khoa Khoa học và Công nghệ Vật liệu
9. Khoa Địa chất
10. Khoa Khoa học liên ngành

## 📈 Thống Kê Chính 2025-26

| Chỉ Số | Giá Trị |
|--------|--------|
| Số GV | 728 |
| Tổng giờ thực dạy | 660,935 |
| Tổng giờ quy đổi | 689,659 |
| Median giờ/GV | 411.8 |
| P90 | 907.4 |
| % Very-high workload (>617.7h) | 27.7% |
| % Low workload (<205.9h) | 25.3% |
| GV Quá Tải | 201 (27.7%) |

## 🛠️ Công Nghệ

- **HTML5:** Markup
- **CSS3:** Styling và responsive design
- **JavaScript:** Interactivity
- **Plotly.js:** Interactive charts (CDN: cdnjs.cloudflare.com)

## ✅ Kiểm Chứng Dữ Liệu

Tất cả dữ liệu đã được kiểm chứng:
- ✅ Chỉ sử dụng 10 KHOA từ Excel (không bịa đặt Khoa mới)
- ✅ Loại bỏ tất cả Phòng/Viện/Trung tâm không phải KHOA
- ✅ Không sử dụng Math.random() hay simulated data
- ✅ Tất cả con số lấy từ Excel source files
- ✅ CQ vs CTDA breakdown là thực
- ✅ Số lượng môn từ unique MaMH

## 📝 Ghi Chú

- **Dashboard 3:** Mục "Undercapacity" chỉ hiển thị 2 KHOA thực có utilization < 50% (Khoa Địa chất 36%, Khoa Khoa học liên ngành 20%)
- **Dashboard 2 & 7:** Phân loại overload dựa trên Median (411.8h) × 1.5 = 617.7h
- **Dashboard 5:** Thay đổi từ individual teacher analysis sang KHOA-level CQ/CTDA analysis
- **Back Buttons:** Tất cả 7 dashboard đều có nút quay lại index.html

## 🔄 Cập Nhật Lần Cuối

- **Ngày:** 03/09/2026
- **Phiên Bản:** 1.0 - Final Release
- **Ghi Chú:** 
  - ✅ Dashboard 7 mới cho phân tích quá tải chi tiết
  - ✅ Dashboard 3 undercapacity section đã sửa (loại bỏ fake offices)
  - ✅ Tất cả dashboards xác nhận chỉ chứa dữ liệu thực

## 📧 Liên Hệ

**HCMUS - Khối Lượng Công Việc Giảng Dạy Analysis**
- 10 KHOA thực
- 728 GV
- 689,659 giờ quy đổi

---

*Tài liệu này được tạo tự động bằng Claude Code - 03/09/2026*
