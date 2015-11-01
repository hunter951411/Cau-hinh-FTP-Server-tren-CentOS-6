#Cài đặt và cấu hình ProFTPD


- Đầu tiên bạn cầu cài đặt EPEL

**#rpm -ivh http://download.fedoraproject.org/pub/epel/6/i386/epel-release-6-5.noarch.rpm**

- Tiếp đó bạn update lại các gói trong yum bằng lệnh:

**#yum update**

- Sau đó dùng lệnh **#yum install -y proftpd** như bình thường

<img src="http://i.imgur.com/3tld7pX.png">

- Để Provsftpd có thể chạy tốt nhất ta sửa lại file cấu hình như sau:

-  Dùng lệnh **#vi /etc/protfpd.conf**

- Đến dòng 8 sửa **ServerName** thành tên server của bạn(hostname)

- Đến dòng 10 sửa ServerAmin thành địa chỉ Email của bạn

<img src="http://i.imgur.com/Mn6ysO4.png">

- Lưu cấu hình lại, và đến sửa file ftpusers, ta dùng lệnh **#vi /etc/ftpusers

- Thêm người dùng bạn muốn cấm truy cập ở đây mình để cấm **user trung**

<img src="http://i.imgur.com/hHQVeyV.png">

- Sau đó bật dịch vụ lênh, và cho dịch vụ chạy cùng khi server khởi động

<img src="http://i.imgur.com/U49vQ11.png">
