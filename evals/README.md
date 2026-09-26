# Các ca kiểm tra

Tất cả input là hư cấu, có nhãn và không dùng để dẫn chứng về Việt Nam. Các file được sao chép từ các lượt thực thi đã có; không tạo lại đầu ra để làm đẹp kết quả.

- inputs/01-paragraph.md, 02-structure.md, 03-evidence.md: bộ pilot ban đầu.
- inputs/long-draft.md: bài dài mới ở vòng v0.1.3; không đưa cho task xây ví dụ.
- expectations.md: oracle dữ kiện của ba ca pilot, dành cho reviewer, không đưa vào task viết.
- v013/old/: đầu ra skill v0.1.2; v013/baseline-skill/: bản tham khảo của runtime cũ, đã lược bỏ ghi chú nguồn phát triển; không còn là bản lưu nguyên trạng để tái lập chính xác, không phải skill cần cài thêm.
- v013/new/: đầu ra ứng viên v0.1.3 trước sửa theo judge, có lỗi đã ghi nhận.
- v013/retest/: đầu ra sau khi làm rõ kiểm nguồn và chú thích; cùng task có lịch sử, không phải lượt chấm độc lập.

L là inputs/long-draft.md; R là inputs/03-evidence.md. Bài L được yêu cầu 330–450 từ English phần thân, kèm 3–5 chú thích Việt trích đúng câu trước/sau. Cả hai ca phải giữ luận điểm, số liệu, nguồn, độ chắc chắn và không tạo trải nghiệm. Giữ nguyên prompt trong từng input nếu replay; tách task giữa các phiên bản và không đưa oracle cho writer.

Nhãn judge lịch sử: L A=new/B=old; R A=old/B=new. Xem [báo cáo](../reports/evaluation.md) trước khi kết luận về chất lượng. Các bản old/new là bằng chứng lịch sử, không phải mẫu đã được chứng nhận đúng hoàn toàn.
