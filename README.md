# Thanh Vân Tu Tiên Lục: gói web game

Game MMO tu tiên chibi chạy thẳng trên trình duyệt, không cần cài đặt.

## Có gì trong gói
| Tệp | Công dụng |
|---|---|
| `index.html` | Toàn bộ game (mã, đồ họa, âm thanh đều nằm trong file này) |
| `game-data.json` | Toàn bộ dữ liệu cấu hình: lớp, thần thông, yêu thú, bản đồ, nhiệm vụ, linh thú, thú cưỡi, hồn kỹ, công thức cân bằng |
| `manifest.webmanifest`, `sw.js`, `icons/` | Biến game thành ứng dụng cài được (PWA), chơi được khi mất mạng |
| `extras/ban-goc-co-anh-mat-phap-tu.html` | Bản gốc có ảnh mặt Pháp Tu nhúng sẵn, KHÔNG nên đăng công khai |

## Chạy thử trên máy
Phải chạy qua máy chủ web nhỏ thì PWA mới hoạt động:
```
cd thư-mục-này
python3 -m http.server 8080
```
Mở `http://localhost:8080`. Mở trực tiếp `index.html` bằng cách nhấp đúp vẫn chơi được nhưng không có chế độ cài ứng dụng.

## Đăng lên web (miễn phí)
- **Netlify Drop**: vào app.netlify.com/drop, kéo cả thư mục vào.
- **GitHub Pages**: đưa các tệp vào repo, bật Pages ở Settings.
- **Cloudflare Pages** hoặc **Vercel**: kéo thả hoặc nối với GitHub.

## Cần biết
- Phần **online** (chat thế giới, bảng xếp hạng, thấy người chơi khác) chỉ chạy trong claude.ai. Ngoài đó game tự chuyển sang chế độ chơi đơn.
- Nhân vật lưu trong trình duyệt từng máy (localStorage), tách riêng theo từng địa chỉ web. Muốn có tài khoản thật cần thêm máy chủ (Firebase, Supabase...).
- Phông chữ lấy từ Google Fonts, không có mạng sẽ dùng phông thay thế.
- Tên đạo hữu giả lập mượn từ truyện huyền huyễn nổi tiếng. Nếu phát hành rộng nên đổi sang tên nguyên bản.
- Khi sửa `index.html`, hãy đổi `const V = 'tutien-v1'` trong `sw.js` sang số mới để người chơi nhận bản cập nhật.
