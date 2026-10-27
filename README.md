# Portfolio CV - Hoàng Minh Quân

## Mô tả

Website portfolio cá nhân dạng trang tĩnh, giới thiệu Hoàng Minh Quân và các thông tin về kỹ năng, dự án, cơ hội nghề nghiệp và liên hệ. Giao diện được xây dựng theo hướng responsive để sử dụng trên điện thoại, máy tính bảng và máy tính.

## Chức năng

- Điều hướng nhanh đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Trình bày thông tin cá nhân, vai trò Frontend Developer và mô tả ngắn.
- Hiển thị các kỹ năng và dự án tiêu biểu dưới dạng thẻ.
- Cung cấp email và liên kết hồ sơ cá nhân.
- Bố cục thích ứng với nhiều kích thước màn hình, có hiệu ứng cuộn mượt.

## Công nghệ

- HTML5: cấu trúc nội dung có ngữ nghĩa.
- CSS3: giao diện, Flexbox, CSS Grid, biến CSS và responsive design.
- Không sử dụng framework, thư viện JavaScript, cơ sở dữ liệu hoặc quy trình build.
- Docker tùy chọn để phục vụ website qua Nginx.

## Yêu cầu môi trường

- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Một trong các hệ điều hành Windows, macOS hoặc Linux.
- Không cần cài Node.js hay trình quản lý gói để chạy website.
- Python 3 chỉ cần thiết nếu muốn chạy máy chủ HTTP cục bộ theo hướng dẫn bên dưới.
- Docker Engine và Docker CLI (hoặc Docker Desktop trên Windows/macOS) chỉ cần thiết nếu chạy bằng Docker.

## Cài đặt

Tải hoặc clone mã nguồn về máy, sau đó mở thư mục dự án. Cấu trúc chính:

```text
.
├── index.html
├── README.md
└── assets/
	├── css/
	│   └── styles.css
	└── img/
```

Không cần cài thêm dependency. Đảm bảo giữ nguyên đường dẫn tương đối giữa `index.html` và `assets/`.

## Cấu hình và tùy chỉnh

Dự án hiện không có tệp cấu hình, biến môi trường hay backend. Có thể tùy chỉnh trực tiếp:

- Nội dung, tên, email và liên kết trong `index.html`.
- Màu sắc, kiểu chữ, khoảng cách và bố cục trong `assets/css/styles.css`.
- Ảnh đại diện hiện được tải từ một URL bên ngoài, vì vậy cần kết nối Internet để hiển thị ảnh này. Có thể thay URL trong `index.html` bằng đường dẫn ảnh cục bộ.
- Các liên kết GitHub, LinkedIn và nút “Xem chi tiết” dự án hiện là liên kết mẫu (`#`); hãy thay bằng URL thật trước khi công bố.

## Chạy thử

### Windows

Mở PowerShell tại thư mục dự án và chạy máy chủ HTTP bằng Python:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có trên máy, thử `python -m http.server 8000`. Mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### macOS

Mở Terminal tại thư mục dự án:

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### Linux

Mở terminal tại thư mục dự án:

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

Với một trang HTML tĩnh đơn giản, cũng có thể mở trực tiếp `index.html` bằng trình duyệt. Dùng máy chủ HTTP giúp kiểm tra gần với cách website được phân phối hơn.

## Chạy bằng Docker

Cần cài và khởi động Docker trước. Các lệnh bên dưới dùng Nginx để phục vụ thư mục dự án chỉ đọc tại cổng `8080`; lần chạy đầu tiên Docker cần tải image `nginx:alpine`.

### Windows PowerShell

Chạy tại thư mục dự án:

```powershell
docker run --name portfolio-cv -d -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

### Windows Command Prompt (cmd)

Chạy tại thư mục dự án:

```bat
docker run --name portfolio-cv -d -p 8080:80 -v "%cd%:/usr/share/nginx/html:ro" nginx:alpine
```

### macOS và Linux

Chạy tại thư mục dự án:

```bash
docker run --name portfolio-cv -d -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Trên tất cả hệ điều hành, mở <http://localhost:8080> để xem trang. Quản lý container:

```bash
docker stop portfolio-cv
docker rm portfolio-cv
```

Nếu container `portfolio-cv` đã tồn tại, hãy dừng và xóa container cũ trước khi chạy lại. Nếu cổng `8080` đang được sử dụng, đổi phần `-p 8080:80` thành một cổng trống khác, chẳng hạn `-p 8081:80`, rồi mở cổng tương ứng trong trình duyệt.

## Thông tin liên hệ

- **Tên:** Hoàng Minh Quân
- **Email:** [hminhquan2811@gmail.com](mailto:hminhquan2811@gmail.com)
- **GitHub:** [github.com/hoangminhquan](https://github.com/hoangminhquan) (cần xác nhận/cập nhật liên kết thật)
- **LinkedIn:** [linkedin.com/in/hoangminhquan](https://linkedin.com/in/hoangminhquan) (cần xác nhận/cập nhật liên kết thật)
