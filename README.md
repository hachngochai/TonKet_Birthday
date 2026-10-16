# 🎂 Birthday VR V2 — Chúc mừng sinh nhật em Chu Tuấn Kiệt

## View Demo

🌐 **[View Demo — Birthday VR V2](https://hachngochai.github.io/TonKet_Birthday/)**

Trải nghiệm sinh nhật 3D bằng **HTML/CSS/JavaScript + Three.js + WebXR**. Sử dụng font **Be Vietnam Pro** hỗ trợ dấu tiếng Việt.

## Trải nghiệm

- Chạm vào không gian 3D để mở hộp quà; nhân vật giới thiệu bằng bong bóng lời thoại 3D.
- Khám phá đảo nổi 360° bằng chuột hoặc cảm ứng.
- Chạm vào bánh để zoom, sau đó **cắm 5 cây nến lần lượt**.
- Đồng ý cấp quyền micro rồi thổi để tắt nến. Ngưỡng âm lượng đo dựa trên tiếng ồn nền; nếu không cấp quyền có thể chạm vào bánh thêm lần nữa để tiếp tục.
- Sau khi nến tắt, website phát **giai điệu Happy Birthday to You tổng hợp bằng Web Audio** (không phải bản thu giọng hát).
- Hết nhạc, lá thư 3D rơi xuống; chạm vào thư để xem lời chúc dành cho **em Kiệt**.
- Nếu thiết bị hỗ trợ WebXR immersive VR, nút vào VR sẽ xuất hiện.

## Chạy local

Mở thư mục repo trong VS Code bằng Live Server hoặc chạy `python -m http.server 5500`, sau đó truy cập `http://localhost:5500/`. Cần internet để tải Three.js và Google Fonts.

## GitHub Pages

Repository: [hachngochai/TonKet_Birthday](https://github.com/hachngochai/TonKet_Birthday). Trong Settings → Pages chọn nguồn **Deploy from a branch**, branch **main**, folder **/ (root)**. Truy cập URL View Demo ở đầu README.

## Lưu ý

- Hãy cấp quyền micro sau khi chạm vào bánh; HTTPS GitHub Pages cho phép trình duyệt hỏi quyền. Âm thanh micro được xử lý cục bộ để phát hiện tín hiệu, không tải lên máy chủ.
- Trên thiết bị không hỗ trợ kính VR, có thể khám phá bằng xoay nhìn 360°.
- Hiện nhân vật chibi là mô hình cách điệu tạo bằng hình học; **chưa ghép ảnh chân dung thật**.
- Nếu thấy phiên bản cũ, hãy làm mới trang không dùng cache.
