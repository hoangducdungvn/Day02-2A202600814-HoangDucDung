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

# 3.3 - Shortlist

*Đánh giá dựa trên các tiêu chí: Hiểu workflow sâu không, Actor cụ thể, Bottleneck rõ ràng, Impact đo được, Vẽ before/after được, So sánh Rule/Workflow/Agent, Quá rộng cho lab không.*

| Candidate | Vì sao vào shortlist | Rủi ro / điều chưa rõ |
|:---|:---|:---|
| **1. AI Agent làm Virtual TA / Tutor hỗ trợ học viên** *(Từ Cluster 1)* | - **Actor cụ thể:** Học viên & Trợ giảng.<br>- **Bottleneck cụ thể:** Bước chờ TA trả lời làm "đóng băng" tiến độ thực hành.<br>- **Impact dễ đo:** Đo bằng thời gian phản hồi, tỷ lệ ticket tự động giải quyết.<br>- **Dễ so sánh:** Rất phù hợp để phân tích điểm khác biệt giữa Rule, Workflow và Agent. | - **Phạm vi lab:** Xây dựng Agent / RAG Agent có thể khá rộng và mất nhiều thời gian gom data knowledge base cho một buổi lab.<br>- Liệu có ai trong nhóm hiểu đủ sâu về luồng học tập để thiết kế workflow chuẩn không? |
| **2. Workflow trích xuất & đối chiếu hồ sơ (OCR)** *(Từ Cluster 2)* | - **Hiểu sâu workflow:** Có người đề xuất trực tiếp là thành viên nhóm.<br>- **Actor cụ thể:** Nhân viên văn phòng, kế toán.<br>- **Bottleneck cụ thể:** Khâu nhìn bằng mắt và gõ lại dữ liệu.<br>- **Vẽ Before/After:** Rất rõ ràng để vẽ luồng quy trình.<br>- **Impact đo được:** Bằng thời gian xử lý trên mỗi bộ hồ sơ. | - Việc cấu hình cho bài toán xử lý hồ sơ/hóa đơn tiếng Việt có thể mất thời gian tuỳ chỉnh.<br>- Có thể chỉ cần Workflow + AI là đủ giải quyết, chưa cần đến tính "Agent" để tự ra quyết định. |
| **3. Gom luồng thông báo tập trung** *(Từ Cluster 3)* | - **Hiểu sâu workflow:** Cả nhóm đều hiểu do gặp vấn đề hàng ngày.<br>- **Vẽ Before/After:** Dễ dàng mô tả sự khác biệt trước và sau.<br>- **Bottleneck cụ thể:** Khâu check thông báo qua Zalo/Teams. | - Có khả năng chỉ cần dùng Rule/Workflow đơn giản (như Zapier/Make) là xử lý xong.<br>- Khó có thể so sánh nổi bật sự ưu việt của Agent so với Workflow cho candidate này. |

# 3.4 - Score để đồng thuận

*Thang điểm 1-5. Mục tiêu là để làm rõ lý do tại sao chọn hay không chọn.*

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|:---|:---|:---|:---|:---|:---|:---|:---|:---|
| **1. AI Agent làm Virtual TA / Tutor** | **5**<br>(Học viên & TA) | **4**<br>(Luồng QA rõ nhưng flow Agent cần chi tiết thêm) | **5**<br>(Ai cũng từng là học viên chờ TA) | **5**<br>(Đo thời gian phản hồi) | **3**<br>(Làm RAG chuẩn mất nhiều thời gian gom data) | **5**<br>(Dễ so sánh Bot cứng / Workflow / Agent) | **4**<br>(Trải nghiệm học viên tốt, nhưng góc nhìn TA thì ít) | **31** |
| **2. Workflow trích xuất OCR hồ sơ** | **5**<br>(Kế toán, HCNS) | **5**<br>(Step-by-step duyệt rất rõ) | **4**<br>(Dựa trên kinh nghiệm thực tế của người đề xuất) | **5**<br>(Đo thời gian xử lý/hồ sơ) | **4**<br>(Dùng API OCR có sẵn nên làm khá nhanh) | **3**<br>(Nghiêng về Workflow tích hợp AI hơn là dùng sức mạnh Agent) | **4**<br>(1 người hiểu sâu, nhưng số đông chưa trải nghiệm) | **30** |
| **3. Gom luồng thông báo tập trung** | **5**<br>(Tất cả User) | **5**<br>(Từ App -> Webhook -> 1 nơi) | **4**<br>(Thường xuyên bị trôi tin nhắn làm lỡ việc) | **3**<br>(Khó quy ra số phút/giờ tiết kiệm cụ thể) | **5**<br>(Rất dễ, nối Zapier/Make là xong) | **2**<br>(Chỉ cần Workflow là giải quyết được, ép Agent vào bị gượng) | **5**<br>(Ai cũng hiểu nỗi đau này) | **29** |