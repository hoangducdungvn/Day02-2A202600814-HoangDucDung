# AI Product Lab - Worksheet

## 1. Scan 5+ Problems (Sử dụng 4 lăng kính)

| # | Tên bài toán | Lăng kính áp dụng | Ai đang đau? (Actor) | Nỗi đau cụ thể (Pain point) & Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Kiểm tra và duyệt hồ sơ hoàn tiền công tác phí (Expense Claim) | Lặp lại, Tốn thời gian, Pain từ người khác | Kế toán nội bộ, Nhân viên đi công tác | Nhân viên nộp sai format/thiếu chứng từ. Kế toán phải dò số thủ công bằng mắt. Tranh cãi qua lại nhiều lần, mất 1-2 tuần để nhận lại tiền. |
| 2 | Trích xuất và kiểm duyệt hồ sơ dịch vụ công/doanh nghiệp trực tuyến | Lặp lại, Tốn thời gian, AI làm tốt hơn | Chuyên viên hành chính công, Cán bộ tiếp nhận | Dân/Doanh nghiệp nộp ảnh chụp giấy tờ hoặc điền form sai quy chuẩn. Cán bộ phải gõ lại tay vào hệ thống lõi, dễ sai sót và gây nghẽn cổ chai trong khâu xử lý. |
| 3 | Đánh giá chất lượng cuộc gọi CSKH (Telesales QA) | Lặp lại, Tốn thời gian, AI làm tốt hơn | Trưởng nhóm CSKH, Nhân viên QA | Phải nghe lại từng file ghi âm dài 10-15 phút để chấm điểm thái độ, kịch bản. Hiện tại chỉ chấm ngẫu nhiên được 5% số lượng cuộc gọi, bỏ lọt lỗi. |
| 4 | Soạn thảo và điền thông tin hợp đồng kinh tế theo mẫu | Lặp lại, Tốn thời gian | Nhân viên Sales B2B, Admin | Mở file template dài 15 trang, dùng Find & Replace thủ công để thay tên, MST, số tiền. Dễ bị sót lại thông tin của khách hàng cũ. |
| 5 | Sàng lọc CV ứng viên vòng hồ sơ | Lặp lại, Tốn thời gian, Pain từ người khác | Chuyên viên Tuyển dụng (Recruiter) | Đọc lướt hàng trăm CV định dạng khác nhau để tìm từ khóa kỹ năng/kinh nghiệm. Dễ bị mỏi mắt, lỡ mất ứng viên tốt hoặc đưa nhầm ứng viên không đạt sang vòng phỏng vấn. |
| 6 | Phân loại bình luận, tin nhắn khiếu nại trên mạng xã hội | Lặp lại, Tốn thời gian | Nhân viên trực page, Community Manager | Đọc hàng ngàn comment mỗi ngày để phân loại: hỏi giá, spam, khiếu nại. Khiếu nại trôi quá nhanh dẫn đến xử lý chậm trễ, gây khủng hoảng. |

## 2. Top 3 Problem Cards

### Problem Card 1: Xử lý hồ sơ hoàn tiền công tác phí
- **Actor:** Kế toán nội bộ (Reviewer) & Nhân viên (Submitter).
- **Lăng kính:** Pain từ người khác (nhân viên làm sai, kế toán phải hối thúc), Lặp lại.
- **Mô tả vấn đề:** Quy trình claim tiền hiện tại yêu cầu nhân viên tự nhập liệu vào Excel và nộp ảnh hóa đơn. Kế toán phải tải về, mở hai màn hình dò số thủ công và đối chiếu với quy chế chi tiêu (file PDF) xem có hợp lệ không.
- **Hậu quả/Dấu hiệu:** Mất trung bình 15-20 phút rà soát cho 1 bộ hồ sơ. Tỷ lệ trả về làm lại lên tới 40%, gây ức chế cho cả hai bên.
- **Metrics (Cách đo):**
  - Thời gian xử lý trung bình/hồ sơ (Average Handling Time).
  - Tỷ lệ hồ sơ phải làm lại (Rework rate).

### Problem Card 2: Trích xuất & kiểm duyệt hồ sơ dịch vụ công trực tuyến
- **Actor:** Cán bộ tiếp nhận hồ sơ / Chuyên viên hành chính.
- **Lăng kính:** Tốn thời gian, Lặp lại, AI có thể tốt hơn.
- **Mô tả vấn đề:** Khi người dân hoặc doanh nghiệp nộp hồ sơ qua cổng dịch vụ trực tuyến (ảnh chụp CMND/CCCD, giấy phép kinh doanh, tờ khai), cán bộ phải mở từng ảnh, đọc và gõ lại tay dữ liệu vào phần mềm quản lý lõi để xử lý tiếp.
- **Hậu quả/Dấu hiệu:** Tốn nhiều giờ đồng hồ gõ phím. Sai sót do gõ nhầm (typos) dẫn đến sai lệch dữ liệu công dân/doanh nghiệp. Thời gian chờ đợi của người nộp bị kéo dài.
- **Metrics (Cách đo):**
  - Thời gian trích xuất dữ liệu từ một bộ hồ sơ.
  - Tỷ lệ lỗi sai sót (Error rate) trong quá trình nhập liệu.

### Problem Card 3: Đánh giá chất lượng cuộc gọi CSKH (Telesales QA)
- **Actor:** Nhân viên Kiểm soát chất lượng (QA) / Trưởng nhóm.
- **Lăng kính:** Lặp lại, AI có thể tốt hơn.
- **Mô tả vấn đề:** Hàng ngày tổng đài tạo ra hàng ngàn phút gọi. QA phải nghe lại thủ công từng file ghi âm, dùng file Excel để chấm điểm theo checklist (chào hỏi, giải quyết vấn đề, từ ngữ cấm).
- **Hậu quả/Dấu hiệu:** Tốn thời gian nghe bằng đúng thời lượng cuộc gọi. Chỉ "cover" được <10% tổng số cuộc gọi. Đánh giá mang tính cảm tính của người chấm.
- **Metrics (Cách đo):**
  - Tỷ lệ % cuộc gọi được audit trên tổng số cuộc gọi (Coverage).
  - Thời gian để audit 1 cuộc gọi.

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
