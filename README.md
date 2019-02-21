# shopee-crawler
Shopee Vietnam Crawler

Tiếng Việt đi cho anh em nào có ghé quá dễ đọc. English update sau nhé.

- Tóm tắt: crawl tất cả sản phẩm từ shopee về theo danh mục.
- Trouble: về cơ bản thì shopee dùng json api, f12 lên là thấy, crawl bằng request quá dễ với bất kì anh em nào. Nhưng vấn đề chính là nó có 1 cái field `If-None-Match-` thay đổi theo mỗi request, không có nó thì data trả về đủ chẳng ra cái thể thống gì. Tôi không tìm ra nó được generate thế nào nên bỏ qua case này. Giải pháp tình thế là dùng puppeteer. Dành cho anh em nào chưa biết, puppeteer giả lập theo tác vào trang web, click chuột, gõ phím các kiểu gần như người bình thường, vào docs xem example là hiểu.
- `If-None-Match-` chứ không phải là `If-None-Match`, thêm 1 dấu `-` nữa. Trong request gốc send cả 2 field.
- Sau 1 hồi tìm kiếm thì có 1 thanh niên cũng trong tình cảnh tương tự: https://social.msdn.microsoft.com/Forums/security/en-US/6d77a7e8-12b3-42a3-89d8-a8c83f84a109/making-httpwebrequest-with-ifnonematch-header-etag?forum=csharpgeneral
