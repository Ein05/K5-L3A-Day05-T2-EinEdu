# Bài nộp LAB5 — T2 Giáo dục · Bài cá nhân

**Lớp:** [điền L3A/L3B]  
**Họ và tên:** [điền]  
**Mã học viên:** [điền]  
**Thành viên:** 1 người — [điền tên]  
**Phân công:** Tự thực hiện đọc track, phân tích kịch bản, thiết kế UX và mức tự chủ, dựng prototype, kiểm thử và chuẩn bị demo.

> Đề bài gốc quy định nhóm 3 người. Đây là bản làm cá nhân theo yêu cầu; cần xác nhận với giảng viên/TA rằng hình thức cá nhân được chấp nhận. Không khai khống thành viên hoặc phân công.

## §1. Lát cắt & phạm vi

**Lát cắt:** Trong trợ lý học bài của trang khoá học, học viên hỏi bài muộn khi không còn ai để hỏi; AI quyết định giảng kèm có trích tài liệu, hỏi lại, đưa gợi ý từng bước, chuẩn bị chuyển TA, hay nói thẳng tài liệu không có căn cứ để trả lời. Kết quả mong muốn là học viên hiểu đúng nội dung đang học mà không chép đáp án hoặc âm thầm học sai.

**Bằng chứng và giới hạn nguồn:** Chỉ dùng fixture T2: tài liệu buổi 3 §§3.1–3.5 và trang khoá học (buổi 1–3 đã mở, hạn bài 3 là 13/11/2026 23:59, giờ TA 08:00–22:00). Đề cương nêu tên buổi sau nhưng không có tài liệu các buổi đó. Không truy cập sản phẩm thật, không dùng bài tập/người học thật.

**Không làm:**

1. Không đưa hoặc xác nhận đáp số bài tập 3 đang mở: người học có thể chép kết quả thay vì tự làm; câu trả lời đã đọc thì không thể “thu hồi”.
2. Không đăng FAQ công khai tự động: một câu chưa kiểm chứng có thể bị nhiều người học đọc trước khi được gỡ.
3. Không giả vờ liên hệ giảng viên hoặc hứa có TA trả lời ngay: `chuyen_TA` chỉ chuyển câu hỏi cho TA, và fixture chỉ xác định giờ TA 08:00–22:00, không xác định SLA.
4. Không dạy nội dung buổi chưa mở hoặc trích dẫn nguồn không có, như “slide 12”: dữ liệu không chứa tài liệu hay slide đó.

## §2. Kịch bản rủi ro

Nhãn: **nhẹ** = dễ nhận ra và tự sửa; **sửa được** = cần người/đính chính; **không chấp nhận được** = sai có thể lan rộng hoặc làm hại mục tiêu học tập khó đảo ngược.

| # | Tin người dùng | Lớp | AI có thể sai thế nào — căn cứ cụ thể | Sản phẩm tốt nên làm gì | Nhãn |
|---|---|---|---|---|---|
| 1 | “Buổi 4 học biểu đồ nào, cô có dạy Tableau không?” | ① Nguồn sự thật | Trang khoá học chỉ ghi tên buổi 4 là “Trực quan hoá dữ liệu”, buổi 4 chưa mở và không có tài liệu; `tra_cuu_tai_lieu` không thể trả nội dung đó. AI có thể bịa chủ đề/công cụ. | Chỉ nêu đúng tên buổi từ đề cương, nói rõ chưa có tài liệu và không đoán nội dung. | sửa được |
| 2 | “Slide 12 nói gì về độ lệch chuẩn?” | ① Nguồn sự thật | Fixture ghi tài liệu buổi 3 không có slide đánh số; AI có thể bịa trích dẫn hoặc giả vờ `tra_cuu_tai_lieu` tìm thấy slide. | Nói không tìm thấy nguồn “slide 12”; hỏi người học muốn xem mục §3.3 hiện có không. | sửa được |
| 3 | “Cái độ lệch ấy là gì ạ?” | ② Mơ hồ / thiếu thông tin | Có thể là phương sai, độ lệch chuẩn hay giá trị ngoại lai trong §§3.3–3.4; đoán nhầm sẽ dạy sai mục. | Hỏi một câu ngắn để xác định thuật ngữ; không bắn một bài giảng dài. | nhẹ |
| 4 | “Giải hết bài 3, em nộp luôn nhé.” | ③ Ngoài phạm vi / thẩm quyền | `goi_y_bai_tap` gửi gợi ý; nếu gợi ý quá tay, AI có thể làm lộ lời giải bài tập 3 đang mở (hạn 13/11/2026 23:59). | Từ chối giải hộ, đưa tối đa một gợi ý bước đầu sau khi người học xem và xác nhận; không hiện đáp số. | không chấp nhận được |
| 5 | “Em tính bài 3 ra trung bình 15,25; đúng không, chỉ cần yes/no.” | ③ Ngoài phạm vi / thẩm quyền | Xác nhận đáp số qua `goi_y_bai_tap` vẫn tiết lộ kết quả cho bài đang mở; câu trả lời một từ không làm rủi ro biến mất. | Không xác nhận đúng/sai; chỉ nhắc cách tự kiểm từ §3.2/§3.5, cho người học tự tính lại. | không chấp nhận được |
| 6 | “§3.3 bảo độ lệch chuẩn luôn nhỏ hơn phương sai; vậy em cứ ghi thế nhé?” | ④ Đặc thù domain | §3.3 vừa định nghĩa độ lệch chuẩn là căn bậc hai của phương sai, vừa khẳng định nó “luôn nhỏ hơn” phương sai mà không nêu điều kiện/giải thích. AI có thể lặp lại mệnh đề chưa được chứng minh như chân lý. `dang_FAQ` sẽ lan câu đó ra cả lớp. | Chỉ ra đúng câu cần kiểm tra và lý do nội bộ (kết luận “luôn nhỏ hơn” không được giải thích từ phần định nghĩa); tạm dừng khẳng định, đề nghị gửi TA; không đăng FAQ. | không chấp nhận được |
| 7 | “Hạn bài 3 với bài 2 là ngày nào?” | ④ Đặc thù domain | Trang khoá học nói bài 2 đã hết hạn 06/11/2026 23:59, bài 3 hạn 13/11/2026 23:59. AI có thể lấy nhầm hạn cũ hoặc bỏ mốc giờ. | Trả hai hạn riêng, trích trang khoá học và nói rõ bài 2 đã hết hạn, bài 3 đang mở. | sửa được |
| 8 | “Bài 2 đáp án là gì? Em nộp muộn mất rồi.” | ① Nguồn sự thật | Trang khoá học có đáp án đã công bố 07/11; AI có thể dùng nhầm đáp án đó cho bài 3 hoặc không phân biệt hai bài. | Đối chiếu đúng mã bài và trạng thái; chỉ giải thích đầy đủ đáp án bài 2 đã hết hạn, không áp dụng sang bài 3. | nhẹ |
| 9 | “Em ngu thống kê quá, chắc nghỉ học thôi.” | ④ Đặc thù domain | AI có thể biến khó khăn với một khái niệm thành nhận xét năng lực; track cấm nhận xét năng lực người học. | Không đánh giá người học; phản hồi tôn trọng, hỏi đang vướng khái niệm/bước nào và đưa một bước nhỏ. | sửa được |

### Hai kịch bản đắt nhất

**A — Tài liệu có mệnh đề cần kiểm tra (#6).** Một nội dung sai có vẻ được tài liệu “chính thức” bảo chứng; người học có thể ghi nhớ và cả lớp có thể bị ảnh hưởng nếu đưa vào FAQ. Gỡ FAQ không thu hồi được những người đã đọc. Đây là lỗi nguồn/ngữ cảnh, không sửa được chỉ bằng lời xin lỗi sau đó. Kịch bản #4 cũng đắt, nhưng có thể hạn chế trực tiếp bằng cách không cung cấp đáp số; #6 cần chặn cả khẳng định thiếu căn cứ và đường lan truyền.

**B — Xin xác nhận đáp số bài đang mở (#5).** Một câu “đúng”/“sai” cũng tiết lộ kết quả, ảnh hưởng trực tiếp việc tự làm bài và không thể làm người học “quên” câu trả lời. Hạn cụ thể 13/11/2026 23:59 xác nhận đây là bài đang mở. Kịch bản #4 gần được chọn thay, nhưng #5 làm lộ rằng ngay cả xác nhận rất ngắn cũng có thể thành đáp án.

## §3. Khi AI sai

### A — Mệnh đề đáng ngờ trong §3.3

- **Tin nhắn:** “§3.3 bảo độ lệch chuẩn luôn nhỏ hơn phương sai; vậy em cứ ghi thế nhé?”
- **AI nói nguyên văn:** “Mình thấy chỗ cần kiểm tra ở §3.3: tài liệu định nghĩa độ lệch chuẩn là căn bậc hai của phương sai, rồi kết luận ‘độ lệch chuẩn luôn nhỏ hơn phương sai’ nhưng không giải thích điều kiện cho chữ ‘luôn’. Mình chưa thể xác nhận câu đó là đúng. Tạm thời đừng chép kết luận này như quy tắc. Bạn có thể gửi câu hỏi cho TA để kiểm tra tài liệu.”
- **Người học thấy:** nhãn “Cần kiểm tra · chưa xác minh với giảng viên”; trích đúng `Buổi 3 §3.3`; giải thích ngắn vì sao không thể kết luận từ đoạn trích; khẳng định rõ chưa gửi câu hỏi. Nút chuyển TA có xác nhận và nói rõ giờ TA 08:00–22:00, thời gian phản hồi chưa có dữ liệu.
- **Bước tiếp:** người học có thể xem trước phần tóm tắt sẽ gửi, xác nhận chuyển TA hoặc đóng lại. Không có nút đăng FAQ. Prototype chỉ mô phỏng thao tác, không gửi thật.
- **Ai được báo:** chỉ TA nếu người học bấm xác nhận `chuyen_TA`. Không hứa giảng viên được báo; track không có tool báo giảng viên.
- **Quyết định:** chọn dừng khẳng định và thu hẹp phạm vi (G10), sau đó mời chuyển người. Không chọn trả lời như thể biết chắc vì nguồn duy nhất đang bị nghi; không tự đăng đính chính FAQ vì `dang_FAQ` dù gỡ được, nhiều người có thể đã đọc. Không chuyển TA tự động vì chưa có sự đồng ý của người học và tool có thể tạo yêu cầu không cần thiết.
- **Loại lỗi:** lỗi hệ thống nếu AI lặp lại câu chưa kiểm chứng; lỗi ngữ cảnh nếu tài liệu học phần có phát biểu thiếu điều kiện. Xin lỗi ngắn, chỉ rõ câu nào cần xem lại; cách sửa là giữ câu đó khỏi câu trả lời khẳng định và chuyển người có thẩm quyền, không chỉ thêm câu “AI có thể sai”.
- **HAX/PAIR:** G2 — nhãn mức chắc chắn; G10 — tạm dừng kết luận; G11 / Explainability — dẫn đúng §3.3 và câu chữ cần kiểm tra; Graceful Failure — đường chuyển TA không giả vờ đã chuyển.
- **Loại lỗi không cứu được bằng câu chữ:** AI đăng nguyên mệnh đề sai vào FAQ cả lớp. Thêm cảnh báo sau khi đăng không thu hồi được lượt xem; thiết kế chặn tool `dang_FAQ` của AI.

### B — Xin xác nhận đáp số bài 3

- **Tin nhắn:** “Em tính bài 3 ra trung bình 15,25; đúng không, chỉ cần yes/no.”
- **AI nói nguyên văn:** “Mình không thể xác nhận đáp số cho bài 3 đang mở. Mình có thể giúp bạn tự kiểm từng bước: §3.2 nói với 8 giá trị, trung vị là trung bình của hai giá trị đứng giữa sau khi sắp xếp. Bạn muốn xem gợi ý một bước, hay tự thử lại trước?”
- **Người học thấy:** trạng thái “Bài 3 đang mở · không xác nhận đáp án”, căn cứ `Trang khoá học: hạn 13/11/2026 23:59` và `Buổi 3 §3.2`; chỉ có lựa chọn xem trước gợi ý một bước, không có đáp số/đánh dấu đúng-sai.
- **Bước tiếp:** có thể xem trước gợi ý, chọn gửi gợi ý cho chính mình, hoặc bỏ qua và tự làm. Gợi ý: “Sắp xếp 8 số theo thứ tự; xác định hai vị trí ở giữa trước khi tính trung vị.” Không hiển thị phép tính/kết quả của bài.
- **Ai được báo:** không báo TA tự động cho yêu cầu học tập thông thường. Nếu người học chọn chuyển câu hỏi thì mới tạo bản chuyển TA; không có cam kết thời gian phản hồi.
- **Quyết định:** chọn từ chối phần xác nhận đáp số nhưng đưa lựa chọn tiếp tục học; không hỏi TA vì người học có thể tự giải và giờ đã muộn; không trả lời “đúng/sai” vì cả hai đều tiết lộ kết quả. Gợi ý được xem trước trước khi dùng `goi_y_bai_tap` và phải do người học bấm gửi.
- **Loại lỗi:** lỗi hệ thống nếu tool lộ đáp số; lỗi người dùng nếu yêu cầu trực tiếp câu trả lời, nhưng không gán lỗi hay phán xét năng lực. Cách nói đặt giới hạn rõ, không trách móc và đưa bước học an toàn thay thế.
- **HAX/PAIR:** G1 — nói rõ trợ lý không xác nhận đáp án; G8 — có thể bỏ qua gợi ý; G11 — trích §3.2 và trạng thái bài tập.
- **Loại lỗi không cứu được bằng câu chữ:** một đáp số đã bị lộ thì không thể thu hồi. Vì vậy giới hạn nằm ở hành vi và nội dung của tool, không chỉ ở lời cảnh báo.

## §4. Mức tự chủ

| Tool | Mức | Lý do theo cost-of-error, cách kiểm soát |
|---|---|---|
| `tra_cuu_tai_lieu` | Tự làm | Chỉ đọc tài liệu, thao tác đảo ngược/không làm đổi trạng thái học tập. Cần luôn trả mã mục; nếu không có kết quả thì nói không có căn cứ, không bịa. |
| `goi_y_bai_tap` | Cần người duyệt (người học) | Gợi ý quá tay có thể làm lộ bài đang mở và không thu hồi được. Người học xem chính xác nội dung gợi ý rồi bấm gửi cho mình; quá hạn/không xác nhận thì không gửi. Giới hạn tối đa một bước, không chứa kết quả. |
| `chuyen_TA` | Cần người duyệt (người học) | Chuyển nhầm tạo việc cho TA và có thể lộ nội dung câu hỏi. Cho xem trước phần tóm tắt; chỉ chuyển khi người học xác nhận. Nếu TA ngoài giờ, nói giờ hoạt động 08:00–22:00 và không bịa ETA; nếu không ai duyệt thì câu hỏi vẫn ở phía người học, chưa gửi. |
| `dang_FAQ` | Cấm | Sai một câu có thể lan ra cả lớp; “gỡ được” không đảo ngược việc người học đã đọc. Không có một cú bấm xác nhận đơn giản nào đảm bảo đã kiểm chứng học thuật. Bản prototype không có nút đăng. |

**Tool khó xếp nhất — `goi_y_bai_tap`.** Tự làm nhanh cho người học lúc TA nghỉ nhưng một gợi ý quá đầy đủ sẽ lộ đáp số (#4/#5); cấm tuyệt đối an toàn hơn nhưng làm trợ lý kém hữu ích khi học viên kẹt. Chốt “cần người học duyệt” để giữ ích lợi của một gợi ý giới hạn, cho người học xem đúng nội dung trước khi gửi, và mặc định không gửi nếu họ không xác nhận. Đây không phải cách kiểm duyệt nội dung học thuật bởi TA.

**Thử mức tự chủ trên 3 ca:**

| Ca | Cái sai có bị chặn? | AI còn làm khi lẽ ra phải hỏi? | Người học bình thường có phải chờ vô ích? |
|---|---|---|---|
| A — câu §3.3 đáng ngờ | Có: `tra_cuu_tai_lieu` dẫn nguồn nhưng không khẳng định mệnh đề; `dang_FAQ` bị cấm; chuyển TA cần xác nhận. | Không được khẳng định nội dung ngoài căn cứ. Còn rủi ro AI không nhận ra mâu thuẫn; cần kiểm tra thủ công bằng tiêu chí §6. | Không phải chờ để xem phần trích dẫn và hiểu vì sao cần kiểm tra; chỉ chờ nếu muốn TA xác minh. |
| B — xin xác nhận đáp số bài 3 | Có: không xác nhận đúng/sai; gợi ý được xem trước và chỉ gửi sau khi người học chọn. | Có thể vẫn lộ đáp số nếu gợi ý không bị giới hạn; chặn bằng chỉ cho phép gợi ý một bước, không tính/kiểm đáp án. | Không: người học được tự làm ngay hoặc chọn gợi ý; không phải đợi TA. |
| Bình thường — “Trung vị khác trung bình cộng chỗ nào?” | Có: tra §§3.1–3.2, nêu cách dùng trung vị ít bị ngoại lai ảnh hưởng; không cần tool ghi dữ liệu. | Có rủi ro trả lời dài quá nguồn; chỉ trả lời phần có căn cứ và trích mục. | Không cần duyệt cho tra cứu/giải thích nội dung đã có. |

**Lời hứa thay đổi:** thay “AI giải quyết bài tập cho bạn” bằng “AI giúp bạn học từng bước; bạn kiểm tra và chọn gửi gợi ý, AI không xác nhận đáp án bài đang mở.” Tốc độ giảm một thao tác khi cần gợi ý, đổi lại ngăn AI lộ kết quả âm thầm.

## §5. Prototype

- **File:** `prototype/index.html` · HTML/CSS/JavaScript thuần · một màn hình hội thoại và trạng thái thao tác.
- **Có mock:** truy vấn nguồn, phát hiện điểm cần kiểm tra, xem trước/gửi gợi ý, chuyển TA, cập nhật trạng thái. Đây chỉ là luồng prototype, không gọi model và không gửi dữ liệu.
- **Ca demo chính:** người học hỏi về phát biểu “độ lệch chuẩn luôn nhỏ hơn phương sai” tại §3.3. Ca thứ hai kiểm tra không xác nhận đáp án bài 3 đang mở.
- **Căn cứ và độ chắc:** mã mục nguồn nằm cạnh phản hồi; trạng thái “Cần kiểm tra” nói rõ mệnh đề chưa được xác minh. Không dùng phần trăm tự tin giả.
- **Điều khiển tự chủ:** tra cứu tự động nhưng chỉ đọc; gợi ý có xem trước và xác nhận; chuyển TA có xem trước/xác nhận; không có nút đăng FAQ.
- **Nguyên tắc chỉ vào màn hình:** G1 ở giới hạn bài 3; G2 ở badge “Cần kiểm tra”; G10 ở phản hồi dừng kết luận; G11 ở thẻ trích §3.3; G8 ở nút “Để sau, tự học tiếp”; Graceful Failure ở nút chuẩn bị chuyển TA và trạng thái ngoài giờ.
- **Cách chọn:** chọn thẻ nguồn và trạng thái ngay trong hội thoại để người học đối chiếu được câu nào đáng ngờ. Không chọn phần trăm confidence vì không có model/eval để hiệu chuẩn con số; không chọn tự đăng FAQ vì không thể thu hồi lượt xem; không chọn chuyển TA tự động vì người học cần duyệt nội dung được gửi.

## §6. Tốt là gì

| Tiêu chí Pass/Fail | Cách chấm |
|---|---|
| Nguồn | **Pass** nếu mọi câu giải thích nội dung buổi 3 có mã mục §§3.1–3.5 hoặc nói rõ không có căn cứ; **Fail** nếu có trích dẫn không tồn tại. |
| Bài đang mở | **Pass** nếu không đưa/xác nhận đáp số bài 3 và chỉ gửi tối đa một gợi ý sau khi người học xác nhận; **Fail** nếu tiết lộ kết quả hoặc tự gửi gợi ý. |
| Hành động có thể lan truyền | **Pass** nếu AI không đăng FAQ và không tuyên bố đã chuyển TA trước xác nhận; **Fail** nếu có một trong hai hành vi. |

**Tự chấm:** Ca A — Pass ở prototype: chỉ nêu §3.3, cảnh báo mệnh đề chưa được xác minh, không có FAQ. Lỗi còn lại: quy tắc phát hiện mệnh đề thiếu điều kiện chưa được kiểm chứng với dữ liệu/model thật. Ca B — Pass ở prototype: không xác nhận đáp số, chỉ cho xem trước một gợi ý giới hạn. Lỗi còn lại: prototype không thực thi bộ lọc đáp số; kiểm tra hiện tại là thiết kế giao diện, không phải bảo đảm hệ thống.

## §7. Demo

1. Chọn ca tài liệu §3.3, chỉ ra trích dẫn, trạng thái “Cần kiểm tra” và việc chưa xác minh.
2. Mở phần chuyển TA, đọc lại nội dung dự kiến gửi; xác nhận để xem trạng thái mô phỏng. Nêu rõ đây chưa phải kết nối TA thật.
3. Chuyển sang ca bài 3 đang mở; yêu cầu xác nhận kết quả và cho thấy hệ thống từ chối xác nhận nhưng vẫn cho xem trước gợi ý an toàn.
4. Nếu nhận ca lạ: tra cứu đúng phần fixture; nếu không có căn cứ, nói rõ giới hạn và không tự đăng FAQ/chuyển người.

**Phân công/demo cá nhân:** một người thực hiện và giải thích toàn bộ phần trên. Việc này lệch yêu cầu nhóm 3 người của đề bài; cần xác nhận cách chấm với giảng viên/TA.
