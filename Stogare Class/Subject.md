# Automatic Variables
- Scope: là phạm vi của một thực thể trong chương trình (ví dụ như biến), để định nghĩa thực thể đó trong một phạm vi nhất định, tránh sự xung đột khi trùng tên nhưng khác phạm vi. 
-- Ví dụ như 2 biến trùng tên a ở 2 hàm khác nhau, không liên quan với nhau, khi đó sẽ được định nghĩa khác nhau theo vị trí, khi chạy chương trình tránh trùng tên
- Automatic variables là một dạng của local variable nhưng khác với biến static
- Tức là biến đó sẽ tự động định vị trong phạm vi hoạt động của nó (trong hàm chứa nó) và không thể xác định và truy cập từ bên ngoài
- Các biến (variable) được khai báo bên trong một khối (block) được gọi là automatic variable hoặc biến cục bộ (local variable). Các biến này tự động phân bổ (allocate) bộ nhớ khi truy cập vào khối đó và giải phóng bộ nhớ bị chiếm dụng khi thoát khỏi khối đó.
- Các biến này chỉ có local scope đối với khối đó, điều đó có nghĩa là chúng có thể được truy cập trong đó biến được khai báo.

# External
- Declaration là thông báo cho compiler biết được tên, kiểu, giá trị khởi đầu của biến: int a=0;
- Definition of a variable says where the variable gets stored
- Có thể khai báo bao nhiêu lần tùy thích, nhưng chỉ được định nghĩa 1 lần. Khi khai báo chương trình sẽ không cung cấp bộ nhớ cho đối tượng:
	extern int a; //Biến a được khai báo nhưng chưa được phân bổ vị trí bộ nhớ
	int add(int, int); //Khai báo hàm add, như trên
	int add(int a, int b)
  	{
   		 return (a+b);
  	}
	// Định nghĩa hàm
- Extern variable says to compiler  ” go outside my scope and you will find the definition of the variable that I declared.”
- Sau khi định nghĩa, hàm sẽ được phân bổ vị trí bộ nhớ riêng, vì vậy chỉ được định nghĩa 1 lần
- Extern variable says to compiler  ” go outside my scope and you will find the definition of the variable that I declared.”
- Compiler belives that whatever that extern variable said is true and produce no error. Linker throws an error when it finds no such variable exists.When an extern variable is initialized, then memory for this is allocated and it will be considered defined.
- (Link tham khảo)[https://www.geeksforgeeks.org/understanding-extern-keyword-in-c/ư
- Từ khóa extern dùng để mở rộng phạm vi của biến, giúp nó có thể dùng được ở cả bên ngoài file, functions dùng được cả ở bên ngoài file vì khi khai báo đã được mặc định extern ở đằng trước

# Static
- Biến duy trì giá trị cũ khi thoát khỏi phạm vi hoạt động của nó 
- Ví dụ như khi khai báo một biến trong một hàm, khi gọi lại, giá trị nó sẽ thay đổi về giá trị mặc định được khai báo. Dùng từ khóa extern sẽ giúp biến lưu lại giá trị cuối cùng trước khi thoát khỏi hàm
- (link tham khảo)[https://www.geeksforgeeks.org/static-variables-in-c/?ref=gcse]

# Register
- Từ khóa giúp đưa biến vào thanh ghi trong cpu, như vậy truy xuất nhanh hơn
- Tuy nhiên biến register chỉ được hoạt động trong 1 hàm
