# CMM Backup – Ứng dụng quản lý thi đua học đường

> Dự án React Native + Expo hỗ trợ theo dõi vi phạm nề nếp, lịch trực và bảng xếp hạng thi đua theo lớp/khối trong trường học.

## 1) Giới thiệu

**CMM Backup** là một ứng dụng di động được xây dựng để phục vụ công tác quản lý thi đua trong trường THPT. Ứng dụng cho phép:

- Đăng nhập theo vai trò (Admin, Sao đỏ, người dùng khác).
- Theo dõi lịch trực theo tuần.
- Xem thống kê vi phạm theo lớp/khối.
- Truy cập khu vực cá nhân và các chức năng quản trị.
- Gửi phản hồi và đăng ký thông tin trường.

Ứng dụng sử dụng mô hình điều hướng kết hợp:

- `Stack Navigator` ở mức app root.
- `Drawer Navigator` cho khu vực chính sau khi vào app.
- Các `Stack` lồng nhau cho từng nhóm chức năng.

---

## 2) Công nghệ sử dụng

- **Framework**: React Native (Expo)
- **Navigation**: React Navigation (stack + drawer)
- **UI**: React Native Paper
- **Lưu trữ cục bộ**: AsyncStorage
- **Thư viện bổ trợ**:
  - `expo-image-picker` (chọn ảnh)
  - `expo-file-system`, `expo-sharing`, `expo-media-library`
  - `react-native-super-grid`
  - `react-native-gifted-charts`
  - `crypto-es`

---

## 3) Cấu trúc thư mục chính

```text
.
├── App.js                 # Entry point, khai báo Stack root + theme
├── TotalScreen.js         # Drawer chính và các Stack lồng
├── Loading/               # Màn hình đăng nhập
├── Register/              # Màn hình đăng ký
├── Home/                  # Trang chủ
├── Grade/                 # Chọn/lọc theo khối lớp
├── Main/                  # Danh sách vi phạm chi tiết theo lớp/tuần
├── User/                  # Khu vực cá nhân + chức năng theo vai trò
├── Drawer/                # Drawer content tùy biến
├── Help/                  # Gửi phản hồi
├── Class/                 # Màn hình lớp (placeholder)
├── toolkit.js             # Hàm tiện ích xử lý thời gian/ngày giờ
└── url.js                 # Khai báo biến môi trường API
```

---

## 4) Luồng sử dụng cơ bản

1. Người dùng mở app tại màn `Loading`.
2. Chọn trường, vai trò và thực hiện đăng nhập.
3. Sau khi vào `TotalScreen`:
   - Truy cập `Home` để xem khối học và lịch trực.
   - Truy cập `Grade`/`Main` để xem vi phạm theo lớp.
   - Truy cập `User` (nếu có quyền) để dùng các chức năng nâng cao.
   - Truy cập `Help` để gửi phản hồi.

---

## 5) Cài đặt & chạy dự án

### Yêu cầu

- Node.js LTS
- npm hoặc yarn
- Expo CLI (tùy chọn, có thể dùng `npx expo`)

### Cài dependencies

```bash
npm install
```

### Chạy app

```bash
npm run start
```

### Chạy theo nền tảng

```bash
npm run android
npm run ios
npm run web
```

---

## 6) Liên hệ
Email: datduyle123456789@gmail.com
Github: https://github.com/didatium
