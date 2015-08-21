#.I Câu lệnh về phân quyền
##1 User
**Định nghĩa**
<li> User là người có thể truy cập đến hệ thống
<li> User có username và password.
<li> Có 2 loại user: superuser ( root ) và regular user
<li> Mỗi user có một định danh riêng là UID ( của người dùng bình thường có giá trị bắt đầu từ 500 ) 
##2.  Group
<li>Group là tập hợp nhiều user lại.
<li>Mỗi user luôn là thành viên của một group.
<li>Khi tạo một user thì mặc định một group được tạo ra.
<li>Mỗi group còn có một định danh riêng gọi là GID.
<li>Định danh của group thường sử dụng giá trị bắt đầu từ 500.
##3.  Tập lệnh quản lý User và Group
###a. Tạo User:
Cú pháp: #useradd [option] <username>
<ul>
<li>-c “Thông tin người dùng”
<li>-d <Thư mục cá nhân>
<li>-m : Tạo thư mục cá nhân nếu chưa tồn tại
<li>-g <nhóm của người dùng>
<li>-p <tạo mậ khẩu>
</ul>
<li>Ví dụ: #useradd –c “Nguyen Van A – Server Admin” –g serveradmin vana
###b. Thay đổi thông tin cá nhân:
Cú pháp: #usermod [option] <username>
<ul>
Những option tương tự Useradd
<li>Ví dụ: #usermod –g kinhdoanh vana  //chuyển vana từ nhóm server admin sang nhóm kinh doanh.
</ul>
###c. Xóa người dùng
Cúpháp : #userdel [option] <username>
<ul>
<li>Vídụ :  #userdel  –r  vana
</ul>
###d. Khóa/Mở khóa người dùng
<li>passwd –l <username>  /  passwd –u <username>
<li>usermod –L <username> /  usermod –U <username>
<li>Trong /etc/shadow có thể khóa tài khoản bằng cách thay từ khóa x bằng từ khóa *.
###e. Tạo nhóm:
Cú pháp: #groupadd <groupname>
<ul>
<li>Ví dụ: #groupadd serveradmin
</ul>
###f. Xóa nhóm
Cú pháp: #groupdel <groupname>
<ul>
<li>Ví dụ: #groupdel <serveradmin>
</ul>
###g.  Xem thông tin về User và Group
Cú pháp: #id <option> <username>
<ul>
<li>Ví dụ: #id -g vana //xem GroupID của user vana
</ul>
Cú pháp: #groups <username>
<ul>
<li>Ví dụ: #groups vana //xem tên nhóm của user vana
</ul>
###h. Lệnh add user vào Group:
<li>usermod -g Sale jenln
##4.  Những file liên quan đến User và Group
/etc/passwd
<ul>
<li>Mỗi dòng trong tập tin gồm có 7 trường, được phân cách bởi dấu hai chấm.
</ul>
/etc/group
<ul>
<li>Mỗi dòng trong tập tin gồm có 4 trường, được phân cách bởi dấu hai chấm.
</ul>
/etc/shadow
<ul>
<li>Lưu mật khẩu đã được mã hóa và chỉ có user root mới được quyền đọc.
</ul>
##5.  Quyền hạn
###a. Trong Linux có 3 dạng đối tượng :
<li>	Owner (người sở hữu).
<li>	Group owner (nhóm sở hữu).
<li>	Other users (những người khác).
###b. Các quyền hạn :
<ul>
<li>	Read – r – 4  : cho phép đọc nội dung.
<li>	Write – w – 2  : dùng để tạo, thay đổi hay xóa.
<li>	Execute – x – 1  : thực thi chương trình.
</ul>
<li>Vídụ : Với lệnh ls –l ta thấy :
<ul>
[root@task ~]# ls -l
<li>total 32
<li>-rw-------. 1 root root  1416 Jan 10 14:06 anaconda-ks.cfg
<li>-rw-r--r--. 1 root root 15522 Jan 10 14:06 install.log
<li>-rw-r--r--. 1 root root  5337 Jan 10 14:06 install.log.syslog
<li>drwxr-xr-x  6 root root  4096 Feb  9 10:02 softs
</ul>
###d. Ngoài ra, chúng ta có thể dùng số.
<li>Vídụ : quyền r, w, x : 4+2+1 = 7
Tổ hợp 3 quyền trên có giá trị từ 0 đến 7.
##6.  Các lệnh liên quan đến quyền hạn
Lệnh Chmod : dùng để cấp quyền hạn.
<ul>
<li>Cú pháp : #chmod  <specification> <file>
<li>Ví dụ: #chmod 644 baitap.txt   //cấp quyền cho owner có thể ghi các nhóm các chỉ có quyền đọc với file taptin.txt
</ul>
	<li>Lệnh Chown : dùng thay đổi người sở hữu.
	<ul>
Cú pháp : #chown  <owner>  <filename>
</ul>
	<li>Lệnh Chgrp : dùng thay đổi nhóm sở hữu.
	<ul>
Cú pháp : #chgrp  <group>  <filename>
 </ul>
