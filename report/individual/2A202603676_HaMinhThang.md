# Báo cáo cá nhân — MSSV_HoTen

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Hà Minh Thắng 
- MSSV: 2A202603676
- Email trường (không bắt buộc, repo có thể để public): 26ai.thanghm@vinuni.edu.vn
- Tên nhóm: ABC
- Link repo nhóm: https://github.com/manhkhai205/K5-L3A-Day02-ABC-DiscoveryProblemFraming.git

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 |Lặp lại |Khi các bác sĩ trực cấp cứu kết thúc ca trực, tôi muốn có báo cáo tình hình bệnh nhân để có thể giám sát, đưa ra quyết định tiếp theo đối với bệnh nhân  |Bác sĩ cấp cứu, y tá trực |Sau mỗi ca, các bác sĩ thường phải ở lại khoảng 30p để bàn giao công việc. |
| 2 |Chỉ cần đọc, tổng hợp nhiều thông tin |Khi có cuộc họp hàng tháng (hàng quý), tôi muốn tổng hợp được thành một bản số liệu gửi tới BLĐ bệnh viện để tổng kết truy thu quỹ bảo hiểm y tế |Kế toán |Tra cứu thông tin gây nguy cơ sai sót và tốn thời gian thao tác |
| 3 |Chỉ cần đọc, tổng hợp nhiều thông tin |Khi tôi là một bác sĩ ngoại khoa có quá nhiều ca mổ trong tuần, tôi muốn có thể tự động lập một thời gian biểu và nhắc tôi khi gần tới ngày thực hiện |Bác sĩ ngoại khoa |Bệnh nhân trở nặng và không kịp sắp xếp ca mổ |
| 4 |Tốn thời gian |Khi mà đầu tháng trưởng khoa, giám đốc bệnh viện muốn có một bản báo cáo về tình hình khám chữa bệnh, doanh thu, tồn kho,... của tháng trước |Kế hoạch tổng hợp, IT bệnh viện |Mỗi tháng cần khoảng 3-4 tiếng để tổng hợp từ các phòng ban liên quan |
| 5 |Lặp lại |Khi lấy xe ở bãi đỗ xe bệnh viện, tôi muốn tăng tốc độ lấy xe và giảm nguy cơ thất lạc xe |Bảo vệ, bệnh nhân |Có những trường hợp mất vé xe, thẻ xe khi thăm bệnh |
| 6 |Tốn thời gian |Khi mà bàn giao công việc cho nhân viên khác, tôi muốn có thể tổng hợp được tất cả các việc tôi đã và chưa hoàn thành trong giai đoạn đó cho nhân viên đó |Nhân viên chuẩn bị nghỉ |Sau khi nghỉ vẫn bị gọi tới để hỏi về công việc đã bàn giao vì họ chưa hiểu, chưa rõ |
| 7 |Pain từ người khác |Khi developer nhận yêu cầu từ bộ phận triển khai, họ muốn tóm tắt được mục đích, vai trò, sự cần thiết của chức năng mới đó với người dùng để đánh giá sự ưu tiên phát triển |Developer |Giao quá nhiều task, developer chỉ chọn các chức năng dễ, không ưu tiên phát triển tính năng cần thiết, gây ra trì hoãn quá trình huấn luyện, triển khai hệ thống ở đơn vị |
| 8 | | | | |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

-

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 |Báo cáo tổng kết (#4) |Quy trình rõ, tốn thời gian, có baseline đo thật |Dữ liệu được tổng hợp có đúng, có đủ tốt để báo cáo cho lãnh đạo |
| 2 |Đánh giá mức độ task (#7) |Quy trình rõ, xác định độ ưu tiên |Phải tổng hợp được nội dung từ nhiều task để phân công, chưa đánh giá được độ tốt |
| 3 |Bàn giao ca (#1) |Tốn thời gian, người trực mệt mỏi sau ca trực |Dữ liệu tổng hợp được nhưng chưa xác nhận được thang đo độ tốt |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi đến đầu tháng, tôi muốn tạo được một bản báo cáo về tình hình bệnh nhân, doanh thu, tồn kho …, để báo cáo lên ban lãnh đạo, giám đốc bệnh viện trước khi họp lúc 9h sáng |
| Actor | Nhân viên phòng Kế hoạch tổng hợp |
| Thời điểm / bối cảnh | Sáng hôm làm việc đầu tiên của tháng, trước buổi họp lúc 9h |
| Quy trình hiện tại (3–7 bước) |1. Export dữ liệu từ các bảng khác nhau trong cơ sở dữ liệu Postgres · 2. Lấy thông tin đó ghi nhận trên Google Sheet · 3. Tổng hợp thêm các thông tin tình hình bệnh nhân từ các chuyên khoa · 4. Viết điểm nổi bật, tình trạng, kế hoạch kế tiếp · 5. Kiểm tra và chỉnh sửa định dạng · 6. Gửi tới máy in để in ra bản cứng  |
| Bottleneck (bước nào, mất bao nhiêu phút) |Tổng hợp tình hình từ các chuyên khoa |
| Impact (nếu không giải thì sao) | Thời gian kết xuất mất thời gian từ 3-4 giờ |
| Success metric (baseline → target) |Tổng thời gian từ cả sáng  | Tổng thời gian giảm xuống còn 30-60p
| Phương án không dùng AI |Tạo link để các chuyên khoa nhập liệu tổng hợp |
| Giả thuyết về AI (nếu có) |AI sẽ tìm và tổng hợp từ các chuyên khoa |
| Cảm nhận nhanh | No AI / Rule / Workflow / Agent / Chưa biết |Agent

Quy trình nháp hiện tại:

[Bắt đầu: Sáng ngày 1 hàng tháng]
       │
       ▼
[Bước 1: Trích xuất tự động / Script] ──> Lấy dữ liệu cơ sở từ Postgres (Doanh thu, Tồn kho, Lượt khám)
       │
       ▼
[Bước 2: AI Agent - Trích xuất] ───────> Gom báo cáo/văn bản thô từ các Chuyên khoa -> Trích xuất chỉ số chính & Key Events
       │
       ▼
[Bước 3: AI Agent - Synthesis] ────────> Tổng hợp số liệu Postgres + Báo cáo chuyên khoa -> Tạo dự thảo Báo cáo tổng hợp & Viết Highlights
       │
       ▼
[Bước 4: Human Review & Approval] ─────> Nhân viên KHTH duyệt số liệu, chỉnh sửa lời văn và điểm nóng
       │
       ▼
[Bước 5: Export & In ấn] ──────────────> Xuất file PDF/In bản cứng trình Ban giám đốc họp 9h

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi có hàng loạt đề xuất/yêu cầu công việc phát sinh từ các phòng ban, tôi muốn phân loại mức độ quan trọng và độ ưu tiên chuyên môn, để phân công đúng người, đúng hạn và không bỏ sót task nguy cơ cao |
| Actor |Team Leader, Trưởng phòng phát triển|
| Thời điểm / bối cảnh |Đầu ca làm việc hoặc khi phát sinh luồng công việc đột xuất/yêu cầu từ các khoa |
| Quy trình hiện tại (3–7 bước) |1. Tiếp nhận yêu cầu/task từ jira, hoặc hệ thống nội bộ · 2. Đọc và đọc lại nội dung để hiểu bối cảnh và độ khẩn cấp · 3. Đánh giá độ ưu tiên (P1, P2, P3) và nguồn lực hiện có · 4. Gán người xử lý và quy định deadline · 5. Cập nhật vào bảng theo dõi công việc, phân công hợp lý cho nhân viên trên jira |
| Bottleneck (bước nào, mất bao nhiêu phút) |Bước 2 & Bước 3 (Đọc hiểu, tổng hợp thông tin đa nguồn và đánh giá độ ưu tiên), mất 90–120 phút/ngày. Phải liên hệ lại người tiếp nhận |
| Impact (nếu không giải thì sao) |Đánh giá sai độ ưu tiên dẫn đến công việc tồn đọng; xử lý chậm các sự cố khẩn cấp của bệnh viện; phân công không đều tải |
| Success metric (baseline → target) |Thời gian phân loại & phân công 1 task: 15–20 phút/task → 2–3 phút/task; Giảm 80% bỏ sót công việc ưu tiên cao |
| Phương án không dùng AI |Xây dựng Ma trận Eisenhower (Rule-based checklist) bắt buộc người gửi phải chọn loại ưu tiên theo khung cố định |
| Giả thuyết về AI (nếu có) |AI phân tích nội dung văn bản/yêu cầu, trích xuất độ khẩn cấp, gợi ý mức độ ưu tiên và đề xuất nhân sự phù hợp dựa trên lịch sử xử lý task |
| Cảm nhận nhanh | No AI / Rule / Workflow / Agent / Chưa biết | Workflow

Quy trình nháp hiện tại:

[Bắt đầu: Yêu cầu/Task mới gửi đến hệ thống]
       │
       ▼
[Bước 1: Input Parser] ────────────────> Thu thập nội dung công việc (Jira, File đính kèm, Text)
       │
       ▼
[Bước 2: AI Classifier (LLM/Rule)] ────> Phân tích nội dung -> Gán tag chủ đề, Đánh giá độ khẩn cấp & Độ phức tạp
       │
       ▼
[Bước 3: AI Recommendation Engine] ────> Đề xuất mức ưu tiên (P1-P4) + Gợi ý Nhân sự xử lý dựa trên khối lượng việc hiện tại
       │
       ▼
[Bước 4: Human-in-the-loop] ───────────> Quản lý duyệt/điều chỉnh đề xuất của AI bằng 1-click
       │
       ▼
[Bước 5: Auto-dispatch & Tracking] ────> Tự động tạo task, gán deadline và gửi thông báo tới nhân sự được phân công

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi kết thúc ca trực mệt mỏi, tôi muốn tóm tắt nhanh và chính xác toàn bộ diễn biến ca trực (bệnh nhân nặng, sự cố phát sinh, công việc còn dang dở), để ca sau tiếp nhận đầy đủ thông tin mà không tốn nhiều thời gian ghi chép |
| Actor | Bác sĩ trực ca / Điều dưỡng trưởng ca |
| Thời điểm / bối cảnh |15–30 phút cuối ca trực (giao thoa giữa 2 ca) |
| Quy trình hiện tại (3–7 bước) |1. Xem lại sổ trực/nhật ký điều dưỡng và hệ thống HIS · 2. Ghi chép/Đánh máy thủ công biên bản bàn giao ca · 3. Hội ý trực tiếp với ca sau để rà soát danh sách bệnh nhân cần theo dõi đặc biệt · 4. Ký xác nhận biên bản bàn giao |
| Bottleneck (bước nào, mất bao nhiêu phút) |Bước 1 & Bước 2 (Tổng hợp thông tin từ nhiều hồ sơ/sổ sách sau một ca trực mệt mỏi), mất 45–60 phút |
| Impact (nếu không giải thì sao) |Người trực mệt mỏi dễ bỏ sót thông tin diễn biến bệnh nhân nguy cơ; giao ca kéo dài làm chậm thời gian nghỉ ngơi của ca trước |
| Success metric (baseline → target) |Thời gian lập biên bản & giao ca: 45–60 phút → 10–15 phút; Đảm bảo 100% bệnh nhân chỉ định đặc biệt được tóm tắt rõ ràng |
| Phương án không dùng AI |Sử dụng Biểu mẫu (Checklist) giao ca chuẩn hóa dạng Form cố định, bắt buộc tích chọn các mục |
| Giả thuyết về AI (nếu có) |AI gom tự động thông tin ghi nhận trong ca từ HIS/sổ điện tử, tự động cô đọng các ca bệnh nặng, sinh hiệu bất thường và danh sách việc chưa hoàn thành thành file tóm tắt giao ca |
| Cảm nhận nhanh | No AI / Rule / Workflow / Agent / Chưa biết | Agent

Quy trình nháp hiện tại:

[Bắt đầu: 30 phút trước khi kết thúc ca trực]
       │
       ▼
[Bước 1: Data Aggregator] ─────────────> Tự động quét log HIS trong ca (Bệnh nhân nhập viện mới, Chỉ định cận lâm sàng, Y lệnh chưa thực hiện)
       │
       ▼
[Bước 2: AI Summarizer (LLM)] ─────────> Trích xuất & Tóm tắt:
                                         - Ca bệnh nặng/chuyển biến bất thường
                                         - Công việc chưa hoàn thành (Pending tasks)
       │
       ▼
[Bước 3: Quick Draft Generation] ──────> Tạo bản nháp "Biên bản bàn giao ca" theo mẫu chuẩn hóa
       │
       ▼
[Bước 4: Human Review & Edit] ─────────> Bác sĩ/Điều dưỡng ca trước kiểm tra nhanh, bổ sung ghi chú bằng giọng nói/gõ tắt (nếu có)
       │
       ▼
[Bước 5: Handover Sign-off] ───────────> Ca sau xác nhận trên hệ thống / In lưu hồ sơ trực (khi cần)

### Card muốn pitch nhất

- Card số: #3
- Vì sao: Tôi thấy việc này diễn ra thường xuyên và gây mệt mỏi
- Câu hỏi muốn nhóm phản biện: Tính thực tiễn qua quy trình

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Rủi ro về tính chính xác và an toàn pháp lý (Safety & Hallucination) | Đồng ý | Ẩn thông tin bệnh nhân quan trọng, và giảm ảo giác, đưa ra số liệu sai|
| Dữ liệu chưa số hoá| Đồng ý | Số hoá toàn bệnh viện |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | | |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: Dựa vào thông tin đó có cần dùng tới AI không? | Chỉnh lại vấn đề đó|
| Nhận phản biện | Câu hỏi tôi nhận được: Tôi có thể tiếp cận được tới các bác sĩ trực lúc giao ca không? | Tôi đã sửa gì: Tôi phải lên kế hoạch cho quá trình xin phỏng vấn. |
| Gom cluster / cây OST | Có 3 nhánh: Đọc hội thoại tóm tắt, Tra cứu thông tin và Xử lý thông tin | |
| Chọn candidate problem |Chọn nhánh tổng hợp thông tin hội thoại | |
| Kiểm chứng / research | | |
| Quy trình nhóm |Đọc ngược đoạn chat tư vấn --> bắt SĐT, địa chỉ --> tìm sản phẩm --> Tạo đơn | |
| Problem Statement |Một nhân viên trực sale mất thời gian để hỗ trợ đồng thời nhiều khách trong 1 khoảng thời gian ngắn gây nguy cơ xao nhãng, khi lập đơn hàng phải hỏi lại người được tư vấn, gây khó chịu | |
| Mức can thiệp AI |ChatBot | |
| Quyết định |Go | |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | | | | |
| CP2 Problem Card |Dựa vào PC1 để sinh thêm cho PC2 và 3 |Tăng nhanh tốc độ |Quy trình khác với quy trình thực tế |Sửa lại các quy trình |
| CP4 Research | | | | |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
Đa phần các bạn hướng tới các bài toán Tóm tắt, tổng hợp nội dung văn bản.
**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**
Có. Lúc đó nhóm bị rối và đưa ra giải pháp trước thay vì đặt vai vào người dùng.
**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
Có. Chatbot có thể thay thế con người trong các việc lặp lại, tần suất liên tục.
**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

**6.5. Điều khó nhất khi viết Problem Statement là gì?**
Làm sao diễn tả được rõ vấn đề người dùng đang vướng phải, khó khăn.
**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**
Tôi sẽ chú trọng vào thông tin được kiểm chứng và lên kế hoạch phỏng vấn rõ ràng.
**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

---

## 7. Tài liệu tham khảo

-
