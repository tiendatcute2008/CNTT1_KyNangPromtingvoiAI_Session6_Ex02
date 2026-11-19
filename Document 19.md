### BÀI LÀM: KHẮC PHỤC LỖI KHAI BÁO BIẾN SỐ TRONG PROMPT MẪU
#### BƯỚC 1: PHÂN TÍCH LỖI KHAI BÁO BIẾN SỐ LỘN XỘN
Cách khai báo biến số thiếu đồng nhất (`[language]` dùng ngoặc vuông chữ thường, `{audience}` dùng ngoặc nhọn chữ thường) gây ra nhiều trở ngại khi tự động hóa và sử dụng prompt mẫu:

1. **Khó tự động hóa bằng script / template parser:** Các hệ thống tự động hóa (như n8n, Make, Zapier, hay hàm thay thế chuỗi/regex) thường quy ước một cú pháp biến cố định (ví dụ chỉ nhận diện `[BIẾN]` hoặc `{{BIẾN}}`). Trộn lẫn `[...]` và `{...}` khiến bộ phân tích bỏ sót biến hoặc thay thế thiếu/sai.

2. **Dễ nhầm lẫn giữa biến số cần điền và nội dung cú pháp thật:** Trong nhiều ngữ cảnh kỹ thuật, JSON, cấu hình hoặc mã nguồn, ngoặc nhọn `{...}` hoặc ngoặc vuông `[...]` có thể là ký tự cấu trúc thực tế. Không quy ước rõ ràng dễ khiến người dùng hoặc hệ thống điền nhầm hoặc để sót biến chưa thay thế.

3. **Thiếu tính trực quan khi điền thủ công và khó chuẩn hóa ngôn ngữ:** Viết tên biến chữ thường tiếng Anh lẫn lộn (`language`, `audience`) trong prompt tiếng Việt làm giảm độ rõ ràng khi người dùng nhập liệu nhanh, dễ gõ sót dấu ngoặc hoặc nhầm thứ tự điền giá trị.
#### **BƯỚC 2: PROMPT MẪU ĐÃ ĐỒNG BỘ BIẾN SỐ**
Plaintext

`Hãy viết một bài chia sẻ ngắn gọn, rõ ràng về chủ đề Ứng dụng AI trong Học tập & Nghiên cứu bằng ngôn ngữ [NGÔN_NGỮ], dành cho đối tượng [ĐỐI_TƯỢNG].` ```Yêu cầu:` `- Trình bày có cấu trúc (mở đầu, ý chính dạng gạch đầu dòng, kết luận ngắn).` `- Ngôn ngữ và văn phong phù hợp với trình độ và nhu cầu của [ĐỐI_TƯỢNG].` `- Bắt đầu trực tiếp vào bài viết, không thêm lời chào xã giao.` 
#### **DỮ LIỆU THỰC TẾ ĐIỀN VÀO BIẾN**
- `[NGÔN_NGỮ]` = `Tiếng Việt`

- `[ĐỐI_TƯỢNG]` = `Sinh viên năm nhất ngành Công nghệ Thông tin`
#### **KẾT QUẢ CHẠY THỬ SAU KHI ĐIỀN DỮ LIỆU**
**Ứng dụng AI trong Học tập & Nghiên cứu dành cho Sinh viên năm nhất Công nghệ Thông tin**

Với sinh viên năm nhất ngành Công nghệ Thông tin, AI là công cụ hỗ trợ đắc lực để làm quen với kiến thức nền tảng, tư duy lập trình và phương pháp nghiên cứu tài liệu ngay từ sớm, miễn là sử dụng có phương pháp.

- **Hỗ trợ hiểu bài và giải thích khái niệm:** Khi gặp các chủ đề mới như cấu trúc dữ liệu, mạng máy tính hay thuật toán, bạn có thể yêu cầu AI giải thích từng bước hoặc dùng ví dụ trực quan để nắm bản chất trước khi đi sâu vào lý thuyết.

- **Rèn luyện tư duy đọc tài liệu và tóm tắt:** Thay vì đọc lan man nhiều nguồn rời rạc, AI giúp tóm tắt ý chính của bài báo, giáo trình hoặc tài liệu kỹ thuật, giúp bạn xác định nhanh trọng tâm cần nghiên cứu.

- **Review code và gợi ý sửa lỗi có định hướng:** Khi viết các đoạn code đầu tiên, AI có thể chỉ ra lỗi cú pháp, lỗi logic hoặc giải thích thông báo lỗi, nhưng bạn nên tự thử sửa trước để tránh phụ thuộc.

- **Lập kế hoạch ôn tập và tự kiểm tra:** Bạn có thể nhờ AI tạo câu hỏi trắc nghiệm, bài tập thực hành hoặc bảng tiêu chí tự đánh giá để kiểm tra mức độ hiểu bài trước kỳ thi.

Tóm lại, AI nên đóng vai trò như một trợ lý học tập và phản biện giúp sinh viên năm nhất rút ngắn thời gian làm quen kiến thức, trong khi tư duy phản biện và tự thực hành vẫn là yếu tố quyết định nền tảng chuyên môn.


