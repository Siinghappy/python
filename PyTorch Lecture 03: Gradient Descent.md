What is the learning??? find the best w that minimizes the loss
<img width="770" alt="image" src="https://github.com/user-attachments/assets/1001fa28-6e5d-48f3-a1db-d0a682a02b53" />
# Gradient descent algorithm
1.intial weight: start random w
<img width="791" alt="image" src="https://github.com/user-attachments/assets/209a9264-b347-468e-86d9-34f57aade290" />
2.compute the gradient
3.define the lr
4.update the w
<img width="487" alt="image" src="https://github.com/user-attachments/assets/b62d2fe6-8f8c-44c6-866c-28bc46ab8d67" />
## How to compute derivative?
<img width="645" alt="image" src="https://github.com/user-attachments/assets/adc7666d-95fe-4ba2-bfab-b385aa8c2dbd" />
<img width="373" alt="image" src="https://github.com/user-attachments/assets/22785cf7-87f9-4083-84c0-ca5c9bc5d37e" />
# compute the gradient
<img width="542" alt="image" src="https://github.com/user-attachments/assets/a030b57a-91bf-48a1-b82b-74f387b9247f" />
<img width="496" alt="image" src="https://github.com/user-attachments/assets/504e00f8-28c5-4a1f-8192-07f2e88f65c4" />
#1.初始条件：定义x，y数据组，导入数据库，定义初始参数
import numpy as np
import matplotlib.pyplot as plt
x = [2.0, 4.0, 6.0, 8.0]
y = [4.0, 8.0, 12.0, 16.0]

#2.定义前向传播模型函数，和损失函数
def forward(x):
    return x*w
def loss(x, y):
    y_pred = forward(x)
    return (y_pred-y)*(y_pred-y)

#5.compute the gradient
def gradient(x, y):
    return 2 * x * (x*w - y)

#6.update w
## training loop
lr = 0.01
w= 0 
for epoch in range(100):
    for x_val, y_val in zip(x, y):
        grad = gradient(x_val, y_val)
        w = w - lr* grad
    l = loss(x_val, y_val)
    print('progress:', epoch, 'w=', w, 'loss=', l)

#7. predict
print('yred=', forward(9.0), 'y=', 18)    
    


