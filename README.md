# Model mẫu phát hiện cơ thể người

Repo này chứa script Python chính và các thứ cần thiết, để tạo ra một model TensorFlow có khả năng phát hiện cơ thể người trong một bức ảnh bất kỳ. Sau khi train xong model thì biểu đồ và các thông số phân tích sẽ được in ra.

Dataset dùng để train nằm trong thư mục `yoga_cg`.

Đây là assignment 2 môn DSS301 của G2.

## Chạy kiểu gì
1. Tạo môi trường ảo Python (`venv`), và kích hoạt nó:
```
python3 -m venv env
source env/bin/activate
```
2. Cài đặt các thư viện cần thiết: `pip install -r requirements.txt`
1. Clone mấy thứ cần thiết về:
```
wget -q -O movenet_thunder.tflite https://tfhub.dev/google/lite-model/movenet/singlepose/thunder/tflite/float16/4?lite-format=tflite
git clone https://github.com/tensorflow/examples.git

wget -O yoga_poses.zip http://download.tensorflow.org/data/pose_classification/yoga_poses.zip
unzip -q yoga_poses.zip -d yoga_cg
rm yoga_poses.zip
```
3. Chạy: `./main.py`. Nhớ để ý nó output những cái gì.