# Đóng gói và tương thích

Version: 0.1.4-provisional.

Nguồn hướng dẫn chạy là SKILL.md và hai tệp trong references/. Các quy tắc này không cần shell, API hoặc dịch vụ bên ngoài. agents/openai.yaml là metadata giao diện dành riêng cho Codex; agents/interface.yaml là metadata kiểm tra nội bộ, không phải adapter bảo đảm tương thích đa nền tảng.

Chạy `python scripts/package.py` để tạo lại hai bản phân phối:

- `dist/english-journalism.zip`: một thư mục english-journalism chứa SKILL.md, references/, agents/openai.yaml và VERSION.
- `dist/english-journalism-chat-guide.md`: nội dung hướng dẫn và ví dụ hợp nhất, với tham chiếu tệp được chuyển thành tham chiếu đến các phần trong cùng tài liệu.

Không đưa evals hoặc baseline vào gói cài đặt. Bản hợp nhất được tạo từ cùng nội dung runtime, không duy trì một bộ quy tắc riêng cho mỗi mô hình.

Lượt này kiểm tra: tên và cấu trúc ZIP, nội dung từng tệp trong ZIP so với runtime, liên kết Markdown cục bộ, tính đầy đủ của bản hợp nhất và các trường metadata. Đây là kiểm tra đóng gói, không phải kết quả chạy thực tế trên ChatGPT, Claude hoặc Antigravity. Chưa có đánh giá đầu cuối riêng cho từng nền tảng.

Các ca thử cũ vẫn được giữ để thể hiện giới hạn quan sát được; một số ghi chú trong baseline đã được biên tập nên không còn là bản lưu nguyên trạng. Thay đổi 0.1.4 chủ yếu là nội dung phân phối, cách trình bày style guide và tính di động; chưa thực hiện một vòng so sánh chất lượng mới.
