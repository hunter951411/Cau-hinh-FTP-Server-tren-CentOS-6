#Cài đặt và cấu hình Vsftpd

- Để cài đặt Vsftpd ta dùng lệnh:

**#yum -y install vsftpd**

<img src="http://i.imgur.com/g5hjmDf.png">

- Tiếp theo để dùng Vsftpd chạy tốt nhất ta nên sửa một số thông số trong file vsftp.conf, ta dùng lệnh:

**#vi /etc/vsftpd/vsftpd.conf**

- Dùng lệnh **:set nu** để set dòng

- Tới dòng 12 sửa YES thành NO, để không bật chết độ enonymous, tránh cho người ngoài telnet hoặc ssh vào server.

<img src="http://i.imgur.com/2utFlwk.png">

- Tới dòng 81,82 bỏ dấu **#** phía trước, để bật chết độ ascii

<img src="http://i.imgur.com/Km8xuek.png">

- Tới dòng 96,97 bỏ dấu **#** phía trước để bật chroot
- Tới dòng 99 bỏ dấu **#** phía trước, để tạo list xác định chroot
- Tới dòng 105 bỏ dấu **#** phía trước

<img src="http://i.imgur.com/AkhgvgA.png">

- Thêm vào phía cuối file **local_root=public_html** xác định thư mục root(nếu không xác dịnh, thư mục home của người dùng sẽ trở thành thư mục home của FTP )
- Thêm dòng use_localtime=YES để sử dụng localtime

<img src="http://i.imgur.com/4DEph7a.png">

- Sau đó ta lưu những thay đổi của file lại.
- Tiếp theo ta sửa file chroot_list bằng lệnh:

**#vi /etc/vsftpd/chroot_list**

- Sau đó thêm vào người dùng không được áp dụng với chroot

<img src="http://i.imgur.com/HgFCA8L.png">

- Lưu file lại và start dịch vụ bằng lệnh:

**#/etc/rc.d/init.d/vsftpd start**

- Để dịch vụ chạy ngay khi server khởi động ta dùng lênh:

**#chkconfig vsftp on**

<img src="http://i.imgur.com/0fBlojd.png">
