# Telegram 50 — Windows x64

Bản tùy biến từ [Telegram Desktop](https://github.com/telegramdesktop/tdesktop), giới hạn phía ứng dụng tối đa 50 tài khoản, Quick Replies và Auto Order.

**Bản hiện tại: 7.4.8 — TEST-API / Pre-release.** Đây là bản phát triển, chưa phải bản production hay bản phát hành chính thức của Telegram. Chưa xác minh 50 tài khoản đăng nhập thật.

## File gốc / Bộ cài đầy đủ — 7.4.8

Dùng khi cài lần đầu hoặc cập nhật thủ công. Bộ cài chứa đầy đủ ứng dụng; không cần cài lần lượt các phiên bản cũ.

| File | Tải xuống |
| --- | --- |
| **Bộ cài Windows x64 — EXE** | [Tải Telegram 50 Setup 7.4.8](https://github.com/tamchef1095-star/telegram50-updates/releases/download/v7.4.8/Telegram50Setup-TEST-API-Release-x64-7.4.8.exe) |
| Bản portable — ZIP | [Tải portable 7.4.8](https://github.com/tamchef1095-star/telegram50-updates/releases/download/v7.4.8/Telegram50-TEST-API-Release-x64-7.4.8.zip) |
| Mã nguồn đầy đủ — ZIP | [Tải source 7.4.8](https://github.com/tamchef1095-star/telegram50-updates/releases/download/v7.4.8/Telegram50-source-7.4.8.zip) |
| Mã kiểm tra file | [SHA256SUMS.txt](https://github.com/tamchef1095-star/telegram50-updates/releases/download/v7.4.8/SHA256SUMS.txt) |
| Báo cáo kiểm thử | [VALIDATION.json](https://github.com/tamchef1095-star/telegram50-updates/releases/download/v7.4.8/VALIDATION.json) |

[Xem Release Update 7.4.8](https://github.com/tamchef1095-star/telegram50-updates/releases/tag/v7.4.8)

## Các bản cập nhật

Nếu đã dùng Telegram 50 có auto update: vào **Cài đặt → Nâng cao → Kiểm tra cập nhật**, tải xong khởi động lại ứng dụng.

Gói `td-update-win-x64-*` dành cho bộ tự cập nhật, có hai chữ ký xác minh. Đây không phải file EXE để nhấp chạy; nếu muốn cập nhật thủ công, dùng bộ cài EXE ở trên.

| Phiên bản | Nội dung | Gói cập nhật |
| --- | --- | --- |
| **[Update 7.4.8](https://github.com/tamchef1095-star/telegram50-updates/releases/tag/v7.4.8)** | Đang được cung cấp qua auto update. Lịch sử theo ngày từng nhóm và tổng, từ khóa riêng theo nhóm, nút gạt trượt, mẫu order PR/inline. | [7004008](https://github.com/tamchef1095-star/telegram50-updates/releases/download/v7.4.8/td-update-win-x64-7004008) |
| [Update 7.4.7](https://github.com/tamchef1095-star/telegram50-updates/releases/tag/v7.4.7) | Lưu trữ: Auto Order UI v2, giới hạn nhận 1–3 task, không dùng ca. | [7004007](https://github.com/tamchef1095-star/telegram50-updates/releases/download/v7.4.7/td-update-win-x64-7004007) |
| [Bản gốc 7.4.4](https://github.com/tamchef1095-star/telegram50-updates/releases/tag/v7.4.4) | Lưu trữ: bản nền có auto update. | [7004004](https://github.com/tamchef1095-star/telegram50-updates/releases/download/v7.4.4/td-update-win-x64-7004004) |

[Xem tất cả Releases](https://github.com/tamchef1095-star/telegram50-updates/releases). Bản 7.4.5 là bản lưu trữ có lỗi cập nhật cũ; không khuyến nghị dùng để cài mới. Release 7.4.6 lỗi đã được gỡ; không dùng tag đó làm gói phát hành.

## File gốc lưu trữ — 7.4.4

Giữ để tham khảo phiên bản nền. Người cài mới nên dùng bộ cài 7.4.8 ở trên.

- [Bộ cài gốc 7.4.4 — EXE](https://github.com/tamchef1095-star/telegram50-updates/releases/download/v7.4.4/Telegram50Setup-TEST-API-AutoUpdate-Release-x64-7.4.4.exe)
- [Portable gốc 7.4.4 — ZIP](https://github.com/tamchef1095-star/telegram50-updates/releases/download/v7.4.4/Telegram50-TEST-API-AutoUpdate-Release-x64-7.4.4-portable.zip)
- [Mã nguồn bản gốc 7.4.4](https://github.com/tamchef1095-star/telegram50-updates/releases/download/v7.4.4/Telegram50-AutoUpdate-source-7.4.4.zip)

## Dữ liệu và cập nhật

Dữ liệu của bản tùy biến nằm riêng trong `Telegram50Data`. Không gỡ app hoặc xóa thư mục dữ liệu để cập nhật. Nếu chạy bộ cài thủ công, hãy thoát hẳn Telegram 50 trước. Bản 7.4.2 cũ chưa có updater nên cần cài bản mới một lần.

Cập nhật dùng feed và khóa xác minh riêng; không nhận gói cập nhật của Telegram gốc. Gói chỉ chứa file chương trình, không chứa phiên đăng nhập hoặc khóa ký riêng. Không sao chép `tdata`, `Telegram50Data`, OTP hay khóa riêng lên GitHub.

Rollback file chương trình đã được kiểm thử trên profile rỗng. Nếu quay về 7.4.7 sau khi nhận task theo mẫu PR/inline mới, Auto Order bản cũ có thể tạm dừng đọc dữ liệu đó; dữ liệu được giữ để mở lại bằng 7.4.8.

## Phạm vi kiểm thử 7.4.8

- Build/link Release Windows x64 thành công, Qt Release, LTO OFF, test harness OFF.
- Core: 62 cases / 20.724 assertions. Native Qt: 112 checks / 25 ảnh.
- Update/rollback gói đầy đủ: 34 checks. App 7.4.7 → 7.4.8 → 7.4.7 trên profile rỗng: 15 checks.
- Gói đã xác minh chữ ký native; cả 6 asset công khai và gói update tải lại khớp SHA256 với bản cục bộ.
- Đã dùng **0 tài khoản thật**, thực hiện **0 thao tác Telegram/Sheet thật**. Chưa xác minh nhận order/race thật, 50 tài khoản hoạt động ổn định hoặc phiên đăng nhập thật qua cập nhật.

Google Sheets tiếp tục OFF. Không tự đăng nhập hàng loạt hoặc bỏ qua xác minh Telegram.

## Mã nguồn và giấy phép

ZIP source đính kèm mỗi Release chứa mã nguồn tương ứng; một số bản cũ có thêm patch. Source 7.4.8 gồm working tree tùy biến và `SOURCE-BASE.json` ghi base/submodule. Base Telegram Desktop: `0128eeb40f2c969913eaf3c9eb741097b607f3b0`.

Giữ nguyên [LICENSE](LICENSE) và [LEGAL](LEGAL) upstream trong source và gói ứng dụng. Hướng dẫn build nằm trong `tools/telegram50/build-win64.ps1`; cơ chế ký trong `docs/telegram50-auto-update.md` bên trong gói mã nguồn. Khóa riêng không được phát hành.

## Feed đang dùng

[current6](https://github.com/tamchef1095-star/telegram50-updates/blob/main/current6) hiện cung cấp **7004008 / 7.4.8**. Feed chỉ được đổi sau khi upload, xác minh file và kiểm tra tải xuống thành công. Nhãn Pre-release trên GitHub không tắt feed riêng của Telegram 50.
