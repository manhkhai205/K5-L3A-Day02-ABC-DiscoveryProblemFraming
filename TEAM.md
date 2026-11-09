# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: ABC
- Candidate problem nhóm chọn (1 câu): Khi khách đã chốt mẫu, số lượng, SĐT và địa chỉ nằm rải rác trong đoạn chat dài, nhân viên sales muốn gom đủ thông tin đặt hàng vào đúng các trường tạo đơn, để không phải cuộn ngược đoạn chat copy-paste từng dòng và tránh nhập sai mã hàng/địa chỉ.
- Quyết định cuối (Go / Not Yet / No-Go): **Go** (phạm vi nhỏ — Pilot 2 tuần trên 100 đơn hội thoại dài)

## Thành viên

| STT | Họ và tên             | MSSV        | Vai trò trong nhóm                                                           | Tài khoản GitHub               |
| --- | --------------------- | ----------- | ---------------------------------------------------------------------------- | ------------------------------ |
| 1   | Nguyễn Viết Mạnh Khải | 2A202603664 | Phụ trách kiểm chứng thực tế, vẽ quy trình trước/sau, viết Problem Statement | https://github.com/manhkhai205 |
| 2   | Hà Minh Thắng         | 2A202603676 | Điều phối thời gian, gom cluster/cây OST, đánh giá 4 rủi ro & quyết định     | https://github.com/HaMThang    |
| 3   | Nguyễn Nho Trọng      | 2A202603666 | Ghi chép, phản biện chính, phụ trách research công cụ & mức can thiệp AI     | https://github.com/trongbipbip |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint                                 | Người chính           | Người hỗ trợ | Sản phẩm                                       |
| ------------------------------------------ | --------------------- | ------------ | ---------------------------------------------- |
| CP3 — Hội tụ nhóm                          | Hà Minh Thắng         | Khải, Trọng  | Cluster, cây OST, bảng chấm điểm               |
| CP4 — Kiểm chứng                           | Nguyễn Viết Mạnh Khải | Thắng        | Assumption map, snapshot hoặc survey           |
| CP4 — Research                             | Nguyễn Nho Trọng      | Khải         | Bảng research có link                          |
| CP5 — Quy trình trước/sau                  | Nguyễn Viết Mạnh Khải | Trọng        | Quy trình + bảng before/after                  |
| CP5 — Problem Statement v0                 | Nguyễn Viết Mạnh Khải | Thắng        | Problem Statement v0                           |
| CP6 — Mức can thiệp + Problem Statement v1 | Nguyễn Nho Trọng      | Khải, Thắng  | Ma trận, AI Canvas, eval, Problem Statement v1 |
| CP6 — Quyết định                           | Hà Minh Thắng         | Khải, Trọng  | 4 rủi ro + Go/Not Yet/No-Go                    |

## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### NguyenVietManhKhai-2A202603664

**Phần việc phụ trách:** Đề xuất bài toán chính (#4 Tạo đơn từ hội thoại chat), phụ trách Kiểm chứng thực tế (CP4), Quy trình trước/sau & Problem Statement v0/v1 (CP5–CP6).

- **Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):
    - Pitch 3 Problem Cards về vận hành TMĐT ở CP3; cung cấp ngữ cảnh thực tế giúp bài toán #4 được chọn (34/35 điểm).
    - Thực hiện kiểm chứng thực tế trên log 15 đơn hàng Fanpage và phỏng vấn nhanh 2 nhân viên trực page theo The Mom Test; đối chiếu quy trình thật trên Pancake POS / Sapo Social để giúp nhóm thu hẹp phạm vi vào 60% đơn hội thoại dài/đổi ý.
    - Vẽ sơ đồ quy trình hiện tại (6 bước, 240s) và quy trình tương lai (5 bước, \~55s) có phân tách rõ Rule – AI – Con người (HITL) và phương án Fallback.
    - Soạn thảo Problem Statement v0 và cập nhật lên v1 (bổ sung metric chất lượng ≥ 85% đơn nháp đúng, quy tắc trả về `null` khi thiếu thông tin kèm trích dẫn `source_quote`).

- **Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):
    - Báo cáo cá nhân: report/individual/202603664_NguyenVietManhKhai.md
    - Báo cáo nhóm: Mục 2.1 (candidate #4–#6), Mục 3.1–3.2 (Assumption Map & Interview Snapshots), Mục 4 (Quy trình trước/sau), Mục 5 & Mục 7 (Problem Statement v0 & v1) trong report/team/group_report.md.

- **Điều mình học được từ phần nhóm:**
    - Học được cách tách bạch rạch ròi giữa bước đã có công cụ giải quyết bằng **Rule** (bắt SĐT, đồng bộ khách cũ trên POS) với bước thực sự cần **Workflow AI** (đọc hiểu ngữ cảnh khách đổi ý màu/size rải rác trong hội thoại dài).
    - Hiểu vì sao trong bài toán tạo đơn, lỗi "điền bừa khi thiếu thông tin" (False Positive) nguy hiểm hơn lỗi "để trống báo thiếu" (False Negative), từ đó thiết kế Boundary ép AI trả về `null` và giữ bước nhân viên sales duyệt cuối cùng.

### NguyenNhoTrong-2A202603666

**Phần việc phụ trách:** Ghi chép, phản biện chính, phụ trách research công cụ và mức can thiệp AI ở CP4–CP6.

- **Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):
    - Pitch các problem card về reset mật khẩu, onboarding tài khoản và cấp quyền folder ở CP3; đặt câu hỏi phản biện về bảo mật, OTP và việc không để AI tự quyết định các thao tác nhạy cảm.
    - Tham gia research Pancake POS/Vpage, Sapo Social và OpenAI Structured Outputs; so sánh phần đã được Rule hỗ trợ với phần còn cần AI đọc hiểu ngữ cảnh.
    - Góp ý thu hẹp phạm vi từ mọi đơn hàng xuống các cuộc hội thoại dài, có nhiều mẫu hoặc khách đổi ý; đề xuất Workflow thay vì Agent tự động hoàn toàn.
    - Góp ý boundary của AI: không tự lưu đơn, không tự đẩy kho, không tự đoán màu/size/địa chỉ khi thông tin chưa rõ; cần trả về `null`, hiển thị trường thiếu và để nhân viên sales kiểm tra.
    - Tham gia xây dựng phần so sánh No AI/Rule/Workflow/Agent, AI Canvas, tiêu chí đánh giá và ngưỡng dừng của pilot.

- **Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):
    - Báo cáo cá nhân: `report/individual/202603666_NguyenNhoTrong.md`.
    - Báo cáo nhóm: Mục 2.1 (các candidate của Trọng), Mục 3.3 (research giải pháp), Mục 6 (mức can thiệp AI), Mục 7 (boundary và tiêu chí đánh giá), Mục 8 (ngưỡng dừng).
    - Bộ eval: `report/assets/cp6-eval-dataset.md`.

- **Điều mình học được từ phần nhóm:**
    - Học được cách phân biệt rõ bước nào chỉ cần Rule, bước nào cần AI và bước nào bắt buộc phải có con người kiểm tra.
    - Hiểu rằng với dữ liệu hội thoại mơ hồ, để trống và báo thiếu thông tin an toàn hơn việc để AI tự đoán rồi làm người duyệt hiểu nhầm là dữ liệu đã chính xác.
