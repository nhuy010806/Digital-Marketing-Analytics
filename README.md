# 🏝️ Phân tích hiệu quả quảng bá du lịch Côn Đảo trên TikTok và YouTube

**Đồ án môn học: Phân tích Marketing số**  
**Trường Đại học Kinh tế - Luật, ĐHQG-HCM**  
**Nhóm nghiên cứu:** Ngũ đủ 8 tiếng  

---

## 📌 Tổng quan

Dự án này thực hiện phân tích dữ liệu đa nền tảng nhằm đánh giá hiệu quả quảng bá của điểm đến Côn Đảo trên **TikTok** và **YouTube**, từ đó so sánh với các đối thủ cạnh tranh trực tiếp là **Phú Quốc** và **Cát Bà**. Nghiên cứu kết hợp phân tích thống kê truyền thống và các mô hình học máy (Random Forest, XGBoost, Prophet) để đưa ra các khuyến nghị chiến lược cho CMO.

---

## 🎯 Mục tiêu

- Đánh giá hiệu suất và vị thế cạnh tranh của Côn Đảo trên mạng xã hội.
- Phân tích hành vi, cảm xúc và các yếu tố nội dung ảnh hưởng đến người xem.
- Xác định khoảng trống thị trường để tạo lợi thế cạnh tranh.
- Xây dựng **AI Agent tự động** thu thập, lọc và phân tích nội dung viral.

---

## 🧠 Phương pháp luận

### 1. Thu thập dữ liệu
- **Apify** – crawl metadata từ TikTok và YouTube.
- **Getsubs.cc** – trích xuất phụ đề/nội dung lời nói từ video.
- Dữ liệu giai đoạn 2024–2026 cho 3 địa điểm: Côn Đảo, Cát Bà, Phú Quốc.

### 2. Phân tích dữ liệu
- **EDA** (Exploratory Data Analysis) – làm sạch, chuẩn hóa, trực quan hóa.
- **Phân tích nâng cao**:
  - Random Forest & XGBoost – xác định yếu tố ảnh hưởng đến lượt xem/tương tác.
  - Prophet – dự báo chuỗi thời gian theo mùa.
  - Hồi quy phi tuyến – tìm điểm bão hòa nội dung.

### 3. AI Agent (Marketing Automation)
- Xây dựng pipeline tự động trên **n8n**.
- Hàng ngày quét video theo từ khóa, lọc bằng rule-based JS, gửi đến **Google Gemini** để sinh insight chiến lược.
- Tự động ghi kết quả vào **Google Sheets** và gửi cảnh báo lỗi qua Gmail.

---

## 🔍 Insights chính

| Insight | Mô tả |
|---------|------|
| **1** | Lượt xem quyết định tương tác (≈80%), **không phải thời lượng video** |
| **2** | Khán giả hoạt động mạnh vào khung giờ “độc lạ”: 1h sáng Thứ 3 (TikTok), 11h trưa Thứ 3 (YouTube) |
| **3** | TikTok phù hợp chiến dịch bùng nổ ngắn hạn, YouTube dành cho chiến lược dài hạn bền vững |
| **4** | Hiệu quả KOL phụ thuộc vào **sự phù hợp**, không phải quy mô (Mid KOL cho ROI tốt nhất) |
| **5** | Ý định du lịch (tỷ lệ lưu video) đang hình thành nhưng chưa bền vững |

---

## 📈 Đề xuất chiến lược (5 trụ cột)

1. **Tối ưu hóa tiếp cận** – đăng bài theo khung giờ vàng riêng cho từng nền tảng.
2. **Phân bổ nền tảng** – ngắn hạn trên TikTok, dài hạn trên YouTube.
3. **Chiến lược KOL đa tầng** – ưu tiên Mid & Micro KOL, kiểm soát tần suất <10 video/tuần.
4. **Chuyển hóa hành vi** – tối ưu CTA, nội kiểu “cẩm nang” để tăng tỷ lệ lưu.
5. **Đo lường & tối ưu liên tục** – A/B testing, dự báo xu hướng bằng Prophet.

---

## 🤖 AI Agent – Marketing Automation

- **Nền tảng**: n8n + Apify + Google Gemini
- **Tác vụ chính**:
  - Tự động thu thập video TikTok/Instagram theo từ khóa (ví dụ: “du lịch Côn Đảo”)
  - Lọc video có lượt xem & tỷ lệ tương tác cao
  - Dùng LLM để sinh insight giải thích lý do thành công
  - Lưu kết quả vào Google Sheets và báo lỗi qua email
- **Output**: 100+ video viral kèm đánh giá chiến lược tự động.

---
