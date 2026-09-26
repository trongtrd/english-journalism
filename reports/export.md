# Bản chuyển sang repository độc lập

Ngày: 26/09/2026. Phiên bản: 0.1.3-provisional.

Năm file runtime được sao chép nguyên byte: SKILL.md, hai references và hai file agents. Giữ ví dụ và đầu ra hư cấu phục vụ kiểm chứng; bổ sung README, kế hoạch phát triển và báo cáo có liên kết tương đối để repository dùng độc lập.

Không đưa kho bài gốc, bài tải từ VnExpress, bản helper dao/yao, ứng viên xây dựng trung gian, tài khoản/đường dẫn máy hoặc nhật ký điều phối task vào repository. Bản gốc tại dự án VietnamWeekly vẫn giữ nguyên. Bản export không thay đổi hành vi skill.

Một số file source chỉ được mang theo dưới dạng báo cáo tóm tắt vì bản gốc liên kết tới kho nguồn và task cục bộ. Manifest [export-manifest.json](export-manifest.json) ghi hash file đã copy; các tài liệu mới được theo dõi bằng Git. Các dấu vết archive tương đối trong style guide chỉ giải thích nguồn ban đầu, không phải dependency của runtime.

Kiểm tra trước khi đẩy: so khớp runtime với nguồn, kiểm liên kết Markdown cục bộ và quét đường dẫn riêng/tokens, chạy hai validator standalone trên bản chuyển. Kết quả máy được ghi ở export-checks.json sau khi thực thi. Chưa cài skill toàn cục, chưa chọn giấy phép nguồn mở.
