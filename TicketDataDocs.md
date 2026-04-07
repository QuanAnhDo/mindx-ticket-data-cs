# XÂY DỰNG KHO TRI THỨC HỖ TRỢ KỸ THUẬT MindX Ticket Knowledge Hub

---

## 1. TÌNH TRẠNG HIỆN TẠI & NHU CẦU CẤP THIẾT
Hiện nay, dữ liệu hỗ trợ kỹ thuật (Tickets) đang gặp các vấn đề sau:
- **Dữ liệu phân mảnh:** Nội dung xử lý lỗi nằm rải rác trong email, khó tra cứu lại khi gặp lỗi tương tự.
- **Khó khăn cho nhân sự mới:** Nhân sự CS hoặc TechTeam mới vào mất nhiều thời gian để hỏi lại các nghiệp vụ cũ (vd: Cách xử lý lỗi đóng tiền, lỗi LMS không hiện khóa học).
- **Thiếu tính hệ thống:** Các giải pháp chỉ mang tính thời điểm, chưa được đúc kết thành các bộ hướng dẫn (Guides) chuẩn chỉnh.

## 2. CHIẾN LƯỢC XÂY DỰNG KHO TRI THỨC TRÊN GITBOOK
Thay vì xây dựng các công cụ phần mềm phức tạp, giai đoạn này chúng ta tập trung vào việc **Tổ chức Thông tin (Information Architecture)** trên nền tảng **GitBook**:

### 2.1. Tại sao chọn GitBook?
- **Tìm kiếm thông minh (Semantic Search):** Nhân sự chỉ cần gõ hiện tượng lỗi (vd: "không nộp được bài"), hệ thống sẽ gợi ý các bài viết liên quan.
- **Phân loại khoa học:** Cho phép chia thư mục theo từng mảng nghiệp vụ (LMS, CRM, Tài chính, Vận hành).
- **Khả năng cộng tác:** Cả team có thể cùng đóng góp, chỉnh sửa và làm giàu nội dung Markdown một cách dễ dàng.

## 3. CẤU TRÚC TỔ CHỨC THÔNG TIN (CONTENT STRUCTURE)
Mỗi bài viết (Ticket tri thức) sẽ được chuẩn hóa theo cấu trúc:
1.  **Tiêu đề:** Tóm tắt ngắn gọn hiện tượng lỗi.
2.  **Phân loại (Tags):** Gắn nhãn hệ thống liên quan (#LMS, #Finance, #Enroll).
3.  **Hiện tượng:** Mô tả chi tiết vấn đề khách hàng gặp phải.
4.  **Cách xử lý:** Các bước thực hiện cụ thể để giải quyết lỗi.
5.  **Lưu ý nghiệp vụ:** Giải thích tại sao lỗi xảy ra để tránh lặp lại.

## 4. QUY TRÌNH VẬN HÀNH (WORKFLOW)
Dự án sẽ thực hiện theo 4 bước chuẩn hóa dữ liệu:
1.  **Thu thập:** Tổng hợp các ticket tiêu biểu từ Mail .
2.  **Chuẩn hóa:** Loại bỏ các trao đổi thừa, chỉ giữ lại cốt lõi nghiệp vụ và giải pháp.
3.  **Phân loại:** Đưa vào đúng danh mục trên GitBook và gắn thẻ (Tag) để tối ưu công cụ tìm kiếm.
4.  **Kiểm duyệt:** TechTeam định kỳ rà soát để cập nhật thông tin nếu nghiệp vụ hệ thống thay đổi.

## 5. PHÂN LOẠI ƯU TIÊN
Để đảm bảo dự án đi đúng hướng và tối ưu nguồn lực, các hạng mục được ưu tiên như sau:

- **MUST-HAVE:**
    - Thiết lập khung danh mục chuẩn trên GitBook (LMS, CRM, Tài chính).
    - Hoàn thiện thống kê các ticket hướng dẫn các lỗi phổ biến nhất hiện nay.
    - Đảm bảo tính năng tìm kiếm (Search) hoạt động chính xác trên GitBook.

- **SHOULD-HAVE:**
    - Hệ thống Gắn thẻ (Tagging) đồng bộ để lọc dữ liệu nhanh (#Finance, #Enroll).
    - Bộ quy tắc viết bài (Style Guide) để nội dung đồng nhất và dễ hiểu.
    - Phân quyền truy cập cho nhân sự theo từng nhóm nghiệp vụ.

- **COULD-HAVE:**
    - Video minh họa ngắn đính kèm cho các quy trình xử lý phức tạp.
    - Hệ thống phản hồi (Feedback) để người dùng đánh giá độ hữu ích của bài viết.
    - Tóm tắt nghiệp vụ (Summary) cho từng nhóm lỗi liên quan.

- **WON'T-HAVE:**
    - Tự động hóa hoàn toàn việc tạo bài viết (Tập trung chuẩn hóa nội dung bằng tay/bán tự động trước).
    - Giao diện tùy chỉnh riêng (Tận dụng giao diện mặc định chuyên nghiệp của GitBook).




