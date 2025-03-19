# Phân tích dữ liệu điện thoại di động

Dự án này thực hiện phân tích dữ liệu về điện thoại di động, bao gồm phân tích thống kê, khai phá luật kết hợp, phân lớp và phân cụm.

## Yêu cầu hệ thống

- Python 3.10 trở lên
- pip (Python package installer)
- Git

## Cài đặt

### 1. Clone repository

```bash
# Clone repository về máy local
git clone https://github.com/baolamabcd13/jupyter-dkk.git

# Di chuyển vào thư mục dự án
cd jupyter-dkk
```

### 2. Tạo môi trường ảo

```bash
# Windows
python -m venv venv
venv\Scripts\activate
```

### 3. Cài đặt các thư viện cần thiết

```bash
# Cài đặt các dependencies
pip install -r requirements.txt
```

### 4. Chuẩn bị dữ liệu

- Đặt file dữ liệu `Mobiles_Dataset.csv` vào thư mục gốc của dự án

### 5. Chạy Jupyter Notebook

```bash
jupyter notebook
```

## Các bước phân tích

1. Phân tích mô tả dữ liệu
2. Vẽ các biểu đồ thống kê
3. Tính toán ma trận tương quan và độ đo Cosin
4. Khai phá luật kết hợp
5. Phân lớp dữ liệu
6. Phân cụm dữ liệu

## Kết quả

Kết quả phân tích được lưu trong thư mục `visualizations/`, bao gồm:

- Các biểu đồ thống kê
- Ma trận tương quan và độ đo tương đồng
- Kết quả phân lớp và phân cụm
