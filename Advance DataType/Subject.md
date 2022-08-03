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
- C99 cà C11 hỗ trợ tạo mảng có chiều dài thay đổi 
	void ar(int a)
	{
  		int arr[a];
  		for(int i=0; i++<a;) arr[i]=1;
	}
- Tuy nhiên, mảng này thực chất chỉ có phạm vi trong hàm, mỗi khi hàm được gọi sẽ refresh lại việc khai báo mảng

# Flexible Array
- Từ C99, chúng ta có thể khai báo mảng mà không cần khai báo kích thước trước, kích thước này có thể thay đổi được, nên được đặt ở cuối struct và struct phải có thêm ít nhất 1 phần tử trước mảng	
	struct student
	{
   		int stud_id;
   		int name_len;
   		int struct_size;
   		char stud_name[];
	};
- Ví dụ cụ thể https://www.geeksforgeeks.org/flexible-array-members-structure-c/?ref=gcse

# Complex number types
- C hỗ trợ thư viện <complex.h>
- Hướng dẫn sử dụng xem thêm ở https://www.geeksforgeeks.org/complex-h-header-file-in-c-with-examples/?ref=gcse

# Designated Intializers
- Chỉ định giá trị của các phần tử không theo thường lệ, ví dụ
	int numbers[100] = {1, 2, 3, [3 ... 9] = 10,
          [10] = 80, 15, [70] = 50, [42] = 400 };
- Khi in ra màn hình giá trị 0-20 và 72, 40 kết quả sẽ hiển thị
	1 2 3 10 10 10 10 10 10 10 80 15 0 0 0 0 0 0 0 0 
	50 400 

