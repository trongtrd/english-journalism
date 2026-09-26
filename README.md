# English Journalism

Skill biên tập bản nháp tiếng Anh về chính sách và kinh tế Việt Nam cho độc giả quốc tế, kèm giải thích tiếng Việt để học từ các thay đổi. Hướng phong cách được rút từ các lựa chọn biên tập trong Vietnam Weekly của Michael Tatarski; đây là dự án cá nhân, không phải sản phẩm chính thức hoặc được tác giả bảo trợ.

**Phiên bản: 0.1.3-provisional.** Có ví dụ và thử nghiệm nội bộ; chưa chứng minh khả năng mô phỏng giọng tác giả hoặc ưu thế nhất quán so với phiên bản trước. Chưa được cài toàn cục.

## Dùng ngay

Trong một task có quyền đọc repository, yêu cầu đọc [SKILL.md](SKILL.md), rồi đưa bản nháp của bạn. Ví dụ:

> Đọc SKILL.md trong repository này và dùng skill để biên tập bản nháp English dưới đây. Được sắp xếp lại cấu trúc nhưng giữ luận điểm, dữ kiện, nguồn và mức chắc chắn. Trả bản sửa tiếng Anh và 3–5 giải thích tiếng Việt với trích đoạn trước/sau.

Skill mặc định biên tập văn bản có sẵn; không phải công cụ dịch, luyện IELTS, viết bài từ đầu hoặc tự nghiên cứu kiểm chứng. Nếu chỉ cần sửa nhẹ, ghi rõ điều đó. Không cần dao-skill, yao-meta-skill hoặc kho bài nguồn khi sử dụng thông thường.

## Nội dung repository

- [SKILL.md](SKILL.md): quy trình và hợp đồng đầu ra.
- [Style guide](references/style-guide.md): 12 lựa chọn có điều kiện và nguồn tham chiếu.
- [Editing examples](references/editing-examples.md): ví dụ hư cấu, gồm hai bộ đối chiếu cách tổ chức đoạn.
- `agents/openai.yaml`: thông tin giao diện Codex; `agents/interface.yaml`: metadata tương thích bộ kiểm tra Yao.
- [Đặc tả ban đầu](docs/design-brief.md) và [kế hoạch phát triển](docs/development-plan.md).
- [Báo cáo thử nghiệm](reports/evaluation.md), [hướng dẫn đọc các ca thử](evals/README.md) và dữ liệu thử hư cấu.
- [Thông tin bản chuyển](reports/export.md): phạm vi sao chép và giới hạn.

Kho bài báo gốc không được đưa vào repository. Đường dẫn archive được nhắc trong style guide là dấu vết nguồn ở dự án ban đầu; liên kết bài công khai là nguồn tham chiếu có thể dùng tại đây. Không cần các đường dẫn archive để chạy skill.

## Đọc thử

- [Bản nháp dài](evals/inputs/long-draft.md).
- [Bản sửa sau retest](evals/v013/retest/L.md).
- [Ca xử lý dữ kiện sau retest](evals/v013/retest/R.md).

Tất cả các ca này là hư cấu có ghi nhãn, không phải kết quả nghiên cứu về một địa phương thật. Các bản trong `old/` và `new/` là kết quả lịch sử, có thể chứa lỗi được chỉ ra trong báo cáo.

## Phạm vi phân phối

Chưa chọn giấy phép nguồn mở; không suy ra quyền tái sử dụng các bài báo được dẫn nguồn. Repository giữ hướng dẫn, ví dụ tự tạo và bằng chứng thử nghiệm, không chứa toàn văn các bài nguồn. Nếu cài skill về sau, chỉ cần SKILL.md, references/ và agents/; các fixture và bản baseline trong evals/ phục vụ phát triển, không phải skill cần cài thêm.
