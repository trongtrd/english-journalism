> Historical design brief from the original build; repository export is now authorized.

# Đặc tả thiết kế — dao-skill

Ngày: 26/09/2026. Đây là đầu vào đã chốt cho giai đoạn yao-meta-skill, không phải skill thành phẩm.

## Mục tiêu gốc

Giúp người dùng chuyển bản nháp English về chính sách/kinh tế Việt Nam thành bài newsletter dễ đọc, có giọng báo chí rõ ràng, giàu giải thích và hoài nghi có căn cứ, đồng thời hiểu các lựa chọn biên tập để tự viết tốt hơn.

## Người dùng, hoàn cảnh và định hướng

Dùng cá nhân cho blog/newsletter hướng tới độc giả quốc tế có quan tâm nhưng không có nhiều bối cảnh Việt Nam. Được phép sửa sâu cả cấu trúc. Giọng giải thích qua hệ quả đời sống làm nền, kết hợp hoài nghi có căn cứ và nhận xét sắc; không tự thêm thái độ, kết luận hoặc trải nghiệm của người viết.

## Nguyên tắc và đánh đổi

- Nội dung của bản nháp là ràng buộc: giữ dữ kiện, nguồn, quan điểm và mức chắc chắn; phát hiện vấn đề thì nêu riêng, không sửa thành sự thật do AI tự tạo.
- Học cấu trúc, cách dẫn dắt, nhịp câu và lựa chọn ngôn ngữ từ ví dụ có nguồn. Viết câu mới; không ghép các câu đặc trưng từ bài mẫu.
- Phong cách là tập lựa chọn theo ngữ cảnh, không phải công thức bắt buộc. Chỉ dùng câu hỏi tu từ, nhận xét hoài nghi, đoạn ngắn hoặc mở bằng đời sống khi đầu vào hỗ trợ.
- Với người đọc quốc tế, giải thích thuật ngữ từ dữ kiện sẵn có; thiếu bối cảnh quan trọng thì ghi điểm cần xác minh. Không tự nghiên cứu web trừ khi được yêu cầu.

## Dạng skill và quy mô

Cognitive Distillation Skill: chắt lọc kỹ thuật từ tư liệu thành lựa chọn biên tập, kèm một quy trình biên tập ngắn. Một prompt chung không lưu được nguồn và điều kiện áp dụng; chưa cần toolbox, scripts tự động hay hệ thống tìm kiếm. Yao mode: Scaffold cho cá nhân.

Target root: repository root (`.`).
Skill name: english-journalism. Các meta-skill đã cài là read-only. Không cài global hoặc xuất bản trong lượt xây này.

## Đầu vào và đầu ra

Đầu vào tối thiểu: một đoạn hoặc bài English do người dùng muốn biên tập. Tùy chọn: nguồn đã có, độ dài, bối cảnh, điểm muốn giữ. Không yêu cầu điền form nếu bản nháp đã đủ để làm việc.

Đầu ra mặc định:

1. Bản sửa tiếng Anh hoàn chỉnh, có thể sao chép; giữ hoặc đề xuất tiêu đề khi phù hợp.
2. 3–5 thay đổi đáng học, giải thích tiếng Việt với đối chiếu trước/sau. Với đoạn cực ngắn, không bịa thêm thay đổi chỉ để đủ số lượng.
3. Điểm cần tác giả xác minh/chốt nếu thực sự có; không tạo mục cảnh báo rỗng.

Chế độ phân tích chi tiết chỉ khi người dùng yêu cầu. Khi chỉ sửa lỗi tối thiểu được yêu cầu rõ, không tự áp đặt biên tập sâu. IELTS, dịch toàn văn, viết từ đầu, fact-check độc lập không thuộc chức năng mặc định.

## Quy trình và tiêu chí kiểm tra

Hiểu luận điểm → kiểm tra thông tin cần giữ → chẩn đoán cấu trúc → chọn kỹ thuật có điều kiện → sửa → đối chiếu nội dung → giải thích.

Chạy ba tình huống tổng hợp được gắn nhãn: sửa đoạn, tổ chức lại bài, xử lý nhận định thiếu nguồn. So sánh cùng mô hình High và cùng bản nháp; ghi rõ ảnh hưởng lịch sử thử nghiệm nếu không tách được ngữ cảnh. Bài đối chiếu nguồn phong cách và bản nháp thử hành vi là hai loại tư liệu khác nhau.

Đạt kiểm tra nội bộ khi không có sai lệch nội dung quan trọng, có thể chỉ ra kỹ thuật đã dùng và giải thích đúng thay đổi. Chỉ người dùng mới xác nhận mức hợp gu. Chưa có bản nháp thật hoặc phản hồi: bàn giao bản thử, không tuyên bố hiệu quả đã được chứng minh.

## Phân quyền thực thi

Điều phối: thiết kế, chọn nguồn, tích hợp và quyết định chất lượng. Luna Max: kiểm kê/kiểm tra có tiêu chí rõ. Sol High: rút kỹ thuật và xây theo yao; task Sol High riêng: thử hành vi. Không tự giao việc tiếp sang task khác. Thư mục ghi được chỉ định trong từng nhiệm vụ.
