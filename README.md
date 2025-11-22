<h1 align="center"> 📱 Khai phá dữ liệu bằng phương pháp phân cụm và phân lớp để dự báo giá điện thoại </h1>
<h3 align="center"> Nhóm 3 </h5>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/852b1c87-1b29-4126-98ad-2311f08586ce" />

## 0. Các bước trước khi chạy:
## 0.1. Chuẩn bị môi trường:
- Cài đặt các thư viện cần thiết, tất cả được lưu trong file requirements.txt, sau đó chạy câu lệnh sau:
  pip install -r requirements.txt
- Cài đặt visual studio code (nếu chưa có)
- Cài đặt python: python 3.x trở lên.
- Môi trường: Trong case này là chạy trên windows 11
## 1. Chạy model preprocessing

- Bước 1: Mở folder chứa toàn bộ dự án lên trong Visual Studio code (Folder Data-mining-group-3-main)

<img width="1919" height="1035" alt="image" src="https://github.com/user-attachments/assets/0b0815d8-5217-402c-84d8-c2dd508b6390" />

- Bước 2: Chọn mở rộng phần folder preprocessing và click vào để mở file preprocessing.ipynb

<img width="1918" height="1036" alt="image" src="https://github.com/user-attachments/assets/ccd27137-23e4-430b-95f0-2a82f2af7530" />

- Bước 3: Copy path của file rootdata.csv

<img width="424" height="1008" alt="image" src="https://github.com/user-attachments/assets/55228cf3-fb52-49bb-a15e-4a62f2ae06cd" />

- Bước 4: Paste đường dẫn vừa copy vào vào [28] ở Step 2: Data Collection. Đổi dòng data = pd.read_csv('Mobiles-Dataset-2025.csv', encoding='latin1')
thành data = pd.read_csv('C:\\Users\\dongq\\Desktop\\Data-mining-group-3-main\\rootdata.csv', encoding='latin1') (lưu ý đường dẫn này mỗi máy khác nhau)

<img width="1569" height="994" alt="image" src="https://github.com/user-attachments/assets/8344b3f1-b3f0-4063-87c3-280718b85438" />

- Bước 5: Chọn "Run All" --> Python Environments --> Python 3.13.2 (trong quá trình này có bất cứ yêu cầu tải thư viện hay gì thì cứ làm theo yêu cầu nếu thiếu)

<img width="1009" height="157" alt="image" src="https://github.com/user-attachments/assets/d11a3c52-e701-4bcc-b222-6d5b8c871607" />

<img width="1577" height="232" alt="image" src="https://github.com/user-attachments/assets/20d8026e-8eb8-4008-898c-3b0906d11092" />

<img width="1567" height="400" alt="image" src="https://github.com/user-attachments/assets/b9a8df23-a408-40c6-8bdf-b4e9251eab4b" />

- Bước 6: Sau đó ta được 3 file model đã được train xong gồm: processor_pca.pkl, processor_vectorizer.pkl và top_companies.pkl
## 2. Chạy model K-means
- Bước 1: Mở folder chứa toàn bộ dự án lên trong Visual Studio code (Folder Data-mining-group-3-main)

<img width="1919" height="1035" alt="image" src="https://github.com/user-attachments/assets/0b0815d8-5217-402c-84d8-c2dd508b6390" />

- Bước 2: Chọn mở rộng phần folder kmean và click vào để mở file K-means.ipynb

<img width="1916" height="1019" alt="image" src="https://github.com/user-attachments/assets/958a7a4d-9852-4d42-ba98-9d66daada428" />

- Bước 3: Copy path của file mobiles_dataset_2025_processed (5).csv

<img width="560" height="1009" alt="image" src="https://github.com/user-attachments/assets/5ca45d7e-c873-4f0c-89a8-ea36c757e523" />

- Bước 4: Paste đường dẫn vừa copy xong vào dòng FILE_PATH đang từ FILE_PATH = "dataAfterPreprocess.csv"  thành 
FILE_PATH = "D:\\GitHub\\Data-mining-group-3\\dataAfterPreprocess.csv"
(tùy từng máy nên phần này không cố định)

<img width="1919" height="1019" alt="image" src="https://github.com/user-attachments/assets/0c1eb580-7a9c-4837-8b50-7e595b3ce027" />

- Bước 5: Chọn "Run All" --> Python Environments (optional) --> Python 3.13.2 (optional) (trong quá trình này có bất cứ yêu cầu tải thư viện hay gì thì cứ làm theo yêu cầu nếu thiếu)

<img width="1602" height="268" alt="image" src="https://github.com/user-attachments/assets/1c091d4f-bfa4-4a76-9a01-ec7a1eaaa7ea" />

- Bước 6: Nhập k bằng 4 vào

<img width="1601" height="370" alt="image" src="https://github.com/user-attachments/assets/f20d3a72-b689-4cde-85ca-4a0bc1ed6091" />

- Bước 7: Chọn scrollable element để biết được sẽ gán nhãn như thế nào, ở đây theo ảnh 2 cột Launched Price là sẽ nhập là Cận cao cấp, Trung cấp, Giá rẻ và Cao cấp Nhập lần lượt tên 3 nhãn vào: Cao, trung bình, thấp:

<img width="1588" height="1015" alt="image" src="https://github.com/user-attachments/assets/5b81d4d9-4323-43c3-b53a-8d8d20043756" />

<img width="1301" height="285" alt="image" src="https://github.com/user-attachments/assets/c5cc0cc7-804f-409d-a6ab-75b292821677" />

<img width="1294" height="210" alt="image" src="https://github.com/user-attachments/assets/1b92129c-6288-4dd8-b9c0-651cbe824c20" />

<img width="1309" height="467" alt="image" src="https://github.com/user-attachments/assets/7fa3c30d-3d73-45dc-b738-f0fb8dc3ca2c" />

<img width="1315" height="436" alt="image" src="https://github.com/user-attachments/assets/e3348e3b-f6df-4a0a-b7fc-f1ff4024c3a0" />

<img width="1312" height="438" alt="image" src="https://github.com/user-attachments/assets/6934b7c8-e2bf-4995-8d4a-a737a041f491" />

- Bước 8: Kết quả: ta thu được bảng kết quả như hình 1 và file csv như trong hình 2: kmeans_model.pkl, preprocessor.pkl và file data_with_clusters_and_labels.csv

<img width="322" height="556" alt="image" src="https://github.com/user-attachments/assets/33e19ad1-02bd-415b-a0d0-a9ca274e824e" />

<img width="1914" height="982" alt="image" src="https://github.com/user-attachments/assets/a00e7697-5a91-49bf-acbc-30e7ad45010e" />

## 3. Chạy model thuật toán phân lớp

- Bước 1: Mở folder chứa toàn bộ dự án lên trong Visual Studio code (Folder Data-mining-group-3-main)

<img width="1919" height="1017" alt="image" src="https://github.com/user-attachments/assets/c48b830f-d564-49b5-9fd0-98f3bdd68c16" />

- Bước 2: Chọn mở rộng phần folder phanlop và click vào để mở file modeling_knn_dt_rf_nn.ipynb

<img width="1919" height="1021" alt="image" src="https://github.com/user-attachments/assets/138f55d0-89d1-45c6-a140-53cd1fc760b5" />

- Bước 3: Copy path của file dataAfterPreprocess.csv

<img width="594" height="1018" alt="image" src="https://github.com/user-attachments/assets/a993df19-644e-4de6-aac3-f1546ed86234" />

- Bước 4: Paste đường dẫn vừa copy xong vào dòng FILE_PATH = 'dataAfterPreprocess.csv' thành 
FILE_PATH = 'D:\\GitHub\\Data-mining-group-3\\dataAfterPreprocess.csv' (tùy từng máy nên phần này không cố định)

<img width="1913" height="976" alt="image" src="https://github.com/user-attachments/assets/2fcfafe3-35d8-44c9-85e9-7443fb71cd54" />


- Bước 5: Chọn "Run All" --> Python Environments (optional) --> Python 3.13.2 (trong quá trình này có bất cứ yêu cầu tải thư viện hay gì thì cứ làm theo yêu cầu nếu thiếu)

<img width="1275" height="461" alt="image" src="https://github.com/user-attachments/assets/68205852-6902-4f1b-8476-f0f2ee0284f3" />

<img width="1279" height="390" alt="image" src="https://github.com/user-attachments/assets/193b0732-536a-47ae-809f-f170b3a33a85" />

<img width="1270" height="369" alt="image" src="https://github.com/user-attachments/assets/50500a8c-e5a3-4415-b2e1-f3e283053e2a" />

- Bước 6: Sau đó ta được 3 file model đã được train xong gồm: decision_tree_model.pkl, knn_model.pkl và random_forest_model.pkl

<img width="433" height="482" alt="image" src="https://github.com/user-attachments/assets/7e304fa1-d52d-46fb-ab0f-b32c4f45c0fd" />
