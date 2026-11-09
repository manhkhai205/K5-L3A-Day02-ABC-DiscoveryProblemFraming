# Báo cáo cá nhân — Nguyễn Nho Trọng

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Nguyễn Nho Trọng
- MSSV: 2A202603666
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: ABC
- Link repo nhóm: https://github.com/manhkhai205/K5-L3A-Day02-ABC-DiscoveryProblemFraming

**Nhân vật:** Nam – Junior IT Helpdesk  tại một công ty product 300 nhân sự. Công ty dùng Active Directory (AD), Google Workspace, hệ thống Ticketing (Jira Service Desk) và Slack/Zalo nội bộ.

Mỗi ngày, Nam nhận hàng chục các yêu cầu/ ticket hỗ trợ, trong đó chiếm phần lớn là các yêu cầu lặp đi, lặp lại như là quên mật khẩu, reset mật khẩu, xin cấp quyền mở

---


## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | lặp lại | Khi nhân viên quên mật khẩu, tôi muốn xác minh danh tính và reset mật khẩu để nhân viên có thể quay lại làm việc | Nhân viên yêu cầu hỗ trợ và IT Helpdesk | Nếu một ngày có khoảng 40 ticket, khoảng 40% liên quan đến mật khẩu, tương đương khoảng 16 ticket/ngày |
| 2 | lặp lại, tốn thời gian | Khi có nhân viên mới onboarding, tôi muốn cấp các tài khoản Jira, GitLab và email để họ có thể làm việc ngay | IT Helpdesk, HR và nhân viên mới | Cấp thủ công mất khoảng 15–20 phút/người; một đợt 15 intern có thể mất khoảng 225–300 phút |
| 3 | tốn thời gian | Khi nhân viên ở phòng ban khác gặp sự cố máy tính, tôi muốn chẩn đoán từ xa để xử lý lỗi mà không phải di chuyển nhiều | IT Helpdesk và nhân viên gặp sự cố | Có trường hợp IT phải di chuyển xuống tận nơi nhưng nguyên nhân chỉ là dây nguồn hoặc dây cắm chưa chặt |

| 4 | cần đọc và tổng hợp | Khi đến cuối tuần hoặc cuối tháng, tôi muốn tổng hợp các ticket đã xử lý và còn tồn đọng để báo cáo cho quản lý | IT Helpdesk và leader | Có nhiều nguồn như Jira và tin nhắn nội bộ; mỗi tuần mất khoảng 1–2 tiếng để tổng hợp báo cáo |
| 5 | pain từ người khác | Khi nhân viên cần mở folder hoặc tài liệu để làm việc, tôi muốn xử lý yêu cầu cấp quyền để họ không bị gián đoạn công việc | Nhân viên các phòng ban và IT Helpdesk | Khi có nhiều ticket, yêu cầu cấp quyền có thể phải chờ khoảng 2–4 tiếng; việc gấp có thể ảnh hưởng tiến độ |
| 6 | pain từ người khác | Khi nhân viên không nhớ quy trình báo lỗi, họ muốn có nơi hướng dẫn tự khắc phục để không phải chờ IT trả lời | Nhân viên trong công ty | IT mất khoảng 15–20 phút để hướng dẫn các lỗi như màn hình không lên hoặc không kết nối được máy in |
| 7 | | | | |
| 8 | | | | |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

-

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 |Reset mật khẩu| Tần suất cao nhất, quy trình lặp lại rõ ràng, tốn nhiều thời gian vô ích| Làm sao xác minh đúng người yêu cầu mà không dùng AI bịa?|
| 2 | Onboarding tài khoản|Pain rõ, quy trình có cấu trúc| Phụ thuộc vào HR|
| 3 | Phê duyệt quyền Folder | Ảnh hưởng trực tiếp tới tiến độ phòng ban khác| cần sự cho phép của các cấp cao hơn|

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi nhân viên quên mật khẩu email/hệ thống, tôi muốn xác minh và reset mật khẩu cho họ một cách an toàn và nhanh chóng, để họ không bị ngưng trệ công việc và IT dành thời gian cho việc quan trọng hơn|
| Actor | Nhân viên yêu cầu hỗ trợ và IT Helpdesk |
| Thời điểm / bối cảnh | Diễn ra rải rác cả ngày, cao điểm vào đầu giờ sáng hoặc sau các đợt nghỉ lễ|
| Quy trình hiện tại (3–7 bước) | 1. User nhắn tin Slack/gửi ticket: "Anh ơi reset pass giúp em" $\rightarrow$ 2. IT nhắn lại hỏi thông tin (MSSV/Mã nhân viên, Tên phòng ban) $\rightarrow$ 3. IT gọi điện/đối chiếu thông tin để xác minh identity $\rightarrow$ 4. IT mở trang Admin (Google Workspace / Active Directory) $\rightarrow$ 5. IT gõ mật khẩu tạm thời $\rightarrow$ 6. IT dán mật khẩu tạm gửi cho user qua channel riêng $\rightarrow$ 7. IT tick đóng ticket|
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 2 & 3 (Xác minh và giao tiếp qua lại): Mất 7-8 phút chờ user phản hồi thông tin xác minh + Bước 4-6 thực hiện thủ công|
| Impact (nếu không giải thì sao) | Nếu một ngày có 40 ticket và 40% liên quan đến mật khẩu thì có khoảng 16 ticket. Với 10 phút/ticket, IT mất khoảng 160 phút, tương đương hơn 2,5 giờ mỗi ngày. |
| Success metric (baseline → target) | Thời gian IT thao tác giảm từ khoảng 10 phút xuống dưới 2 phút/ticket; thời gian người dùng chờ giảm từ khoảng 35 phút xuống dưới 3 phút/ticket. Đo bằng log ticket và bấm giờ trong pilot. |
| Phương án không dùng AI | Xây dựng self-service password reset dùng OTP qua ứng dụng xác thực hoặc số điện thoại. Với người dùng khó thao tác, IT vẫn hỗ trợ theo quy trình thủ công. |
| Giả thuyết về AI (nếu có) | AI nhận diện yêu cầu reset mật khẩu, hướng dẫn người dùng chuẩn bị thông tin và chuyển yêu cầu sang workflow xác thực OTP; AI không tự reset mật khẩu. |
| Cảm nhận nhanh | Workflow kết hợp Rule và Human-in-the-loop. |

Quy trình nháp hiện tại:

```text

HIỆN TẠI — 10phút (Thời gian IT thao tác) / 35 phút (Thời gian User chờ)

[1 Nhận yêu cầu: 1'] → [2 Hỏi thông tin: 3'] → [3 Xác minh identity: 4'] ← BOTTLENECK
→ [4 Mở Admin AD/Google: 1'] → [5 Gõ pass tạm: 1'] → [6 Gửi pass cho user: 1'] → [7 Đóng ticket: 1']

```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| **Job Story** | Khi có nhân viên mới onboard (hoặc đợt intern mới gia nhập), tôi muốn tự động hóa việc khởi tạo và cấp quyền các tài khoản làm việc (Jira, GitLab, Email), để nhân viên mới có đủ công cụ làm việc ngay trong ngày đầu tiên và IT không bị tốn thời gian thao tác lặp đi lặp lại. |
| **Actor** | IT Helpdesk Technician, HR Manager |
| **Thời điểm / bối cảnh** | Đầu tuần hoặc ngày đầu tiên của các đợt tiếp nhận nhân sự/intern mới (có những đợt cao điểm lên đến 15 người/ngày). |
| **Quy trình hiện tại (3–7 bước)** | 1. HR gửi danh sách nhân viên mới (file Excel/email) cho IT<br>2. IT đọc danh sách và phân loại vị trí<br>3. IT đăng nhập Admin Jira, gõ thông tin và tạo tài khoản<br>4. IT đăng nhập Admin GitLab, gõ thông tin và phân quyền repository<br>5. IT tạo email công vụ<br>6. IT dán thông tin tài khoản tạm vào file/gửi lại cho HR<br>7. Đóng ticket hỗ trợ |
| **Bottleneck (bước nào, mất bao nhiêu phút)** | **Bước 3, 4 & 5** (Thao tác nhập tay từng tài khoản trên từng hệ thống Admin riêng lẻ): Mất 15–20 phút/người. Khi có đợt 15 intern, IT tốn khoảng 225–300 phút (~4–5 tiếng) chỉ để bấm tạo tài khoản thủ công. |
| **Impact (nếu không giải thì sao)** | IT mất cả ngày làm việc thủ công vô ích; dễ gõ sai tên/email hoặc cấp nhầm quyền; nhân viên mới phải ngồi chờ 2–3 tiếng ngày đầu tiên mới có tài khoản để làm việc. |
| **Success metric (baseline → target)** | • **Thời gian khởi tạo tài khoản:** Từ 20 phút/người → dưới 2 phút/người.<br>• **Độ chính xác thông tin:** 100% khớp danh sách HR (baseline: hay sai chính tả 5–10% ca làm tay). |
| **Phương án không dùng AI** | Viết kịch bản tự động (Bash/Python Script hoặc Ansible) đọc file CSV từ HR để gọi API của Jira, GitLab và Google Workspace khởi tạo hàng loạt (Batch creation). |
| **Giả thuyết về AI (nếu có)** | Dùng AI để đọc và trích xuất thông tin tự động từ file/văn bản đề xuất tuyển dụng không chuẩn hóa của HR → Tự phân loại vai trò (Dev/QA/Design) → Gợi ý nhóm quyền phù hợp trước khi chạy script tạo. |
| **Cảm nhận nhanh** | **Rule** (Chủ yếu dùng Rule/Script API, AI chỉ hỗ trợ nếu file đầu vào của HR không đúng định dạng chuẩn). |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 15–20 phút/người (Tốn 4–5 tiếng nếu onboard 15 người)

[1 HR gửi file danh sách: 2'] → [2 IT đọc & phân loại: 3'] 
→ [3 Tạo tài khoản Jira thủ công: 5'] ← BOTTLENECK
→ [4 Tạo tài khoản GitLab & gán nhóm: 5'] ← BOTTLENECK
→ [5 Tạo Email công vụ: 3'] 
→ [6 Gửi lại tài khoản tạm cho HR: 2'] → [7 Đóng ticket: 0']

```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| **Job Story** | Khi nhân viên phòng ban khác gửi yêu cầu cấp quyền truy cập vào folder tài liệu/dự án, tôi muốn tự động hóa khâu thu thập chữ ký phê duyệt của Trưởng phòng và cấp quyền trên hệ thống, để nhân viên có tài liệu làm việc ngay mà không bị nghẽn tiến độ dự án. |
| **Actor** | IT Helpdesk Technician, Trưởng phòng/Lead dự án (Người phê duyệt), Nhân viên xin cấp quyền (User) |
| **Thời điểm / bối cảnh** | Diễn ra rải rác trong tuần khi có dự án mới, nhân sự mới chuyển nhóm hoặc cần tài liệu inter-team. |
| **Quy trình hiện tại (3–7 bước)** | 1. User nhắn tin cho IT: "Cho em xin quyền vào folder X"<br>2. IT nhắn lại bảo User xin ý kiến Trưởng phòng<br>3. User quay sang nhắn Trưởng phòng xin xác nhận<br>4. Trưởng phòng bận họp chưa trả lời hoặc nhắn confirm miệng cho User<br>5. User chụp màn hình tin nhắn confirm gửi lại cho IT<br>6. IT vào trang Admin (Google Drive / Sharepoint / Server nội bộ) phân quyền thủ công<br>7. IT báo lại cho User và đóng ticket |
| **Bottleneck (bước nào, mất bao nhiêu phút)** | **Bước 3 & 4** (Chờ chữ ký phê duyệt từ Trưởng phòng qua lại thủ công): Mất từ 2 đến 4 tiếng (đôi khi mất cả ngày nếu Trưởng phòng đi công tác/bận họp) chỉ để nhận một xác nhận "Đồng ý". |
| **Impact (nếu không giải thì sao)** | Ảnh hưởng trực tiếp tới tiến độ công việc của phòng ban khác (nhân viên không có dữ liệu để làm report/slide); IT bị dán nhãn xử lý chậm dù lỗi nằm ở khâu chờ phê duyệt; rủi ro bảo mật do IT cấp quyền dựa trên ảnh chụp màn hình dễ bị làm giả. |
| **Success metric (baseline → target)** | • **Thời gian chờ phê duyệt & cấp quyền:** Từ 2–4 tiếng → dưới 15 phút.<br>• **Thời gian IT thao tác phân quyền:** Từ 10 phút/ticket → 0 phút (tự động hóa sau khi có duyệt). |
| **Phương án không dùng AI** | Dùng Slack Workflow / Google Form / Jira Service Desk có tính năng **Approval Workflow** cố định: User gửi request → Hệ thống bắn nút `[Approve / Reject]` trực tiếp cho Trưởng phòng → Trưởng phòng bấm `Approve` → Webhook tự động gọi API phân quyền. |
| **Giả thuyết về AI (nếu có)** | Dùng AI Chatbot tự động phân tích ma trận phân quyền (Matrix Access) và lịch sử làm việc của User để đề xuất đúng Trưởng phòng cần duyệt, đồng thời phát hiện các yêu cầu cấp quyền bất thường (vượt cấp/nhạy cảm) để cảnh báo cho Trưởng phòng trước khi bấm duyệt. |
| **Cảm nhận nhanh** | **Rule** (Quy trình phê duyệt cố định bằng Rule/Workflow, khâu kiểm soát phê duyệt bắt buộc phải do Trưởng phòng - Khâu Human thực hiện). |
Quy trình nháp hiện tại:

```text
HIỆN TẠI — Chờ 2–4 tiếng (Ảnh hưởng trực tiếp tiến độ phòng ban khác)

[1 User nhắn IT xin quyền: 2'] → [2 IT bảo User xin duyệt: 2'] 
→ [3 User nhắn Trưởng phòng: 5'] → [4 Trưởng phòng xác nhận (Human): Chờ 2-4 tiếng] ← BOTTLENECK
→ [5 User dán ảnh chụp màn hình cho IT: 3'] 
→ [6 IT vào Admin phân quyền: 5'] → [7 Đóng ticket: 1']

```

### Card muốn pitch nhất

- Card số: #1 — Tự động hóa quy trình Reset mật khẩu Email / Tài khoản nội bộ
- Vì sao:
  1. Đây là bài toán có tần suất lặp lại cao nhất trong ngày (chiếm ~40% tổng số ticket, mất 4 tiếng/ngày của IT).
  2. Quy trình hiện tại có các bước rất rõ ràng, nốt thắt bottleneck nằm ở khâu nhắn tin qua lại xác minh thông tin.
  3. Có baseline đo đạc thời gian cụ thể (10 phút thao tác IT / 35 phút user chờ) và dễ dàng đánh giá thành công sau khi tối ưu.
  4. Phù hợp hoàn hảo để so sánh 4 mức can thiệp (No AI / Rule / Workflow / Agent), giúp nhóm chứng minh được tư duy phân tích rủi ro an ninh mạng khi không chọn Agent hoàn toàn.
- Câu hỏi muốn nhóm phản biện:
  1. Nếu không dùng AI để xác minh danh tính nhằm tránh bịa đặt/rủi ro an ninh, khâu xác minh OTP qua Slack/SĐT có đủ độ tin cậy đối với các tài khoản cấp cao không?
  2. Làm sao để xử lý đối tượng người dùng lớn tuổi/ít thạo công nghệ khi họ không biết dùng các công cụ Self-Service tự động?

### AI đã phản biện card thế nào

Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| **Chưa tính đến rủi ro an toàn thông tin:** AI chỉ ra việc dùng Chatbot tự đổi mật khẩu mà không có xác thực OTP hoặc người duyệt có thể bị hacker lợi dụng (Prompt Injection / Social Engineering) để chiếm quyền tài khoản. | **Đồng ý hoàn toàn** | Đã bổ sung **Boundary** bắt buộc: AI chỉ dừng ở mức nhận diện tin nhắn và hỗ trợ gom thông tin, khâu đổi mật khẩu phải có xác thực OTP và nút bấm `[Approve]` 1-click từ con người (HITL). |
| **Success Metric chưa rõ ràng và chưa tách biệt:** Bản nháp ban đầu ghi chung chung "giảm xuống dưới 5 phút", chưa phân tách giữa thời gian IT làm việc và thời gian User phải chờ đợi. | **Đồng ý** | Chuẩn hóa lại Baseline → Target rõ ràng: **Thời gian IT thao tác** (từ 10 phút → dưới 2 phút/ticket) và **Thời gian User chờ** (từ 35 phút → dưới 3 phút). |
| **Gợi ý giải pháp quá phức tạp:** AI ban đầu đề xuất xây dựng Agent nhận diện khuôn mặt hoặc giọng nói qua FaceTime để xác minh danh tính. | **Không đồng ý** | Giữ nguyên phương án đơn giản hơn: Dùng Slack Workflow Form + gửi mã OTP qua App Authenticator/SĐT để tối ưu chi phí và dễ triển khai trong thực tế. |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Tôi trình bày các problem card về hỗ trợ IT, trong đó có reset mật khẩu, onboarding tài khoản và cấp quyền folder. | Cung cấp thêm các candidate để nhóm so sánh với các vấn đề của những thành viên khác. |
| Phản biện bài của bạn khác | Tôi đặt câu hỏi về việc nếu dùng AI trích xuất thông tin tạo đơn thì làm sao tránh AI điền nhầm màu, size hoặc địa chỉ khi khách đã đổi ý. | Nhóm bổ sung ranh giới không cho AI tự đoán thông tin thiếu và phải có nhân viên kiểm tra. |
| Nhận phản biện | Tôi nhận phản biện rằng không nên áp dụng AI cho mọi đơn hàng vì các đơn ngắn đã có Rule của POS xử lý nhanh. | Tôi đồng ý và ủng hộ nhóm thu hẹp phạm vi vào các cuộc hội thoại dài, có nhiều mẫu hoặc khách đổi ý. |
| Gom cluster / cây OST | Tôi tham gia gom các vấn đề liên quan đến việc đọc thông tin rời rạc, chuẩn hóa dữ liệu và bàn giao công việc. | Nhóm nhận diện opportunity chung là tổng hợp thông tin từ nội dung tự nhiên vào một quy trình có cấu trúc. |
| Chọn candidate problem | Tôi tham gia so sánh các candidate theo mức độ đau, tần suất, khả năng kiểm chứng và mức phù hợp với AI. | Nhóm chọn bài toán gom thông tin chốt đơn từ hội thoại dài để tạo đơn hàng. |
| Kiểm chứng / research | Tôi phụ trách research các công cụ như Pancake POS, Sapo Social và Structured Outputs; đồng thời đối chiếu điểm mạnh, khoảng trống và rủi ro của từng giải pháp. | Bài nhóm tận dụng Rule có sẵn của POS và chỉ dùng AI cho phần đọc hiểu hội thoại, trích xuất thông tin chốt đơn. |
| Quy trình nhóm | Tôi góp ý phân biệt rõ phần Rule, AI và con người trong quy trình tương lai, đồng thời phải có phương án quay về quy trình cũ khi AI sai hoặc chậm. | Quy trình tương lai có bước AI tạo bản nháp, nhân viên sales kiểm tra và tự bấm lưu đơn. |
| Problem Statement | Tôi góp ý bổ sung boundary, đặc biệt là không tự lưu đơn, không tự đoán màu/size/địa chỉ và phải trả về `null` khi thiếu thông tin. | Problem Statement v1 có thêm tiêu chí chất lượng và cơ chế hiển thị trường thiếu để nhân viên kiểm tra. |
| Mức can thiệp AI | Tôi tham gia so sánh No AI, Rule, Workflow và Agent, tập trung vào câu hỏi AI cần dữ liệu gì và con người kiểm tra ở đâu. | Nhóm chọn Workflow: Rule bắt SĐT, AI trích xuất JSON, nhân viên sales duyệt trước khi lưu đơn. |
| Quyết định | Tôi góp ý đánh giá giải pháp theo Value, Usability, Feasibility và Viability, đồng thời cần có ngưỡng dừng rõ ràng. | Nhóm quyết định Go pilot 2 tuần trên 100 đơn hội thoại dài, có điều kiện dừng nếu chất lượng hoặc tốc độ không đạt. |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Gợi ý thêm các vấn đề có thể gặp khi nhân viên sales phải đọc hội thoại và nhập đơn hàng. | AI giúp tôi mở rộng góc nhìn về các pain liên quan đến dữ liệu rời rạc và thao tác lặp lại. | Một số gợi ý quá rộng hoặc bắt đầu từ giải pháp như chatbot, chưa có bằng chứng hành vi. | Tôi chỉ giữ các problem có quy trình cụ thể và tự bổ sung dấu hiệu thực tế từ bối cảnh của mình. |
| CP2 Problem Card | Hỗ trợ phản biện job story, bottleneck, impact và success metric của các card. | AI giúp phát hiện các điểm còn thiếu như boundary, người kiểm tra và phương án fallback. | AI có xu hướng đề xuất Agent tự động hoặc gom cả các đơn ngắn vào cùng phạm vi. | Tôi giữ cách tiếp cận Workflow có người duyệt và ủng hộ nhóm chỉ tập trung vào hội thoại dài. |
| CP4 Research | Gợi ý các công cụ và pattern để nghiên cứu như Pancake POS, Sapo Social và Structured Outputs. | AI giúp tạo danh sách hướng nghiên cứu và các tiêu chí so sánh nhanh. | AI có thể nói quá khả năng của công cụ hoặc đưa claim chưa được kiểm chứng. | Tôi tự mở link, đối chiếu tính năng, ghi rõ khoảng trống và không dùng AI thay cho dữ liệu phỏng vấn/log thật. |
| CP5 Quy trình | Hỗ trợ chuyển mô tả quy trình tạo đơn thành các bước hiện tại và tương lai. | AI giúp nhìn rõ điểm có thể dùng Rule, AI và con người. | Bản nháp ban đầu dễ gộp bước đọc chat, chuẩn hóa địa chỉ và tạo đơn thành một bước quá đơn giản. | Tôi tách các bước, giữ bước sales kiểm tra và bổ sung fallback về thao tác thủ công trên POS. |
| CP5–6 Problem Statement | Hỗ trợ kiểm tra actor, phạm vi, metric và boundary của Problem Statement v0/v1. | AI giúp phát hiện metric v0 chỉ đo tốc độ mà chưa đo chất lượng đầu ra. | AI không tự biết phạm vi nào phù hợp với số liệu kiểm chứng của nhóm. | Tôi ủng hộ thu hẹp phạm vi vào hội thoại dài, thêm mục tiêu ≥85% bản nháp đúng và giới hạn số đơn sai. |
| CP6 Mức can thiệp / quyết định | So sánh No AI, Rule, Workflow và Agent cho bài toán tạo đơn từ hội thoại. | AI giúp hệ thống hóa ưu điểm, rủi ro và điều kiện sử dụng của từng mức. | AI có thể ưu tiên Agent dù quy trình vẫn cần người duyệt và dữ liệu đầu vào còn mơ hồ. | Tôi chọn Workflow: Rule bắt SĐT, AI trích xuất JSON, sales kiểm tra và bấm lưu; nếu AI sai hoặc chậm thì quay về POS thủ công. |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
tôi học được thêm nhiều góc nhìn từ những người ở ngành nghề khác, của bạn Khải là về hệ thống thương mại điện tử, của bạn thắng là hệ thống trong bệnh viện

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**
có. Lúc đầu khi nghe những vấn đề của các bạn cũng như của mình thì việc đầu tiên mình luôn nghĩ đến là xây dựng chatbot để giải quyết những vấn đề đó, nhưng sau khi ngồi lại và nghĩ đến những nghiệp vụ đặc thù thì mình nhận ra ko phải vấn đề nào cũng cần có chatbot để giải quyết

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
có, lúc đầu với vấn đề reset mật khẩu do tốn nhiều thời gian thì tôi có đề xuất sự dụng chatot để tự động hóa hướng dẫn nhân viên xử lý khi mật khẩu bị sai, thế nhưng sau khi xem xét lại nghiệp vụ và những lý do bảo mật thì tôi quyết định chỉ nên can thiệp vào phần hướng dẫn cho nhân viên thôi

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**
kết quả phỏng vấn thì tôi thấy cũng bình thường, vì tôi hỏi những người đi làm trong nhóm tôi thì khi họ có những vấn đề lên quan đến ticket thì vẫn phải đợi tầm 15 đến 30p để đc giải quyết

**6.5. Điều khó nhất khi viết Problem Statement là gì?**Khó nhất là viết đúng vấn đề mà không bị chuyển sang mô tả giải pháp. Ban đầu tôi thường viết theo kiểu “cần làm chatbot reset mật khẩu”, nhưng câu đó mới chỉ nói về giải pháp chứ chưa nói rõ vấn đề. Sau đó tôi phải tập trung vào actor, hoàn cảnh, bottleneck, ảnh hưởng và kết quả muốn đạt được. Việc tách thời gian IT thao tác với thời gian người dùng chờ cũng hơi khó vì trước đó tôi chỉ nghĩ chung là xử lý dưới 5 phút. Ngoài ra, boundary về bảo mật cũng cần viết rõ để tránh cho AI làm quá quyền của nó.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**
Nếu làm lại, tôi sẽ cố gắng thu thập thêm số liệu thực tế về số ticket reset mật khẩu mỗi ngày, thời gian xử lý trung bình và số lần người dùng phải bổ sung thông tin. Tôi cũng sẽ tìm hiểu kỹ hơn về chính sách bảo mật trước khi đề xuất giải pháp. Tôi nghĩ mình nên phản biện nhóm mạnh hơn ở việc không phải cứ dùng AI là tốt hơn dùng Rule hoặc Workflow. Đặc biệt, tôi sẽ hỏi kỹ hơn về trường hợp OTP bị lộ, người giả mạo nhân viên hoặc AI nhận diện sai yêu cầu. Ngoài ra, tôi sẽ đề xuất thử nghiệm với một nhóm nhỏ trước, nếu ổn thì mới triển khai rộng.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.
Vấn đề là trong một ngày có quá nhiều tiket liên quan đến reset mật khẩu cho nhân viên. Đầu tiên là nhân viên đó sẽ cần gửi yêu cầu/ticket cho it helpdesk để reset mật khẩu, sau đó it sẽ gọi xác nhận để xem nhân viên đó phòng ban, vị trí nào, tiếp đó it sẽ vào trang chủ và cấp cho nhân viên đó 1 mật khẩu mới để nhân viên đó đăng nhập thành công vào rồi sẽ sửa mật khẩu. Metric là sẽ làm sao để giảm cho it xử lý các yêu cầu này từ 10p xuống dưới 2 phút. Boundary của giải pháp là AI không được tự ý reset mật khẩu hoặc cấp quyền khi chưa xác minh người dùng. Qua đó mức độ cho vấn đề này nên là Workflow kết hợp Rule, OTP và sự kiểm tra của nhân viên IT. AI chỉ hỗ trợ nhận diện yêu cầu, hướng dẫn người dùng và thu thập thông tin cần thiết


## 7. Tài liệu tham khảo

-
