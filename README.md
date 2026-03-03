1. Giới thiệu

Nghiên cứu “Sử dụng XAI và ENFCM trong nhận dạng khối u não” được thực hiện nhằm giải quyết các thách thức trong bài toán phân đoạn và phân loại khối u não từ ảnh MRI.

Mục tiêu của nghiên cứu là xây dựng một hệ thống tự động hóa không chỉ phân loại chính xác các loại khối u não mà còn tích hợp các phương pháp AI giải thích được (Explainable AI - XAI) để làm rõ cách thức và lý do đưa ra các quyết định của mô hình.

Bên cạnh đó, hệ thống còn thực hiện trực quan hóa khối u bằng công nghệ 3D, giúp cung cấp cho bác sĩ và nhà nghiên cứu một cái nhìn trực quan và toàn diện về cấu trúc, vị trí và biên giới của khối u.

2. Dataset
2.1 Brain Tumor MRI Dataset (Kaggle)

Tập dữ liệu được cung cấp bởi Masoud Nickparvar trên nền tảng Kaggle, phục vụ nghiên cứu về nhận diện và phân loại khối u não từ ảnh MRI.

Dataset là sự kết hợp từ ba nguồn:

Figshare – nguồn dữ liệu chất lượng cao.

SARTAJ dataset – đã được thay thế lớp Glioma do vấn đề phân loại.

Br35H dataset – cung cấp ảnh cho lớp “No Tumor”.

2.2 Số lượng và cấu trúc dữ liệu

Tổng số ảnh: 7023 ảnh MRI não, được phân loại thành 4 nhóm chính:

Glioma Tumor: Khối u tế bào thần kinh đệm.

Meningioma Tumor: Khối u màng não.

Pituitary Tumor: Khối u tuyến yên.

No Tumor: Không có khối u.

2.3 Phân bổ dữ liệu

Tập dữ liệu được chia thành hai tập con phục vụ huấn luyện và đánh giá:

Tập huấn luyện (Training set): Dùng để mô hình học và tối ưu hóa tham số.

Tập kiểm tra (Testing set): Dùng để đánh giá độ chính xác và hiệu quả trên dữ liệu chưa từng thấy.

<p align="center"> <img src="https://github.com/user-attachments/assets/fb5990ab-bf3a-4d7b-a1d2-75d7215dc73a" width="800"> </p>
3. Phương pháp đề xuất

Hệ thống được xây dựng theo một quy trình xử lý tuần tự bao gồm:

Tiền xử lý ảnh MRI.

Phân đoạn khối u bằng Enhanced Fuzzy C-Means (ENFCM).

Phân loại khối u dựa trên vùng phân đoạn.

Áp dụng Explainable AI (XAI) để giải thích quyết định của mô hình.

Trực quan hóa khối u dưới dạng 3D.

Phương pháp đề xuất nhằm đảm bảo ba yếu tố chính:

Độ chính xác trong phân đoạn và phân loại.

Tính minh bạch và khả năng giải thích của mô hình AI.

Khả năng trực quan hóa phục vụ hỗ trợ chẩn đoán.

<p align="center"> <img src="https://github.com/user-attachments/assets/c0d6f926-6bb4-4015-a115-ba788747984f" width="850"> </p>
