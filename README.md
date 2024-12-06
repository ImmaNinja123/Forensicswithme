# Forensicswithme
# Cách giải bài OperationOni
Theo cách của tôi để giải được bài này tôi sẽ dùng Auto spy để xem về file disk image :
Cách tạo bạn có thể tham khảo bằng chat gpt 
Sau khi tạo case và them file img của đề bài cho ta sẽ thấy giao diện như sau :
![image](https://github.com/user-attachments/assets/5e328ff0-c7c1-448e-83b3-1d6fae5cf159)
Ở đây ta sẽ tập trung vào disk image, tôi sẽ soát từng disk để xem nó, nghi ngờ ở vol3 và trong file root, ta nhận thấy sẽ có 2 file được mã khoá 
![image](https://github.com/user-attachments/assets/78ca6078-d4c6-4951-9bba-9288948e9de1)
Bước đầu tiên ta sẽ extract 2 file này ra môi trường mà bạn đang làm việc bằng chuột phải sau đó extract.
Sau khi extract xong ta sẽ xem được 2 file trong môi trường làm việc, ở đây tôi dùng ubuntu để xem.
![image](https://github.com/user-attachments/assets/3ae1b014-de5a-445f-9811-d0129bb44c96)
Ở đây ta sẽ đọc được 2 file này, vì ta không thể đoán được mật khẩu đối với loại mã hoá này nên tôi sẽ nghĩ cách để đặt lại mật khẩu cho nó.
Tôi sẽ thử đổi mật khẩu bằng câu lệnh như sau :
ssh-keygen -p -f path/to/your/key -m pem 
![image](https://github.com/user-attachments/assets/0cf14b4b-633e-4395-84fc-496e40dc44ae)
Từ đây ta đã thành công đổi mật khẩu cho việc đăng nhập.
Tiếp theo ta sẽ phải chỉ định thêm file khoá để kết nối tới sever, từ đó ta sẽ sử dụng được mật khẩu để đăng nhập vào sever.
Trước khi làm điều này tôi sẽ thử vào sever 
![image](https://github.com/user-attachments/assets/5414587a-9d5d-458d-ae4a-1871a7b0dc16)
khi đó nó bắt tôi phải nhập mật khẩu, nhận thấy rằng câu lệnh này sẽ chỉ định thêm khoá ở file tên key_file để kết nối tới sever.
Như vậy tôi sẽ đổi tên file khoá của mình thành Key_file
sau khi đổi tên xong tôi sẽ chạy lại sever như đề bài cho và ta sẽ vào được nó.


