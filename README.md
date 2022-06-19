# VanArsdel-Sales-Report---Power-BI
Báo cáo đánh giá tổng quan VanArsdel
I, Thông tin về data:
Dữ liệu lấy từ bộ dữ liệu mẫu về Sales và Marketing của Microsoft: https://docs.microsoft.com/en-us/power-bi/create-reports/sample-sales-and-marketing
Bộ dữ liệu chứa thông tin về tình hình kinh doanh (doanh thu, doanh số bán hàng) và đánh giá từ khách hàng với thương hiệu của công ty VanArsdel – một công ty giả hoạt động tại thị trường Mỹ, cũng như thông tin về các đối thủ cạnh tranh.

II, Quá trình làm:

Bước đầu tiên là data profiling - kiểm tra dữ liệu. Bộ dữ liệu này đã được làm sạch và build model hợp lý theo mô hình ngôi sao – star schema với hai bảng Fact là SalesFact và Sentiment. Các bảng Dimension khác cũng có liên kết với nhau.

Tiếp đến là xóa và ẩn các cột, các thông tin không cần thiết, xóa các Measure sẵn có không dùng đến, sau đó tạo các hierarchy để sử dụng cho visual. Các hierarchy được tạo gồm có Date hierarchy về mặt thời gian, Geo hierarchy về mặt địa lý và Product hierarchy về mặt sản phẩm.
![Hierarchy](https://user-images.githubusercontent.com/93377175/174472752-b32561ca-15b6-4032-bab0-e0057e1f8f6c.png)

Bước tiếp theo là tiến hành đặt câu hỏi:
-	Q: Khán giả/người xem report này là ai?
A: Là giám đốc và ban lãnh đạo (manager, C-levels)
-	Q: Mục đích của báo cáo này là gì?
A: Báo cáo tình hình kinh doanh tổng quan của công ty trong giai đoạn 5 năm vừa qua, giúp đưa ra quyết định về việc đầu tư/phát triển cho công ty
-	Q: Báo cáo này sẽ mang lại thêm giá trị gì?
A: Giúp những người đưa ra quyết định (decision makers) có được Insights về tình hình tổng quan cũng như phương hướng tập trung để đầu tư nguồn lực phát triển
-	Q: Báo cáo này thuộc loại gì?
A: Sales Overview report
-	Q: Nên tập trung vào những thông tin nào?
A: Các metric thể hiện kết quả kinh doanh, so sánh tổng quan công ty với các đối thủ cạnh tranh, phân tích tình hình kinh doanh theo giai đoạn, theo sản phẩm, theo vùng, cảm xúc và sự hài lòng của khách hàng đối với thương hiệu.
-	Q: Nên sử dụng những metric nào để thể hiện thông tin?
A: Doanh thu và doanh số đơn vị bán ra cùng điểm đánh giá cảm tình của khách hàng với thương hiệu

III, Các trang trong báo cáo:

![Menu](https://user-images.githubusercontent.com/93377175/174472841-a5942728-e958-465c-a4db-46e2c03082e6.png)
-	Trang 1: Menu điều hướng các trang
-	Trang 2: Overview về tình hình kinh doanh của công ty trong giai đoạn 5 năm trở lại đây (2010 – 2014), thể hiện tổng doanh thu trong giai đoạn theo thời gian, theo danh mục sản phẩm và vùng địa lý 
-	Trang 3: Overview về sự hài lòng của khách hàng đối với thương hiệu, phân tích theo từng bang và doanh thu. Sử dụng hồi quy tuyến tính, ta thấy hệ số tương quan Pearson giữa điểm hài lòng và doanh thu là -0,07, tức là giữa hai yếu tố này hầu như không có mối liên hệ nào
-	Trang 4: So sánh toàn cảnh giữa thương hiệu và thị trường với các đối thủ cạnh tranh
-	Trang 5: Phân tích tình hình kinh doanh theo sản phẩm
-	Trang 6: Phân tích tình hình kinh doanh theo khu vực địa lý


IV, Kết luận:

Trong giai đoạn 5 năm gần đây, tình hình kết quả kinh doanh của VanArsdel rất ổn định và giữ được mức tăng trưởng nhẹ - doanh thu từ 2010 đến 2014 tăng trưởng 127,64%, từ 163 triệu đô la lên đến 209 triệu đô la.

Doanh thu và doanh số bán hàng của công ty đi theo một đồ thị hình Sin, với đáy ở Quý 2 và đạt đỉnh vào Quý 4. Công ty nên tập trung đẩy mạnh khả năng bán hàng vào thời điểm Quý 4 và tìm cách cải thiện doanh thu ở Quý 2. Doanh thu và doanh số bán hàng từ năm 2010 – 2011 và 2012 – 2013 tăng trưởng không đáng kể, thậm chí có sự sụt giảm.
![Overview](https://user-images.githubusercontent.com/93377175/174472889-4fa1d880-4911-4704-9962-fa5dcee81c02.png)

Điểm Sentiment - đánh giá cảm tình của khách hàng với thương hiệu -  của VanArsdel thấp hơn mức trung bình của toàn thị trường (50,58 điểm so với 66,86 điểm). Điểm Sentiment của VanArsdel cũng có chu kỳ lên xuống tương ứng với kết quả kinh doanh theo thời gian. 

Khi tiến hành phân tích bằng phương pháp hồi quy tuyến tính, hệ số tương quan Pearson R giữa doanh thu và điểm Sentiment theo các bang là -0,07, tức là hầu như không tồn tại mối liên hệ nào giữa hai yếu tố này. Điều này gợi ý rằng công ty không cần thiết phải đầu tư cải thiện điểm Sentiment.
Tuy nhiên, doanh thu của công ty còn bị ảnh hưởng bởi quy mô của thị trường đó – một nơi có dân số đông thì vẫn có thể có doanh thu cao kể cả khi điểm Sentiment tại nơi đó chỉ đạt mức thấp. Các bang có doanh thu cao nhất như Texas, California, Florida… đều là những bang có dân số đứng đầu cả nước. Vậy nên chưa thể có kết luận rõ ràng về Sentiment và doanh thu.

![2022-06-19_151957](https://user-images.githubusercontent.com/93377175/174472971-1295ae03-e1eb-4815-bde3-e89c18fdb81f.png)

Công ty VanArsdel trong giai đoạn 5 năm gần đây vẫn là thương hiệu lớn nhất trên thị trường, áp đảo hoàn toàn các đối thủ cạnh tranh. VanArsdel chiếm đến 30% thị phần theo doanh số sản phẩm bán ra và có doanh thu bằng tổng tất cả các công ty đối thủ cộng lại.

![Market share](https://user-images.githubusercontent.com/93377175/174472991-44f883b1-8b1b-4eaa-9d69-44dedc0b34e6.png)

Hầu như toàn bộ doanh thu đến từ 2 phân khúc sản phầm là Urban Moderation và Urban Convenience, với các mã sản phẩm chủ lực như UM-11,…
![product](https://user-images.githubusercontent.com/93377175/174473004-39268ffa-130f-4849-93f5-4c427bb1ec55.png)
Doanh thu từ vùng miền Đông (East) chiếm phần nhiều (có thể vì khu vực này có nhiều bang), theo sát là khu vực miền Trung (Central). Vùng miền Tây (West) có doanh thu thấp hơn hẳn.
![2022-06-19_151943](https://user-images.githubusercontent.com/93377175/174473010-00fe86f2-4bf6-46bf-b4d5-3e202842875d.png)

Nhìn chung, công ty nên đẩy mạnh kinh doanh vào thời điểm Quý 4 hàng năm, tập trung vào các sản phẩm chủ lực và các bang tại miền Đông và miên Trung, đồng thời cải thiện tình hình vào Quý 2 và tại miền Tây.
