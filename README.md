# Web-SangTaoTruyen
## Giới thiệu:
- Dạng web: SPA

- Công nghệ sử dụng:

    - FrontEnd: HTML, javaScript, ReactJs, SASS/SCSS, Redux-Toolkit,SignalR,...
   
    - BackEnd: Asp.net core Api, entity framework, Sql Server,SignalR,...

- Deploy: "http://sangtaotruyen.surge.sh/"
 
- Tài khoản có thể dùng:
    - tài khoản: "admin" ; mật khẩu: "admin"
## Chức năng:
### Người dùng
          +) Đăng nhập, đăng ký.
          +) Cập nhật thông tin tài khoản người dùng, đổi mật khẩu.
          +) Xác thực tài khoản bằng email, khôi phục mật khẩu bằng email.
          +) Tìm kiếm, lọc truyện theo nhiều dạng dữ liệu.
          +) Xắp sếp theo nhiều dạng dữ liệu.
          +) Phân trang.
          +) Lịch sử đọc truyện, đọc tiếp phần trước.
          +) Truyện mới cập nhật, truyện đánh giá cao.
          +) Đánh dấu truyện yêu thích.
          +) Đánh giá truyện.
          +) Đề cử truyển, lịch sử đề cử, tự động tăng lượt được đề cử hàng ngày khi đăng nhập.
          +) Thích chương truyện.
          +) Thích bình luận cấp 1, thích bình luận cấp 2.
          +) Thích đánh giá cấp 1, thích phản hồi đánh giá.
          +) Bình luận 2 cấp.
          +) Xóa bình luận cả 2 cấp, xóa đánh giá cả 2 cấp.
          +) Thông báo truyện ra chương mới cho những tài khoản đang theo dõi truyện đó.
          +) Xếp hạng truyên theo lượt đọc, đề cử, bình luận, thích, donate.
          +) Chỉnh sửa màu nền, màu chử, font chữ, dãn dòng của trang đọc truyện.
          +) Theme dark/light cho web.
          +) Responsive mobile, tablet, pc
### Tác Giả:          
          +) Đăng ký làm tác giả.
          +) Thêm sửa xóa tìm kiếm bản thảo.
          +) Tự động thêm mới cập nhật bản thảo.
          +) Thêm, sửa, xóa, tìm kiếm truyện bản thân đã sáng tác.
          +) Thêm, sửa, xóa chương cho mỗi truyền.
          +) Tìm chương theo tên, lọc chương theo trạng thái truyện.
          +) Hẹn giờ, lập lịch tự động đăng chương truyện.
          +) Thống kê, lập sơ đồ theo dữ liệu của truyện.
          +) Theme dark/light cho web.
### Chat:
          +) Tạo nhóm chat.
          +) Tạo Chat private một - một.
          +) Thu hồi tin nhắn.
          +) Nhắn tin trực tiếp.
          +) Thêm mới thành viên vào nhóm.
          +) Tự động cập nhất nhóm chat có tin nhắn mới nhất lên đầu.
          +) Tìm kiếm nhóm của bản thân, tài khoản người dùng khác để chat.
          +) Tìm kiếm tin nhắn trong chat.
## Api của web:

- DefaultUrl: "http://dkaizz02-001-site1.gtempurl.com/api/";
- link view Json Api: <a href="http://dkaizz02-001-site1.gtempurl.com/api/swagger/view/" download="WebTruyenApiSwagger.json"><button class="btn btn-green">View Swagger JSON Api</button></a>;
- Link download Json Api: <a href="http://dkaizz02-001-site1.gtempurl.com/api/swagger/download/" download="WebTruyenApiSwagger.json"><button class="btn btn-green">Download Swagger JSON Api</button></a>(Sao chép link và dán ra tap mới);
- Note: Muốn sử dụng api thì dùng DefaultUrl + path trong Json Api + param/body(nếu có);
