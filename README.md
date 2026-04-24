# 🚗 Phân Tích & Khám Phá Dữ Liệu (EDA): Tai Nạn Giao Thông Tại Anh Quốc 

## 🎯 Tổng quan Dự án (Project Overview)
Dự án này thực hiện Phân tích Khám phá Dữ liệu (EDA) chuyên sâu trên tập dữ liệu Tai nạn giao thông tại Anh Quốc. Thay vì chỉ thống kê bề mặt, phân tích được chia làm hai dòng chảy song song: (1) Giải mã cơ chế của các vụ va chạm nhẹ thường ngày do mật độ giao thông và (2) Truy tìm nguyên nhân cốt lõi biến một vụ tai nạn thành thảm họa chết người.

## 🛠️ Công cụ & Kỹ thuật sử dụng
- **Ngôn ngữ:** Python
- **Thư viện:** Pandas (Data Cleaning & Manipulation), Matplotlib & Seaborn (Data Visualization).
- **Môi trường:** Jupyter Notebook.

## 📂 Cấu trúc Dự án
```text
UK-Traffic-Accidents-Analysis/
├── UK_Road_Traffic_Accident_DA.ipynb          # Source code chính xử lý và phân tích bằng Python
├── UK_Road_Traffic_Accident_Presentation.pdf  # Slide báo cáo đúc kết Insights và Đề xuất
└── README.md                                  # Tài liệu mô tả dự án
```

## 🔍 Quy trình Phân tích
- **Bước 1:** Tiền xử lý dữ liệu: Xử lý Missing values, loại bỏ các biến nhiễu và hợp nhất dữ liệu (Accident & Vehicle datasets).
- **Bước 2:** Phân tích Đơn biến (Univariate Analysis): Sử dụng quy tắc 4W (When, Where, Who, What) để phác họa chân dung các vụ va chạm nhẹ.
- **Bước 3:** Phân tích Đa biến (Multivariate Analysis): Khám phá sự tương tác chéo giữa Không gian - Thời gian - Con người để tìm ra các yếu tố "chết chóc" thực sự.

## 💡 Kết quả & Insights Nổi bật
### Bức tranh tai nạn giao thông được cấu thành bởi hai cơ chế rủi ro hoàn toàn khác biệt:
#### 1. Cơ chế của Va chạm nhẹ (Sự cố về Mật độ & Tần suất)
Các va chạm nhẹ chiếm áp đảo 84.22% tổng số vụ tai nạn. Chúng không xảy ra ngẫu nhiên mà tuân theo một quy luật mật độ rõ ràng:
  - Thời gian (When): Tập trung vào chiều tối (15h-19h) các ngày trong tuần (đạt đỉnh vào Thứ 6). Đây là lúc áp lực giao thông và sự mệt mỏi cộng dồn.
  - Không gian (Where): Chủ yếu xảy ra ở khu vực đô thị (67.04%), đặc biệt là trên các tuyến đường đơn (Single carriageway) có không gian lưu thông hạn chế, ngay cả trên các đoạn đường thẳng không có giao lộ.
  - Chân dung rủi ro điển hình (Who & What): Nhóm Nam giới trung niên (26-45 tuổi) điều khiển xe hơi chiếm ưu thế tuyệt đối. Đây là lực lượng lao động chính, tham gia giao thông liên tục vào giờ cao điểm.

#### 2. Nguyên nhân của Tử vong & Nghiêm trọng (Sự cố về Bối cảnh & Thể chất)
Chỉ chiếm ~15% số vụ, nhưng các tai nạn nghiêm trọng bị khuếch đại bởi 3 yếu tố "chết chóc":
  - Bóng tối (Không phải Thời tiết): Trái với suy nghĩ thông thường, thời tiết xấu (mưa, sương mù) không làm tăng tỷ lệ tử vong. Tuy nhiên, ban đêm lại đẩy tỷ lệ tử vong lên gần 10% (so với 6% ban ngày) do hạn chế tầm nhìn và tốc độ cao.
  - Tốc độ (Động năng): Tai nạn trên đường có giới hạn tốc độ cao (>60 km/h) có tỷ lệ tử vong (14.2%) cao gấp đôi so với đường tốc độ thấp (7.0%).
  - Sự tổn thương thể chất: Tài xế lớn tuổi (≥66 tuổi) có tỷ lệ tử vong cao nhất (9.8%) khi xảy ra va chạm, cho thấy thể chất là yếu tố then chốt quyết định hậu quả cuối cùng.

## 🚀 Đề xuất Chiến lược (Actionable Recommendations)
- Để giảm va chạm nhẹ: Tập trung phân luồng quản lý giao thông đô thị, tối ưu hóa hạ tầng đường đơn trong các khung giờ cao điểm (chiều tối các ngày làm việc).
- Để giảm tỷ lệ tử vong: Ưu tiên tăng cường hệ thống chiếu sáng ban đêm, siết chặt kiểm soát tốc độ trên các tuyến đường >60 km/h và có cảnh báo an toàn đặc biệt dành cho nhóm tài xế cao tuổi.

## 🔗 Nguồn Dữ liệu (Dataset)
- **Nguồn gốc:** Tải về từ Kaggle - [UK Road Safety: Traffic Accidents and Vehicles](https://www.kaggle.com/datasets/tsiaras/uk-road-safety-accidents-and-vehicles/data).
- **Quy mô dữ liệu (Big Data):** Tập dữ liệu khổng lồ với **2.047.256 bản ghi** (hơn 2 triệu vụ tai nạn) và **34 thuộc tính** (được hợp nhất từ bảng thông tin Tai nạn và thông tin Phương tiện).
- *(Lưu ý: Do quy mô dữ liệu vượt quá giới hạn của GitHub, file raw data không được tải trực tiếp lên repo này. Vui lòng truy cập vào file Jupyter Notebook để có thể xem toàn bộ cấu trúc và quá trình làm sạch dữ liệu).*
