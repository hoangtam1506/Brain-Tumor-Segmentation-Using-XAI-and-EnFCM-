Brain Tumor Segmentation Using XAI and ENFCM - SỬ DỤNG XAI VÀ ENFCM TRONG 
NHẬN DẠNG KHỐI U NÃO

" SỬ DỤNG XAI VÀ ENFCM TRONG NHẬN DẠNG KHỐI U NÃO" được thực hiện nhằm giải quyết những thách thức này. Mục tiêu của nghiên cứu là xây dựng một hệ thống tự động hóa không chỉ phân loại chính xác các loại khối u não mà còn tích hợp các phương pháp AI giải thích được (Explainable AI - XAI) để làm rõ cách thức và lý do đưa ra các quyết định của mô hình. Bên cạnh đó, hệ thống còn thực hiện trực quan hóa khối u bằng công nghệ 3D, giúp cung cấp cho bác sĩ và nhà nghiên cứu một cái nhìn trực quan và toàn diện về cấu trúc, vị trí và biên giới của khối u

DATASET: 
Tập dữ liệu Brain Tumor MRI Dataset được cung cấp bởi Masoud Nickparvar trên nền tảng Kaggle, là một nguồn dữ liệu được thiết kế cho các nghiên cứu về nhận diện và phân loại khối u não thông qua ảnh MRI. Tập dữ liệu này bao gồm các hình ảnh MRI (Magnetic Resonance Imaging) được phân loại thành các nhóm chính, phục vụ mục đích học máy và thị giác máy tính (computer vision).
Nguồn gốc tập dữ liệu: Tập dữ liệu này là sự kết hợp từ ba nguồn khác nhau:
•	Figshare: Một nguồn cung cấp dữ liệu chất lượng cao.
•	SARTAJ dataset: Tuy nhiên, có vấn đề với việc phân loại hình ảnh khối u glioma, do đó, các ảnh trong lớp này đã được thay thế bởi dữ liệu từ Figshare.
•	Br35H dataset: Cung cấp hình ảnh cho lớp "No Tumor
Số lượng và cấu trúc:
Tổng số ảnh: Tập dữ liệu bao gồm 7023 ảnh MRI não được phân loại thành 4 nhóm chính:
•	Glioma Tumor: Khối u tế bào thần kinh đệm.
•	Meningioma Tumor: Khối u màng não.
•	Pituitary Tumor: Khối u tuyến yên.
•	No Tumor: Không có khối u.
Phân bổ dữ liệu: Tập dữ liệu được chia thành hai tập con phục vụ quá trình huấn luyện và đánh giá:
•	Tập huấn luyện (Training set): Được sử dụng để mô hình học và tối ưu hóa các tham số.
•	Tập kiểm tra (Testing set): Dùng để đánh giá độ chính xác và hiệu quả của mô hình trên dữ liệu chưa từng thấy

<img width="875" height="407" alt="image" src="https://github.com/user-attachments/assets/fb5990ab-bf3a-4d7b-a1d2-75d7215dc73a" />



3.2	 Phương pháp đề xuất
<img width="991" height="493" alt="image" src="https://github.com/user-attachments/assets/c0d6f926-6bb4-4015-a115-ba788747984f" />
