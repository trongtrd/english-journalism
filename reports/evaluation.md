# Kết quả kiểm chứng và giới hạn

## Lịch sử ngắn

v0.1.2 có ba ca giả định và hai validator cấu trúc đạt. Baseline no-skill chạy trước with-skill trong cùng task, nên so sánh có ảnh hưởng lịch sử. Một vòng thử trên các trích đoạn ngắn sau đó dùng hai task Sol High mới, cùng ba đoạn tối đa 45 từ và một task chấm ẩn nhãn: có khác biệt nhỏ về diễn đạt, chưa chứng minh giọng xuyên suốt.

## Vòng v0.1.3

Hai task Sol High mới chạy bản cũ và ứng viên trên cùng một bản dài giả định và ca kiểm dữ kiện. Đây là old-versus-new, không phải no-skill-versus-skill. Task chấm riêng nhận cặp ẩn nhãn; được dùng lại từ một phép thử khác, không có đầu ra hai ca mới trong lịch sử trước khi chấm.

- Bài dài: task chấm thích bản cũ hơn, do mở từ quyết định thực tế của doanh nghiệp.
- Ca dữ kiện: task chấm chọn bản cũ; ứng viên giữ nhãn nguồn chưa được ghi chú bằng chứng xác nhận rõ và một chú thích trích câu gần như không đổi.
- Astra làm rõ bước kiểm provenance và việc trích đúng câu thể hiện thay đổi; retest cả hai ca bằng cùng task ứng viên, giữ nguyên kết quả trước đó.
- Retest: hai lỗi cụ thể được xử lý; nội dung cần giữ còn đầy đủ. Cả 10 cặp trích đoạn khớp input/output. Bài dài sau retest có 372 từ phần thân; ca ngắn có 164 từ.

Retest có lịch sử và phản hồi nên không phải chiến thắng phong cách độc lập. Vẫn chưa có bản nháp thật hoặc lựa chọn của người dùng. Deployment status: provisional. Không công bố tỷ lệ mimic hoặc hiệu quả vượt trội.

## Bằng chứng kèm theo

- [Inputs và cách đọc](../evals/README.md).
- [Judge nguyên bản](../evals/v013/judgment.md) và [Astra review trước khi nhận judge](../evals/v013/astra-review.md).
- [Kiểm trích đoạn lượt đầu](../evals/v013/excerpt-checks.json) và [kiểm tra sau phản hồi](../evals/v013/post-feedback-checks.json).

Khóa nhãn lượt đầu: L: A=new, B=old; R: A=old, B=new. Các thư mục đã đặt tên điều kiện, vì vậy người đọc repository không được coi là người chấm mù. Toàn bộ kiểm tra trên là bằng chứng lịch sử của dự án nguồn; kiểm tra bản chuyển được ghi riêng tại [export](export.md).

## Công cụ

Dao quality_check và Yao validate_skill standalone đã đạt. CLI chính Yao 2.1.0 gặp lỗi import fcntl trên Windows; chương trình check_update.py chạy trực tiếp đã thành công, báo local/remote version đều 2.1.0 ngày 26/09/2026. Không sửa helper hoặc tuyên bố toàn bộ CLI hoạt động. Kiểm tra cấu trúc không chứng minh chất lượng giọng, và bộ trigger_eval theo cụm từ không được dùng làm bằng chứng router Codex thật.
