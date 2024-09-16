# Python
This is a transnational data set which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail. The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.
- InvoiceNo: Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with letter 'C', it indicates a cancellation.
- StockCode: Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product.
- Description: Product (item) name. Nominal.
- Quantity: The quantities of each product (item) per transaction. Numeric.
- InvoiceDate: Invoice Date and time. Numeric, the day and time when each transaction was generated.
- UnitPrice: Unit price. Numeric, Product price per unit in sterling.
- CustomerID: Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.
- Country: Country name. Nominal, the name of the country where each customer resides.
## EDA
Các bước thực hiện:
- Lấy dữ liệu và xem cấu trúc cũng như type của dữ liệu
- Loại bỏ những giá trị Null, sửa đổi type không phù hợp
- Với những yêu cầu của đề bài, loại bỏ các giá trị không phù hợp
## RFM analysis
- Tính các chỉ số R,F,M của từng khách hàng
- Dùng Concat để nối các điểm của từng khách hàng
- Lập biểu đồ phân loại các nhóm khách hàng
## Visualization
![image](https://github.com/user-attachments/assets/c74ae8d2-d4cd-4d03-b154-ec32edb4c4e0)

Từ biểu đồ này ta thấy được nhóm Khách hàng **Champions** chiếm nhiều nhất, sau đó tới nhóm **Hibernating Customer**, từ đây có thể phán đoán nhanh được nhóm khách hàng nào đang chiếm đa số, nhóm nào không, thấy được số lượng khách hàng của từng .Tuy nhiên nhìn vào biểu đồ này chỉ thấy được sự cách biệt giữa các nhóm, vậy nên có thêm một biểu đồ nữa. Từ đây thấy được tỉ trọng của từng nhóm khách hàng
![image](https://github.com/user-attachments/assets/f4959d1d-2297-491f-a929-3bb99644a351)
Dưới đây là sự phân phối của nhóm khách hàng theo tổng doanh thu: Thấy được nhóm khách hàng **Champion** chiếm tổng doanh thu là cao nhất, với trên 4 triệu USD. Thêm một biểu đồ nữa, thấy được tỉ trọng của từng nhóm khách hàng
![image](https://github.com/user-attachments/assets/bf1fe51a-5f26-42ea-a697-b6725ef4ca40)

Nhóm khách hàng **Champions** chiếm tới hơn 60% tổng doanh thu, thấy được đây là nhóm khách hàng lớn nhất của doanh nghiệp. Từ đây có thể đưa ra các đề xuất phù hợp để thúc tiến nhóm khách hàng này  
![image](https://github.com/user-attachments/assets/f44bb229-b991-49f4-8604-c366571b4932)

## Một số đề xuất đưa ra cho doanh nghiệp
### Definition and recommended action for each customer segment:

| Segment | Characteristics | Recommendation |
| :-: | :-: | :-: |
| Champions | Bought recently, buy often and spend the most! | Reward them. Can be early adopters for new products. Will promote your brand. |
| Loyal | Spend good money with us often. Responsive to promotions. | Upsell higher value products. Ask for reviews. Engage them. |
| Potential Loyalist | Recent customers, but spent a good amount and bought more than once. | Offer membership / loyalty program, recommend other products. |
| New customers | Bought most recently, but not often. | Provide on-boarding support, give them early success, start building relationship. |
| Promising | Recent shoppers, but haven’t spent much. | Create brand awareness, offer free trials |
| Need attention | Above average recency, frequency and monetary values. May not have bought very recently though. | Make limited time offers, Recommend based on past purchases. Reactivate them. |
| About to sleep | Below average recency, frequency and monetary values. Will lose them if not reactivated. | Share valuable resources, recommend popular products / renewals at discount, reconnect with them. |
| At risk | Spent big money and purchased often. But long time ago. Need to bring them back! | Send personalized emails to reconnect, offer renewals, provide helpful resources. |
| Cannot lose them | Made biggest purchases, and often. But haven’t returned for a long time. | Win them back via renewals or newer products, don’t lose them to competition, talk to them. |
| Hibernating customers | Last purchase was long back, low spenders and low number of orders. | Offer other relevant products and special discounts. Recreate brand value. |
| Lost customers | Lowest recency, frequency and monetary scores. | Revive interest with reach out campaign, ignore otherwise. |

Chi tiết bài làm tại đây [RFM analysis](https://github.com/HienPham2k1/Python/blob/31dcd9f4bf86ed902776b28bb702bd60a2f7e058/Ph%E1%BA%A1m_Th%E1%BB%8B_Thu_Hi%E1%BB%81n_RFM_project.ipynb)
