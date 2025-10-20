# Hướng dẫn Remake Code (file: script.js)

Tất cả chỉnh sửa bạn cần làm đều nằm trong file script.js. Làm theo các bước dưới đây để tùy biến lại project theo ý bạn:

---

## 1. 🖼️ Thêm Ảnh ở dòng **87**

- Tới dòng **87** trong script.js
- thay length tương ứng với số ảnh ở folder images

---

## 2. 📝 Thay Text ở dòng **614**

- Tìm tới dòng **614** trong script.js
- Thay nội dung văn bản thành bất kỳ nội dung nào bạn muốn.
- Ví dụ: thay tiêu đề, mô tả, lời chào, v.v.

---

## 3. 🎵 Bật Nhạc Nền

- Trong `index.html` đã có thẻ `<audio id="bg-music">` với nguồn MP3 hợp lệ.
- Trong `script.js` hàm `preloadGalaxyAudio()` sẽ gán nguồn MP3 và `playGalaxyAudio()` sẽ phát nhạc.
- Do chính sách trình duyệt, nhạc sẽ phát khi bạn CLICK lần đầu vào scene (khi intro bắt đầu).

### Cách thay nhạc từ YouTube:

1. **Tải MP3 từ YouTube:**

   - Dùng tool online: yt-dlp, 4K Video Downloader, hoặc youtube-dl
   - Hoặc dùng website: y2mate.com, savefrom.net
   - Lưu file dạng `.mp3`

2. **Upload lên hosting:**

   - Upload file MP3 lên Google Drive, Dropbox, hoặc GitHub
   - Lấy link trực tiếp (phải kết thúc bằng `.mp3`)

3. **Cập nhật code:**
   - Sửa mảng `audioSources` trong `script.js` dòng 820-825
   - Thay link YouTube bằng link MP3 thật
   - Ví dụ: `'https://drive.google.com/uc?export=download&id=FILE_ID'`

### Debug nhạc không phát:

1. **Mở DevTools (F12) > Console** để xem log:

   - `🎵 Attempting to play audio:` - đang thử phát
   - `✅ Audio started successfully` - thành công
   - `❌ Audio play failed:` - lỗi gì đó

2. **Kiểm tra:**

   - Tab trình duyệt có bị mute không (icon loa bị gạch)
   - Volume máy tính có bật không
   - Click vào hành tinh để kích hoạt phát nhạc

3. **Nếu vẫn không được:**
   - Thử link MP3 khác: `https://www.soundjay.com/misc/sounds/bell-ringing-05.wav`
   - Hoặc tải file MP3 về máy, đặt trong folder `galaxy/` và dùng `'./music.mp3'`
