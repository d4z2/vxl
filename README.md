# Luyện thi Kỹ thuật vi xử lý (APK)

Nội dung ứng dụng nằm trong `www/index.html` (một file duy nhất, chạy offline).
Đóng gói thành APK bằng Capacitor.

## Cách 1: Build trên GitHub (không cần cài gì)
1. Tạo tài khoản GitHub (miễn phí), tạo repository mới, ví dụ `luyen-thi-vxl`.
2. Tải toàn bộ thư mục này lên repository (nút "Add file" > "Upload files"). Nhớ tải cả thư mục ẩn `.github`.
3. Vào tab **Actions** > "Build APK" > **Run workflow**. Đợi khoảng 5–8 phút.
4. Mở lần chạy vừa xong, kéo xuống mục **Artifacts**, tải `luyen-thi-vxl-apk` (file zip chứa `app-debug.apk`).

## Cách 2: Build trên máy (Android Studio)
Cần Node.js 18+, JDK 17, Android Studio.
```
npm install
npx cap add android
npx cap sync android
npx cap open android
```
Trong Android Studio: Build > Build Bundle(s) / APK(s) > Build APK(s).
File nằm ở `android/app/build/outputs/apk/debug/app-debug.apk`.

## Cài lên Samsung
1. Chép file `app-debug.apk` sang điện thoại (Zalo, Drive, cáp USB, hoặc tải trực tiếp).
2. Mở file bằng ứng dụng "Tệp của tôi" (My Files). Khi được hỏi, bật **Cho phép cài đặt từ nguồn này**.
3. Nếu Google Play Protect cảnh báo ứng dụng chưa xác minh, chọn **Vẫn cài đặt**. Đây là bình thường với APK tự build.

## Cập nhật nội dung
Sửa `www/index.html`, đẩy lên GitHub và chạy lại workflow để ra APK mới.
