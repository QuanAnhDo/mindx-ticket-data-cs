# QUY TRÌNH VẬN HÀNH (WORKFLOW DIAGRAMS) - GIAI ĐOẠN 1

## 1. Quy trình Nghiệp vụ Hiện tại (Current Business Workflow)
Sơ đồ mô tả luồng công việc thủ công: Từ lúc nhận Mail đến khi đăng tải lên GitHub để đồng bộ GitBook.

```mermaid
graph TD
    A[Email Ticket từ Khách hàng] --> B{Lọc & Lựa chọn}
    B -->|Lỗi tiêu biểu/phổ biến| C[Trích xuất nội dung từ Odoo/Mail]
    B -->|Lỗi cá nhân| D[Bỏ qua]
    
    C --> E[Chuẩn hóa nội dung theo Template Markdown]
    E --> F[Gắn Metadata vào file .md]
    F --> G[Tạo mới/Push file lên GitHub Repo]
    
    G --> H((GitHub Sync))
    H --> I[Dữ liệu hiển thị trên GitBook]
    
    I --> J[Nhân sự mới Tra cứu/Search]
    J --> K[Áp dụng xử lý thực tế]
```

---

## 2. Luồng Tương tác Hệ thống (System Sync Flow)
Mô tả cách dữ liệu được luân chuyển giữa các nền tảng trong giai đoạn thủ công hiện tại.

```mermaid
sequenceDiagram
    participant P as Nhân sự TechTeam (User)
    participant G as GitHub Repository
    participant GB as GitBook Platform

    P->>P: 1. Thu thập & Chuẩn hóa nội dung (Manual)
    P->>G: 2. Commit & Push file .md (vào thư mục /tickets)
    
    Note right of G: GitHub kích hoạt Webhook
    
    G->>GB: 3. Tự động đồng bộ nội dung mới
    
    Note over GB: 4. Cập nhật Mục lục & Chỉ mục tìm kiếm
    
    GB-->>P: 5. Tra cứu kết quả trên giao diện Web
```

---

## 3. Cấu trúc chuẩn của một bài viết (Template Structure)
Đảm bảo mọi thành viên khi đăng bài lên GitHub đều tuân theo quy chuẩn này để GitBook hiển thị tốt nhất.

```mermaid
classDiagram
    class MarkdownFile {
        +YAML Frontmatter (Tags, Description)
        +Section: Hiện tượng (Phenomenon)
        +Section: Cách xử lý (Solution)
        +Section: Lưu ý nghiệp vụ (Business Note)
    }
    
    MarkdownFile --> YAML : #LMS, #Finance
    MarkdownFile --> Content : Nội dung chi tiết
```
