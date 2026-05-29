# AI Product Lab - Worksheet

## 1. Scan 5+ Problems

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại, Tốn thời gian, Pain từ người khác | Kiểm tra và duyệt hồ sơ hoàn tiền công tác phí (Expense Claim) | Kế toán nội bộ, Nhân viên đi công tác | Nhân viên nộp sai format/thiếu chứng từ. Kế toán phải dò số thủ công bằng mắt. Tranh cãi qua lại nhiều lần, mất 1-2 tuần để nhận lại tiền. |
| 2 | Lặp lại, Tốn thời gian, AI làm tốt hơn | Trích xuất và kiểm duyệt hồ sơ dịch vụ công/doanh nghiệp trực tuyến | Chuyên viên hành chính công, Cán bộ tiếp nhận | Dân/Doanh nghiệp nộp ảnh chụp giấy tờ hoặc điền form sai quy chuẩn. Cán bộ phải gõ lại tay vào hệ thống lõi, dễ sai sót và gây nghẽn cổ chai trong khâu xử lý. |
| 3 | Lặp lại, Tốn thời gian, AI làm tốt hơn | Đánh giá chất lượng cuộc gọi CSKH (Telesales QA) | Trưởng nhóm CSKH, Nhân viên QA | Phải nghe lại từng file ghi âm dài 10-15 phút để chấm điểm thái độ, kịch bản. Hiện tại chỉ chấm ngẫu nhiên được 5% số lượng cuộc gọi, bỏ lọt lỗi. |
| 4 | Lặp lại, Tốn thời gian | Soạn thảo và điền thông tin hợp đồng kinh tế theo mẫu | Nhân viên Sales B2B, Admin | Mở file template dài 15 trang, dùng Find & Replace thủ công để thay tên, MST, số tiền. Dễ bị sót lại thông tin của khách hàng cũ. |
| 5 | Lặp lại, Tốn thời gian, Pain từ người khác | Sàng lọc CV ứng viên vòng hồ sơ | Chuyên viên Tuyển dụng (Recruiter) | Đọc lướt hàng trăm CV định dạng khác nhau để tìm từ khóa kỹ năng/kinh nghiệm. Dễ bị mỏi mắt, lỡ mất ứng viên tốt hoặc đưa nhầm ứng viên không đạt sang vòng phỏng vấn. |
| 6 | Lặp lại, Tốn thời gian | Phân loại bình luận, tin nhắn khiếu nại trên mạng xã hội | Nhân viên trực page, Community Manager | Đọc hàng ngàn comment mỗi ngày để phân loại: hỏi giá, spam, khiếu nại. Khiếu nại trôi quá nhanh dẫn đến xử lý chậm trễ, gây khủng hoảng. |


## 2. Chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Xử lý hồ sơ hoàn tiền công tác phí  | Actor rõ ràng. Bottleneck cụ thể ở khâu đối chiếu hóa đơn và quy chế. Impact dễ đo bằng thời gian xử lý. Có thể so sánh rõ ràng Rule-based vs AI-based. Phù hợp cho 1 buổi lab. | Chất lượng ảnh chụp hóa đơn mờ, khả năng OCR chữ viết tay, cách xử lý các hóa đơn đặc thù không chuẩn mẫu. |
| 2 | Trích xuất và kiểm duyệt hồ sơ dịch vụ công | Workflow vẽ được ngay. Bottleneck rõ ở khâu gõ lại dữ liệu tay. Impact tiết kiệm giờ làm cực lớn. | Vấn đề bảo mật dữ liệu giấy tờ. Đa dạng mẫu form, dễ bị lỗi nhận diện nếu giấy tờ cũ, nhòe. |
| 3 | Đánh giá chất lượng cuộc gọi CSKH  | Impact cực kỳ lớn (tăng audit coverage từ <5% lên 100%). Không thể làm bằng rule thường mà bắt buộc phải dùng AI. | Độ chính xác của model Speech-to-Text tiếng Việt vùng miền. Đánh giá sai cảm xúc của khách nếu chỉ dựa vào văn bản. |

### 2.1. Xử lý hồ sơ hoàn tiền công tác phí 

| Tiêu chí | Mô tả |
|---|---|
| **Actor** | Kế toán nội bộ & Nhân viên đi công tác. |
| **Workflow** | Nhân viên nộp form/chứng từ -> Kế toán tải về -> Đối chiếu thủ công với quy chế -> Duyệt hoặc yêu cầu làm lại. |
| **Bottleneck** | Kế toán mất 15-20 phút dò số thủ công từng dòng hóa đơn so với quy chế (PDF) cho mỗi bộ hồ sơ. |
| **Impact** | Rút ngắn thời gian duyệt từ 20 phút xuống 2 phút; giảm tỷ lệ làm lại (hiện tại là 40%). |
| **Success Metric** | Giảm 80% thời gian rà soát hồ sơ; giảm tỷ lệ trả về xuống dưới 10%. |
| **Boundary** | AI không tự động chuyển khoản tiền; chỉ cảnh báo lỗi sai và highlight để kế toán duyệt cuối. |
| **Điểm AI can thiệp** | Ngay khi nhân viên upload ảnh chứng từ, AI bóc tách và đối chiếu quy chế trước khi gửi cho kế toán. |
| **Mức chọn** | **Workflow**: AI kiểm tra trước (Pre-check) và trích xuất dữ liệu, con người duyệt (Approve). |
| **Rủi ro & HITL** | AI nhận diện sai số tiền hoặc phân loại sai chi phí -> Kế toán luôn kiểm duyệt lại các hồ sơ báo rủi ro (Vàng/Đỏ). |

### 2.2. Trích xuất và kiểm duyệt hồ sơ dịch vụ công

| Tiêu chí | Mô tả |
|---|---|
| **Actor** | Cán bộ tiếp nhận hồ sơ & Người dân/Doanh nghiệp. |
| **Workflow** | Dân nộp ảnh giấy tờ -> Cán bộ mở ảnh -> Đọc và gõ lại dữ liệu vào phần mềm -> Lưu trữ. |
| **Bottleneck** | Gõ lại tay tốn thời gian, dễ sai sót (typos) gây nghẽn cổ chai. |
| **Impact** | Tiết kiệm hàng ngàn giờ làm việc mỗi tháng cho cán bộ; dân không phải chờ đợi lâu. |
| **Success Metric** | Tiết kiệm 90% thời gian nhập liệu tay; tỷ lệ sai sót < 1%. |
| **Boundary** | AI không tự động từ chối hồ sơ pháp lý; chỉ auto-fill và cảnh báo ảnh mờ/giả mạo. |
| **Điểm AI can thiệp** | Bước gõ dữ liệu (Data Entry). AI đọc ảnh và tự động điền form. |
| **Mức chọn** | **Workflow**: AI auto-fill thông tin, Cán bộ nhìn lướt đối chiếu (Side-by-side) và click xác nhận. |
| **Rủi ro & HITL** | AI nhận diện sai chữ mờ -> Cán bộ kiểm tra đối chiếu trực tiếp trên màn hình và sửa lại trước khi lưu. |

### 2.3. Đánh giá chất lượng cuộc gọi CSKH 

| Tiêu chí | Mô tả |
|---|---|
| **Actor** | Nhân viên QA (Kiểm soát chất lượng) & Trưởng nhóm CSKH. |
| **Workflow** | Cuộc gọi kết thúc -> QA chọn ngẫu nhiên -> Nghe lại toàn bộ -> Ghi chú và chấm điểm Excel. |
| **Bottleneck** | Phải nghe lại 100% thời lượng cuộc gọi; chỉ chấm được <5% tổng số cuộc gọi. |
| **Impact** | Tăng độ bao phủ đánh giá lên 100%; phát hiện ngay lập tức các cuộc gọi có vấn đề. |
| **Success Metric** | Audit 100% cuộc gọi; giảm thời gian QA 1 cuộc gọi từ 15 phút xuống 1 phút. |
| **Boundary** | AI không tự động trừ lương nhân viên; chỉ gợi ý điểm và highlight đoạn vi phạm. |
| **Điểm AI can thiệp** | Phân tích file ghi âm ngay sau khi cuộc gọi kết thúc (Speech-to-Text -> LLM Check). |
| **Mức chọn** | **Workflow**: AI chấm điểm nháp 100% và lọc lỗi; QA chỉ tập trung nghe lại các cuộc gọi bị AI đánh cờ (Flagged). |
| **Rủi ro & HITL** | AI hiểu sai ngữ cảnh văn nói -> QA nghe lại đoạn vi phạm đã được highlight để chốt điểm cuối. |


## 3. Draft Workflow Trước/Sau (Before vs. After AI)

### 3.1. Workflow 1: Xử lý hồ sơ hoàn tiền công tác phí

```text
CURRENT STATE — 25 phút

[Nhân viên gõ Excel & nộp ảnh: 5']
→ [Kế toán tải & dò số liệu: 5']
→ [Kế toán lật quy chế kiểm tra: 10']  <-- bottleneck
→ [Chat yêu cầu sửa/bổ sung: 3']
→ [Đẩy sếp duyệt chi: 2']

FUTURE STATE — 3 phút

[Nhân viên nộp ảnh qua bot: 1']
→ [AI bóc tách dữ liệu hóa đơn: 0.5']
→ [AI đối chiếu nội quy công ty: 0.5']
→ [Kế toán kiểm duyệt Dashboard: 1']  <-- human boundary

Fallback: AI báo đỏ/vàng → Kế toán kiểm tra thủ công
```

### 3.2. Workflow 2: Kiểm duyệt hồ sơ dịch vụ trực tuyến

```text
CURRENT STATE — 15 phút

[Dân upload ảnh giấy tờ: 2']
→ [Cán bộ mở & tải ảnh: 1']
→ [Đọc thông tin trên ảnh: 2']
→ [Gõ lại toàn bộ dữ liệu: 8']  <-- bottleneck
→ [Kiểm tra chéo & xác nhận: 2']

FUTURE STATE — 2.5 phút

[Dân upload ảnh giấy tờ: 1']
→ [AI crop & làm nét ảnh: 0.5']
→ [AI auto-fill vào form: 0.5']
→ [Cán bộ đối chiếu side-by-side: 0.5']  <-- human boundary

Fallback: AI nhận diện mờ/tẩy xóa → Cán bộ kiểm tra kỹ lại
```

### 3.3. Workflow 3: Đánh giá chất lượng cuộc gọi (QA)

```text
CURRENT STATE — 20 phút

[Tải ngẫu nhiên file ghi âm: 2']
→ [Nghe toàn bộ & ghi nhận xét: 10']  <-- bottleneck
→ [Cộng điểm & gửi báo cáo: 3']
→ [Họp 1-1 nhắc nhở nhân sự: 5']

FUTURE STATE — 3 phút

[Đẩy file tự động vào hệ thống: 0.5']
→ [AI Speech-to-Text: 0.5']
→ [AI chấm điểm theo Checklist: 1']
→ [QA mở nghe đoạn vi phạm: 1']  <-- human boundary

Fallback: AI hiểu sai ngữ cảnh → QA ghi đè (override) điểm
```
