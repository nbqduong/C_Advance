- Trong c nếu một macro chưa được define mà đã được gọi thì chương trình sẽ tự định nghĩa macro đó bằng 0
# Macros vs Functions
- Macros là chỉ thị tiền xử lý, không có type check, không có check compilation error
- Vì thế nếu dùng macro không khéo sẽ dẫn đến những kết quả không mong đợi. Còn hàm sẽ quy định được, đảm bảo tính ổn định hơn
- Tuy nhiên xử lý macro sẽ nhanh hơn function

# Create Macros

# Preprocessor Operators

# Predefined Macros
- __LINE__ trả về số dòng hiện tại trong code
- __FILE__ trả về tên file hiện tại
- __DATE__ trả về ngày tháng năm hiện tại
- __TIME__ trả về giờ phút giây hiện tại
- __STDC__ xác nhận chuẩn của trình biên dịch, thường nó sẽ trả về 1 nếu trình biên dịch dựa trên chuẩn ISO

