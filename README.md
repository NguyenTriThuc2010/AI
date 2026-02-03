# clustering 
```Python
import numpy as np

from sklearn.datasets import load_digits

data, labels = load_digits(return_X_y=True) #dữ liệu, bảng 0-9
n_samples, n_features  = data.shape 
n_digits = np.unique(labels).size

print(f"# digits: {n_digits}; # samples: {n_samples}; # features {n_features}")
```
"data, labels lần lượt nhận giá trị của X và y, return_X_y=true chả về x và y với thông tin được rút ngắn" 

``` sklearn.datasets.load_digits(*, n_class=10, return_X_y=False, as_frame=False)```
```Python
n_class: int, default=10 số của lớp chả về từ 0 đến 9.

return_X_y: bool, default=False nếu đúng, chả về (data, target) thay vì một đối tượng Bunch.

as_frame : bool, default = False

Nếu as_frame=True: data sẽ là một pandas DataFrame Bao gồm các cột với kiểu dữ liệu phù hợp (chủ yếu là số – numeric) target sẽ là: pandas Series → nếu chỉ có một cột nhãn pandas DataFrame → nếu có nhiều cột nhãn Nếu đồng thời return_X_y=True → Hàm sẽ trả về trực tiếp (data, target)
Trong đó:
data: pandas DataFrame
target: pandas Series hoặc DataFrame (tùy số lượng cột nhãn)
```

```n_samples, n_features  = data.shape ```
chúng ta có thể hiểu như sau n_smaples gọi là ảnh, còn n_feature là đặc trưng gắn cho 2 giá trị của dữ liệu 2 chiều ```data.shape(số ảnh, số đặc trưng mỗi ảnh)``` 
```dataset digits có ảnh 8×8 = 64 pixel → 64 features```
