# AI
import numpy as np

from sklearn.datasets import load_digits

data, labels = load_digits(return_X_y=True) #dữ liệu, bảng 0-9
n_samples, n_features  = data.shape 
n_digits = np.unique(labels).size

print(f"# digits: {n_digits}; # samples: {n_samples}; # features {n_features}")

data, labels lần lượt nhận giá trị của X và y, return_X_y=true chả về x và y với thông tin được rút ngắn
