# Bài nộp LAB5 — T2 Giáo dục

Prototype và đặc tả cho trợ lý học bài của trang khoá học, dành cho học viên tự học buổi tối.

## Mở prototype

Mở `prototype/index.html` trực tiếp bằng trình duyệt. Không cần cài package, máy chủ, tài khoản hay API key; toàn bộ tương tác dùng dữ liệu dựng và chạy trong trình duyệt.

Trong prototype:

1. Chọn một trong hai ca dựng ở đầu màn hình: tài liệu có câu cần kiểm tra, hoặc xin xác nhận đáp số bài đang mở.
2. Thử xem trước gợi ý, gửi gợi ý theo xác nhận, hoặc chuẩn bị chuyển câu hỏi cho TA.
3. Đọc trạng thái và chú thích để phân biệt việc nào chỉ được mô phỏng với việc nào thực sự đã gửi.

Prototype **không** gọi AI, không kết nối TA, không ghi vào FAQ và không gửi dữ liệu ra ngoài. Các thao tác ghi rõ “mô phỏng”; không được hiểu là đã có người nhận yêu cầu.

## Nội dung

- `spec.md`: phạm vi, 8 kịch bản rủi ro, cách xử lý hai ca đắt nhất, mức tự chủ cho từng tool và tiêu chí Pass/Fail.
- `prototype/index.html`: prototype tương tác một màn hình, có thể mở offline.

## Thông tin cần bổ sung trước khi nộp

- Điền họ tên, mã học viên và lớp trong `spec.md`.
- Đổi tên repository theo quy ước của lớp: `K5-<lớp>-Day05-T2-<tên>`.
- Đề bài quy định nhóm 3 người; bài này được chuẩn bị theo yêu cầu làm một mình. Hãy hỏi giảng viên/TA xem bài cá nhân có được chấp nhận và cần điều chỉnh phần demo/phân công thế nào trước khi nộp chính thức.
- Nếu nộp lên repository riêng, đặt nội dung của folder này ở root repository rồi push lên `main`. Không đưa các file đề bài hoặc dữ liệu thật vào repo bài nộp.

Tất cả ví dụ trong bài là dữ liệu dựng từ track T2. Không sử dụng thông tin học viên, bài tập hay khoá học thật.
