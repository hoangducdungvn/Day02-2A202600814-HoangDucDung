# Phase 3 — Group Problem Statement

## Group convergence

## Bước 3.1 — Trình bày top 3

| # | Người đưa ra | Candidate problem | Người gặp vấn đề | Điểm nghẽn (Bottleneck) | Cảm nhận nhanh (Quick gut) |
|:---|:---|:---|:---|:---|:---|
| 1 | [Đoàn Công Phú] | Tài liệu học tập mở quá sát giờ học nên không kịp ôn trước. | Học viên | Không có đủ thời gian để đọc trước, dẫn đến không theo kịp tốc độ bài giảng. | Quy trình (Process fix) |
| 2 | [Đoàn Công Phú] | Học viên trái ngành không load kịp kiến thức khi học lab buổi chiều do lượng kiến thức tăng quá nhanh. | Học viên trái ngành | Bị choáng ngợp thông tin, tốc độ nạp kiến thức chậm hơn tốc độ dạy. | AI Agent (Tutor cá nhân) |
| 3 | [Đoàn Công Phú] | Không có AI tutor hỗ trợ recap kiến thức nền hoặc giải thích nhanh thuật ngữ. | Học viên | Tốn thời gian tự tra cứu thủ công, dễ hiểu sai lệch thuật ngữ chuyên môn. | RAG Agent |
| 4 | [Vũ Quang Vinh] | Học viên nhiều nhưng trợ giảng ít dẫn đến việc thắc mắc nhưng không được giải đáp kịp thời. | Học viên | Thời gian chờ đợi TA quá lâu gây "đóng băng" tiến độ thực hành code. | Agent (Virtual TA) |
| 5 | [Vũ Quang Vinh] | Các học viên đều có thắc mắc giống nhau (cài đặt môi trường, hỏi đường...). | Trợ giảng (TA) | Trợ giảng bị quá tải, phải lặp lại thao tác copy/paste câu trả lời như một cái máy. | Agent / Rule-based FAQ |
| 6 | [Vũ Quang Vinh] | Khó nắm bắt được các thông tin do có quá nhiều kênh thông báo (Zalo, Teams, Discord). | Học viên | Phải lướt dò thủ công nhiều app, dễ trôi tin và lỡ deadline quan trọng. | Workflow + AI (Gom luồng) |
| 7 | [Hoàng Đức Dũng] | Xử lý hồ sơ hoàn tiền công tác phí chậm và tốn công. | Kế toán / Hành chính | Khâu đối chiếu hóa đơn với quy chế công ty phải làm hoàn toàn bằng mắt thường. | AI Workflow (OCR + LLM) |
| 8 | [Hoàng Đức Dũng] | Trích xuất và kiểm duyệt hồ sơ dịch vụ công tốn nhiều thời gian. | Nhân viên xử lý hồ sơ | Phải gõ lại dữ liệu thủ công từ các form giấy tờ cũ, dễ bị mờ/nhòe. | Workflow (OCR) |
| 9 | [Hoàng Đức Dũng] | Đánh giá chất lượng cuộc gọi CSKH chỉ đạt tỷ lệ rất thấp (dưới 5%). | QA / Quản lý CSKH | Phải nghe lại từng file ghi âm thủ công, không đủ sức người để cover 100% cuộc gọi. | AI (Speech-to-Text) |

## Bước 3.2 — Gom trùng / cluster

| Cluster | Candidate examples | Pattern chung |
| :--- | :--- | :--- |
| Hỗ trợ học tập | #3 AI tutor recap thuật ngữ, #4 Virtual TA, #5 FAQ cho câu hỏi lặp lại | Học viên cần giải đáp nhanh trong lúc học/lab nhưng mentor/TA không đủ thời gian để trả lời lặp lại. |
| Tiếp thu kiến thức | #1 Tài liệu mở sát giờ, #2 Học viên trái ngành không load kịp | Tốc độ nạp kiến thức của học viên chậm hơn tốc độ cung cấp tài liệu/độ khó bài lab. |
| Giao tiếp & thông báo | #6 Gom thông tin từ Zalo, Teams, Discord | Thông tin nằm rải rác nhiều kênh khiến học viên phải tự lọc deadline và việc cần làm. |
| Vận hành B2B | #7 Hoàn tiền công tác phí, #8 Hồ sơ dịch vụ công, #9 QA cuộc gọi CSKH | Nhân sự vận hành phải xử lý dữ liệu phi cấu trúc bằng mắt/tai/tay, tốn thời gian và khó mở rộng coverage. |

## Bước 3.3 — Shortlist và score

Chấm 1-5 theo từng candidate cụ thể. Cluster chỉ dùng để gom ý; quyết định cuối chọn một candidate đủ rõ để đào sâu.

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
| :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| #9 — Đánh giá chất lượng cuộc gọi CSKH chỉ đạt tỷ lệ rất thấp, QA phải nghe file ghi âm thủ công | 5 | 5 | 5 | 5 | 4 | 5 | 4 | 33 |
| #4 — Học viên nhiều nhưng trợ giảng ít, thắc mắc không được giải đáp kịp thời | 5 | 5 | 4 | 4 | 5 | 5 | 4 | 32 |
| #7 — Xử lý hồ sơ hoàn tiền công tác phí chậm và tốn công | 5 | 5 | 3 | 5 | 4 | 5 | 3 | 30 |
| #3 — Không có AI tutor hỗ trợ recap kiến thức nền hoặc giải thích thuật ngữ | 4 | 4 | 4 | 4 | 5 | 5 | 4 | 30 |
| #6 — Khó nắm bắt thông tin do có quá nhiều kênh thông báo | 5 | 4 | 3 | 4 | 4 | 5 | 4 | 29 |

Nhóm chọn: **#9 — Đánh giá chất lượng cuộc gọi CSKH**.

Vì sao chọn:

```text
Candidate #9 có tổng điểm cao nhất và ít bị trùng với các bài toán học tập/Virtual TA phổ biến. Đây là bài toán business rõ: actor cụ thể là QA/quản lý CSKH, bottleneck nằm đúng ở bước nghe lại và chấm từng cuộc gọi thủ công, impact đo được bằng tỷ lệ cuộc gọi được QA, thời gian chấm mỗi cuộc gọi, điểm compliance và số lỗi được phát hiện.

Về AI, candidate này có AI-fit mạnh nhưng vẫn kiểm soát được: Rule kiểm tra script/compliance cố định, Workflow dùng speech-to-text + scoring rubric, Agent có thể là hướng mở rộng sau để đề xuất coaching. Trong lab hôm nay có thể prototype bằng transcript mẫu thay vì xử lý audio thật, nên vừa đủ khả thi.
```

Vì sao không chọn các candidate còn lại:

```text
#4 Impact cần đo qua hành vi học viên và adoption, không trực tiếp ra KPI vận hành như QA cuộc gọi.

#7 có ROI rõ nhưng cần quy chế công tác phí và hóa đơn mẫu đủ thật. Nếu thiếu dữ liệu, bài toán dễ biến thành demo OCR chung chung.

#3 gần với #4 và thuộc nhóm AI tutor, dễ bị trùng hướng với nhiều nhóm. Scope cũng dễ phình thành trợ lý học tập tổng quát.

#6 phù hợp automation nhưng phụ thuộc quyền truy cập nhiều kênh chat. Nếu chỉ dùng dữ liệu giả lập, phần business impact yếu hơn #9.
```

Nếu có disagreement, nhóm xử lý thế nào:

```text
Nhóm dùng điểm số làm cơ sở, sau đó áp dụng tie-break business: ưu tiên candidate ít trùng, có KPI vận hành rõ, có before/after workflow cụ thể và prototype được trong lab. Vì vậy chọn #9 thay vì các bài toán học tập dù nhóm cũng hiểu domain học tập tốt.
```

---

# Phase 4 — Quick Validation + Research giải pháp

## Bước 4.1 — Quick validation

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
| :--- | ---: | :--- | :--- | :--- |
| Candidate evidence | 1 candidate #9 | Problem nêu rõ QA chỉ đánh giá được tỷ lệ rất thấp, dưới 5%, vì phải nghe lại từng file ghi âm thủ công. Đây là tín hiệu pain đủ mạnh để shortlist. | Chưa có log thật về số cuộc gọi/ngày, thời lượng cuộc gọi trung bình, thời gian QA/call và rubric QA hiện tại. | Giữ problem, nhưng giới hạn pilot ở "chấm transcript cuộc gọi theo rubric" thay vì làm toàn bộ hệ thống contact center. |
| Quick interview đề xuất | 1 QA lead + 1 supervisor + 1 agent | Cần hỏi: mỗi ngày có bao nhiêu cuộc gọi, QA nghe bao nhiêu cuộc, mất bao lâu/call, lỗi nào cần phát hiện, rubric đang gồm những tiêu chí nào. | Nếu volume cuộc gọi thấp hoặc QA thủ công đã đủ cover, AI không tạo nhiều ROI. | Chỉ tiếp tục nếu có volume đủ lớn và QA coverage hiện tại thật sự thấp. |
| Micro sample đề xuất | 10-20 transcript hoặc recording mẫu | Có thể kiểm tra AI chấm được các tiêu chí cơ bản như chào hỏi, xác minh thông tin, tư vấn đúng quy trình, thái độ, kết thúc cuộc gọi. | Nếu transcript quá nhiễu, thiếu speaker diarization, hoặc rubric quá mơ hồ, kết quả AI sẽ khó tin. | Bắt đầu bằng transcript sạch, rubric ngắn 5-7 tiêu chí, có QA review lại. |
| Log / vận hành cần thu thập | 1 tuần dữ liệu QA | Cần đo baseline: số cuộc gọi phát sinh, tỷ lệ được QA, thời gian chấm/call, lỗi compliance phát hiện, số coaching action. | Nếu không có quyền dùng recording vì privacy/compliance, phải dùng dữ liệu ẩn danh hoặc transcript giả lập. | Thêm boundary: ẩn thông tin cá nhân, chỉ dùng transcript đã được phép, QA là người duyệt cuối. |

Kết luận validation nhanh:

```text
Pain có logic business mạnh vì QA thủ công thường bị giới hạn bởi thời gian nghe lại cuộc gọi. Tuy nhiên, nhóm chưa được xem dữ liệu thật nên cần validate bằng 10-20 transcript/recording mẫu và rubric QA cụ thể trước khi kết luận rollout.
```

## Bước 4.2 — Research giải pháp đã có

| Nguồn / tool / case | Link | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Amazon Connect Contact Lens | [aws.amazon.com/connect/contact-lens](https://aws.amazon.com/connect/contact-lens) | Phân tích hội thoại contact center, transcript, sentiment, contact drivers, performance evaluation và generative AI summary. | Cho thấy use case QA tự động trên contact center là bài toán thị trường thật, không phải ý tưởng tưởng tượng. | Gắn với hệ sinh thái Amazon Connect; triển khai thật cần tích hợp dữ liệu, quyền truy cập và privacy. | Prototype nên tập trung vào transcript + rubric + QA review trước, chưa cần tích hợp platform. |
| Google Cloud Conversational Insights / Quality AI | [cloud.google.com/contact-center/insights/docs/qai-overview](https://cloud.google.com/contact-center/insights/docs/qai-overview) | Dùng scorecard để đánh giá chất lượng cuộc trò chuyện và hiệu suất agent. | Nhấn mạnh cần scorecard/rubric rõ, dữ liệu conversation và hướng dẫn chấm cụ thể. | Nếu rubric mơ hồ thì AI và người đều khó chấm nhất quán. | Trước khi dùng AI phải chuẩn hóa rubric: tiêu chí, thang điểm, ví dụ pass/fail. |
| Observe.AI Quality Assurance | [observe.ai](https://www.observe.ai/post-interaction/contact-center-manual-qa) | Hỗ trợ QA contact center, evaluation form, assignments, calibration, auto QA và coaching. | Mạnh ở workflow hậu kiểm: chấm, phân công QA, calibration và coaching agent. | Có thể quá đầy đủ so với scope lab; nếu copy toàn bộ sẽ quá rộng. | Chỉ lấy pattern: auto-score trước, QA review sau, dùng kết quả để coaching. |
| CallMiner Conversation Analytics | [callminer.com](https://callminer.com/conversation-analytics/call-center-analytics) | Phân tích hội thoại bằng speech analytics/NLP, theo dõi quality, compliance, sentiment, agent behavior. | Xác nhận các metric như compliance, agent behavior, sentiment và SLA là các output có giá trị. | Phân tích sentiment/behavior có thể gây tranh cãi nếu không có bằng chứng rõ trong transcript. | Trong pilot chỉ chấm tiêu chí quan sát được từ transcript, tránh kết luận cảm xúc quá sâu. |

Kết luận research:

```text
Thị trường đã có các pattern rõ cho automated QA trong contact center: speech-to-text, transcript analytics, scorecard, auto-evaluation, human review và coaching. Với phạm vi lab, nhóm nên làm workflow nhỏ bằng transcript mẫu + rubric, chưa làm tích hợp call center thật.
```

---

# Phase 5 — Workflow + Problem Statement

## Bước 5.1 — Current workflow bản nhóm


```text
CURRENT STATE — 6 bước, ~55 phút / 1 cuộc gọi được QA

+----------------------+     +----------------------+     +----------------------+
| Bước 1               |     | Bước 2               |     | Bước 3               |
| Cuộc gọi phát sinh   | --> | Chọn sample nhỏ      | --> | Nghe lại recording   |
|                      |     | để QA                |     | gần như toàn bộ      |
| Ai: Hệ thống/Agent   |     | Ai: QA/Supervisor    |     | Ai: QA               |
| ⏱ 1'                 |     | ⏱ 5'                 |     | ⏱ 20' 🔴             |
| In: cuộc gọi         |     | In: danh sách call   |     | In: file ghi âm      |
| Out: recording       |     | Out: call được chọn  |     | Out: ghi chú thô     |
+----------------------+     +----------------------+     +----------------------+
                                                                  |
                                                                  v
+----------------------+     +----------------------+     +----------------------+
| Bước 6               |     | Bước 5               |     | Bước 4               |
| Feedback/coaching    | <-- | Tổng hợp báo cáo     | <-- | Chấm điểm rubric     |
| cho agent            |     | QA thủ công          |     | + ghi lỗi            |
| Ai: QA/Supervisor    |     | Ai: QA/Supervisor    |     | Ai: QA               |
| ⏱ 10'                |     | ⏱ 10'                |     | ⏱ 9'                 |
| In: report           |     | In: điểm từng call   |     | In: ghi chú thô      |
| Out: coaching note   |     | Out: QA report       |     | Out: điểm QA         |
+----------------------+     +----------------------+     +----------------------+

🔴 = Bottleneck        ⏱ Tổng: ~55 phút/call được QA
Bottleneck: QA phải nghe và chấm thủ công từng file, nên coverage thấp và feedback chậm.
```

| Bước | Actor | Input | Output | Thời gian/tần suất | Ghi chú |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Agent CSKH / hệ thống tổng đài | Cuộc gọi khách hàng | File ghi âm + metadata cuộc gọi | Hằng ngày, volume lớn | Đây là nguồn dữ liệu thô. |
| 2 | QA / supervisor | Danh sách cuộc gọi | Chọn một mẫu nhỏ để kiểm tra | Thường chỉ kiểm được tỷ lệ thấp | Candidate nêu coverage dưới 5%. |
| 3 | QA | File ghi âm | Nghe và ghi chú thủ công | Ước lượng 10-30 phút/call tùy độ dài | Bottleneck chính nằm ở bước nghe và ghi chú. |
| 4 | QA | Ghi chú + rubric | Điểm QA theo tiêu chí | Lặp lại từng cuộc gọi | Dễ thiếu nhất quán giữa các QA nếu rubric không rõ. |
| 5 | QA / supervisor | Điểm QA | Báo cáo lỗi, feedback, coaching | Theo ngày/tuần | Feedback đến agent bị trễ. |
| 6 | Quản lý CSKH | Báo cáo QA mẫu nhỏ | Quyết định coaching/cải thiện quy trình | Theo kỳ báo cáo | Vì sample thấp nên nhiều rủi ro compliance/quality không được phát hiện. |

Bottleneck chính:

```text
Bottleneck nằm ở bước QA phải nghe và chấm từng cuộc gọi thủ công. Đây là bước tốn thời gian tuyến tính theo số cuộc gọi, khiến tỷ lệ kiểm tra thấp và feedback cho agent bị chậm.
```

## Bước 5.2 — Future workflow bản nhóm


```text
FUTURE STATE — 6 bước, ~18 phút / 1 cuộc gọi cần QA review

+----------------------+     +----------------------+     +----------------------+
| Bước 1               |     | Bước 2               |     | Bước 3               |
| Auto-transcribe      | --> | Rule/script check    | --> | AI chấm rubric       |
| audio -> transcript  |     | compliance cơ bản    |     | + trích evidence     |
| 🔵 Workflow step     |     | 🔵 Rule/script       |     | 🔵 Workflow step     |
| ⏱ 2'                 |     | ⏱ 1'                 |     | ⏱ 3'                 |
| In: recording        |     | In: transcript       |     | In: transcript       |
| Out: transcript      |     | Out: rule flags      |     | Out: score + quote   |
+----------------------+     +----------------------+     +----------------------+
                                                                  |
                                                                  v
+----------------------+     +----------------------+     +----------------------+
| Bước 6               |     | Bước 5               |     | Bước 4               |
| Feedback/coaching    | <-- | Tổng hợp insight     | <-- | QA review case       |
| cho agent            |     | lỗi phổ biến         |     | fail/low confidence |
| 🟢 Human             |     | 🔵 Workflow step     |     | 🟢 Human boundary   |
| ⏱ 3'                 |     | ⏱ 2'                 |     | ⏱ 7'                |
| In: report final     |     | In: score đã duyệt   |     | In: score + quote   |
| Out: coaching note   |     | Out: dashboard       |     | Out: score final    |
+----------------------+     +----------------------+     +----------------------+

🔵 = AI/Rule xử lý      🟢 = Human boundary      ⏱ Tổng: ~18 phút/call cần review
Fallback: AI score thấp / transcript lỗi / compliance nghiêm trọng -> QA nghe lại recording gốc và tự chấm.
Bottleneck mới: QA lead/supervisor cần giữ rubric rõ và audit sample để tránh AI chấm sai có hệ thống.
```

Before/after impact:

| Metric | Trước | Sau kỳ vọng | Ghi chú |
| :--- | ---: | ---: | :--- |
| Tỷ lệ cuộc gọi được QA | Dưới 5% theo candidate | 50-100% được AI pre-screen trong pilot dữ liệu mẫu | QA vẫn review các case rủi ro, không cần nghe toàn bộ. |
| Thời gian QA thủ công/call | Ước lượng 10-30 phút | 3-7 phút cho case cần review | AI chuẩn bị transcript, điểm gợi ý và evidence. |
| Số bước thủ công của QA | 5-6 bước | 2-3 bước | QA chuyển từ nghe toàn bộ sang kiểm chứng điểm và bằng chứng. |
| Lỗi compliance/script bị bỏ sót | Chưa đo | Giảm nhờ quét toàn bộ transcript | Cần so sánh với QA người trên sample chuẩn. |
| Tốc độ feedback cho agent | Theo ngày/tuần | Gần real-time hoặc cuối ngày | Phụ thuộc tích hợp hệ thống thật. |
| Risk mới | QA chậm nhưng người kiểm soát trực tiếp | AI chấm sai, bias, hiểu nhầm transcript | Giảm bằng rubric rõ, confidence, human review, audit sample. |

## Bước 5.3 — Problem Statement v0

| Field | Nội dung |
| :--- | :--- |
| **Actor** | QA / quản lý CSKH cần kiểm tra chất lượng cuộc gọi; agent CSKH là người nhận feedback. |
| **Workflow** | Mỗi ngày phát sinh nhiều cuộc gọi, QA chọn một mẫu nhỏ, nghe lại recording, ghi chú, chấm theo rubric, tổng hợp lỗi và feedback cho agent. |
| **Bottleneck** | Bước nghe lại và chấm từng cuộc gọi thủ công tốn nhiều thời gian nên chỉ kiểm tra được tỷ lệ rất thấp. |
| **Impact** | Nhiều cuộc gọi không được kiểm tra, lỗi compliance/script có thể bị bỏ sót, feedback cho agent chậm, quản lý thiếu dữ liệu để coaching và cải thiện chất lượng dịch vụ. |
| **Success Metric** | Tăng tỷ lệ cuộc gọi được pre-screen từ dưới 5% lên ít nhất 50% trong pilot; giảm thời gian QA thủ công/call; phát hiện được lỗi script/compliance phổ biến; QA đánh giá độ hữu ích của AI score >= 4/5. |
| **Boundary** | Pilot chỉ dùng transcript/recording đã được phép và ẩn thông tin cá nhân; chỉ chấm 5-7 tiêu chí rubric rõ; AI không tự đưa ra quyết định kỷ luật hoặc đánh giá cuối cùng. |

Điểm còn cần kiểm ở v0:

```text
Baseline cần kiểm: số cuộc gọi/ngày, thời lượng trung bình, thời gian QA/call, rubric hiện tại, và tỷ lệ QA coverage thực tế. Nếu không có dữ liệu thật, pilot chỉ nên coi là proof-of-concept.
```

---

# Phase 6 — Rule / Workflow / Agent + Decision

## Bước 6.0 — Ma trận độ phù hợp với AI

Bài toán của nhóm nằm ở ô nào?

```text
Độ mơ hồ trung bình, độ phức tạp trung bình-cao.
```

Vì sao?

```text
Một phần tiêu chí QA là rõ ràng và có thể rule-based, ví dụ có chào hỏi, có xác minh thông tin, có nói câu compliance bắt buộc hay không. Nhưng các tiêu chí như thái độ, mức độ giải quyết vấn đề, nguyên nhân khiếu nại cần hiểu ngữ cảnh transcript, nên cần AI hỗ trợ. Workflow gồm nhiều bước nối tiếp: transcribe, rule check, chấm rubric, trích evidence, QA review, tổng hợp insight. Vì vậy phù hợp nhất là Workflow, chưa cần Agent tự quyết định nhiều bước.
```

## Bước 6.1 — So sánh Rule / Workflow / Agent

| Mức | Phương án cho bài toán nhóm | Khi nào đủ | Rủi ro | Chọn? |
| :--- | :--- | :--- | :--- | :--- |
| **Rule** | Keyword/script checker: kiểm có câu chào, xác minh thông tin, từ khóa cấm, câu compliance bắt buộc. | Đủ cho tiêu chí đúng/sai rõ ràng và ít phụ thuộc ngữ cảnh. | Bỏ sót khi agent diễn đạt khác keyword; không đánh giá được resolution, thái độ, nguyên nhân khiếu nại. | Dùng như một lớp trong workflow, không chọn độc lập. |
| **Workflow** | STT hoặc transcript input -> rule check -> LLM chấm rubric -> trích evidence -> gắn confidence -> QA review case rủi ro -> dashboard insight. | Đủ cho pilot với 10-20 transcript và rubric 5-7 tiêu chí. | Phụ thuộc chất lượng transcript và rubric; AI có thể chấm sai nếu tiêu chí mơ hồ. | **Chọn cho pilot.** |
| **Agent** | Agent tự lấy call từ hệ thống, đối chiếu CRM, mở ticket coaching, đề xuất action plan cho từng agent, theo dõi cải thiện sau training. | Hữu ích khi đã tích hợp tổng đài/CRM/LMS và có owner vận hành. | Quá rộng, nhiều rủi ro privacy/compliance, khó kiểm soát quyết định tự động. | Chưa chọn; để roadmap sau khi workflow chứng minh hiệu quả. |

Mức chọn:

```text
Workflow
```

Vì sao chọn:

```text
Workflow giải đúng bottleneck chính: giảm thời gian nghe và chấm thủ công bằng cách AI chuẩn bị transcript, điểm gợi ý và bằng chứng. QA vẫn là người duyệt cuối nên rủi ro thấp hơn Agent. Workflow cũng dễ đo bằng coverage, thời gian QA/call, tỷ lệ AI score được QA chấp nhận và số lỗi compliance phát hiện.
```

Vì sao không chọn mức đơn giản hơn:

```text
Rule chỉ xử lý được các tiêu chí cứng như keyword hoặc script bắt buộc. QA cuộc gọi cần đọc ngữ cảnh: khách hàng hỏi gì, agent có giải quyết đúng chưa, agent có làm khách hàng hiểu nhầm không. Vì vậy cần LLM trong workflow để chấm rubric kèm evidence.
```

Vì sao chưa chọn Agent:

```text
Agent chưa cần thiết vì pilot chưa tích hợp tổng đài, CRM, ticket coaching hoặc hệ thống nhân sự. Cho AI tự tạo action/kỷ luật agent là rủi ro cao. Trước mắt chỉ để AI pre-score và QA review.
```

## Bước 6.2 — Problem Statement v1

| Field | Nội dung |
| :--- | :--- |
| **Actor** | QA / quản lý CSKH cần kiểm tra chất lượng cuộc gọi; agent CSKH nhận feedback/coaching. |
| **Workflow** | Mỗi ngày có nhiều cuộc gọi CSKH, QA chỉ nghe được một mẫu nhỏ, chấm thủ công theo rubric rồi tổng hợp lỗi và feedback. |
| **Bottleneck** | Nghe lại recording và chấm từng cuộc gọi là bước tốn thời gian nhất, khiến QA coverage thấp và feedback chậm. |
| **Impact** | Lỗi compliance/script có thể bị bỏ sót; chất lượng tư vấn không được theo dõi đủ rộng; quản lý thiếu dữ liệu để coaching agent và cải thiện quy trình. |
| **Success Metric** | Pilot với 10-20 transcript: AI pre-screen được 100% mẫu; QA chỉ cần review case fail/low confidence; giảm ít nhất 50% thời gian chấm/call trên sample; AI score được QA chấp nhận >= 80%; QA đánh giá insight hữu ích >= 4/5. |
| **Boundary** | Không dùng dữ liệu có PII chưa ẩn danh. Không tự ra quyết định kỷ luật/thưởng phạt. Không chấm tiêu chí cảm xúc nếu không có bằng chứng trong transcript. Không thay QA final review. |
| **AI intervention point** | Sau khi có transcript: AI kiểm rule, chấm rubric, trích evidence, gắn confidence, flag cuộc gọi rủi ro và tổng hợp lỗi phổ biến cho QA. |
| **Mức chọn** | Workflow: STT/transcript + rule check + LLM scorecard + human review. |
| **Rủi ro & người thật kiểm tra** | Rủi ro chính là transcript sai, rubric mơ hồ, AI chấm sai hoặc bias. QA/supervisor review case fail/low confidence, audit ngẫu nhiên case pass, và cập nhật rubric sau mỗi vòng pilot. |

## Bước 6.3 — Final decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú |
| :--- | :--- | :--- |
| Actor và workflow đã rõ chưa? | Yes | Actor chính là QA/quản lý CSKH; workflow thủ công và workflow sau tối ưu đã rõ. |
| Baseline và success metric đã đo được chưa? | Not Yet | Có baseline định tính "dưới 5%" từ candidate, nhưng cần số liệu thật về volume, thời gian QA/call và rubric hiện tại. |
| Có data/input đủ dùng chưa? | Not Yet | Cần 10-20 transcript hoặc recording đã ẩn danh, cộng với rubric QA 5-7 tiêu chí. |
| Nếu AI sai, hậu quả có chấp nhận được không? | Yes, nếu có human review | AI chỉ pre-score; QA duyệt cuối. Không dùng AI để tự động kỷ luật hoặc thưởng phạt agent. |
| Có người review/owner vận hành không? | Yes | QA lead/supervisor là owner rubric, review output và calibration. |
| Có cách non-AI đơn giản hơn không? | Yes | Có thể cải thiện bằng sampling tốt hơn, checklist/rubric rõ hơn, calibration QA. Nhưng non-AI không mở rộng coverage tốt bằng workflow AI. |

Decision:

```text
Go cho pilot nhỏ bằng transcript mẫu; Not Yet cho rollout production nếu chưa có dữ liệu thật, rubric chuẩn và quy trình privacy.
```

Lý do:

```text
Candidate #9 đáng chọn vì ít trùng, có KPI vận hành rõ, AI intervention nằm đúng bottleneck và có thể prototype trong lab bằng transcript. Tuy nhiên, đây là bài toán có rủi ro compliance/nhân sự nên chỉ Go ở mức pilot có human review, chưa Go cho tự động hóa hoàn toàn.
```

Nếu Go, pilot nhỏ nhất là:

```text
Làm AI QA prototype cho 10-20 transcript cuộc gọi CSKH:
1. Input: transcript ẩn danh, metadata tối thiểu, rubric QA 5-7 tiêu chí.
2. AI output: điểm từng tiêu chí, pass/fail, evidence quote, confidence, lý do cần QA review.
3. Human review: QA so sánh AI score với điểm người chấm.
4. Đo: thời gian chấm/call, tỷ lệ AI score được QA chấp nhận, số lỗi phát hiện, mức hữu ích 1-5.
```

Nếu Not Yet, cần validate gì trước:

```text
Trước rollout cần validate: quyền dùng dữ liệu cuộc gọi, quy trình ẩn danh PII, rubric QA đủ rõ, transcript quality, baseline QA coverage, và mức đồng thuận giữa QA người với AI score.
```

Nếu No-Go, nên làm gì thay AI:

```text
Nếu không có quyền dùng dữ liệu hoặc rubric chưa ổn, làm non-AI trước: chuẩn hóa scorecard, sampling theo rủi ro, checklist compliance, calibration giữa các QA và template feedback cho agent.
```