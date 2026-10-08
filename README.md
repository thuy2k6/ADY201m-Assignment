# ADY201m Assignment – Cardiovascular Disease Analysis

Phân tích bộ dữ liệu 70.000 bệnh nhân (cardio_train_raw.csv) để tìm các yếu tố liên quan đến bệnh tim mạch.
Thay vì IBM Db2 on Cloud, bài dùng **SQLite** để chạy các truy vấn SQL.

## Nội dung
1. Tạo database SQLite, nạp dữ liệu vào bảng `CARDIO_TRAIN`
2. 10 truy vấn SQL (đếm dòng, đếm ca bệnh, giới tính, top AP_HI, ...)
3. Xuất bảng ra `CARDIO_TRAIN.csv`
4. Phân tích: EDA, xử lý outlier, kiểm định (ANOVA, t-test, Pearson, Chi-square), OLS
5. Mô hình phân loại: Ridge, RandomForest, GradientBoosting, AdaBoost, Bagging, ExtraTrees, Stacking

## Cách chạy
```bash
pip install -r requirements.txt
# đặt cardio_train_raw.csv cùng thư mục với notebook
jupyter notebook ADY201m_Assignment.ipynb
```

## Kết quả chính
- Có 34.979 / 70.000 ca mắc bệnh; không có giá trị null, nhưng AP_HI / AP_LO có outlier.
- AGE, CHOLESTEROL, WEIGHT, huyết áp liên quan có ý nghĩa thống kê; ALCO thì không (p ≈ 0.0545).
- Accuracy tốt nhất ≈ 74% (Gradient Boosting).
