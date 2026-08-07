# 🛒 CDZen Retail Analytics — Phân tích Doanh thu, Lợi nhuận & Khách hàng

Phân tích toàn diện hoạt động kinh doanh của **CDZen** — chuỗi bán lẻ điện máy & nội thất tại Việt Nam giai đoạn 2011–2017, bao gồm doanh thu, lợi nhuận, hiệu suất sản phẩm, hành vi khách hàng, dự báo xu hướng và đề xuất chiến lược — xây dựng trên Tableau.

![Tableau](https://img.shields.io/badge/Tableau-E97627?style=flat&logo=tableau&logoColor=white)
![Status](https://img.shields.io/badge/status-completed-brightgreen)

![Doanh thu - Bức tranh tổng thể](Tong%20quan.png)

---

## 📑 Mục lục

- [1. Mục đích báo cáo](#1-mục-đích-báo-cáo)
- [2. Mô tả dữ liệu](#2-mô-tả-dữ-liệu)
- [3. Thiết kế Dashboard](#3-thiết-kế-dashboard)
- [4. Kết quả & Insights](#4-kết-quả--insights)
- [5. Đề xuất & Chiến lược](#5-đề-xuất--chiến-lược)
- [6. Công cụ sử dụng](#6-công-cụ-sử-dụng)

---

## 1. Mục đích báo cáo

Báo cáo phân tích dữ liệu bán hàng của CDZen (giai đoạn 2011–2017) nhằm trả lời các câu hỏi kinh doanh cốt lõi:

- Doanh thu và lợi nhuận đến từ khu vực, kênh bán hàng, sản phẩm nào là chủ lực?
- Nhóm sản phẩm/kênh nào đang **lỗ** và cần điều chỉnh chiến lược giá?
- Khách hàng nào đóng góp doanh thu lớn nhất, phân bố theo khu vực ra sao?
- Xu hướng doanh thu & lợi nhuận trong tương lai (2018–2019) sẽ diễn biến thế nào?
- Cần tối ưu điều gì về giá, danh mục sản phẩm, kênh bán hàng và logistics để tăng trưởng bền vững?

## 2. Mô tả dữ liệu

### a. Phạm vi dữ liệu
- Giai đoạn: **2011 – 2017** (dữ liệu thực tế), dự báo mở rộng đến **2019**.
- Ngành hàng: **Hàng điện lạnh** (Tủ lạnh, Máy giặt, Máy điều hòa), **Hàng điện tử** (Điện thoại, Máy tính bảng, Phụ kiện điện tử, TV), **Nội thất** (Ghế, Giường, Bàn, Kệ sách).
- Khu vực: Hồ Chí Minh City, Hà Nội, Hải Dương, Bà Rịa - Vũng Tàu, Ninh Bình, Đà Nẵng, Thừa Thiên - Huế, Quảng Ninh.
- Kênh bán hàng: **Đại lý ủy quyền, Chuỗi cửa hàng, Online**.
- Phương thức giao hàng: Giao hàng bằng xe, Đường sắt, Đường biển.

### b. Các chỉ số chính
| Nhóm chỉ số | Mô tả |
|---|---|
| **Doanh thu / Lợi nhuận** | Theo sản phẩm, khu vực, kênh bán, năm |
| **Số lượng đơn hàng** | Theo sản phẩm, kênh bán, mức giảm giá |
| **Khách hàng** | Doanh thu, lợi nhuận theo từng khách hàng; phân nhóm KH Vàng/Bạc/Kim cương |
| **Dự báo (Forecast)** | Doanh thu & lợi nhuận ước tính theo nhóm sản phẩm và kênh bán |

### c. Chuẩn bị dữ liệu
- Tính tỷ suất lợi nhuận trên doanh thu cho từng sản phẩm để xác định nhóm sinh lời/thua lỗ.
- Phân nhóm khách hàng theo tổng doanh thu đóng góp: KH Kim cương, KH Vàng, KH Bạc.
- Xây dựng mô hình dự báo doanh thu & lợi nhuận đến 2019 theo nhóm sản phẩm và kênh bán.
- Tổng hợp ảnh hưởng của mức giảm giá đến số lượng đơn hàng theo sản phẩm.

## 3. Thiết kế Dashboard

Story Tableau gồm **6 trang phân tích chính**:

| Trang | Nội dung chính |
|---|---|
| 💵 Dashboard Doanh thu | Tổng thể doanh thu theo khu vực, sản phẩm, kênh bán, xu hướng theo năm |
| 📉 Dashboard Lợi nhuận | Lợi nhuận theo nhóm sản phẩm, khu vực, năm, kênh bán |
| 📦 Dashboard Sản phẩm | Hiệu suất bán hàng, top sản phẩm, ảnh hưởng giảm giá |
| 👥 Dashboard Khách hàng | Phân nhóm khách hàng, top khách hàng, phân bố khu vực |
| 🔮 Dashboard Dự đoán | Dự báo doanh thu & lợi nhuận đến 2019 |
| 🎯 Đề xuất & Chiến lược | Khuyến nghị hành động cụ thể |

## 4. Kết quả & Insights

### 💵 Doanh thu — Bức tranh tổng thể

![Doanh thu tổng thể](Tong%20quan.png)

- Tổng doanh thu đạt **~29,96 tỷ đồng** với **779 khách hàng**.
- **TP. Hồ Chí Minh áp đảo** với doanh thu **15,47 tỷ** — gấp hơn 3 lần khu vực đứng thứ 2 (Hà Nội, 4,42 tỷ).
- **Máy giặt** đóng góp doanh thu lớn nhất (101.989), theo sau Tủ lạnh (73.966), Máy điều hòa (45.903).
- Kênh **Đại lý ủy quyền** chiếm tỷ trọng doanh thu cao nhất (49,67%).
- Doanh thu biến động mạnh: đạt đỉnh **13,1 tỷ (2012)**, giảm sâu 2013–2015, phục hồi lên **10,3 tỷ (2017)**.
- Giảm giá tác động rõ rệt đến **Ghế (-19,2%)** và **Máy giặt (-19,45%)**.

### 📉 Lợi nhuận — Nhìn từ dữ liệu

![Lợi nhuận](Loi%20nhuan.png)

- Tổng lợi nhuận đạt **2.885.259 nghìn đồng**, tỷ suất lợi nhuận **9,6%**.
- Nhóm **Hàng điện tử** lợi nhuận cao nhất (Máy tính bảng 607.710) nhưng **TV lỗ -94.216**.
- Trong nội thất, **Bàn (-14.728)** và **Kệ sách (-89.173)** đang thua lỗ.
- Kênh **Đại lý ủy quyền đóng góp 71,27%** tổng lợi nhuận.
- Lợi nhuận theo năm biến động mạnh, đỉnh **989.536 (2012)**, đáy 2015 (35.209), phục hồi **1.078.468 (2017)**.

### 📦 Hiệu suất sản phẩm — Xu hướng đang lên

![Hiệu suất sản phẩm](Hieu%20suat.png)

- Tổng số lượng sản phẩm đã bán: **373.361 sản phẩm**.
- **Máy giặt** dẫn đầu tuyệt đối (101.989), theo sau Tủ lạnh (73.966), Máy điều hòa (45.903).
- **2017 là năm bùng nổ** về số lượng đơn hàng, Máy giặt tăng vọt lên **4.353 đơn**.
- Nhóm điện lạnh có xu hướng tăng trưởng ổn định và mạnh nhất toàn danh mục.

### 👥 Khách hàng CDZen — Chìa khóa tăng trưởng

![Khách hàng](Khach%20hang.png)

- Số khách hàng dao động 136–731 theo khu vực; **Hà Nội (731) và Hải Dương (658)** đông nhất.
- Top khách hàng doanh thu cao nhất: **Tiêu Thị Loan (1.155.312), Trường Ngọc Trầm (1.126.130), Trần Lý Khan (890.169)**.
- **KH Kim cương** là nhóm đóng góp doanh thu vượt trội.
- Doanh thu và lợi nhuận khách hàng tương quan thuận nhưng không tuyệt đối — cần rà soát chính sách chiết khấu cho khách hàng lớn.

### 🔮 Doanh thu & Lợi nhuận — Góc nhìn tương lai

![Dự đoán tương lai](Tuong%20lai.png)

- Dự báo 2018–2019: doanh thu và lợi nhuận có xu hướng **đi ngang hoặc giảm nhẹ** so với đỉnh 2017.
- Nhóm **Nội thất** có biến động dự báo mạnh nhất.
- **Đại lý ủy quyền** tiếp tục dẫn dắt tăng trưởng chính; **Online** quy mô nhỏ hơn nhưng ổn định.

## 5. Đề xuất & Chiến lược

![Chiến lược tối ưu](Chien%20luoc.png)

**Tăng doanh thu tại các tỉnh ngoài TP.HCM**
- Tăng giá trị đơn hàng trung bình bằng combo/sản phẩm cao cấp.
- Giữ giá cao ở TP.HCM, ưu đãi linh hoạt hơn ở tỉnh khác.
- Triển khai chương trình khách hàng thân thiết.

**Tối ưu danh mục sản phẩm & nhóm khách hàng**
- Tăng cường bán chéo (cross-sell) sản phẩm liên quan.
- Upsell cho nhóm khách hàng Kim cương với ưu đãi độc quyền.
- Chương trình tri ân riêng cho top 10 khách hàng.

**Tối ưu phương thức giao hàng**
- Tận dụng đường sắt cho đơn hàng lớn giữa các tỉnh.
- Hợp tác đơn vị logistics, gom đơn theo tuyến.
- Giao hàng nhanh tại TP.HCM.

**Kiểm soát chính sách giảm giá hiệu quả hơn**
- Chỉ giảm sâu cho nhóm sản phẩm lợi nhuận cao.
- Ưu đãi gián tiếp (quà tặng, miễn phí ship, bảo hành mở rộng) thay vì giảm giá trực tiếp.
- Giảm giá có điều kiện theo combo/hạng thành viên.

**Tận dụng kênh online để tăng trưởng doanh thu**
- Đẩy mạnh thương mại điện tử (Shopee, Lazada, Tiki).
- Xây dựng hệ thống đặt hàng trực tuyến trên website.
- Tận dụng mạng xã hội (Facebook, Zalo, TikTok) để tiếp thị.

## 6. Công cụ sử dụng

- **Tableau Desktop** — xây dựng dashboard, story, mô hình dự báo
- **Excel/Data Prep** — chuẩn hóa và xử lý dữ liệu

---
