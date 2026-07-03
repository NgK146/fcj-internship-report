---
title: "Worklog Tuần 8"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Phân tích chi phí chuyên sâu bằng Cost and Usage Reports (CUR) và Athena.
* Thao tác lập trình với DynamoDB thông qua Python SDK (boto3).
* Xây dựng luồng Data Lake và phân tích dữ liệu toàn diện (Glue, EMR, Redshift, QuickSight).

### Các công việc triển khai trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Đẩy dữ liệu CUR lên S3 <br> - Chạy Glue Crawler + Athena cho CUR DB <br> - Truy vấn chi phí theo service, tag, account <br> - Phân tích hiệu quả của RI, Savings Plans và On-Demand | 08/06/2026 | 08/06/2026 | <https://docs.aws.amazon.com/cur/latest/userguide/what-is-cur.html> |
| 3   | - Dùng Python SDK (boto3) thao tác CRUD trên DynamoDB <br> - Tải hàng loạt hơn 250 bộ phim từ moviedata.json <br> - Thực hiện Scan và Query phức tạp với FilterExpressions | 09/06/2026 | 09/06/2026 | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GettingStartedDynamoDB.html> |
| 4   | - Tải dataset Airbnb qua Cloud9, upload lên S3 <br> - Chạy Glue DataBrew Profile Job để làm sạch dữ liệu <br> - Chuyển đổi CSV sang Parquet bằng Glue ETL PySpark <br> - Chạy Glue Crawler để cập nhật Data Catalog | 10/06/2026 | 10/06/2026 | <https://docs.aws.amazon.com/glue/latest/dg/what-is-glue.html> |
| 5   | - Thiết kế visual ETL bằng Glue Studio <br> - Khởi tạo EMR Cluster, chạy PySpark aggregation <br> - Triển khai Kinesis Data Analytics Studio (Flink SQL) <br> - Khởi tạo Redshift Cluster, chạy ETL từ S3 qua Glue | 11/06/2026 | 11/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Đưa dataset vào Amazon QuickSight <br> - Tạo Line Chart (Forecast), KPI, Insights tự động <br> - Tạo Donut Chart (Drill-down) và Pivot Table <br> - Publish dashboard tương tác | 12/06/2026 | 12/06/2026 | <https://docs.aws.amazon.com/quicksight/latest/user/what-is-quicksight.html> |
| 7   | - Format QuickSight dashboard: custom theme, màu sắc <br> - Thêm Sankey chart, Sales Map và Conditional Formatting <br> - Cấu hình Cascading Filters và Navigation Actions | 13/06/2026 | 13/06/2026 | <https://docs.aws.amazon.com/quicksight/latest/user/what-is-quicksight.html> |
| CN  | - Rà soát toàn bộ cấu hình data pipeline <br> - Tổng hợp kiến trúc Data Lake và analytics <br> - Rút ra bài học trước khi bắt đầu đồ án cuối kỳ | 14/06/2026 | 14/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 8:

* Thực hiện phân tích chi phí AWS chi tiết qua CUR và Athena SQL.
* Nắm vững kỹ năng lập trình thao tác với DynamoDB bằng Python/boto3.
* Xây dựng Data Lake Airbnb hoàn chỉnh với S3, DataBrew, Glue và định dạng Parquet.
* Triển khai hệ thống phân tích doanh nghiệp end-to-end: Kinesis → EMR → Athena → Redshift.
* Thiết kế QuickSight dashboard chuyên nghiệp với AI forecast, filter phân tầng và action điều hướng.
