# 💼 Phân tích Thị trường Tuyển dụng CNTT Ấn Độ (Indian Tech Jobs 2026)

Phân tích hơn 23.000 tin tuyển dụng ngành công nghệ thông tin từ hơn 7.000 doanh nghiệp tại Ấn Độ, khai thác 32 biến dữ liệu về kỹ năng, mức lương, kinh nghiệm, quy mô doanh nghiệp và phân bố địa lý — từ dữ liệu thô đến dashboard Power BI trực quan.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/status-completed-brightgreen)

![Tổng quan thị trường tuyển dụng](Tong%20quan.png)

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

Báo cáo phân tích bộ dữ liệu **Indian Tech Jobs – Snapshot 2026** nhằm khái quát bức tranh tuyển dụng ngành công nghệ thông tin tại Ấn Độ, trả lời các câu hỏi:

- Vai trò, kỹ năng nào đang được thị trường săn đón nhiều nhất?
- Mức lương trung bình theo cấp độ kinh nghiệm, hình thức làm việc và quy mô doanh nghiệp ra sao?
- Cơ hội việc làm cho Fresher (mới ra trường) như thế nào?
- Thành phố và doanh nghiệp nào đang dẫn đầu về nhu cầu tuyển dụng?
- Hình thức làm việc (Remote/Hybrid/On-site) khác biệt ra sao giữa các thành phố và quy mô công ty?

## 2. Mô tả dữ liệu

![Giới thiệu bộ dữ liệu](Gioi%20thieu.png)

### a. Nguồn dữ liệu
Dataset: **Indian Tech Jobs – Snapshot 2026**
- Quy mô: hơn **23.000 bản ghi tuyển dụng** từ hơn **7.000 doanh nghiệp**
- **32 biến dữ liệu (features)**

### b. Tổng quan dữ liệu

| Nhóm chỉ số | Mô tả |
|---|---|
| **Role & Skills** | Nhóm công việc, kỹ năng chính, số lượng kỹ năng yêu cầu |
| **Salary & Experience** | Mức lương công bố, mức kinh nghiệm yêu cầu |
| **Company & Location** | Quy mô doanh nghiệp, hình thức làm việc, thành phố tuyển dụng |

### c. Chuẩn bị dữ liệu
- Chuẩn hóa các nhóm kỹ năng (`skill_domain`) thành 5 nhóm chính: Data Science, Business Intelligence, AI/ML/DL, Data Engineering, Cloud & DevOps.
- Phân loại cấp độ kinh nghiệm: Fresher, Junior (0–2 năm), Mid (3–5 năm), Senior (6–8 năm), Lead/Architect.
- Phân loại quy mô doanh nghiệp: Small/Startup (<100), Mid (100–999), Large (1000+).
- Tính cột phụ `is_senior`, `Avg Days Active` để phục vụ phân tích lương và tốc độ tuyển dụng.

## 3. Thiết kế Dashboard

Dashboard Power BI gồm **4 trang phân tích chính**, có bộ lọc chung: **Role category, Experience tier**.

| Trang | Nội dung chính |
|---|---|
| 📊 Tổng quan | Bức tranh toàn cảnh thị trường tuyển dụng CNTT |
| 💰 Lương | Phân tích mức lương theo kinh nghiệm, hình thức làm việc, quy mô công ty |
| 🛠️ Kỹ năng & Tuyển dụng | Kỹ năng được yêu cầu nhiều nhất, tốc độ và độ phức tạp tuyển dụng |
| 🏢 Company & Location | Phân bố doanh nghiệp, địa điểm, hình thức làm việc |

## 4. Kết quả & Insights

### 📊 Tổng quan thị trường

![Tổng quan](Tong%20quan.png)

- Thị trường ghi nhận **23K tin tuyển dụng** từ **7K doanh nghiệp**, kinh nghiệm yêu cầu trung bình **4,14 năm**, mỗi tin tuyển dụng yêu cầu trung bình **7,6 kỹ năng**.
- Chỉ **18,03%** cơ hội việc làm dành cho Fresher — thị trường ưu tiên ứng viên có kinh nghiệm.
- **Data Science** là vai trò được tuyển dụng nhiều nhất (6,5K), theo sau là Data Analyst (4,7K) và Business Analyst (4,5K).
- Cấp độ **Mid (3–5 năm)** chiếm phần lớn nhu cầu tuyển dụng (10K), trong khi Lead/Architect chỉ chiếm 11,3%.
- **80,6% việc làm là On-site**, Hybrid và Remote chỉ chiếm lần lượt 10,12% và 9,28%.
- **Mumbai, Bangalore, Chennai** là 3 thành phố có nhu cầu tuyển dụng cao nhất.

### 💰 Phân tích mức lương

![Phân tích mức lương](Muc%20luong.png)

- Chỉ **11,93%** tin tuyển dụng công bố mức lương cụ thể.
- Lương trung bình **15,32 LPA**, lương trung vị **14,00 LPA**, mức cao nhất **90,00 LPA**.
- **Hybrid** có mức lương trung vị cao nhất (20,0 LPA), vượt trội so với Remote (14,0) và On-site (13,5).
- Lương tăng dần theo quy mô doanh nghiệp: **Large (1000+)** trả lương cao và ổn định nhất.
- Nhóm kỹ năng **Cloud, AI/ML/DL** có mức lương cao nhất.
- Lương trung vị tăng rõ rệt theo cấp bậc: Fresher/Junior (~5) → Lead/Architect (26).

### 🛠️ Kỹ năng & Tuyển dụng

![Kỹ năng và tuyển dụng](Ki%20nang%20tuyen%20dung.png)

- **89,85%** tin tuyển dụng yêu cầu kỹ năng phức tạp.
- Kỹ năng được yêu cầu nhiều nhất: **Python (4,3K), Data Analysis (3,8K), Machine Learning (3,5K), SQL (2,9K)**.
- Nhóm **Cloud & DevOps** có tỷ lệ việc làm phù hợp Fresher cao nhất (92,79%); **Business Intelligence** thấp nhất (78,69%).
- Thời gian tuyển dụng trung bình dao động **13,2–16,8 ngày**, **Data Science** mất nhiều thời gian tuyển nhất (16,81 ngày).
- Độ phức tạp kỹ năng khá đồng đều giữa các nhóm nghề (~7,5–7,7 kỹ năng trung bình/tin).

### 🏢 Doanh nghiệp & Địa điểm

![Doanh nghiệp và địa điểm](Doanh%20nghiep%20dia%20diem.png)

- **7K doanh nghiệp** đang tuyển dụng, điểm đánh giá trung bình **3,59/5**, tỷ lệ làm việc từ xa trung bình chỉ **19,4%**.
- **On-site chiếm ưu thế tuyệt đối ở mọi thành phố** (80–92%); Mumbai cao nhất (92,12%).
- Doanh nghiệp quy mô **Mid (100–999)** yêu cầu On-site nhiều nhất (92,31%); **Small/Startup** linh hoạt hơn.
- **Top doanh nghiệp tuyển dụng nhiều nhất**: Tata Consultancy (654), Accenture (438), EY (340), Infosys (209), Capgemini (195).

## 5. Khuyến nghị

**Dành cho ứng viên**
- Ưu tiên trang bị kỹ năng **Python, Data Analysis, Machine Learning, SQL**.
- Fresher nên nhắm đến nhóm **Cloud & DevOps** — tỷ lệ cơ hội phù hợp cao nhất.
- Cân nhắc tích lũy kinh nghiệm hướng đến mốc **3–5 năm (Mid level)**.

**Dành cho doanh nghiệp/nhà tuyển dụng**
- Cân nhắc công bố mức lương để tăng tỷ lệ ứng tuyển chất lượng.
- Với vị trí Data Science, cần chuẩn bị quy trình tuyển dụng dài hơn.
- Xem xét linh hoạt hóa hình thức làm việc để mở rộng nguồn ứng viên chất lượng cao.

**Dành cho nhà đầu tư/nghiên cứu thị trường**
- Mumbai, Bangalore, Chennai là thị trường lao động CNTT sôi động nhất.
- Nhóm kỹ năng Cloud & AI/ML/DL có mức lương và nhu cầu tuyển dụng cao — tín hiệu tốt cho đầu tư đào tạo nhân lực.

## 6. Công cụ sử dụng

- **Power Query** — làm sạch và biến đổi dữ liệu
- **Power BI** — xây dựng data model, DAX, thiết kế dashboard 4 trang

---