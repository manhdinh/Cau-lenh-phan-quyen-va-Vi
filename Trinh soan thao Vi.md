#I.Khái niệm
Chương trình vi là một chương trình soạn thảo mạnh mà gần như chắc chắn được tìm
thấy trên tất cả các hệ điều hành họ UNIX bởi kích thước và khả năng của nó.vi
không đòi hỏi nhiều tài nguyên, thêm vào đó là các chức năng soạn thảo cơ bản. vi có
thể tìm kiếm, thay thế, và kết nối các file,và nó có ngôn ngữ macro của chính nó, cũng
như một số các đặc điểm bổ sung
#II.Các chế độ trong Vi
##1.Chế độ thứ nhất là chế độ input. Trong chế độ này, văn bản được đưa vào trong tài
liệu, bạn có thể chèn hoặc bổ sung văn bản.
##2.Chế độ thứ hai là chê độ dòng lệnh. Khi ở chế độ này, bạn có thể dịch chuyển trên tài
liệu, trộn các dòng, tìm kiếm, …Bạn có thể thực hiện tất cả các chức năng của vi từ
chế độ dòng lệnh ngoại trừ việc nhập vào văn bản. Văn bản chỉ có thể được vào trong
chế độ input. 
#.III Các câu lệnh
<li>Ctrl + D : Chuyển cửa sổ xuống bằng một nửa màn hình
<li>Ctrl + U : Chuyển cửa sổ lên bằng một nửa màn hình
<li>Ctrl + F : Dịch chuyển cửa sổ lên phía trước bằng một màn hình
<li>Ctrl + B : Dịch chuyển cửa sổ về phía sau một màn hình
<li>k hoặc up arrow : Dịch chuyển con trỏ lên một dòng
<li>j hoặc down arrow : Dịch chuyển con trỏ xuống một dòng
<li>l hoặc right arrow : Dịch chuyển con trỏ sang phải một ký tự
<li>h hoặc left arrow : Dịch chuyển con trỏ sang trái một kí tự
<li>Return : Dịch chuyển con trỏ đến vị trí bắt đầu dòng tiếp theo
<li> - : Dịch chuyển con trỏ đến vị trí bắt đầu của dòng trước
<li>w : dịch chuyển con trỏ đến vị trí bắt đầu của từ tiếp theo
<li>b : dịch chuyển con trỏ đến vị trí bắt đầu của từ trước
<li>^ : hoặc 0 dịch chuyển con trỏ đến vị trí bắt đầu của dòng hiện tại
<li>$ : dịch chuyển con trỏ đến vị trí kết thúc của dòng hiện tại 
<li>i,a : Chèn văn bản ngay trước/sau vị trí con trỏ
<li>o : Mở một dòng mới ngay sau dòng hiện tại
<li>O : Mở một dòng mới ngay trước dòng hiện tại
<li>x : Xóa ký tự sau con trỏ
<li>dw : Xoá một từ (bao gồm cả ký tự trống ngay sau nó)
<li>D : Xoá từ vị trí con trỏ đến kết thúc dòng
<li>d^ : Xoá từ vị trí bắt đầu dòng ñến vị trí ký tự trống hay ký tự bên
trái con trỏ
<li>u : Huỷ bỏ thay đổi trước ñó
<li>/pattern : Tìm xâu pattern. Theo hướng tiến.
<li>?pattern : Tìm xâu pattern, theo hướng lùi về ñầu văn bản.
<li>n,N : Lặp lại việc tìm kiếm theo cùng hướng / ngược hướng
<li>p, : P Dán đoạn văn bản vừa xoá vào trước / sau con chạy
<li>. : Lặp lại câu lệnh cuối.
<li>dd : Xóa dòng có con trỏ chạy
<li>:w : Ghi lại tất cả các thay đổi của file hiện tại và tiếp tục soạn thảo
<li>:q! : Kết thúc, không lưu trữ bất kỳ thay ñổi
<li>:ZZ : Lưu thay đổi của file hiện tại và kết thúc. 
