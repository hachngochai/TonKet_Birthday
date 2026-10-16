# 🎉 KIỆT'S BIRTHDAY UNIVERSE — 3D · 360° · VR

Website sinh nhật dành cho **Chu Tuấn Kiệt**, xây dựng bằng **HTML/CSS/JavaScript ES Modules + Three.js + WebXR**. Không cần backend hoặc framework build.

## Tính năng

- 6 chương: mở quà, đảo nổi, avatar có mặt thật, không gian 360°, thổi nến, sân khấu pháo hoa.
- Nhân vật chibi có khuôn mặt ghép bằng ảnh thật đã tách từ poster (photo-face trên hình học 3D). Có thể thay bằng ảnh riêng; đây **không phải bản quét khuôn mặt 3D**.
- Dùng chuột/cảm ứng xoay 3D; panorama 360° dùng được trên máy tính/điện thoại.
- **WebXR immersive VR**: nút VR tự xuất hiện **chỉ khi** trình duyệt + thiết bị hỗ trợ headset. WebXR cần HTTPS (GitHub Pages đáp ứng).
- Web Audio tạo nhạc chúc mừng và hiệu ứng sau khi người dùng bật âm thanh. Không phụ thuộc MP3 bên ngoài.
- Tự tối ưu tỷ lệ pixel/particle cho mobile, có dự phòng khi WebGL không chạy, và lưu ý `prefers-reduced-motion`.

## Chạy local

**Không** nhấp đúp `index.html` bằng giao thức `file://` vì ES Modules, texture và WebXR cần web server.

**VS Code:** cài extension **Live Server**, mở thư mục project, nhấn **Go Live**. Hoặc chạy:

```bash
python -m http.server 5500
```

Mở `http://localhost:5500/`. Phải có internet để tải thư viện Three.js từ CDN và font Google (có font hệ thống dự phòng).

## Đăng lên GitHub Pages

1. Tạo repository GitHub mới, ví dụ `birthday-kiet`.
2. Tải **toàn bộ file và thư mục nằm bên trong** dự án lên root repository, sao cho `index.html` nằm ngay root.
3. Vào **Settings → Pages → Build and deployment**.
4. Chọn **Deploy from a branch**, branch `main`, folder `/ (root)` rồi **Save**.
5. Đợi workflow Pages hoàn thành, mở `https://<github-user>.github.io/birthday-kiet/`.
6. Sau khi sửa file `config.js` hoặc ảnh, commit/push rồi tải lại trang (có thể hard-refresh).

> Đường dẫn trong code là tương đối (`./assets/...`), nên deploy với repo path vẫn chạy. Đừng đặt import `three` ở địa chỉ tuyệt đối thuộc domain riêng.

## Cá nhân hóa

File `js/config.js` chứa:
- `name`: tên người sinh nhật.
- `birthdayMessage`, `secretMessage`: hai lời chúc.
- `poster` và `face`: đường dẫn ảnh.
- `scenes`: tiêu đề, mô tả, nút bấm của sáu cảnh.

Ảnh gốc là `assets/chu-tuan-kiet-poster.jpg`; ảnh mặt tách nền oval là `assets/kiet-face.png`. Để ghép mặt chính xác hơn, cung cấp một ảnh chân dung rõ nét, chính diện, ánh sáng tốt rồi thay file PNG đã được tách nền, giữ nguyên tên file.

## Hướng dẫn điều khiển

- **PC:** kéo chuột để xoay quanh mô hình, cuộn chuột để zoom, chạm vật thể để kích hoạt; phím ← / → chuyển cảnh.
- **Mobile:** vuốt để xoay, chạm để tương tác; nút **360°** mở thế giới xung quanh.
- **VR headset:** khi hỗ trợ WebXR immersive-vr, nhấn **ENTER VR** và sử dụng nút trigger của tay cầm để chọn vật thể. Có thể chọn các trạm tương tác trong thế giới 360°.

### Lưu ý thực tế về VR

- Xem 360° bằng chuột/cảm ứng **không tương đương** VR stereo immersive qua headset. WebXR VR thực sự chỉ có trên thiết bị/trình duyệt hỗ trợ. iPhone/Safari thông thường **không có WebXR immersive VR**; vẫn xem 360° bằng thao tác vuốt.
- VR dùng web scene 3D (không cần một file video 360 hay ảnh pano chụp sẵn).
- Modal HTML chỉ hiển thị ở chế độ màn hình thông thường; trong kính VR, các trạm vẫn có vật thể 3D để chọn. Nếu muốn bảng lời chúc đọc trực tiếp trong headset, có thể bổ sung scene-anchored 3D text panels.

## Cấu trúc

```text
birthday-vr-chu-tuan-kiet/
  index.html
  style.css
  .nojekyll
  README.md
  assets/
    favicon.svg
    chu-tuan-kiet-poster.jpg
    kiet-face.png
  js/
    audio.js
    config.js
    main.js
    world.js
```

## Kỹ thuật / lưu ý

- Three.js **0.180.0** import map CDN jsDelivr.
- Các hình khối được tạo theo thủ tục (procedural geometry), không có file GLB phụ thuộc bên ngoài.
- Nếu bị trang trống: kiểm tra Developer Tools → Console, internet/CDN, đường dẫn chữ hoa/chữ thường và kiểm tra thư mục asset.
- App sử dụng poster mà người triển khai cung cấp; nếu đưa lên repo public, hãy chắc rằng bạn có quyền sử dụng/chia sẻ ảnh.

**Chúc mừng sinh nhật Chu Tuấn Kiệt!** 🎂