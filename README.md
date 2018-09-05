Xin chào các bạn, hôm này mình sẽ hướng dẫn các bạn sử dụng git để quản lý mã nguồn trên Ubuntu.
Để cài đặt git trên Ubuntu ta mở Terminal lên (có thể dùng phím tắt Ctrl + Alt + T) rồi gõ lệnh:

$ sudo apt-get install git

Sau khi load xong repository, ta nhấn Y sau đó nhấn Enter để bắt đầu quá trình download và cài đặt git lên Ubuntu.

Sau khi cài đặt xong, bạn có thể gõ lệnh:

$ git --version 

để kiểm tra phiên bản git vừa được cài đặt, nếu hiển thị phiên bản thì có nghĩa là việc cài đặt của chúng ta đã thành công.
Bây giờ để cấu hình git trên Ubuntu ta làm như sau:
$git config --global user.name <Tên tài khoản github của bạn>
$git config --global user.email <Email bạn dùng để đăng ký github>
$git init <Tên kho chứa> 

Ví dụ: mình muốn tạo kho chứa có tên là MyRepository thì gõ như sau:
$git init MyRepository
Nó sẽ tạo một kho chứa ngay thư mục chúng ta đang đứng (ở ví dụ trên là thư mục người dùng của mình).

Tiếp theo chúng ta sẽ di chuyển đến thư mục MyRepository vừa tạo.
$ cd MyRepository
Bây giờ chúng ta tạo 1 file bất kỳ trong thư mục này bằng cách:
$gedit hello.c
Câu lệnh trên dùng để mở chương trình gedit (1 trình soạn thảo có sẵn trên Ubuntu giống notepad trên Windows) và tạo mới 1 file có tên hello.c (nếu file này chưa tồn tại) hoặc mở file hello.c (nếu nó đã tồn tại).
Bạn gõ 1 đoạn code bất kỳ gì vào cho nó có nội dung (chương trình Hello World chẳng hạn :v).

Sau khi tạo xong file hello.c, bạn sử dụng câu lệnh:
git status
Câu lệnh này dùng để kiểm tra trạng thái git hiện tại.
Ở trên hình file hello.c đang có màu đỏ, có nghĩa là file hello.c chưa được thêm vào chỉ mục ở trên git. Để làm điều ta dùng câu lệnh:
git add <tên file>
Ví dụ ở đây là:
git add hello.c
Bây giờ ta sử dụng câu lệnh kiểm tra trạng thái git ở trên thì file hello.c lúc này đã chuyển sang màu xanh, tức là ta đã có thể đưa file này lên git.
Tiếp đến, để thực hiện đánh dấu phiên bản ta sử dụng lệnh:
git commit -m <Nội dung>
Chẳng hạn mình muốn đánh dấu phiên bản hello.c với nội dung là "Chương trình hello world" thì làm như sau:
git commit -m "Chương trình hello world"
Với tham số -m thể hiện đoạn message.
Để tìm hiểu thêm về lệnh commit thì ra gõ:
git commit --help
Sau khi commit xong, ta tiến hành tạo kho chứa ở trên trang chủ github bằng tài khoản của chúng ta.




Các bạn làm theo như hình, cũng rất đơn giản.
Sau khi tạo xong kho chứa, các bạn sẽ thấy phần link mình tô đen chính là link kho chứa trên github của chúng ta vừa tạo ra, các bạn copy lại để thực hiện lệnh tiếp theo.



Bây giờ ta sẽ kết nối git ở local tới git trên web bằng cách:
git remote add <tên> <url>
Trong đó "tên" bạn đặt bất kỳ còn "url" chính là đường link mà bạn vừa copy lúc nãy.
Ví dụ:
git remote add myGit https://github.com/xuho/MyRepository.git

Cuối cùng, để đưa file từ kho chứa local lên kho chứa của github, bạn sử dụng lệnh:
git push <tên> <nhánh>
Ví dụ ở đây tên đặt lúc trước là "myGit", nhánh mặc định là master (vì ta chưa tạo nhánh mới, mặc định là master luôn).
git push myGit master
Nó sẽ yêu cầu nhập username và pass tài khoản git của bạn.
Ok, vậy là code của bạn đã được đưa lên github, bạn có thể lên kiểm tra :).


Cám ơn các bạn đã theo dõi :D. 

