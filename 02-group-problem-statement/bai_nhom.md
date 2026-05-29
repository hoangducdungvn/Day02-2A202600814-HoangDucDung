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
| **1. AI Agent làm Virtual TA / Tutor** | **5**<br>(Học viên & TA) | **3**<br>(Luồng QA rõ nhưng flow Agent cần chi tiết thêm) | **5**<br>(Ai cũng từng là học viên chờ TA) | **5**<br>(Đo thời gian phản hồi) | **2**<br>(Làm RAG chuẩn mất nhiều thời gian gom data) | **5**<br>(Dễ so sánh Bot cứng / Workflow / Agent) | **4**<br>(Trải nghiệm học viên tốt, nhưng góc nhìn TA thì ít) | **31** |
| **2. Workflow trích xuất OCR hồ sơ** | **5**<br>(Kế toán, HCNS) | **5**<br>(Step-by-step duyệt rất rõ) | **4**<br>(Dựa trên kinh nghiệm thực tế của người đề xuất) | **5**<br>(Đo thời gian xử lý/hồ sơ) | **4**<br>(Dùng API OCR có sẵn nên làm khá nhanh) | **3**<br>(Nghiêng về Workflow tích hợp AI hơn là dùng sức mạnh Agent) | **4**<br>(1 người hiểu sâu, nhưng số đông chưa trải nghiệm) | **30** |
| **3. Gom luồng thông báo tập trung** | **5**<br>(Tất cả User) | **5**<br>(Từ App -> Webhook -> 1 nơi) | **4**<br>(Thường xuyên bị trôi tin nhắn làm lỡ việc) | **3**<br>(Khó quy ra số phút/giờ tiết kiệm cụ thể) | **5**<br>(Rất dễ, nối Zapier/Make là xong) | **2**<br>(Chỉ cần Workflow là giải quyết được, ép Agent vào bị gượng) | **5**<br>(Ai cũng hiểu nỗi đau này) | **29** |

### Kết luận: Quyết định của nhóm

**1. Nhóm chọn Candidate nào?**
 Nhóm quyết định chọn **Candidate 2: Workflow trích xuất & đối chiếu hồ sơ (OCR)**.

**2. Vì sao lại chọn Candidate này?**
- **Domain knowledge sâu sắc:** Nhóm có thành viên trực tiếp đưa ra vấn đề nên thấu hiểu rất rõ nghiệp vụ, các bước xử lý và cả những "góc khuất" (edge cases) của quy trình. Điều này đảm bảo việc thiết kế Workflow sẽ cực kỳ sát thực tế và tính khả thi cao.
- **Impact đo lường được ngay lập tức:** Nút thắt (bottleneck) "nhìn và gõ lại bằng mắt thường" là một nỗi đau nhức nhối có bằng chứng rõ ràng. Giải quyết được khâu này sẽ trả về con số tiết kiệm thời gian (giờ/hồ sơ) ngay tắp lự.
- **Khả năng demo Before/After thuyết phục:** Dễ dàng thiết kế một quy trình so sánh minh bạch giữa việc làm tay truyền thống và một Workflow tích hợp AI (OCR kết hợp LLM để bóc tách thông tin phức tạp), rất phù hợp để làm ra sản phẩm thực tế trong buổi lab.

**3. Vì sao KHÔNG nên chọn các bài khác?**
- ❌ **Đối với bài "AI Agent làm Virtual TA" (Candidate 1):** Dù tính năng Agent rất hấp dẫn nhưng rủi ro thất bại trong buổi lab là quá cao. Việc phải chuẩn bị dữ liệu (Knowledge Base) đủ sạch và đủ nhiều để RAG trả lời chính xác mà không bị "ảo giác" (hallucinate) là một thách thức lớn. Nếu bot trả lời sai kiến thức, hậu quả sẽ khá nghiêm trọng.
- ❌ **Đối với bài "Gom luồng thông báo" (Candidate 3):** Quá đơn giản. Vấn đề này hoàn toàn có thể được xử lý gọn gàng bằng các tool tự động hóa cơ bản (Rule/Workflow) như Make hay Zapier. Nếu áp dụng AI/Agent vào đây thì mang tính chất "dao mổ trâu giết gà", không tận dụng hết và không phô diễn được năng lực suy luận của hệ thống LLM.

**4. Nếu có disagreement (bất đồng quan điểm), nhóm xử lý thế nào?**
- **Bám sát tiêu chí chấm điểm (Data-driven):** Dùng lại bảng matrix điểm 1-5 ở trên làm mỏ neo. Khi tranh luận, mọi ý kiến phải dựa trên các con số thay vì cảm tính cá nhân.
- **Ưu tiên tính khả thi (Time-boxing):** Đặt câu hỏi thực tế *"Liệu có làm kịp ra sản phẩm demo trong thời gian buổi lab hôm nay không?"*. Ý tưởng hay đến mấy nhưng tốn quá nhiều thời gian setup data hoặc code thì bắt buộc phải hạ độ ưu tiên hoặc thu hẹp phạm vi (scope down).
- **Trọng tài Domain Knowledge:** Nếu hai ý tưởng có điểm bằng nhau, quyền quyết định cuối cùng (tie-breaker) sẽ nghiêng về ý tưởng mà nhóm có người hiểu thật sự sâu sắc (domain expert) nghiệp vụ đó nhất, để đảm bảo chất lượng workflow khi thiết kế.
- **Biểu quyết (Voting):** Sau khi đã đi qua 3 bước trên mà vẫn chưa chốt được, nhóm sẽ tiến hành vote theo nguyên tắc đa số thắng. Các thành viên thiểu số sẽ "cam kết" (commit) đồng lòng thực hiện cùng team để giữ vững tiến độ.

<!-- # 3.5 - Các giải pháp/ứng dụng công nghệ có sẵn (Không cần code từ đầu)

Để giải quyết bài toán OCR và đối chiếu hồ sơ một cách nhanh chóng trong buổi lab, nhóm đề xuất tận dụng phương pháp **Lắp ghép các công cụ có sẵn (No-code/Low-code)**. Dưới đây là các ứng dụng và dịch vụ nổi bật có thể ứng dụng ngay:

### 1. Nhóm API lõi trích xuất dữ liệu (OCR & Document AI)
Nhóm này làm nhiệm vụ "đọc hiểu" ảnh chụp và trả về dữ liệu văn bản đã được phân loại rõ ràng (Mã số thuế, Tổng tiền, Ngày tháng...).
- **Giải pháp nội địa (Rất mạnh cho form mẫu Tiếng Việt):** FPT.AI Reader, Viettel AI, VNPT Smart Vision, VNG Cloud OCR.
- **Giải pháp Big Tech quốc tế:** Google Cloud Document AI (rất giỏi đọc hóa đơn/biên lai), Microsoft Azure Document Intelligence (nhận diện bảng biểu xuất sắc), Amazon Textract, ABBYY Vantage.

### 2. Nhóm nền tảng tự động hóa (Workflow Automation)
Nhóm này đóng vai trò như "đường ống" nối các ứng dụng lại với nhau mà không cần viết code.
- **Make.com / Zapier / n8n:** Cho phép thiết lập luồng tự động (VD: Có file mới ở Google Drive -> Gọi API Google Vision đọc ảnh -> Ghi kết quả vào file Google Sheets).
- **Microsoft Power Automate:** Rất phù hợp nếu doanh nghiệp đang sử dụng hệ sinh thái Microsoft 365.

### 3. Nhóm giải pháp SaaS trọn gói (End-to-End Invoice/Document Processing)
Nếu doanh nghiệp cần "mua đứt" một phần mềm làm từ A-Z (có sẵn cả chức năng OCR và luồng phê duyệt):
- **Bizzi.vn:** Nền tảng số 1 tại Việt Nam chuyên tự động xử lý, trích xuất và kiểm tra tính hợp lệ của hóa đơn điện tử.
- **Ubot Invoice (FPT akaBot):** Kết hợp Robot tự động hóa (RPA) và OCR để tự tải hóa đơn từ email, đọc dữ liệu rồi nhập thẳng vào phần mềm kế toán (MISA, FAST, SAP).
- **Base.vn (Base Workflow / Base Request):** Ứng dụng số hóa quy trình và phê duyệt đề xuất cực kỳ phổ biến ở Việt Nam, có thể kết nối với các API OCR thông qua Webhook. -->

# 4.1 Quick validation
# 4.2 Research giải pháp đã có
| Nguồn / tool / case | Link | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|:---|:---|:---|:---|:---|:---|
| **Bizzi.vn**<br>(SaaS xử lý hóa đơn tự động) | [bizzi.vn](https://bizzi.vn/) | Giải quyết trọn gói từ khâu nhận file (email/upload) -> OCR trích xuất -> Đối chiếu tính hợp lệ của hóa đơn với cơ quan thuế -> Chuyển vào ERP. | Cực kỳ am hiểu hóa đơn Việt Nam, xử lý end-to-end hoàn thiện, không cần người dùng tự cấu hình kỹ thuật. | Đóng gói sẵn (Blackbox), khó tuỳ biến nếu hồ sơ, giấy tờ của công ty là loại đặc thù riêng (phi tiêu chuẩn). | Cần xây dựng luồng phê duyệt rõ ràng giống Bizzi. Nhận ra rằng bài toán không chỉ dừng ở việc "đọc chữ" mà phải "hiểu và đối chiếu" dữ liệu. |
| **Google Cloud Document AI**<br>(API Trích xuất lõi) | [cloud.google.com/document-ai](https://cloud.google.com/document-ai) | Tập trung vào bước lõi (Core): Dùng AI trích xuất dữ liệu từ PDF/Ảnh thành JSON có cấu trúc (nhận diện form, key-value, table). | Model AI cực mạnh, nhận diện cấu trúc bảng biểu phức tạp rất tốt, độ chính xác cao kể cả với bản scan mờ. | Chỉ cung cấp API xử lý dữ liệu. Chưa có giao diện luồng (workflow) luân chuyển tài liệu giữa các phòng ban (cần dùng tool khác ráp vào). | Không nên cố tự train mô hình OCR từ đầu vì rất tốn kém và khó bằng Big Tech. Nên tận dụng API có sẵn này và tập trung vào việc ráp nối Workflow. |
| **FPT.AI Reader**<br>(Giải pháp OCR nội địa) | [fpt.ai/vi/fpt-ai-reader](https://fpt.ai/vi/fpt-ai-reader) | Trích xuất thông tin giấy tờ tùy thân (CCCD) và các loại chứng từ, hóa đơn đỏ nội địa đặc thù của Việt Nam. | Đọc Tiếng Việt xuất sắc, đáp ứng chuẩn bảo mật trong nước, hỗ trợ kỹ thuật sát sao tại local. | Yêu cầu đội ngũ IT nội bộ để tích hợp API vào hệ thống quản lý hoặc ERP cũ của công ty. | Tiếng Việt có dấu rất phức tạp. Việc chọn công cụ lõi OCR phải ưu tiên công cụ hiểu tốt ngữ cảnh Tiếng Việt và các form mẫu đặc thù trong nước. |

# 5. Đóng góp của tôi trong nhóm

Dựa trên quá trình thảo luận và định hướng làm bài, dưới đây là tổng hợp đóng góp cá nhân của **Hoàng Đức Dũng**:

| Hoạt động | Dũng đã làm gì? | Kết quả |
| :--- | :--- | :--- |
| **Scan cá nhân** | Đưa ra 3 problems thực tế về mảng Back-office (OCR hồ sơ công tác phí, dịch vụ công, QA âm thanh). | Nhóm có được các candidate rất sát với thực tiễn doanh nghiệp, impact đo lường được ngay. |
| **Pitch** | Thuyết phục và định hướng nhóm tập trung vào Candidate 2: "Workflow trích xuất OCR hồ sơ". | Bài toán OCR được vào shortlist và cuối cùng được nhóm vote chọn làm giải pháp chính thức. |
| **Challenge** | Đề xuất bổ sung phần "Quy tắc xử lý disagreement" và thúc đẩy chấm điểm rõ ràng (Scoring). | Nhóm ra quyết định dựa trên data (data-driven) và tính khả thi (time-boxing) thay vì cảm tính. |
| **Research** | Khảo sát các công nghệ có sẵn (Bizzi.vn, Google Cloud Document AI, FPT.AI Reader). | Giúp nhóm thay đổi tư duy: Dùng công cụ lắp ghép (No-code) thay vì tốn thời gian build model từ đầu. |
| **Rule / Workflow / Agent** | Lập luận ưu tiên Workflow OCR, chỉ ra rủi ro fail lab của Agent (Virtual TA) và bàn lùi việc lạm dụng Agent cho báo cáo (Candidate 3). | Nhóm thống nhất decision cuối cùng, không rơi vào bẫy "dùng dao mổ trâu giết gà", chọn hướng đi thực tế nhất. |


