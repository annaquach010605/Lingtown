# LingoTown V2.0 — City + Academy (IELTS / HSK)

Đây là **bản nâng cấp từ LingoTown V1**, giữ lại City (từ vựng, 6 khu vực, minigames, XP/Coins, thú cưng) và bổ sung **Academy** để học Grammar, IELTS/giao tiếp và HSK. Chạy bằng HTML/CSS/JavaScript thuần, **không cần API key, Node.js hay backend**.

## Cập nhật lên GitHub Pages hiện có (không cần tạo repo mới)

1. Giải nén `LingoTown_V2_GitHub_Ready.zip`.
2. Truy cập **repository Lingtown** trên GitHub của bạn.
3. Chọn **Add file → Upload files**, upload 5 file vào **thư mục gốc** của repository: `index.html`, `academy.html`, `academy.css`, `academy.js`, `README.md`.
4. Khi GitHub hỏi về `index.html`/`README.md` cũ, hãy cập nhật file mới trong cùng đường dẫn (overwrite bằng commit mới). Nhấn **Commit changes**.
5. GitHub Pages đã bật sẵn ở **Settings → Pages** nên thường không cần bật lại. Chờ deploy; tải lại trang bằng **Ctrl + Shift + R** nếu trình duyệt còn cache bản cũ.
6. Mở link chính của game (đã có) → nhấn **🎓 IELTS & HSK**. Hoặc mở `https://<username>.github.io/Lingtown/academy.html` (điều chỉnh username/tên repository theo thực tế).

**Không upload trực tiếp file ZIP.** Khi dùng `github.com` Upload files, có thể chọn nhiều file từ máy cùng lúc.

## Tính năng hiện có trong Academy

- **Dashboard riêng English/Chinese**: mục tiêu IELTS 7.0–7.5; HSK từ kiến thức nền.
- **Placement Test mẫu**: 8 câu / ngôn ngữ, chỉ để định hướng, KHÔNG quy đổi thành band IELTS/HSK.
- **Grammar Lessons**: 6 chủ điểm/ngôn ngữ × 3 câu hỏi/chủ điểm, có giải thích và ví dụ.
- **Mini Practice**: English Reading/Listening/Vocabulary, Chinese Vocabulary-Pinyin/Listening/Grammar.
- **Speaking Corner**: nghe mẫu qua `speechSynthesis`, dùng `SpeechRecognition` khi trình duyệt hỗ trợ và cho phép microphone; có phương án nhập transcript thủ công. **Chỉ so khớp chữ, KHÔNG chấm chất lượng phát âm/ thanh điệu/IELTS Speaking.**
- **Writing**: bản nháp IELTS Task 2, đếm từ/đoạn/checklist; Trung: canvas viết chữ Hán, tự kiểm tra với gợi ý nét, và bài viết câu HSK theo đáp án mẫu. **Không tự chấm nét bút chính xác hay band IELTS.**
- **Smart Review**: lịch giãn cách 0–1–3–7–14–30–60 ngày (theo chuỗi đúng liên tiếp).
- **Error Tracking**: lưu câu sai, đáp án đã chọn, giải thích, điểm yếu theo kỹ năng và số câu đã làm.
- **Export/Import JSON**: sao lưu/khôi phục **dữ liệu Academy**.
- **Tích điểm trong City**: nếu tiến độ v1 tồn tại, các câu đúng trong Academy cộng XP/Coins vào v1. Tiến độ V1 được lưu nguyên ở `lingotown-save-v1`.

## Độ bao phủ nội dung / giới hạn

Đây là **bản V2.0 có thể trải nghiệm**, không phải kho nội dung đầy đủ của toàn bộ IELTS/HSK. Hiện có khoảng **36 câu Grammar**, **16 câu Placement Test**, **13 câu Mini Practice** và một số bài nói/viết mẫu. Cần mở rộng dần ngân hàng câu hỏi, cấp HSK và IELTS theo giai đoạn.

**Tính năng AI chưa có trong V2.0.** Smart Coach hiện dùng thống kê theo quy tắc (rule-based), không gọi mô hình AI, không hỗ trợ AI hội thoại tự do, không chấm ngữ âm thật và không chấm IELTS essay chuyên sâu. Các phần này cần giải pháp backend/auth và dịch vụ phù hợp; không đưa API key vào frontend GitHub Pages.

**Dữ liệu được lưu theo trình duyệt**, không đồng bộ thiết bị. Phần Academy có sao lưu riêng; dữ liệu City v1 chưa nằm trong file sao lưu Academy. Xóa dữ liệu trình duyệt hoặc thay thiết bị có thể mất tiến độ nếu không sao lưu.

## Cấu trúc

```text
LingoTown_V2/
├── index.html    # Game LingoTown v1 được giữ lại, thêm liên kết Academy
├── academy.html  # Learning Dashboard và các phân hệ học
├── academy.css   # Giao diện responsive
├── academy.js    # Nội dung học + gameplay + lưu điểm/lỗi
└── README.md
```

## Kiểm tra nhanh

1. Mở `index.html` và xác minh City/minigame vẫn chạy.
2. Nhấn `🎓 IELTS & HSK` để mở Academy.
3. Chọn English → Grammar → làm sai 1 câu → Errors sẽ ghi lại.
4. Chọn Smart Review → ôn câu vừa sai (due ngay).
5. Chọn Chinese → Writing → viết chữ Hán bằng chuột/cảm ứng.
6. Reload `academy.html` → tiến độ vẫn còn trong cùng trình duyệt.
7. Mở Errors → Sao lưu tiến độ, kiểm tra tệp `.json`.

Để kiểm tra micro, cần trang `https://` (GitHub Pages đã có HTTPS), quyền micro, và trình duyệt hỗ trợ Web Speech Recognition. Không phải trình duyệt nào cũng có tính năng này.
