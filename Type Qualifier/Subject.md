# Qualifier
- Trong ngôn ngữ lập trình C, các type qualifier là các từ khóa (keyword) được sử dụng để sửa đổi các thuộc tính của các biến (variable). Sử dụng các type qualifier chúng ta có thể thay đổi các thuộc tính của các biến. Ngôn ngữ lập trình c cung cấp hai type qualifier là const và volatile.

# const

- con trỏ trỏ đến hằng số không thể thay đổi giá trị của biến, nhưng có thể trỏ đến biến khác
	int *const ptr = &i; //constant pointer to variable
- Con trỏ có thể thay đổi giá trị của biến nhưng không thể trỏ đến biến khác
 	const int *const ptr; //constant pointer to constant
- Không thể thay đổi giá trị của con trỏ và không thể thay đổi giá trị của biến

# Volatile
- Trong khi complie chương trình, các trình biên dịch có xu hướng tối ưu hóa thuật toán bằng nhiều cách. 
- Các biến được quy định khi giao tiếp với bên ngoài (giá trị nhận từ các cổng IO) sẽ thay đổi giá trị theo phần cứng, nhưng trong chương trình các biến này không thay đổi giá trị. Do đó compiler có thể tối ưu hóa những biến này khiến cho chương trình chạy sai cách.
	bool status = input(pin_b0);
	while(status==1){//do somethings}
- Chương trình trên không có sự thay đổi giá trị, trình biên dịch có thể hiểu nhầm và tối ưu thành while(1) gây ra hoạt động sai
- An object that has volatile-qualified type may be modified in ways unknown to the implementation or have other unknown side effects

# restrict
- Dùng khi khai báo con trỏ, nói cho trình biên dịch rằng chỉ có con trỏ này được trỏ vào đối tượng mà nó trỏ tới. Nếu vi phạm sẽ xảy ra vấn đề chưa được xác định trước
