# 📊 Jupyter DKK Project

Phân tích & khai phá dữ liệu điện thoại di động sử dụng Jupyter Notebook, Python, và các thư viện khai thác dữ liệu phổ biến.

## 🚀 Clone repository

```bash
git clone https://github.com/baolamabcd13/jupyter_dkk.git
cd jupyter_dkk
```

## 🧪 Thiết lập môi trường ảo (Windows)

```bash
python -m venv venv
venv\Scripts\activate
```

## 📦 Cài đặt thư viện cần thiết

```bash
pip install -r requirements.txt
```

## 📂 Mở dự án Jupyter Notebook

```bash
jupyter notebook
```

Mở file `mobile.ipynb` để bắt đầu.

---

## 📚 Nội dung chính của dự án

- Tiền xử lý dữ liệu thực tế
- Phân tích thống kê và trực quan
- Khai phá dữ liệu:
  - Luật kết hợp (Apriori)
  - Phân lớp (Random Forest)
  - Phân cụm (KMeans + PCA)
- Đánh giá mô hình với ROC, AUC, classification report

---

# 📝 BÁO CÁO CHI TIẾT

## Đề tài: Phân tích và khai phá dữ liệu điện thoại di động

---

## PHẦN 1: GIỚI THIỆU CƠ SỞ DỮ LIỆU

### 1.1. Tổng quan

- Dữ liệu chứa thông tin về các mẫu điện thoại như: RAM, Camera, Trọng lượng, Bộ xử lý, Dung lượng pin, Giá bán,...
- Số lượng bản ghi: 1000
- Số lượng thuộc tính: 14
- Nguồn dữ liệu: Tổng hợp từ nhiều nền tảng thương mại điện tử và công bố trên Kaggle

### 1.2. Thông tin thuộc tính

Bảng mô tả gồm: Tên cột, kiểu dữ liệu, số giá trị null, số unique. Ví dụ:

- `RAM`: số, đơn vị GB
- `Weight`: số, đơn vị gram
- `FrontCamera`, `RearCamera`: số, đơn vị MP
- `USD_Price`: giá bán ở USD

Đối với các cột số, đã tính:

- Min, Max, Mean, Median, Mode
- Five-number summary: Min, Q1, Median, Q3, Max

### 1.3. Tiền xử lý

- Loại bỏ đơn vị (`GB`, `MP`, `g`, `in`) để chuyển về số
- Tạo cột `IsCheap` (điện thoại rẻ nếu `USD_Price < 300`)
- Chuẩn hóa và kiểm tra dữ liệu thiếu/null

---

## PHẦN 2: PHÂN TÍCH – TRỰC QUAN – THỐNG KÊ

### 2.1.1. Trực quan thuộc tính số

- **Boxplot RAM** → phần lớn điện thoại có RAM từ 4–8GB
- **Histogram FrontCamera** → đa số có camera trước từ 8–16MP
- **Scatter RAM vs USD_Price** → xu hướng RAM cao thì giá cao
- **Q-Q Plot USD_Price** → phân phối lệch phải, không chuẩn

### 2.1.2. Theo nhóm danh nghĩa

- **Boxplot USD_Price theo Brand** → Apple, Samsung có giá cao hơn
- Nhận xét: Một số brand như Realme, Xiaomi tập trung phân khúc rẻ

### 2.1.3. Tương đồng – khác biệt

- **Ma trận tương quan** → RAM và giá có tương quan dương
- **Khoảng cách Cosine** → dùng để so sánh giữa 4 mẫu ngẫu nhiên

---

### 2.2. Tiền xử lý bằng Python

- Sử dụng pandas, numpy, sklearn để xử lý, tách chuỗi, ép kiểu, tạo nhãn mới

### 2.3. Tổng hợp dữ liệu

- Group by Brand → trung bình giá mỗi thương hiệu
- Nhận xét: iPhone có giá trung bình cao nhất

### 2.4. Trực quan hóa tổng quát

- Biểu đồ scatter, histogram, boxplot, heatmap

---

## PHẦN 2.5: KHAI PHÁ DỮ LIỆU

### 2.5.1. Phương pháp 1 – Khai phá luật kết hợp (Apriori)

- Tìm luật từ tập rời rạc hóa: RAM, Camera, Brand
- Luật ví dụ: Nếu RAM cao → Camera cao (lift > 1.5)
- Nhận xét: Có thể dùng để tìm gợi ý cấu hình thường đi kèm

### 2.5.1. Phương pháp 2 – Phân lớp (Random Forest)

- Nhãn: `IsCheap`
- Đặc trưng: RAM, Weight, Front/Rear Camera
- Kết quả:
  - **Classification report**
  - **Confusion matrix**
  - **AUC Score > 0.85**
  - **Hình: ROC Curve**
- Nhận xét: Mô hình dự đoán khá tốt, phân biệt rõ sản phẩm rẻ/đắt

### 2.5.1. Phương pháp 3 – Phân cụm (KMeans + PCA)

- Sử dụng PCA giảm chiều dữ liệu
- Chọn số cụm tối ưu bằng Elbow
- **Hình: Scatter các cụm**
- Nhận xét: Cụm 0 – giá rẻ, Cụm 1 – trung, Cụm 2 – cao cấp

---

### 2.5.2. Đánh giá mô hình

- Accuracy: ...
- AUC: ...
- Precision, Recall: ...

---

## PHẦN 3: KẾT LUẬN

- Các thương hiệu như Realme, Xiaomi phù hợp phân khúc giá rẻ
- Cấu hình càng cao thì giá càng cao (RAM, Camera)
- Mô hình phân lớp và phân cụm cho kết quả rõ ràng
- Có thể dùng để hỗ trợ định vị sản phẩm, gợi ý cấu hình tối ưu theo phân khúc

---

## TÀI LIỆU THAM KHẢO

- https://pandas.pydata.org
- https://scikit-learn.org
- https://seaborn.pydata.org
- https://www.kaggle.com
