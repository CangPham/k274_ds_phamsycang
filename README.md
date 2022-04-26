# Sentiment Analysis - Phân tích trạng thái tình cảm của khách hàng - Foody.vn (Phạm Sỹ Cang)

Foody.vn là một kênh phối hợp với các nhà hàng/quán ăn bán thực phẩm online. Chúng ta có thể lên đây để xem các đánh giá, nhận xét cũng như đặt mua thực phẩm. Từ những đánh giá của khách hàng, vấn đề được đưa ra là làm sao để các nhà hàng/ quán ăn hiểu được khách hàng rõ hơn, biết họ đánh giá về mình như thế nào để cải thiện hơn trong dịch vụ/ sản phẩm.

## Cấu trúc thư mục
``` 
Week
    crawl foody data source code
    files
    Foody_review_streamlit
    DoAn_Phamsycang.ipynb
    foody2.json
    data_Foody.csv
```
File đồ án chính thức là DoAn_Phamsycang.ipynb
File report là K274_DS_PhamSyCang.docx nằm ngoài thư mục source
File slide là Foody Review sentiment analysis.pptx nằm ngoài thư mục source

## Hướng dẫn sử dụng scrapy để crawl data
Vào thư mục "crawl foody data source code" run dòng lệnh bên dưới

```python
scrapy crawl crawlFoody -o foody2.json
```

## Hướng dẫn sử dụng streamlit
Vào thư mục Foody_review_streamlit -> mở source code bằng visual code và chạy với dòng lệnh sau
```python
streamlit run mystreamlit.py
```
Cấu trúc file upload như ví dụ dưới.
Phải có tên column là comment ở dòng đầu tiên. Các dòng tiếp theo là mỗi một comment
``` excel
comment
Tay nghề nướng của nhân viên cao không bị xém hay dai sống như ở yoyo hay những nơi khác.
Dỡ quá không ủng hộ lần nào nữa. 
Ngon nhưng dạo này chất lượng đồ ăn giảm trong khi giá lên 
Không gian chiều tối nhiều muỗi 
Thái độ nhân viên dễ thương nhiệt tình
món ngon thơm mềm ủng hộ thêm
dỡ tệ
```
## Deploy lên heroku
https://foody-review-classification.herokuapp.com/
Sử dụng các dòng lệnh sau để deploy lên heroku
```python
heroku login
heroku git:remote -a foody-review-classification
git commit -am "Init project"
git push heroku master
```