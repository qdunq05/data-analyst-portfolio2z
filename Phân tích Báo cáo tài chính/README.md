# 🛒 CDZen Retail Analytics — Phân tích Doanh thu, Lợi nhuận & Khách hàng

Phân tích toàn diện hoạt động kinh doanh của **CDZen** — chuỗi bán lẻ điện máy & nội thất tại Việt Nam giai đoạn 2011–2017, bao gồm doanh thu, lợi nhuận, hiệu suất sản phẩm, hành vi khách hàng, dự báo xu hướng và đề xuất chiến lược — xây dựng trên Tableau.

![Tableau](https://img.shields.io/badge/Tableau-E97627?style=flat&logo=tableau&logoColor=white)
![Status](https://img.shields.io/badge/status-completed-brightgreen)

![Doanh thu - Bức tranh tổng thể](Tong_quan.png)

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
- Ngành hàng: 3 nhóm sản phẩm chính — **Hàng điện lạnh** (Tủ lạnh, Máy giặt, Máy điều hòa), **Hàng điện tử** (Điện thoại, Máy tính bảng, Phụ kiện điện tử, TV), **Nội thất** (Ghế, Giường, Bàn, Kệ sách).
- Khu vực: Hồ Chí Minh City, Hà Nội, Hải Dương, Bà Rịa - Vũng Tàu, Ninh Bình, Đà Nẵng, Thừa Thiên - Huế, Quảng Ninh.
- Kênh bán hàng: **Đại lý ủy quyền, Chuỗi cửa hàng, Online**.
- Phương thức giao hàng: Giao hàng bằng xe, Đường sắt, Đường biển.

### b. Các chỉ số chính
| Nhóm chỉ số | Mô tả |
|---|---|
| **Doanh thu / Lợi nhuận** | Theo sản phẩm, khu vực, kênh bán, năm |
| **Số lượng đơn hàng** | Theo sản phẩm, kênh bán, mức giảm giá |
| **Khách hàng** | Doanh thu, lợi nhuận theo từng khách hàng; phân nhóm KH Vàng/Bạc/Kim cương |
| **Dự báo (Forecast)** | Doanh thu & lợi nhuận ước tính (Estimate) theo nhóm sản phẩm và kênh bán |

### c. Chuẩn bị dữ liệu
- Tính **tỷ suất lợi nhuận trên doanh thu** cho từng sản phẩm để xác định nhóm sinh lời/thua lỗ.
- Phân nhóm khách hàng theo tổng doanh thu đóng góp: **KH Kim cương, KH Vàng, KH Bạc**.
- Xây dựng mô hình dự báo (Forecast) cho doanh thu & lợi nhuận đến năm 2019 theo nhóm sản phẩm và kênh bán hàng.
- Tổng hợp ảnh hưởng của mức giảm giá đến số lượng đơn hàng theo từng sản phẩm.

## 3. Thiết kế Dashboard

Story Tableau gồm **6 trang phân tích chính** (kèm bộ lọc theo năm, khu vực, kênh bán):

| Trang | Nội dung chính |
|---|---|
| 💵 Dashboard Doanh thu | Bức tranh tổng thể doanh thu theo khu vực, sản phẩm, kênh bán, xu hướng theo năm |
| 📉 Dashboard Lợi nhuận | Lợi nhuận theo nhóm sản phẩm, khu vực, năm, kênh bán hàng |
| 📦 Dashboard Sản phẩm | Hiệu suất bán hàng, top sản phẩm, ảnh hưởng giảm giá đến số lượng đơn |
| 👥 Dashboard Khách hàng | Phân nhóm khách hàng, top khách hàng, phân bố theo khu vực |
| 🔮 Dashboard Dự đoán | Dự báo doanh thu & lợi nhuận theo nhóm sản phẩm và kênh bán đến 2019 |
| 🎯 Đề xuất & Chiến lược | Khuyến nghị hành động cụ thể dựa trên toàn bộ phân tích |

## 4. Kết quả & Insights

### 💵 Doanh thu — Bức tranh tổng thể

![Doanh thu tổng thể](Tong_quan.png)

- Tổng doanh thu đạt **~29,96 tỷ đồng** với **779 khách hàng**.
- **TP. Hồ Chí Minh áp đảo** với doanh thu **15,47 tỷ** — gấp hơn 3 lần khu vực đứng thứ 2 (Hà Nội, 4,42 tỷ).
- **Máy giặt** là sản phẩm đóng góp doanh thu lớn nhất (101.989), theo sau là Tủ lạnh (73.966) và Máy điều hòa (45.903).
- Kênh **Đại lý ủy quyền** chiếm tỷ trọng doanh thu cao nhất (49,67%), tiếp theo là Chuỗi cửa hàng (33,82%) và Online (16,51%).
- Phương thức giao hàng chủ yếu là **giao hàng bằng xe (54,6%)**.
- Doanh thu biến động mạnh qua các năm: đạt đỉnh **13,1 tỷ (2012)**, giảm sâu 2013–2015, rồi phục hồi mạnh trở lại đạt **10,3 tỷ (2017)**.
- Giảm giá có tác động rõ rệt đến doanh thu ở nhóm sản phẩm như **Ghế (giảm 19,2%)** và **Máy giặt (19,45%)** — cho thấy độ nhạy giá cao ở các nhóm này.

### 📉 Lợi nhuận — Nhìn từ dữ liệu

![Lợi nhuận](Loi_nhuan.png)

- Tổng lợi nhuận đạt **2.885.259 nghìn đồng**, tỷ suất lợi nhuận **9,6%**.
- Nhóm **Hàng điện tử** có lợi nhuận cao nhất (Máy tính bảng 607.710, Phụ kiện điện tử 598.640) nhưng đồng thời cũng có sản phẩm **lỗ nặng** — TV lỗ **-94.216**.
- Trong nội thất, **Bàn (-14.728)** và **Kệ sách (-89.173)** đang thua lỗ.
- **Máy tính bảng** có tỷ suất lợi nhuận/doanh thu cao nhất (26,2%), trong khi **Kệ sách (-6,4%)** và **Bàn (-0,6%)** âm.
- Lợi nhuận theo khu vực tập trung mạnh ở **Hà Nội (493.070)**, Hải Dương (271.854), Ninh Bình (204.403).
- Kênh **Đại lý ủy quyền đóng góp 71,27%** tổng lợi nhuận — vượt trội so với Chuỗi cửa hàng (17,15%) và Online (11,58%).
- Lợi nhuận theo năm biến động mạnh, đạt đỉnh **989.536 (2012)**, giảm sâu 2015 (35.209) rồi phục hồi lên **1.078.468 (2017)**.

### 📦 Hiệu suất sản phẩm — Xu hướng đang lên

![Hiệu suất sản phẩm](Hieu_suat.png)

- Tổng số lượng sản phẩm đã bán: **373.361 sản phẩm**.
- **Máy giặt** dẫn đầu tuyệt đối về số lượng bán ra (101.989), tiếp theo Tủ lạnh (73.966), Máy điều hòa (45.903).
- Kênh **giao hàng (Giao hàng)** chiếm phần lớn số lượng đặt hàng cho các sản phẩm chủ lực như Máy giặt, Tủ lạnh, Máy điều hòa.
- **2017 là năm bùng nổ** về số lượng đơn hàng cho hầu hết sản phẩm, đặc biệt Máy giặt tăng vọt lên **4.353 đơn** so với các năm trước đó (dưới 3.000).
- Nhóm sản phẩm điện lạnh có xu hướng tăng trưởng ổn định và mạnh nhất trong toàn bộ danh mục.

### 👥 Khách hàng CDZen — Chìa khóa tăng trưởng

![Khách hàng](Khach_hang.png)

- Tổng cộng **theo dõi được lượng khách hàng trải rộng nhiều khu vực**, dao động từ 136 đến 731 khách hàng/khu vực.
- **Hà Nội (731) và Hải Dương (658)** là 2 khu vực có số lượng khách hàng đông nhất.
- Top khách hàng đóng góp doanh thu cao nhất: **Tiêu Thị Loan (1.155.312), Trường Ngọc Trầm (1.126.130), Trần Lý Khan (890.169)**.
- Phân nhóm khách hàng theo giá trị: **KH Kim cương** (nhóm cao cấp nhất) là nhóm đóng góp doanh thu vượt trội, phần lớn phân bố ở vùng doanh thu 400K trở lên trên biểu đồ phân tán doanh thu-lợi nhuận.
- Mối quan hệ giữa doanh thu và lợi nhuận khách hàng có xu hướng **tương quan thuận nhưng không tuyệt đối** — một số khách hàng doanh thu cao nhưng lợi nhuận âm, cho thấy cần rà soát chính sách giá/chiết khấu riêng cho từng khách hàng lớn.

### 🔮 Doanh thu & Lợi nhuận — Góc nhìn tương lai

![Dự đoán tương lai](Tuong_lai.png)

- Mô hình dự báo (2018–2019) cho thấy cả doanh thu và lợi nhuận có xu hướng **đi ngang hoặc giảm nhẹ** so với đỉnh 2017, với khoảng tin cậy (band dự báo) khá rộng — phản ánh mức độ bất định cao.
- Nhóm **Nội thất** có biến động dự báo mạnh nhất, khoảng tin cậy nới rộng đáng kể ở 2018–2019.
- Theo kênh bán hàng, **Đại lý ủy quyền** tiếp tục được dự báo là kênh dẫn dắt tăng trưởng chính, trong khi kênh **Online** có quy mô nhỏ hơn nhưng ổn định.
- Cảnh báo: xu hướng dự báo giảm nhẹ sau đỉnh 2017 cho thấy cần có chiến lược chủ động để duy trì đà tăng trưởng thay vì để thị trường tự điều chỉnh.

## 5. Đề xuất & Chiến lược

![Chiến lược tối ưu](Chien_luoc.png)

**Tăng doanh thu tại các tỉnh ngoài TP.HCM**
- Tăng giá trị đơn hàng trung bình bằng combo/sản phẩm cao cấp.
- Giữ giá cao ở TP.HCM, áp dụng ưu đãi linh hoạt hơn ở tỉnh khác.
- Triển khai chương trình khách hàng thân thiết để tăng tần suất mua hàng.

**Tối ưu danh mục sản phẩm & nhóm khách hàng**
- Tăng cường bán chéo (cross-sell): gợi ý điện tử/nội thất kèm khi mua điện lạnh.
- Tập trung upsell cho nhóm khách hàng Kim cương với ưu đãi độc quyền.
- Triển khai chương trình tri ân riêng cho top 10 khách hàng doanh thu cao nhất.

**Tối ưu phương thức giao hàng**
- Tận dụng đường sắt cho các đơn hàng lớn giữa các tỉnh để giảm chi phí vận chuyển.
- Hợp tác đơn vị logistics, gom đơn theo tuyến để tiết kiệm chi phí.
- Triển khai giao hàng nhanh tại TP.HCM để tăng trải nghiệm khách hàng.

**Kiểm soát chính sách giảm giá hiệu quả hơn**
- Giữ mức giảm giá thấp nhưng có chiến lược: chỉ giảm giá sâu cho nhóm sản phẩm lợi nhuận cao để kích cầu.
- Ưu đãi gián tiếp (tặng quà, miễn phí vận chuyển, bảo hành mở rộng) thay vì giảm giá trực tiếp.
- Áp dụng giảm giá có điều kiện: theo combo hoặc theo hạng thành viên.

**Tận dụng kênh online để tăng trưởng doanh thu**
- Đẩy mạnh thương mại điện tử: đưa sản phẩm lên Shopee, Lazada, Tiki.
- Xây dựng hệ thống đặt hàng trực tuyến ngay trên website công ty.
- Tận dụng mạng xã hội (Facebook, Zalo, TikTok) để tiếp thị và tư vấn trực tuyến.

## 6. Công cụ sử dụng

- **Tableau Desktop** — xây dựng dashboard, story, mô hình dự báo (Forecast)
- **Excel/Data Prep** — chuẩn hóa và xử lý dữ liệu đầu vào

---