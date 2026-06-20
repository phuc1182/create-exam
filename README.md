# Phần mềm làm đề thi tương tác

Dự án này là một ứng dụng web 1 file (HTML + CSS + JavaScript) để làm bài trắc nghiệm trực tiếp trên trình duyệt.

## Mục tiêu

- Làm bài trắc nghiệm theo từng câu.
- Chấm điểm tự động khi nộp bài.
- Hiển thị đáp án đúng khi trả lời sai.
- Điều hướng nhanh giữa các câu hỏi.
- Nạp đề thi từ file JSON.

## Cấu trúc project

- `Làm đề_v2.html`: Giao diện và logic chính của ứng dụng.
- `mau_de_thi.json`: File mẫu định dạng đề thi để bạn tham khảo.

## Cách sử dụng

1. Mở file `Làm đề_v2.html` bằng trình duyệt (Chrome, Edge, Firefox...).
2. Bấm nút **Thêm đề từ file JSON** để chọn một hoặc nhiều file JSON.
3. Chọn đề ở ô **Chọn đề**.
4. Bấm **Bắt đầu làm bài**.
5. Chọn đáp án A/B/C/D cho từng câu.
6. Bấm **Nộp bài** để xem kết quả.

## Phím tắt

- `A`, `B`, `C`, `D`: Chọn nhanh đáp án.
- `ArrowLeft`: Về câu trước.
- `ArrowRight`: Sang câu tiếp theo.

## Định dạng JSON đề thi

File JSON cần có các trường cơ bản:

- `id`: Mã đề.
- `title`: Tên đề.
- `subject`: Môn học.
- `duration_minutes`: Thời gian làm bài (phút).
- `questions`: Danh sách câu hỏi.

Mỗi câu hỏi trong `questions` gồm:

- `id`: Số thứ tự câu.
- `text`: Nội dung câu hỏi.
- `options`: Các lựa chọn `A`, `B`, `C`, `D`.
- `answer`: Đáp án đúng (một trong `A/B/C/D`).
- `note` (tùy chọn): Ghi chú thêm.
- `table` (tùy chọn): Dữ liệu bảng hiển thị kèm câu hỏi.

Bạn có thể xem mẫu đầy đủ trong file `mau_de_thi.json`.

## Lưu ý

- Dự án không cần cài đặt thêm thư viện hoặc công cụ build.
- Chỉ cần mở file HTML là có thể sử dụng.
- Nếu JSON không đúng định dạng, ứng dụng sẽ báo lỗi khi import.
