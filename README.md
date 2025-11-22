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
- Bước 1: Mở file chứa code và dataset lên:

<img width="840" height="599" alt="image" src="https://github.com/user-attachments/assets/1b4918dd-4945-4a73-a1fe-34ee9b3420ff" />

- Bước 2: Mở file K-means.ipynb bằng Visual studio code lên

<img width="838" height="589" alt="image" src="https://github.com/user-attachments/assets/3af8cbdd-1bbb-4a78-af7f-43add660d32b" />

- Bước 3: Copy path của file mobiles_dataset_2025_processed (5).csv

<img width="549" height="743" alt="image" src="https://github.com/user-attachments/assets/86625a53-46a1-4948-8ce7-71533265e6cd" />

- Bước 4: Paste đường dẫn vừa copy xong vào dòng FILE_PATH đang từ FILE_PATH = "/kaggle/input/mobile-data-set/Mobiles-Dataset-2025-processed (1).csv"  thành 
FILE_PATH = "C:\\Users\\dongq\\Desktop\\kmeans\\mobiles_dataset_2025_processed (5).csv" (tùy từng máy nên phần này không cố định)

<img width="1597" height="734" alt="image" src="https://github.com/user-attachments/assets/a16b585b-50c0-490f-833f-12ee11836da8" />

- Bước 5: Chọn "Run All" --> Python Environments --> Python 3.13.2 (trong quá trình này có bất cứ yêu cầu tải thư viện hay gì thì cứ làm theo yêu cầu nếu thiếu)

<img width="1609" height="381" alt="image" src="https://github.com/user-attachments/assets/17a16b37-119c-4be2-ad44-f00505bea07e" />

<img width="1601" height="352" alt="image" src="https://github.com/user-attachments/assets/d44f3df0-3fce-4652-9310-e0929e130e4f" />

<img width="1615" height="378" alt="image" src="https://github.com/user-attachments/assets/2092c9b8-5154-40d4-91b3-041db03df20d" />

- Bước 6: Nhập b bằng 3 vào

<img width="1622" height="468" alt="image" src="https://github.com/user-attachments/assets/97471999-52ef-4781-b590-c19af5075638" />

- Bước 7: Nhập lần lượt tên 3 nhãn vào: Cao, trung bình, thấp:

<img width="1277" height="332" alt="image" src="https://github.com/user-attachments/assets/da323a20-5f7d-43f8-a72d-4d8ce3c56097" />

<img width="1276" height="377" alt="image" src="https://github.com/user-attachments/assets/fc9f2a5d-4a75-469e-b474-19750be3f775" />

<img width="1276" height="457" alt="image" src="https://github.com/user-attachments/assets/9f7c4c68-3e8e-4537-af28-7fe62a279ea6" />

- Bước 8: Kết quả: ta thu được bảng kết quả như hình 1 và 2 và các file như trong hình 3: kmeans_model.pkl và preprocessor.pkl

<img width="1262" height="749" alt="image" src="https://github.com/user-attachments/assets/17d926a8-a9f4-4bfd-95d6-3eacf8cda91c" />

<img width="1215" height="583" alt="image" src="https://github.com/user-attachments/assets/ad1bfdcc-8509-4537-8725-830cb7baeee3" />

<img width="312" height="405" alt="image" src="https://github.com/user-attachments/assets/75ab673c-289f-4119-bf2b-b836137ea060" />

## 3. Chạy model thuật toán phân lớp

- Bước 1: Mở file chứa code và dataset lên:

<img width="897" height="472" alt="image" src="https://github.com/user-attachments/assets/cf58866e-0937-4974-83ca-c373fff30791" />

- Bước 2: Mở file modeling_knn_dt_rf_nn.ipynb bằng Visual Studio Code

<img width="803" height="671" alt="image" src="https://github.com/user-attachments/assets/ce0b1c14-8c68-4ee6-a5f5-6ca8a96ddea9" />

- Bước 3: Copy path của file mobiles_dataset_2025_clustered_labeled.csv

<img width="737" height="791" alt="image" src="https://github.com/user-attachments/assets/68906efb-e100-4a0b-8a80-2a3a1e7b157f" />

- Bước 4: Paste đường dẫn vừa copy xong vào dòng FILE_PATH đang từ FILE_PATH = "/media/hoang/HDD_Code/Tài liệu học tập/Kỳ 1 năm 4/Khai phá dữ liệu/mobiles_dataset_2025_clustered_labeled.csv" thành 
FILE_PATH = "C:\\Users\\dongq\\Desktop\\phanlop\\mobiles_dataset_2025_clustered_labeled.csv" (tùy từng máy nên phần này không cố định)

<img width="1601" height="962" alt="image" src="https://github.com/user-attachments/assets/917bb270-41e4-4968-bfbf-0b46622b2614" />

- Bước 5: Chọn "Run All" --> Python Environments --> Python 3.13.2 (trong quá trình này có bất cứ yêu cầu tải thư viện hay gì thì cứ làm theo yêu cầu nếu thiếu)

<img width="1275" height="461" alt="image" src="https://github.com/user-attachments/assets/68205852-6902-4f1b-8476-f0f2ee0284f3" />

<img width="1279" height="390" alt="image" src="https://github.com/user-attachments/assets/193b0732-536a-47ae-809f-f170b3a33a85" />

<img width="1270" height="369" alt="image" src="https://github.com/user-attachments/assets/50500a8c-e5a3-4415-b2e1-f3e283053e2a" />

- Bước 6: Sau đó ta được 3 file model đã được train xong gồm: decision_tree_model.pkl, knn_model.pkl và random_forest_model.pkl

<img width="433" height="482" alt="image" src="https://github.com/user-attachments/assets/7e304fa1-d52d-46fb-ab0f-b32c4f45c0fd" />
