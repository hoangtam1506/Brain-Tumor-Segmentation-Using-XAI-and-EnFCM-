**1. Giới thiệu**
Nghiên cứu “Sử dụng XAI và ENFCM trong nhận dạng khối u não” được thực hiện nhằm giải quyết các thách thức trong bài toán phân đoạn và phân loại khối u não từ ảnh MRI.
Mục tiêu của nghiên cứu là xây dựng một hệ thống tự động hóa không chỉ phân loại chính xác các loại khối u não mà còn tích hợp các phương pháp AI giải thích được (Explainable AI - XAI) để làm rõ cách thức và lý do đưa ra các quyết định của mô hình.
Bên cạnh đó, hệ thống còn thực hiện trực quan hóa khối u bằng công nghệ 3D, giúp cung cấp cho bác sĩ và nhà nghiên cứu một cái nhìn trực quan và toàn diện về cấu trúc, vị trí và biên giới của khối u.

**2. Dataset**
2.1 Brain Tumor MRI Dataset (Kaggle)
Tập dữ liệu được cung cấp bởi Masoud Nickparvar trên nền tảng Kaggle, phục vụ nghiên cứu về nhận diện và phân loại khối u não từ ảnh MRI.
Dataset là sự kết hợp từ ba nguồn:
•	Figshare – nguồn dữ liệu chất lượng cao
•	SARTAJ dataset – đã được thay thế lớp Glioma do vấn đề phân loại
•	Br35H dataset – cung cấp ảnh cho lớp “No Tumor”

2.2 Số lượng và cấu trúc dữ liệu
Tổng số ảnh: 7023 ảnh MRI não, được phân loại thành 4 nhóm chính:
•	Glioma Tumor: Khối u tế bào thần kinh đệm
•	Meningioma Tumor: Khối u màng não
•	Pituitary Tumor: Khối u tuyến yên
•	No Tumor: Không có khối u

2.3 Phân bổ dữ liệu
Tập dữ liệu được chia thành hai tập con phục vụ huấn luyện và đánh giá:
•	Training set: Dùng để mô hình học và tối ưu hóa tham số
•	Testing set: Dùng để đánh giá độ chính xác và hiệu quả trên dữ liệu chưa từng thấy

Biểu đồ phân chia dữ liệu
<p align="center"> <img src="https://github.com/user-attachments/assets/fb5990ab-bf3a-4d7b-a1d2-75d7215dc73a" width="750"> </p> 

**3. Phương pháp đề xuất**

Hệ thống được xây dựng theo một quy trình xử lý tuần tự bao gồm:
1. Thu thập dữ liệu
Sử dụng tập Brain Tumor MRI Dataset bao gồm nhiều loại khối u não khác nhau. Dữ liệu là cơ sở cho bài toán phân đoạn và phân loại. Việc tích hợp XAI giúp làm rõ cách mô hình phân tích và đưa ra quyết định.
2. Tiền xử lý dữ liệu
Chia dữ liệu thành Training và Testing.
Cắt ảnh (Cropping) bằng phát hiện contours để tập trung vào vùng khối u.
Resize ảnh về 224×224 và chuẩn hóa pixel về khoảng [0,1].
Tăng cường dữ liệu (Data Augmentation): xoay, dịch chuyển, lật ảnh.
3. Xây dựng mô hình
Sử dụng CNN (MobileNetV2, InceptionV3) để trích xuất đặc trưng.
Kết hợp LSTM để tăng khả năng xử lý đặc trưng phức tạp.
Áp dụng ENFCM để cải thiện phân cụm và phân đoạn vùng khối u.
4. Explainable AI (XAI)
Sử dụng Integrated Gradients hoặc SHAP để giải thích quyết định của mô hình, tăng tính minh bạch và độ tin cậy.
5. Đánh giá mô hình
Đánh giá dựa trên Accuracy, Precision, Recall, F1-score và Loss để đo lường hiệu suất tổng thể


Sơ đồ phương pháp đề xuất
<p align="center"> <img src="https://github.com/user-attachments/assets/c0d6f926-6bb4-4015-a115-ba788747984f" width="850"> </p>

**4. Kết quả **
4.1 Kết quả huấn luyện
<img width="949" height="330" alt="image" src="https://github.com/user-attachments/assets/281195cc-4092-47d9-bea9-36da7d9b533c" />

<img width="949" height="331" alt="image" src="https://github.com/user-attachments/assets/c194ccfc-94f8-4fea-990e-d3025ab5155c" />

4.2 Kết quả test
<img width="950" height="315" alt="image" src="https://github.com/user-attachments/assets/c35ffc56-4814-4e4f-8da7-5ac9cd6f5712" />
<img width="949" height="302" alt="image" src="https://github.com/user-attachments/assets/3af4df0f-0a2f-45e9-bd6e-8c816af72073" />

 4.3 Kết quả GARDCAM
 
<img width="708" height="308" alt="image" src="https://github.com/user-attachments/assets/f877c809-70da-4d0b-997d-a158b7c4699f" />

<img width="660" height="284" alt="image" src="https://github.com/user-attachments/assets/53708d9c-30df-4630-bd46-4fd6d847f708" />

4.4 INTERGATED GRADIENTS

<img width="728" height="333" alt="image" src="https://github.com/user-attachments/assets/8021cd1f-b378-4c62-b960-e5a66189f6cf" />

4.5 SHAP

<img width="727" height="329" alt="image" src="https://github.com/user-attachments/assets/31ac1a81-fc61-412e-91fa-c19981d236a8" />

4.6 ENFCM

<img width="631" height="326" alt="image" src="https://github.com/user-attachments/assets/014b0e28-6915-4c4e-98ef-7e7386ea86ce" />






