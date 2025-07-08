# Phân Tích Dữ Liệu Cổ Phiếu với Python - EDA & Chỉ Báo Kỹ Thuật

## Thông tin chung
Dữ liệu: Yahoo Finance (các mã: NVDA, META, TSLA, JPM, AMZN)

## Mục tiêu chung
Phân tích dữ liệu lịch sử của các mã cổ phiếu nhằm:
Trực quan hóa biến động giá (Open, Close, High, Low)
Hiển thị khối lượng giao dịch
Tính toán và trực quan các chỉ báo kỹ thuật như: RSI, MACD, MA20, MA50, VWAP, SMA, EMA
Vẽ biểu đồ nến nâng cao kết hợp với volume và các chỉ báo kỹ thuật

## Công cụ sử dụng
yfinance: Lấy dữ liệu giá cổ phiếu
pandas: Tiền xử lý dữ liệu dạng bảng
ta: Tính toán chỉ báo kỹ thuật
matplotlib, seaborn: Trực quan hóa cơ bản
plotly.graph_objects: Biểu đồ nến nâng cao, subplot động
mplfinance: Vẽ biểu đồ nến tùy chỉnh (bổ sung)

## Nội dung chính trong Notebook
***1. Tải dữ liệu và chuẩn hóa***
Tải dữ liệu các mã cổ phiếu từ Yahoo Finance giai đoạn 2023-01-01 đến 2025-05-18
Gộp dữ liệu thành DataFrame thống nhất, xử lý tên cột theo ticker

***2. Tính toán chỉ báo kỹ thuật***
RSI (14 ngày): đo lường động lượng tăng/giảm
MACD + Signal line: xác định phân kỳ/hội tụ
MA20 & MA50: trung bình trượt ngắn và trung hạn
SMA5 & EMA20 (ở bài khác): được tính theo mẫu riêng
VWAP: tính toán giá trung bình theo khối lượng (ở bài khác)

***3. Phân tích EDA và trực quan***
Sai phân bậc 1 ΔClose: biểu đồ cột thể hiện biến động tăng/giảm giá hằng ngày
Boxplot giá đóng cửa theo ngày trong tuần: trực quan xu hướng theo thứ
Histogram giá Adj Close theo năm: phân phối giá mỗi năm, dùng Seaborn FacetGrid
Rolling Mean 1 năm: xu hướng dài hạn của giá

***4. Trực quan chỉ báo kỹ thuật***
Biểu đồ RSI: vẽ kèm đường 70 (quá mua) và 40 (quá bán)
Biểu đồ MACD: so sánh với đường Signal, vẽ đường 0
Diễn giải phân kỳ tăng/giảm (Bullish/Bearish Divergence) và hội tụ

***5. Biểu đồ giá và khối lượng nâng cao***
Biểu đồ đường giá + MA20, MA50: giúp so sánh xu hướng ngắn hạn
Biểu đồ nến Plotly (OHLC): thể hiện rõ vùng giá mở, cao, thấp, đóng
Kết hợp volume trên trục y phụ
Khoảng thời gian riêng: từ 2024-09-01 đến 2024-12-31
Giao diện tối, hiện đại, hỗ trợ phân tích nhiều mã trên các subplot

