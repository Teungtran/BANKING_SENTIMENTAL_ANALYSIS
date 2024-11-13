# 🏦 BANKING_SENTIMENTAL_ANALYSIS

## 🔍 Tổng quan
Dự án này sử dụng mô hình BERT Neural Network và thư viện Hugging Face Transformers để phân tích cảm xúc từ đánh giá của khách hàng về 5 ngân hàng hàng đầu tại Việt Nam.

## 🌟 Tính năng chính
- Thu thập dữ liệu đánh giá từ Google Maps Reviews
- Sử dụng BERT để phân tích cảm xúc
- Giao diện tương tác với Streamlit
- Hỗ trợ đa dạng định dạng dữ liệu đầu vào
- Xử lý ngôn ngữ tự nhiên tiếng Việt

## 🛠 Công nghệ sử dụng
- BERT Neural Network
- Hugging Face Transformers
- Python
- Streamlit
- Data Scraper (Chrome Extension)
- Pandas
- NumPy

## 📊 Xử lý dữ liệu
### Thu thập dữ liệu
- Sử dụng Data Scraper Extension để thu thập đánh giá từ Google Maps
- Lưu trữ dữ liệu dưới dạng CSV
- Tự động làm sạch và chuẩn hóa dữ liệu

### Đặc điểm dữ liệu
- Hỗ trợ nhiều định dạng đầu vào:
  - Chuỗi văn bản đơn
  - Danh sách các câu
  - Đánh giá có biểu tượng cảm xúc

## 💻 Cài đặt
```bash
pip install transformers torch pandas numpy streamlit
```

## 🚀 Hướng dẫn sử dụng
1. Cài đặt các thư viện cần thiết
2. Chạy ứng dụng Streamlit:
```bash
streamlit run app.py
```
3. Nhập văn bản cần phân tích
4. Xem kết quả phân tích cảm xúc

## 📈 Mô hình
### Kiến trúc
- BERT Neural Network
- Fine-tuned cho tiếng Việt
- Tối ưu hóa cho phân tích cảm xúc

### Xử lý đầu vào
```python
def process_input(sentence):
    if isinstance(sentence, str):
        return sentence
    elif isinstance(sentence, list):
        return sentence[0]
    else:
        raise ValueError("Input must be string or list")
```



## 📊 Hiệu suất
- Độ chính xác: > 97%


## 🔍 Đặc điểm dữ liệu
### Biến thể dữ liệu
- Dataset từ Google Maps Reviews có cấu trúc đa dạng
- Mỗi đánh giá có thể chứa:
  - Chuỗi văn bản đơn
  - Danh sách các câu
  - Biểu tượng cảm xúc
  - Đánh giá sao

### Xử lý dữ liệu
- Kiểm tra và xử lý cả hai loại dữ liệu:
  - String
  - List of strings
- Đảm bảo tương thích với Hugging Face Transformers pipeline

## ⚠️ Lưu ý
- Mô hình được tối ưu hóa cho ngôn ngữ tiếng Việt
- Cần xử lý đặc biệt với biểu tượng cảm xúc và ký tự đặc biệt
- Giới hạn độ dài văn bản đầu vào: 512 tokens

## 🔒 Bảo mật
- Không lưu trữ dữ liệu người dùng
- Xử lý dữ liệu cục bộ
- Tuân thủ quy định GDPR

## 🙏 Lời cảm ơn
- Hugging Face Team
- Google Maps Platform
- Cộng đồng Data Science Việt Nam
- Các nhà đóng góp mã nguồn mở

---
**Tuyên bố miễn trừ trách nhiệm**: Kết quả phân tích cảm xúc chỉ mang tính tham khảo và không nên được sử dụng làm cơ sở duy nhất cho các quyết định kinh doanh.
