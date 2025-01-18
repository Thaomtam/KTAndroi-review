Hướng Dẫn Chi Tiết Root Android Không Cần TWRP
1️⃣ Đối Với Thiết Bị Không Có TWRP
👉 Bước 1: Tải boot.img hoặc init_boot.img
Nếu ROM có boot.img và init_boot.img, chọn init_boot.img.
Nếu ROM chỉ có boot.img, sử dụng boot.img.
👉 Bước 2: Patch boot.img hoặc init_boot.img bằng Magisk
Cài đặt Magisk trên điện thoại.
Mở Magisk → Chọn "Patch a file" → Chọn boot.img/init_boot.img.
Chờ Magisk patch xong, file mới sẽ nằm trong thư mục /Download.
👉 Bước 3: Flash file đã patch bằng Fastboot
Khởi động vào Fastboot Mode:
Dùng tổ hợp phím cứng (thường là Power + Volume Down).
Hoặc dùng ADB:
adb reboot bootloader
Flash file đã patch:
Nếu file là boot.img
	fastboot flash boot patchboot.img
Nếu file là init_boot.img
	fastboot flash init_boot initboot.img
Reboot lại máy
fastboot reboot
✔ Máy sẽ khởi động lại và có root!

2️⃣ Đối Với ROM Có Recovery (Dễ Dàng Hơn)
👉 Cách Cài TWRP Hoặc OrangeFox Recovery
Khởi động vào Fastboot Mode.
Flash recovery
	fastboot flash recovery recovery.img
Reboot vào Recovery Mode:
	fastboot reboot recovery
Trong TWRP/OrangeFox:
Chọn Install.
Chọn Magisk.zip.
Kéo để cài đặt.
Reboot lại máy.
✔ Xong, máy có root!
