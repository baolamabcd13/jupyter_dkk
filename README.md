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

# PHÂN TÍCH DỮ LIỆU ĐIỆN THOẠI DI ĐỘNG

## MÔN HỌC: KHO DỮ LIỆU VÀ KHAI PHÁ DỮ LIỆU

### MỤC LỤC

- Nhận xét của Giảng viên
- Danh mục hình ảnh
- Danh mục bảng biểu

### PHẦN 1: GIỚI THIỆU VỀ CSDL SỬ DỤNG CHO ĐỀ TÀI

1.1. Tổng quan về CSDL

- Nguồn dữ liệu: Kaggle - Mobile Phones Dataset
- Phạm vi dữ liệu: Thông tin về điện thoại di động
- Số lượng bản ghi: xxx records
- Mục đích sử dụng dữ liệu

1.2. Giới thiệu từng thuộc tính
1.2.1. Brand (Thương hiệu)

- Ý nghĩa: Tên hãng sản xuất điện thoại
- Số giá trị null: xxx
- Số giá trị unique: xxx
- Kiểu dữ liệu: Nominal (Danh nghĩa)
- Phân bố giá trị và tỷ lệ phần trăm

  1.2.2. Weight (Trọng lượng)

- Ý nghĩa: Trọng lượng của điện thoại
- Số giá trị null: xxx
- Số giá trị unique: xxx
- Kiểu dữ liệu: Numeric (Số)
- Các giá trị thống kê:
  - Mean: xxx
  - Median: xxx
  - Mode: xxx
  - Min: xxx
  - Max: xxx
  - Five-number summary

[Tiếp tục với các thuộc tính khác...]

1.3. Quá trình tiền xử lý dữ liệu

- Xử lý missing values
- Chuẩn hóa dữ liệu
- Chuyển đổi kiểu dữ liệu
- Tạo các thuộc tính phái sinh

### PHẦN 2: PHÂN TÍCH – THỐNG KÊ THỦ CÔNG

2.1. Tìm hiểu dữ liệu
2.1.1. Phân tích 3 thuộc tính

- Boxplot cho Weight, RAM, Price
- Q-Q Plot cho cặp thuộc tính Weight-Price
- Histogram cho cặp thuộc tính RAM-Price
- Scatter plot cho cặp thuộc tính Weight-RAM

  2.1.2. Phân tích theo nhóm Brand

- Boxplot theo thương hiệu
- Histogram theo thương hiệu

  2.1.3. Đo lường sự tương đồng và khác biệt

- Ma trận tương quan
- Độ đo Cosin
- So sánh và nhận xét kết quả

2.2. Tiền xử lý dữ liệu

- Mã Python xử lý dữ liệu
- Giải thích các bước xử lý
- Kết quả sau xử lý

2.3. Tổng hợp dữ liệu

- Phân tích thống kê mô tả
- Các metric tổng hợp
- Nhận xét về dữ liệu

2.4. Trực quan hóa dữ liệu

- Các biểu đồ thống kê
- Biểu đồ phân tích xu hướng
- Nhận xét từ trực quan hóa

2.5. Thực hiện khai thác dữ liệu
2.5.1. Áp dụng các phương pháp khai phá
a) Khai phá luật kết hợp (Association Rules)

- Thuật toán Apriori
- Các tham số sử dụng
- Kết quả và phân tích

b) Phân lớp (Classification)

- Thuật toán Random Forest
- Quá trình huấn luyện
- Kết quả và đánh giá

  2.5.2. Đánh giá kết quả
  a) Đánh giá luật kết hợp

- Thang đo Lift
- Độ tin cậy (Confidence)

b) Đánh giá phân lớp

- Ma trận nhầm lẫn (Confusion Matrix)
- Độ chính xác (Accuracy)
- Đường cong ROC

### KẾT LUẬN VÀ KIẾN NGHỊ

- Tổng kết các phát hiện chính
- Ý nghĩa thực tiễn của kết quả
- Hạn chế và hướng phát triển

### TÀI LIỆU THAM KHẢO

### PHỤ LỤC

- Mã nguồn
- Dữ liệu mẫu
- Kết quả chi tiết
