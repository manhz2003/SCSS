Learn SASS - hướng dẫn
Các bước biên dịch từ sass sang css
Bước 1: Tạo 2 thư mục ngang cấp chứa sass và css
Bước 2: Tạo trước file scss cần sử dụng trong folder sass
Bước 3: Mở teminal gõ câu lệnh sass input output --watch
trong đó ví dụ input là app.scss output là app.css ta có câu lệnh
"sass sass/app.scss ./css/app.css --watch" , watch giúp tự động biên dịch
*lưu ý: Mỗi file sass ta cần dùng 1 terminal khác nhau để biên dịch các
file đó sang css, với câu lệnh như dòng 7, tên file tương ứng.

Các kiến thức trong SASS
1. Variable (đặt biến)
2. Netsted (viết lồng các CSS vào nhau)
3. Mixin (Kế thừa lại các thuộc tính CSS do người dùng tạo ra)
4. extend (Kế thừa lại các thuộc tính CSS có sẵn trong selector)
5.

1. variable
- sử dụng kí tự $ + tên biến : màu sắc, kích thước...
- nếu viết ở 1 file khác ta sử dụng key: import 'đường dẫn file';
- ex: textColor: #333; itemSize: 24px; ...
2. Nested
- viết các css lồng vào nhau, khi đặt các id class nằm bên trong nó
- khi sử dụng hover viết ngay bên trong thẻ cần hover và sử dụng kí tự
  &:hover{},... firtchild, lastchild, active.... sử dụng tương tự.
3. Mixin
- Tạo mixin bằng cách sử dụng 
@mixin nameMixin (){
    attribute 1
    attribute 2
    attribute 3
    ...
}
- Sử dụng mixin bằng cách dùng key: @include nameMixin();
- Ta có thể truyền tham số cho mixin là các biến, sau đó gọi lại các biến đối số tại @include nameMixin();

- ex: @mixin button($textColor, $bgColor) {
        color: $textColor;
        background-color: $bgColor;
}
    .button1{
        @include button(#222, #3541);
    }
    .button2{
        @include button(#122, #4521);
    }

4. extend (ví dụ bên file app.scss từ dòng 88 - 110)

