# 3.1 - Trình bày top 3 của nhóm

| # | Người đưa ra | Candidate problem | Người gặp vấn đề | Điểm nghẽn (Bottleneck) | Cảm nhận nhanh (Quick gut) |
|:---|:---|:---|:---|:---|:---|
| 1 | [Đoàn Công Phú] | Tài liệu học tập mở quá sát giờ học nên không kịp ôn trước. | Học viên | Không có đủ thời gian để đọc trước, dẫn đến không theo kịp tốc độ bài giảng. | Quy trình (Process fix) |
| 2 | [Đoàn Công Phú] | Học viên trái ngành không load kịp kiến thức khi học lab buổi chiều do lượng kiến thức tăng quá nhanh. | Học viên trái ngành | Bị choáng ngợp thông tin, tốc độ nạp kiến thức chậm hơn tốc độ dạy. | AI Agent (Tutor cá nhân) |
| 3 | [Đoàn Công Phú] | Không có AI tutor hỗ trợ recap kiến thức nền hoặc giải thích nhanh thuật ngữ. | Học viên | Tốn thời gian tự tra cứu thủ công, dễ hiểu sai lệch thuật ngữ chuyên môn. | RAG Agent |
| 4 | [Vũ Quang Vinh] | Học viên nhiều nhưng trợ giảng ít dẫn đến việc thắc mắc nhưng không được giải đáp kịp thời. | Học viên | Thời gian chờ đợi TA quá lâu gây "đóng băng" tiến độ thực hành code. | Agent (Virtual TA) |
| 5 | [Vũ Quang Vinh] | Các học viên đều có thắc mắc giống nhau (cài đặt môi trường, hỏi đường...). | Trợ giảng (TA) | Trợ giảng bị quá tải, phải lặp lại thao tác copy/paste câu trả lời như một cái máy. | Agent / Rule-based FAQ |
| 6 | [Vũ Quang Vinh] | Khó nắm bắt được các thông tin do có quá nhiều kênh thông báo (Zalo, Teams, Canvas). | Học viên | Phải lướt dò thủ công nhiều app, dễ trôi tin và lỡ deadline quan trọng. | Workflow + AI (Gom luồng) |
| 7 | [Hoàng Đức Dũng] | Xử lý hồ sơ hoàn tiền công tác phí chậm và tốn công. | Kế toán / Hành chính | Khâu đối chiếu hóa đơn với quy chế công ty phải làm hoàn toàn bằng mắt thường. | AI Workflow (OCR + LLM) |
| 8 | [Hoàng Đức Dũng] | Trích xuất và kiểm duyệt hồ sơ dịch vụ công tốn nhiều thời gian. | Nhân viên xử lý hồ sơ | Phải gõ lại dữ liệu thủ công từ các form giấy tờ cũ, dễ bị mờ/nhòe. | Workflow (OCR) |
| 9 | [Hoàng Đức Dũng] | Đánh giá chất lượng cuộc gọi CSKH chỉ đạt tỷ lệ rất thấp (dưới 5%). | QA / Quản lý CSKH | Phải nghe lại từng file ghi âm thủ công, không đủ sức người để cover 100% cuộc gọi. | AI (Speech-to-Text) |

# 3.2 - Gom trùng

| Cluster | Candidates included | Pattern chung | Ghi chú |
|:---|:---|:---|:---|
| **Hỗ trợ học tập & Giải đáp thắc mắc (Virtual TA / AI Tutor)** | 2, 3, 4, 5 | Học viên gặp khó khăn khi nạp kiến thức mới hoặc tiến độ bị "đóng băng" do phải chờ đợi giải đáp lâu. Cùng lúc đó, Trợ giảng (TA) bị quá tải vì phải trả lời các câu hỏi lặp lại. | Hướng giải quyết tập trung vào các AI Agent / RAG đóng vai trò là gia sư hoặc trợ giảng ảo, giúp cá nhân hóa và tự động hóa việc hỏi đáp. |
| **Tự động hóa xử lý giấy tờ, hồ sơ (Document Processing / OCR)** | 7, 8 | Các nghiệp vụ back-office (hành chính, kế toán, dịch vụ công) đang phải nhập liệu và đối chiếu các form mẫu giấy tờ hoàn toàn bằng mắt thường thủ công. | Áp dụng Workflow kết hợp công nghệ OCR và LLM để tự động trích xuất dữ liệu, giúp tiết kiệm công sức và giảm sai sót cho con người. |
| **Tối ưu luồng thông tin & Quy trình (Workflow / Info Flow)** | 1, 6 | Luồng phân phối thông tin và tài liệu chưa hợp lý (tài liệu mở sát giờ, thông báo rải rác ở quá nhiều app) khiến học viên khó theo dõi, bị ngợp hoặc lỡ deadline. | Cần điều chỉnh lại quy trình (Process fix) hoặc xây dựng Workflow gom luồng thông báo tập trung về một nơi. |
| **Kiểm duyệt tự động qua âm thanh (Speech-to-Text / QA)** | 9 | Lượng dữ liệu cần kiểm duyệt quá lớn (file ghi âm cuộc gọi), dùng sức người nghe lại thủ công không thể đạt được độ bao phủ (coverage) mong muốn. | Ứng dụng AI phân tích giọng nói (Speech-to-Text) để chuyển đổi và đánh giá chất lượng tự động thay vì dùng sức người. |
