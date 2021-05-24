Generalized probabilistic principal component analysis of
correlated data
https://www.jmlr.org/papers/volume21/18-595/18-595.pdf

# 1	Bài toán mà bài báo giải quyết là gì? Minh hoạ input/output (tìm hình ảnh có trong bài báo để minh hoạ).

	Phân tích thành phần chính (PCA) là một trong những kỹ thuật quan trọng trong học máy và xử lí dữ liệu nhằm giảm số chiều dữ liệu.
Input: Véc tơ x = (x1, x2,…,xp)T
Output: Véc tơ y(x) = (y1(x), y2(x),…,yk(x))T với k < p.

 


# 2	Các câu hỏi đặt ra là gì? Đã giải quyết được đến đâu?

	Sử dụng phương pháp ước lượng hợp lý cực đại ta có các thành phần chính tương đương với các giá trị riêng của ma trận tương quan của véc tơ dữ liệu quan sát và giả định rằng các thành phần của véc tơ dữ liệu có phân phối độc lập theo phân phối chuẩn và không tương quan. Tuy nhiên, giả định về tính độc lập có thể không thực tế đối với nhiều trường hợp như mô hình hóa nhiều chuỗi thời gian, quá trình không gian (spatial processes) và hàm dữ liệu, trong đó các thành phần véc tơ dữ liệu có sự tương quan. 
	Trong bài báo này, tác giả giới thiệu phương pháp xác suất tổng quát phân tích thành phần chính (GPPCA) để nghiên cứu mô hình dữ liệu cho nhiều thành phần tương quan, trong đó mỗi thành phần được mô hình hóa bằng một quá trình Gaussian. Phương pháp này đã đưa ra công thức tổng quát hơn để xác định các tham số so với trước đây bằng phương pháp ước lượng hợp lý cực đại. 
	Dựa vào ma trận biểu thị độ chính xác trong ước lượng hợp lý cực đại đưa ra số lượng các biến tính toán là tuyến tính với số lượng biến đầu ra. 
	Hơn nữa, nhóm  tác giả đưa ra biểu thức của ước lượng hợp lý cực đại cho kỳ vọng cho các biến tương quan.
	Lợi thế của GPPCA xét về mức độ phù hợp thực tế, ước tính độ chính xác và tính thuận tiện trong tính toán. Thí nghiệm trên bộ dữ liệu thực và dữ liệu mô phỏng đạt đạt hiệu quả cao hơn so với các cách tiếp cận khác.

# 3 Ý tưởng giải quyết là gì? Minh hoạ trực quan (diễn giải bằng lời hoặc hình ảnh)

Ý tưởng chính: Dùng thuật toán gradient descent đi ước lượng hợp lý cực đại của ma trận A trong mô hình y(x)=Az(x)+ϵ.
