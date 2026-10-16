# 🎂 Birthday VR — Chúc mừng sinh nhật Tuấn Kiệt

Một món quà sinh nhật dưới dạng thế giới **3D tương tác** được xây dựng bằng HTML, CSS, JavaScript, **Three.js** và WebXR. Có thể khám phá trên điện thoại hoặc máy tính.

## 🌐 View Demo

### 🎮 [NHẤN VÀO ĐÂY ĐỂ XEM BẢN DEMO TRỰC TIẾP](https://hachngochai.github.io/TonKet_Birthday/)

**Địa chỉ GitHub Pages:** https://hachngochai.github.io/TonKet_Birthday/

> 💡 Link ở trên dành cho tất cả mọi người và không cần tài khoản GitHub. Nếu trình duyệt lưu bản cũ, có thể mở `https://hachngochai.github.io/TonKet_Birthday/?v=3.0` hoặc tải lại trang không dùng cache.

## ✨ Tính năng

- Thế giới sinh nhật 3D, điều khiển bằng chuột hoặc cảm ứng và có trải nghiệm xoay nhìn 360°.
- **Nhãn tương tác 3D nhỏ gọn** nổi phía trên hộp quà, nhân vật, bánh sinh nhật và lá thư; tối ưu cho mobile.
- **Font Noto Serif** hỗ trợ tiếng Việt, nội dung chúc mừng gọi trực tiếp **Tuấn Kiệt**.
- Mở quà, chạm vào bánh sinh nhật, cắm từng cây nến, sử dụng micro để thổi nến; có thao tác thay thế nếu không thể cấp quyền micro.
- Phát giai điệu *Happy Birthday to You* tổng hợp bằng Web Audio sau khi nến tắt.
- Lá thư xuất hiện sau giai điệu, chạm vào để đọc lời chúc.
- WebXR VR dành cho thiết bị và trình duyệt hỗ trợ; các thiết bị khác vẫn có thể xem 3D bình thường.

## 🚀 Chạy project và triển khai

Dùng **Live Server** trong VS Code hoặc chạy:

```bash
python -m http.server 5500
```

Mở `http://localhost:5500/`. Nếu triển khai qua GitHub Pages, trong **Settings → Pages** chọn **Deploy from a branch**, nhánh **main**, thư mục **/ (root)**.

## 📌 Lưu ý

- Truy cập demo qua **HTTPS** để trình duyệt có thể xin quyền micro. Phần phát hiện tín hiệu thổi được xử lý trong trình duyệt, không gửi ghi âm lên máy chủ.
- Three.js và font Google cần kết nối internet. VR qua kính đòi hỏi WebXR tương thích.
- Nhân vật chibi hiện là mô hình cách điệu, chưa phải bản tái dựng khuôn mặt 3D từ ảnh thật.

**🎉 Happy Birthday, Tuấn Kiệt!**
