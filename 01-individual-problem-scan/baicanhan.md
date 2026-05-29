# AI Product Lab - Worksheet

## 1. Scan 5+ Problems (Sử dụng 4 lăng kính)

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

### Workflow 1: Xử lý hồ sơ hoàn tiền công tác phí

**[As-Is] Quy trình thủ công:**
1. Nhân viên mở file Excel mẫu, gõ tay từng khoản chi (tiền taxi, tiền ăn) và đính kèm file ảnh hóa đơn gửi kế toán.
2. Kế toán tải file, dò số liệu trên Excel có khớp với ảnh chụp không.
3. Kế toán lật mở quy chế (PDF) xem khoản chi có vượt định mức của cấp bậc nhân viên đó không.
4. Nếu sai/thiếu, chat qua Zalo/Teams yêu cầu nhân viên giải trình hoặc gõ lại form. (Vòng lặp 2-3 lần).
5. Hồ sơ hợp lệ -> Đẩy lên sếp duyệt chi.

**[To-Be] AI-Assisted Workflow:**
1. Nhân viên chụp ảnh hóa đơn gửi vào bot nội bộ/App.
2. AI (OCR + LLM) tự động đọc ảnh, bóc tách: Số tiền, Ngày tháng, Phân loại chi phí (Ăn uống, Đi lại) và tự tạo form.
3. AI (Rule Engine) tự động đối chiếu thông tin với bảng nội quy công ty. Nếu hóa đơn vượt mức, AI báo đỏ và yêu cầu nhân viên bổ sung lý do ngay lập tức.
4. Kế toán nhận một Dashboard đã được AI phân loại. Chỉ cần click "Duyệt" cho các hồ sơ báo Xanh (Chuẩn 100%), và dành thời gian kiểm tra các hồ sơ Vàng/Đỏ (Ngoại lệ/Rủi ro).

### Workflow 2: Kiểm duyệt hồ sơ dịch vụ trực tuyến

**[As-Is] Quy trình thủ công:**
1. Người dân/Doanh nghiệp upload ảnh giấy tờ lên cổng thông tin.
2. Cán bộ tiếp nhận mở hệ thống, tải ảnh về màn hình phụ.
3. Dùng mắt đọc thông tin trên ảnh (Tên, Số giấy tờ, Địa chỉ...).
4. Gõ tay lại toàn bộ thông tin vào các trường (fields) trên phần mềm quản lý nghiệp vụ.
5. Kiểm tra chéo bằng mắt một lần nữa rồi nhấn xác nhận chuyển hồ sơ cho phòng ban xử lý.

**[To-Be] AI-Assisted Workflow:**
1. Người dân/Doanh nghiệp upload ảnh.
2. AI (OCR + Vision Models) tự động crop, làm nét ảnh và bóc tách 100% các trường thông tin quan trọng.
3. AI tự động điền (auto-fill) vào form trên phần mềm nghiệp vụ của cán bộ.
4. AI đánh dấu (highlight) các vùng thông tin bị mờ, nghi ngờ giả mạo hoặc có dấu hiệu tẩy xóa.
5. Cán bộ tiếp nhận chỉ việc nhìn lướt qua để đối chiếu các trường AI đã điền với ảnh gốc (hiển thị side-by-side) và bấm nút "Tiếp nhận".

### Workflow 3: Đánh giá chất lượng cuộc gọi (QA)

**[As-Is] Quy trình thủ công:**
1. Cuối ngày, QA tải ngẫu nhiên 10 file ghi âm từ hệ thống tổng đài.
2. Đeo tai nghe, bật file. Vừa nghe vừa pause để gõ nhận xét vào file Excel chấm điểm.
3. Cuối tuần, cộng điểm tay và gửi file báo cáo cho Trưởng nhóm CSKH.
4. Trưởng nhóm họp 1-1 với nhân sự để nhắc nhở dựa trên 10 file ngẫu nhiên đó.

**[To-Be] AI-Assisted Workflow:**
1. Các file ghi âm sau khi kết thúc được tự động đẩy vào hệ thống.
2. AI (Speech-to-Text) tự động chuyển băng ghi âm thành văn bản (Transcript).
3. AI (LLM Sentiment & Logic) phân tích Transcript dựa trên Checklist cho trước: Đã chào khách chưa? Khách có giận dữ không? Có chửi bậy không? Có bán chéo (cross-sell) được không?
4. AI tự động chấm điểm 100% cuộc gọi.
5. QA và Trưởng nhóm mở Dashboard: Nhìn thấy ngay nhân viên nào điểm thấp nhất trong ngày, và AI đã tóm tắt sẵn lý do (VD: Nhân viên A ngắt lời khách 3 lần ở phút thứ 2:05). Con người chỉ nghe lại các đoạn vi phạm để kiểm chứng.
