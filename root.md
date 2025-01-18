Tổng Quan về Root Thiết Bị Android Theo Chipset
Root một thiết bị Android yêu cầu mở khóa bootloader và sử dụng công cụ phù hợp theo từng loại chipset. Dưới đây là hướng dẫn cơ bản:

1. Yêu Cầu Cơ Bản
Mở khóa Bootloader: Bước bắt buộc trước khi root.
Root bằng Magisk: Công cụ phổ biến nhất để root Android.

2. Phương Pháp Root Theo Chipset

📌 Snapdragon
Có hai cách root:

Dùng TWRP (nếu thiết bị hỗ trợ):
Cài đặt TWRP Recovery. 
	fastboot flash recovery recovery.img
Flash Magisk.zip qua TWRP.

Dùng Fastboot (nếu thiết bị không có TWRP):
Patch boot.img bằng Magisk.
Flash boot.img đã patch qua fastboot:
	fastboot flash boot magisk_patched.img
	fastboot reboot
	
📌 MediaTek
Dùng Fastboot (tương tự Snapdragon):
Patch boot.img bằng Magisk.
Flash boot.img đã patch:
Sao chép
Chỉnh sửa
	fastboot flash boot magisk_patched.img
	fastboot reboot
Một số thiết bị MediaTek có chế độ Brom Mode yêu cầu SP Flash Tool để flash firmware.

📌 Samsung (Snapdragon & MediaTek)
Dùng Odin: Vì Samsung sử dụng định dạng boot khác (AP.tar thay vì boot.img).
Trích xuất firmware gốc, lấy file AP.tar.
Patch AP.tar bằng Magisk.
Flash file đã patch qua Odin vào chế độ Download Mode.
