# shopee-crawler
Shopee Vietnam Crawler

Tiếng Việt đi cho anh em nào có ghé quá dễ đọc. English update sau nhé.

- Tóm tắt: crawl tất cả sản phẩm từ shopee về theo danh mục.
- Trouble: về cơ bản thì shopee dùng json api, f12 lên là thấy, crawl bằng request quá dễ với bất kì anh em nào. Nhưng vấn đề chính là nó có 1 cái field `If-None-Match-` thay đổi theo mỗi request, không có nó thì data trả về đủ chẳng ra cái thể thống gì. Tôi không tìm ra nó được generate thế nào nên bỏ qua case này. Giải pháp tình thế là dùng puppeteer. Dành cho anh em nào chưa biết, puppeteer giả lập theo tác vào trang web, click chuột, gõ phím các kiểu gần như người bình thường, vào docs xem example là hiểu.
