# FCJ Workshop Template

Website báo cáo thực tập và nội dung workshop của AWS FCJ, được xây dựng bằng Hugo và theme `hugo-theme-learn`. Website hỗ trợ hai ngôn ngữ: English và Tiếng Việt.

Website gồm các nội dung chính:

- Worklog theo từng tuần
- Proposal
- Các bài blog đã đăng
- Các sự kiện đã tham gia
- Tài liệu workshop AWS
- Tự đánh giá
- Phản hồi

## Công nghệ sử dụng

- [Hugo](https://gohugo.io/) - static site generator
- [Hugo Learn Theme](https://github.com/matcornic/hugo-theme-learn) - giao diện tài liệu
- Markdown - định dạng nội dung
- Mermaid - biểu đồ trong tài liệu
- GitHub Actions - build và deploy lên GitHub Pages

## Yêu cầu môi trường

- Hugo Extended `0.134.3` hoặc mới hơn
- Git

Kiểm tra Hugo đã được cài đặt:

```bash
hugo version
```

Trên macOS, có thể cài Hugo bằng Homebrew:

```bash
brew install hugo
```

## Chạy dự án local

Clone repository và di chuyển vào thư mục dự án:

```bash
git clone <repository-url>
cd fcj-workshop-template
```

Khởi động development server:

```bash
hugo server
```

Mở [http://localhost:1313](http://localhost:1313) trên trình duyệt. Hugo sẽ tự động rebuild và refresh trang khi file nguồn thay đổi.

Để hiển thị cả nội dung có `draft: true`, sử dụng:

```bash
hugo server -D
```

## Build website

Build phiên bản production vào thư mục `public/`:

```bash
hugo --minify
```

Có thể xem thử bản build tĩnh bằng một HTTP server đơn giản:

```bash
cd public
python3 -m http.server 8080
```

Sau đó mở [http://localhost:8080](http://localhost:8080).

Thư mục `public/` là kết quả sinh tự động, không chỉnh sửa trực tiếp nội dung trong thư mục này. Khi cần tạo lại, chạy lại lệnh `hugo --minify`.

## Cấu trúc dự án

```text
.
├── archetypes/       # Mẫu front matter cho nội dung mới
├── content/          # Nội dung Markdown của website
├── layouts/          # Partial và shortcode tùy biến của dự án
├── static/           # CSS, font, hình ảnh và tài nguyên tĩnh
├── themes/           # Hugo Learn Theme và các tùy chỉnh liên quan
├── config.toml       # Cấu hình Hugo, ngôn ngữ và theme
├── public/            # Website đã build, được Hugo sinh ra
└── .github/workflows/ # Quy trình build và deploy tự động
```

Các nhóm nội dung trong `content/`:

```text
content/
├── 1-Worklog/
├── 2-Proposal/
├── 3-BlogsPosted/
├── 4-EventParticipated/
├── 5-Workshop/
├── 6-Self-evaluation/
└── 7-Feedback/
```

Mỗi thư mục có thể chứa `_index.md` cho trang tổng quan và các thư mục con cho từng bài hoặc từng tuần. Bản tiếng Việt sử dụng hậu tố `.vi.md`, ví dụ `_index.vi.md`.

## Thêm hoặc chỉnh sửa nội dung

1. Tạo hoặc chỉnh sửa file Markdown trong thư mục phù hợp bên trong `content/`.
2. Khai báo front matter ở đầu file, tối thiểu thường có `title` và `weight`.
3. Chạy `hugo server -D` để xem kết quả local.
4. Kiểm tra cả hai ngôn ngữ nếu nội dung có bản English và Tiếng Việt.

Ví dụ một trang mới:

```markdown
---
title: "Tên bài viết"
weight: 10
---

Nội dung bài viết ở đây.
```

## Cấu hình quan trọng

Cấu hình chính nằm trong [`config.toml`](config.toml):

- Theme mặc định: `hugo-theme-learn`
- Ngôn ngữ mặc định: English
- Ngôn ngữ bổ sung: Tiếng Việt
- Theme variant: `workshop`
- Output trang chủ: HTML, RSS và JSON để hỗ trợ tìm kiếm
- Base URL production: `https://workshop-sample.awsfcaj.com/`

## Deploy

Workflow [`.github/workflows/hugo.yml`](.github/workflows/hugo.yml) được chạy khi có push lên nhánh `main`. Workflow sẽ:

1. Cài Hugo Extended `0.134.3`.
2. Build website bằng `hugo --minify`.
3. Deploy thư mục `public/` lên nhánh `gh-pages` bằng GitHub Pages.

Để deploy tự động, push thay đổi lên `main` và bảo đảm repository đã bật GitHub Pages với source là nhánh `gh-pages`.

## Theme và tùy biến

Theme nằm trong `themes/hugo-theme-learn/`. Các tùy biến riêng của website nên ưu tiên đặt trong `layouts/` và `static/` ở thư mục gốc để dễ bảo trì khi cập nhật theme.

## Giấy phép

Theme Hugo Learn được phát hành theo giấy phép MIT. Nội dung báo cáo và tài liệu trong repository thuộc về tác giả dự án.