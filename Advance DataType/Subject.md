# #define statement
- giúp định nghĩa hằng số, hằng số này có thể dùng ở bất cứ đâu trong code, không thể thay đổi giá trị vì đây là hằng số
- Các ví dụ:
	#define AGE 10
	#define NAME "TechOnTheNet.com"
	#define AGE (20 / 2)
	#define MAX(a,b) ((a < b) ? (b) : (a))
	#define rep(i,a) for(int i=0;i<a;i++) 
- thực tế khi gặp define, compiler sẽ cố gắng tìm ra một giá trị cố định để gán vào hằng số mỗi lần hằng số được gọi

# using typedef
- định nghĩa lại tên của data type, ví dụ
	typedef int MOUSE;
- từ giờ, kiểu int sẽ được đổi tên thành MOUSE
- Ngoài ra còn có chức năng rút gọn tên struct
	typedef struct Author {
    		// Creating variables
    		NSString *Title;
    		NSString *Publisher;
    		int Book_Number;
	} Author;
- Từ giờ thay vì mỗi lần phải ấn struct Author <tên biến>; để định nghĩa thì chỉ cần dùng cú pháp Author <tên biến>;

# Vairiable Length Arrays

# Flexible Array

# Complex number types

# Designated Intializers
