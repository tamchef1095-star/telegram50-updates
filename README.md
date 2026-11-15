# Telegram 50 — Windows x64

Bản tùy biến từ [Telegram Desktop](https://github.com/telegramdesktop/tdesktop), giữ giao diện gốc, mở giới hạn phía ứng dụng lên 50 tài khoản và thêm mẫu trả lời nhanh cục bộ.

[Tải bản 7.4.4](https://github.com/tamchef1095-star/telegram50-updates/releases/tag/v7.4.4)

## Cập nhật

Bản 7.4.4 có cơ chế cập nhật gốc của Telegram Desktop, dùng feed và khóa xác minh riêng. Gói cập nhật cần hai chữ ký hợp lệ; không nhận gói phát hành của Telegram gốc. Tự kiểm tra và tải nền, sau đó khởi động lại để áp dụng.

Bản 7.4.2 cũ chưa có updater nên cần cài bản mới một lần. Dữ liệu nằm riêng trong `Telegram50Data`. Hãy thoát hẳn Telegram 50 trước khi chạy bộ cài. Giữ dữ liệu khi gỡ cài đặt nếu muốn giữ phiên đăng nhập. Không sao chép tdata hoặc khóa ký lên kho này.

## Phạm vi đã kiểm thử

- Debug và Release x64 biên dịch thành công; Qt Release, tối ưu tốc độ, LTO tắt.
- 58/58 kiểm thử xác minh chữ ký đạt.
- Kiểm thử cục bộ qua HTTP: gói bị sửa bị từ chối; gói hợp lệ nâng 7.4.3 → 7.4.4, thay EXE và mở lại renderer thành công.
- Marker trong hồ sơ thử giữ nguyên. EXE đang cài và Registry gỡ cài đặt hiện có không thay đổi.
- Kiểm thử auto update dùng **0 tài khoản thật**, gửi **0 tin nhắn**. Chưa xác minh 50 tài khoản hoạt động ổn định hoặc giữ phiên đăng nhập thật qua bản cập nhật này.

Đây là build phát triển dùng **TEST API upstream có hạn chế**, chưa phải bản production có api_id/api_hash riêng. Không bỏ qua xác minh đăng nhập hoặc tự đăng nhập hàng loạt.

## Mã nguồn và giấy phép

Mỗi Release chứa ZIP mã nguồn tương ứng và patch đầy đủ. Bản 7.4.4 dựa trên commit `0128eeb40f2c969913eaf3c9eb741097b607f3b0` của Telegram Desktop. Giữ nguyên LICENSE và LEGAL upstream trong source và gói ứng dụng. Đây là bản tùy biến độc lập, không phải bản phát hành chính thức của Telegram.

Để khôi phục checkout có submodule:

```sh
git clone https://github.com/telegramdesktop/tdesktop.git
cd tdesktop
git checkout 0128eeb40f2c969913eaf3c9eb741097b607f3b0
git submodule update --init --recursive
git apply --binary ../telegram50-auto-update-7.4.4.patch
```

Hướng dẫn build nằm trong `tools/telegram50/build-win64.ps1`; cơ chế ký nằm trong `docs/telegram50-auto-update.md`. Khóa riêng không được phát hành.

## Feed

`current6` trên nhánh `main` chỉ được cập nhật sau khi file Release đã tải xuống và kiểm tra SHA-256 thành công. Mỗi tính năng mới vẫn cần build, kiểm thử, ký và phát hành trước khi ứng dụng nhận được.

