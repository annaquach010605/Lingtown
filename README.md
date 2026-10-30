# LingoTown ✿ – Game học từ vựng English & Chinese

Game web (HTML/CSS/JavaScript thuần), giao diện pastel, chạy trực tiếp trên GitHub Pages. **Không cần Node.js, không cần `npm install` và không cần API key.**

## Chơi ngay trên máy

Mở file `index.html` bằng Chrome, Edge, Safari hoặc Firefox.

## Đăng lên GitHub Pages

1. Đăng nhập GitHub và tạo repository công khai tên `lingotown` (New repository → Public → Create repository).
2. Trong repository chọn **Add file → Upload files**; tải **file `index.html`** và `README.md` từ thư mục này lên (không tải file `.zip` vào repo). Sau đó bấm **Commit changes**.
3. Vào **Settings → Pages → Build and deployment**, chọn **Deploy from a branch**.
4. Đặt **Branch: `main`** và **Folder: `/(root)`**, rồi bấm **Save**.
5. Website sẽ có dạng `https://TEN-TAI-KHOAN.github.io/lingotown/` khi GitHub Pages triển khai xong. Đường dẫn chính xác sẽ hiển thị trong Settings → Pages.

> Nếu đặt repo tên `TEN-TAI-KHOAN.github.io`, game có thể xuất hiện tại trang gốc `https://TEN-TAI-KHOAN.github.io/`.

## Tính năng v1.0

- Chuyển chế độ **English / 中文** với tiến độ học riêng cho từng ngôn ngữ.
- **72 từ vựng cho mỗi ngôn ngữ**, 6 địa điểm, 144 mục học theo ngôn ngữ.
- Flashcard: từ, nghĩa tiếng Việt, Pinyin, phát âm (Web Speech API).
- Nhiệm vụ NPC (6 câu mỗi lượt); đạt 5/6 câu nhận sao, mở khu vực tiếp theo.
- Minigame ghép cặp và nghe/chọn từ.
- Sổ từ vựng tìm kiếm tiếng Anh, tiếng Trung, Pinyin và tiếng Việt.
- Ôn tập theo lịch giãn cách (Spaced Repetition) đơn giản.
- XP, Level, xu, sao, Daily Quest, chuỗi ngày học, thú cưng và shop.
- Tự lưu tiến độ trên thiết bị/trình duyệt bằng `localStorage`.
- Mobile responsive; không tải thư viện hay hình ảnh từ bên ngoài.

## Lưu ý

- Dữ liệu chỉ lưu **trên trình duyệt hiện tại**; xóa dữ liệu trình duyệt hoặc đổi thiết bị sẽ không tự đồng bộ. Muốn đồng bộ tài khoản sẽ cần backend/auth trong phiên bản tiếp theo.
- Phát âm phụ thuộc giọng đọc có sẵn trên máy. Một số thiết bị không có giọng đọc tiếng Trung; khi đó các phần học còn lại vẫn dùng bình thường.
- Đây là phiên bản MVP, hội thoại NPC mới ở dạng nhiệm vụ nhận diện từ, chưa có AI trò chuyện tự do.
- Chưa có chức năng tài khoản/đăng nhập hoặc mua hàng bằng tiền thật.

## Cấu trúc

```text
LingoTown/
├── index.html    # Toàn bộ game – không phụ thuộc file ngoài
└── README.md     # Hướng dẫn
```

## Gợi ý mở rộng

V2: animation bản đồ, nhiều loại nhiệm vụ, âm thanh chuyên nghiệp, battle/boss, nhiệm vụ theo ngày. V3: backend đăng nhập, đồng bộ cloud, đối thoại AI, luyện thanh điệu tiếng Trung.

Bản quyền nội dung/game: dùng cho mục đích học tập và cá nhân hóa.
