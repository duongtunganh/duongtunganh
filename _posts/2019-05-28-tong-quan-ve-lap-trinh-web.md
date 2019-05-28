---
title: Tổng quan về lập trình web
comments: true
---

<p class="lead">Bài viết này sẽ nói về tổng quan của ngành lập trình web dưới góc nhìn của mình - một thằng nhóc 16 tuổi, dựa trên những kiến thức về lập trình web mình đã tự học được.</p>

Đầu tiên, hãy cùng mình tìm hiểu về các khái niệm sau đây:

### Internet là gì?
>Là tập hợp các máy tính nối mạng trên toàn thế giới liên kết với nhau qua giao thức TCP/IP (Transmission Control Protocol/Internet Protocol)

* Internet đã và đang mang lại rất nhiều lợi ích cho người dùng, nhất là khả năng gửi thư điện tử (Email), các dịch vụ trò chuyện trực tiếp (Chat) và các bộ máy tìm kiếm (Search Engine).

* Dịch vụ đang rất phổ biến và nhiều người sử dụng nhất trên Internet là World Wide Web (WWW, hay còn gọi là Web)

### Web Server (Máy chủ web)
>Là máy tính lưu trữ website. Có nhiệm vụ trả kết quả về cho Web Client khi nhận được yêu cầu.

### Web Client (Người dùng web)
>Là máy tính dùng để truy cập các trang web. Có khả năng yêu cầu và nhận kết quả từ Web Server

### Web Browser (Trình duyệt web)
>Là phần mềm dùng để xem các tài liệu hoặc tìm kiếm các tài nguyên trên World Wide Web

#### Một số trình duyệt thông dụng hiện nay:  
* Chrome của Google
* Safari của Apple, có sẵn trên MacOS và IOS
* Edge/Internet Explorer (IE) của Microsoft, có sẵn trong Windows
* Mozilla Firefox của Mozilla

Và còn nhiều trình duyệt khác...

### HTTP/HTTPS (HyperText Transfer Protocol/HTTP Secure)
>Là giao thức chuyển giao siêu văn bản trên web.  
>Giao thức này tập hợp các quy định dùng để trao đổi các tài liệu (văn bản, hình ảnh, âm thanh, video, các tập tin đa truyền thông,...) giữa Web Server và Web Browser

### URL (Uniform Resource Locator)
>Là đường dẫn chỉ tới một trang web cụ thể trên Internet.

Cú pháp đầy đủ: <strong>scheme://host:port/path?querystring</strong>  
###### Trong đó:  
* **scheme** - *Loại dịch vụ Internet*
* **host** - *Địa chỉ máy chủ chứa tài nguyên*
* **port** - *Cổng dịch vụ trên máy chủ*
* **path** - *Đường dẫn và tên của tập tin tài nguyên trên máy chủ*
* **querystring** - *Các tham số được gửi kèm theo http*

![ví dụ](/img/url-uniform-resource-locator.png "ví dụ")

### HTML (HyperText Markup Language)
>Ngôn ngữ dùng để xây dựng các trang web  
>Gồm các **tag** giúp Web Browser biết cách định dạng thông tin hiển thị

**Ví dụ:** Nội dung trang web helloworld.html
<p class="codepen" data-height="265" data-theme-id="0" data-default-tab="html,result" data-user="tunganh03" data-slug-hash="yWqNVR" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="Xin chào thế giới">
  <span>See the Pen <a href="https://codepen.io/tunganh03/pen/yWqNVR/">
  Xin chào thế giới</a> by Duong Tung Anh (<a href="https://codepen.io/tunganh03">@tunganh03</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
  
---
### Tổng quan về lập trình web
Sau khi đã hiểu được những khái niệm cơ bản về Internet, chắc hẳn các bạn sẽ muốn tạo ra một website của riêng mình. Nhưng để làm được điều đó, trước hết ta phải hiểu về những khái niệm về lập trình web sau đây:

* Web tĩnh và lập trình Client-side
* Web động và lập trình Server-side

### Web tĩnh là gì?
>Là trang web được trình bày dưới dạng cố định. Nội dung của trang web được tạo ra từ lúc thiết kế và không thay đổi khi có người truy cập.

* Chủ yếu được lập trình bằng ngôn ngữ HTML và không có sự kết nối với cơ sở dữ liệu
* Dùng ngôn ngữ Client-side Script để xử lý trên trang web tĩnh &rarr; Lập trình Client-side
* Toàn bộ quá trình xử lý chỉ diễn ra trên Web Client

##### Đặc điểm khi thiết kế web tĩnh:
* Nhanh, mất ít thời gian để trả về kết quả và hiện lên trang web
* Khả năng giới hạn trong những xử lý đơn giản và độc lập
* Không cần phải cài đặt phần mềm mở rộng trên Web Server
* Trình duyệt cần phải hiểu những ngôn ngữ (script) mà trang HTML đang sử dụng

### Web động là gì?
>Là trang web có nội dung chủ yếu được lấy từ cơ sở dữ liệu. Nội dung của trang web có thể thay đổi khi có sự tương tác của người truy cập.

* Dùng ngôn ngữ Server-side script để xử lý
* Quá trình xử lý diễn ra tại Web Server &rarr; Lập trình Server-side

##### Đặc điểm khi thiết kế web động:
* Chậm, mất nhiều thời gian để trả về và thể hiện kết quả lên trang web
* Có khả năng thực hiện những xử lý phức tạp và truy cập sơ sở dữ liệu
* Trang web sinh động, nhiều chức năng phục vụ nhiều yêu cầu của người dùng
* Cần phải cài đặt phần mềm mở rộng tại Web Server

### Môi trường lập trình
* Codepen.io
* Notepad, Notepad ++
* Visual Studio
* Sublime Text

Vừa rồi là tổng hợp toàn bộ những kiến thức mà mình đã tìm hiểu về lập trình web. Trong những bài tiếp theo mình sẽ hướng dẫn các bạn cách tự tạo cho mình một trang web sử dụng những kiến thức mà mình đã chia sẻ cho các bạn. Các bạn cảm thấy bài viết này hữu ích đừng quên để lại một comment ở bên dưới bài viết này nhé! Mình rất mong nhận được những ý kiến đóng góp của các bạn để bài viết của mình ngày một tốt hơn.

