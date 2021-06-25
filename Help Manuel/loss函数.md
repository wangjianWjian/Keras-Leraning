# 损失函数loss
这里列出了常见的损失函数与使用范围

回归问题  
| 全写 | 缩写 | 应用范围 |  
| ---- | ---- | ---- |  
| mean_squared_error | mse | 均方误差 |  
| mean_absolute_error | mae | 平均绝对误差 |   



如何使用：  
model.compile(loss='mean_squared_error', optimizer='sgd')  
model.compile(loss='mse', optimizer='sgd')  

后面可以使用自定义的损失函数：  
def myLoss(y_pred, y_true):  
        loss_value = np.abs(y_pred - y_true) ** 3  
    return loss_value

model.compile(loss=myLoss, optimizer='sgd') # 允许直接传入函数句柄
