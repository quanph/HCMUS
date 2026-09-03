# 📤 Hướng Dẫn Đẩy Lên GitHub

## Lệnh Để Đẩy Lên GitHub

Chạy các lệnh sau trong thư mục `HCMUS_Dashboard`:

### Option 1: Sử dụng HTTPS (Nếu chưa setup SSH)

```bash
cd HCMUS_Dashboard
git remote add origin https://github.com/quanph/HCMUS.git
git branch -M main
git push -u origin main
```

**Lưu ý:** GitHub sẽ yêu cầu Personal Access Token (PAT) thay vì password kể từ tháng 8/2021.

### Option 2: Sử dụng SSH (Recommended)

```bash
cd HCMUS_Dashboard
git remote add origin git@github.com:quanph/HCMUS.git
git branch -M main
git push -u origin main
```

**Lưu ý:** Cần setup SSH key trước (xem hướng dẫn bên dưới)

---

## 🔑 Setup SSH Key (Lần Đầu Tiên)

### 1. Tạo SSH Key
```bash
ssh-keygen -t ed25519 -C "quanph@gmail.com"
```

Hoặc nếu máy cũ không hỗ trợ ed25519:
```bash
ssh-keygen -t rsa -b 4096 -C "quanph@gmail.com"
```

### 2. Thêm SSH Key Vào SSH Agent
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

### 3. Copy Public Key
```bash
cat ~/.ssh/id_ed25519.pub
```

### 4. Thêm Vào GitHub
1. Đi tới https://github.com/settings/keys
2. Click "New SSH key"
3. Paste public key
4. Click "Add SSH key"

---

## 📦 Cấu Trúc Được Commit

```
HCMUS_Dashboard/
├── Dashboard_Executive.html       (15 KB)
├── Dashboard_1_Trend.html         (14 KB)
├── Dashboard_2_Distribution.html  (11 KB)
├── Dashboard_3_Capacity.html      (12 KB)
├── Dashboard_4_ProgramMix.html    (11 KB)
├── Dashboard_5_Individual.html    (11 KB)
├── Dashboard_6_Courses.html       (15 KB)
├── Dashboard_7_Overload.html      (13 KB)
├── README.md                      (10 KB)
└── .git/                          (git repository)
```

**Total Size:** ~120 KB (rất nhẹ)

---

## ✅ Kiểm Tra Status

```bash
cd HCMUS_Dashboard

# Xem status
git status

# Xem log
git log --oneline

# Xem remote
git remote -v
```

---

## 🚀 Cập Nhật Sau Này

Nếu cần cập nhật sau này:

```bash
cd HCMUS_Dashboard

# Sửa file
# (edit Dashboard files...)

# Commit thay đổi
git add -A
git commit -m "update: Description of changes"

# Push lên GitHub
git push
```

---

## 📋 Commit Message Đã Tạo

```
feat: Complete HCMUS Teaching Load Dashboard System

- Executive Dashboard with 8 strategic KPIs
- Dashboard 1: 4-Year Trend analysis (2022-2026)
- Dashboard 2: Workload Distribution (Median, P25, P75, P90, Overload)
- Dashboard 3: Capacity vs Demand analysis with HR recommendations
- Dashboard 4: Program Mix breakdown (CQ, CLC, DKD, SĐH)
- Dashboard 5: Individual 360° workload (CQ vs CTDA)
- Dashboard 6: Course count statistics by Khoa
- Dashboard 7: PHÂN TÍCH QUÁ TẢI GIẢNG DẠY HCMUS - Detailed overload analysis

Features:
✅ Real data only - 10 KHOA from Excel, no fabricated information
✅ All dashboards linked with back buttons to Executive Dashboard
✅ Responsive design with Plotly.js interactive charts
✅ Vietnamese language throughout
✅ Data verification completed - no Math.random() or simulated data

Statistics 2025-26:
- 728 faculty members
- 689,659 equivalent hours total
- 27.7% with very high workload (>617.7h)
- 201 overloaded faculty requiring attention

Co-Authored-By: Claude Haiku 4.5 <noreply@anthropic.com>
```

---

## 🔗 GitHub Repository URL

```
https://github.com/quanph/HCMUS
```

---

## 💡 Tips

1. **Tạo Branch Mới:** 
   ```bash
   git checkout -b feature/new-dashboard
   ```

2. **Merge Branch:**
   ```bash
   git checkout main
   git merge feature/new-dashboard
   ```

3. **Xem Diff:**
   ```bash
   git diff
   ```

4. **Undo Commit (Chưa Push):**
   ```bash
   git reset HEAD~1
   ```

---

## 🆘 Troubleshooting

### Error: "fatal: remote origin already exists"
```bash
git remote remove origin
git remote add origin https://github.com/quanph/HCMUS.git
```

### Error: "Permission denied (publickey)"
- Kiểm tra SSH key đã được thêm vào GitHub chưa
- Thử: `ssh -T git@github.com`

### Error: "Repository not found"
- Kiểm tra URL repository có đúng không
- Kiểm tra quyền access trên GitHub

---

## 📧 Câu Hỏi?

Xem hướng dẫn chính thức: https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository

---

*Hướng dẫn này được tạo: 03/09/2026*
