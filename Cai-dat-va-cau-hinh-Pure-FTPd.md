#Cài đặt và cấu hình Pure_FTPd

- Đầu tiên bạn cầu cài đặt EPEL

**#rpm -ivh http://download.fedoraproject.org/pub/epel/6/i386/epel-release-6-5.noarch.rpm**

- Tiếp đó bạn update lại các gói trong yum bằng lệnh:

**#yum update**

- Sau đó dùng lệnh **#yum install -y pure-ftpd** như bình thường

- Để Pure-ftpd chạy ổn định và an toàn hơn ta sửa file cấu hình bằng lênh:

**#vi /etc/pure-ftpd/pure-ftpd.conf**

- Đến dòng 77 đổi no thành yes để ngăn ko cho Anonymous được truy cập

<img src="http://i.imgur.com/qlP66MD.png">

- Đến dòng 143 bỏ dấu **#** để kích hoạt xác thực với Unix

<img src="http://i.imgur.com/LCzvb8y.png">

- Sau đó ta lưu file cấu hình lại và start dịch vụ và dùng lệnh kích hoạt dịch vụ cùng lúc với khi server khởi động

<img src="http://i.imgur.com/K00Dj7B.png">
