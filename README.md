Giới thiệu

Dự án này xây dựng mô hình phân loại ảnh sử dụng Deep Learning để phân loại ảnh tự nhiên thành 8 lớp :
airplane, car, cat, dog, flower, fruit, motorbike, person.
Mô hình được xây dựng bằng ResNet50 và triển khai bằng PyTorch.

Công nghệ sử dụng : Python, PyTorch, Torchvision, ResNet50, Matplotlib, Seaborn
Kaggle / Jupyter Notebook

Tiền xử lý dữ liệu

Ảnh được xử lý bằng torchvision.transforms:
Resize ảnh về 224 × 224
Data augmentation: Random Horizontal Flip, Random Rotation
Chuyển ảnh sang Tensor
Chuẩn hóa dữ liệu theo ImageNet

Huấn luyện mô hình

Quá trình huấn luyện gồm 2 bước:
Transfer Learning : Freeze các lớp của ResNet50, Huấn luyện lớp Fully Connected cuối
Fine-tuning : Unfreeze toàn bộ mô hình, Huấn luyện lại với learning rate nhỏ hơn

Đánh giá mô hình
Mô hình được đánh giá bằng: Validation Accuracy, Confusion Matrix
Kết quả đạt khoảng 85–90% độ chính xác trên tập validation.
