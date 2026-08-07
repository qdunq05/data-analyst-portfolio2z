# 🎮 Phân tích dữ liệu 17k Game — Thị trường Game Chiến thuật trên App Store

Phân tích hơn 17.000 game trên Apple App Store (thể loại Games/Strategy) nhằm khám phá xu hướng phát hành, mô hình doanh thu, vòng đời sản phẩm, nhà phát triển và mức độ hài lòng người dùng — từ dữ liệu thô đến dashboard Power BI trực quan.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Data Source](https://img.shields.io/badge/Data-Kaggle-20BEFF?style=flat&logo=kaggle&logoColor=white)
![Status](https://img.shields.io/badge/status-completed-brightgreen)

![Tổng quan](Tong%20quan.png)

---

## 📑 Mục lục

- [1. Mục đích báo cáo](#1-mục-đích-báo-cáo)
- [2. Mô tả dữ liệu](#2-mô-tả-dữ-liệu)
- [3. Thiết kế Dashboard](#3-thiết-kế-dashboard)
- [4. Kết quả & Insights](#4-kết-quả--insights)
- [5. Khuyến nghị](#5-khuyến-nghị)
- [6. Công cụ sử dụng](#6-công-cụ-sử-dụng)

---

## 1. Mục đích báo cáo

Báo cáo phân tích bộ dữ liệu **17K Apple App Store Strategy Games** nhằm trả lời:

- Thị trường game chiến thuật phát triển theo xu hướng nào qua các năm?
- Mô hình doanh thu nào (Free, Freemium, Paid, Paid + IAP) chiếm ưu thế và mang lại rating/review tốt nhất?
- Vòng đời trung bình của một game là bao lâu, tỷ lệ còn duy trì cập nhật ra sao?
- Những nhà phát triển và tựa game nào dẫn đầu thị trường?
- Yếu tố nào (thể loại, độ tuổi, mô hình giá) ảnh hưởng đến mức độ hài lòng người dùng?

## 2. Mô tả dữ liệu

### a. Nguồn dữ liệu
[**17K Mobile Strategy Games**](https://www.kaggle.com/datasets/tristan581/17k-apple-app-store-strategy-games) — Kaggle, ~17.000 game trên Apple App Store.

### b. Tổng quan dữ liệu

| Cột | Mô tả |
|---|---|
| **Name / Subtitle** | Tên và mô tả ngắn của game |
| **Genres / Primary Genre** | Thể loại chính/phụ |
| **Original Release Date** | Ngày phát hành đầu tiên |
| **Current Version Release Date** | Ngày cập nhật gần nhất |
| **Age Rating** | 4+, 9+, 12+, 17+ |
| **Price** | Mức giá (0 = miễn phí) |
| **In-app Purchases** | Có/không IAP |
| **Average User Rating** | Điểm đánh giá trung bình |
| **User Rating Count** | Tổng lượt review |
| **Developer** | Nhà phát triển |

### c. Chuẩn bị dữ liệu
- Chuẩn hóa ngày tháng để tính tuổi đời game & số ngày kể từ lần cập nhật gần nhất.
- Phân loại 4 mô hình doanh thu dựa trên `Price` và `In-app Purchases`.
- Tạo cột tình trạng duy trì (Còn duy trì / Ngừng cập nhật).
- Xử lý dữ liệu thiếu, chuẩn hóa Developer/Genre trùng lặp.

## 3. Thiết kế Dashboard

5 trang, bộ lọc chung: **Năm phát hành, Độ tuổi, Mức giá**.

| Trang | Nội dung |
|---|---|
| 🟦 Tổng quan | Số lượng game, tỷ lệ miễn phí, rating, phân bố thể loại/độ tuổi/năm |
| 💰 Doanh thu & Giá | Mô hình kiếm tiền, quy mô người chơi, giá TB theo thể loại |
| 📈 Xu hướng & Vòng đời | Tốc độ ra mắt, tuổi đời TB, tỷ lệ duy trì cập nhật |
| 👨‍💻 Nhà phát triển | Xếp hạng theo số game và điểm đánh giá |
| ⭐ Chất lượng & Hài lòng | Rating theo thể loại/độ tuổi, top game yêu thích |

## 4. Kết quả & Insights

### 🟦 Tổng quan
![Tổng quan](Tong%20quan.png)
- ~17.000 game, **83,74% miễn phí**, 24,76M lượt review, rating TB **4,06/5**.
- Games & Strategy chiếm ưu thế (~16,6K mỗi thể loại).
- Số lượng phát hành đạt đỉnh 2015–2016 rồi giảm dần — thị trường bão hòa.
- Rating TB cải thiện liên tục theo thời gian (3,5 → hơn 4,0).
- 69,41% game hướng đến đối tượng 4+ (mọi lứa tuổi).

### 💰 Mô hình Doanh thu & Chiến lược Giá
![Doanh thu giá](Doanh%20thu%20gia.png)
- Miễn phí hoàn toàn (42,15%) và Freemium (41,33%) chiếm gần hết thị trường; Paid chỉ 13,08%.
- 45,2% game có IAP — IAP là mô hình kiếm tiền chủ đạo.
- Giá TB game trả phí chỉ $5,01.
- Freemium tạo lượt review vượt trội (~20,3M) so với Miễn phí hoàn toàn (~2,1M).

### 📈 Xu hướng & Vòng đời game
![Xu hướng vòng đời](Xu%20huong%20vong%20doi.png)
- Tuổi đời TB chỉ ~1,14 năm; TB 913 ngày kể từ lần cập nhật gần nhất.
- Chỉ 26,3% game còn duy trì cập nhật — mức đào thải cao.
- Game "sống lâu" chủ yếu là casual/puzzle (Sudoku, Chess, Marple).

### 👨‍💻 Nhà phát triển
![Nhà phát triển](Nha%20phat%20trien.png)
- ~9.000 developer, TB chỉ 1,94 review/developer.
- Top số lượng game là các studio mass-production, không đi kèm rating cao.
- Không có tương quan rõ giữa số lượng game và rating TB.

### ⭐ Chất lượng & Mức độ hài lòng
![Chất lượng hài lòng](Chat%20luong%20hai%20long.png)
- Rating cao nhất ở Food & Drink, News, Health & Fitness.
- Nhóm tuổi 9+/12+ rating cao nhất (4,1); nhóm 17+ thấp nhất (3,9).
- Top game yêu thích: Clash of Clans, Clash Royale, PUBG Mobile, Plants vs. Zombies, Pokémon GO.

## 5. Khuyến nghị

- **Chiến lược thể loại:** ưu tiên Strategy/Games kết hợp casual/puzzle để vòng đời bền vững hơn.
- **Mô hình doanh thu:** ưu tiên Freemium; giá tham khảo cho Paid quanh $5.
- **Duy trì sản phẩm:** đầu tư kế hoạch cập nhật dài hạn — điểm yếu chung của ngành.
- **Đối tượng mục tiêu:** ưu tiên nhóm tuổi 4+/9+/12+.
- **Chiến lược phát triển:** tập trung chất lượng thay vì số lượng game.

## 6. Công cụ sử dụng

- **Kaggle Dataset** — nguồn dữ liệu thô
- **Power Query** — làm sạch & biến đổi dữ liệu
- **Power BI** — data model, DAX, dashboard 5 trang

---
