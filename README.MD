# 🚦 PHÂN TÍCH VÀ KHAI PHÁ DỮ LIỆU TAI NẠN GIAO THÔNG

## 📖 1. Tổng quan đồ án (Project Overview)
Đồ án này được thực hiện nhằm khai thác và phân tích tập dữ liệu về tai nạn giao thông (hơn 200000 bản ghi). Mục đích cốt lõi của đồ án là tìm ra các quy luật tiềm ẩn, đánh giá mức độ ảnh hưởng của các yếu tố (môi trường, hạ tầng, hành vi) đến tai nạn, đồng thời xây dựng các mô hình học máy để dự báo và phân nhóm rủi ro. 

Kết quả của dự án kỳ vọng sẽ cung cấp những cơ sở khoa học để đề xuất các giải pháp nâng cao an toàn giao thông đô thị.

## 🗂️ 2. Cấu trúc thư mục (Directory Structure)
Dự án được tổ chức theo cấu trúc sau:
* `data/raw/`: Chứa file dữ liệu gốc ban đầu.
* `data/processed/`: Chứa dữ liệu đã qua bước tiền xử lý, sẵn sàng đưa vào mô hình.
* `notebooks/`: Chứa toàn bộ mã nguồn thực thi dự án (Jupyter Notebook).
* `reports/`: Chứa file báo cáo (.docx).

## ⚙️ 3. Giải thích các phần chính (Main Workflows)

Toàn bộ quy trình thực hiện được chia thành 5 phần, tương ứng với các thư mục và file code trong thư mục `notebooks/`:

### 🛠️ 3.1. Tiền xử lý dữ liệu (1_Preprocessing.ipynb)
* Xử lý các giá trị trùng lặp (Duplicates), khuyết thiếu (Missing values) và các dữ liệu không xác định (Unknown).
* Chuẩn hóa kiểu dữ liệu (Datetime, Binary,...) từ dữ liệu gốc.
* Chuyển các cột dạng text về cùng định dạng (xóa khoảng trắng thừa, đưa về chữ in hoa ,...).
* Xuất dữ liệu sạch lưu vào thư mục `data/processed/`.

### 📊 3.2. Phân tích Dữ liệu Khám phá - EDA (2_EDA/)
* Trực quan hóa dữ liệu bằng các biểu đồ thống kê.
* Đánh giá phân bố tai nạn theo mức độ nghiêm trọng, thời gian, điều kiện thời tiết và tình trạng mặt đường.
* Phân tích sự ảnh hưởng đơn yếu tố và đa yếu tố đến mức độ nghiêm trọng của tai nạn.
* Phân tích mối tương quan giữa các yếu tố.

### 🎯 3.3. Mô hình Phân lớp - Classification (3_Classification.ipynb)
* **Mục tiêu:** Dự báo một vụ tai nạn có khả năng gây thương tích (Injury) hay không.
* Xử lý bài toán mất cân bằng dữ liệu nghiêm trọng giữa các nhóm phân lớp.
* Huấn luyện, đánh giá và tinh chỉnh siêu tham số cho các mô hình học máy.

### 🧩 3.4. Mô hình Phân cụm - Clustering (4_Clustering/)
* **Mục tiêu:** Nhóm các vụ tai nạn có tính chất tương đồng lại với nhau để tìm ra các phân khúc rủi ro.
* Áp dụng và so sánh bộ 3 thuật toán: **PAM** (Partitioning Around Medoids), **HAC** (Hierarchical Agglomerative Clustering) và **DBSCAN**.

### 🔗 3.5. Khai phá Luật kết hợp - Association Rules (5_Association_Rules.ipynb)
* **Mục tiêu:** Tìm ra các chuỗi kịch bản thường xuyên xảy ra cùng nhau và các chuỗi kịch bản dễ đến các vụ tai nạn có thương vong.
* Khám phá mối liên hệ giữa các patterns phổ biến và các patterns dẫn đến hậu quả nghiêm trọng.

## 👥 4. Thành viên nhóm (Contributors)
* [Võ Minh Xuân Kiều] - [23110245] 
* [Dương Quỳnh Như] - [23110281] 
* [Nguyễn Thị Quyến] - [23110297] 
* [Trần Thị Như Quỳnh] - [23110299] 