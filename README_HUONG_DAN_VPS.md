# 📺 HƯỚNG DẪN TRIỂN KHAI TDSHOP TRÊN VPS DVTSHOPHCM.COM

## 1. Cấu trúc thư mục trên VPS
Hãy tạo thư mục `/var/www/dvtshophcm.com/iptv/tdshop/` trên VPS và upload toàn bộ các file trong thư mục `server_tdshop` này lên:

```text
/var/www/dvtshophcm.com/iptv/tdshop/
├── admin/
│   └── index.php              <-- Trang Web Admin dành riêng cho TDShop trên PC
├── api.php                    <-- API cấp phát luồng & tự kích hoạt thiết bị
├── playlist.m3u               <-- Danh sách kênh riêng của TDShop
├── notification.json          <-- Thông báo chữ chạy riêng của TDShop
└── admin_config.json          <-- Cấu hình mật khẩu quản trị (Tự sinh)
```

## 2. Phân quyền trên VPS (Linux)
Chạy lệnh sau trên VPS để cấp quyền ghi cho file danh sách kênh và thông báo:
```bash
sudo chown -R www-data:www-data /var/www/dvtshophcm.com/iptv/tdshop/
sudo chmod -R 775 /var/www/dvtshophcm.com/iptv/tdshop/
```

## 3. Đường link bàn giao cho đối tác TDShop:
- **Trang Quản Trị Kênh (Duyệt trên máy tính PC/Điện thoại)**:
  `https://dvtshophcm.com/iptv/tdshop/admin/index.php`
  - **Mật khẩu mặc định**: `tdshop2026` (Bên TDShop có thể tự đổi sang mật khẩu khác trong trang web).
- **Link Playlist M3U Trực Tiếp**:
  `https://dvtshophcm.com/iptv/tdshop/playlist.m3u`
