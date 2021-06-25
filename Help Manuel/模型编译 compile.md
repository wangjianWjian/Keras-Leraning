# 模型编译 compile

训练模型之前要先通过 compile 配置模型，接收至2~3个参数：  
* optimizer：优化器
* loss：损失函数
* metrics：评价标准（回归问题可以没有）

更详细的optimzer，loss，metrics用法可以在当前文件夹下找到


## 多分类
```python
model.compile(
    optimizer="rmsprop",
    loss="categorical_crossentropy",
    metrics=["accuracy"]
)
```

## 二分类
```python
model.compile(
    optimizer="rmsprop",
    loss="binary_crossentropy",
    metrics=["accuracy"]
)
```

## 回归（均方误差）
```python
model.compile(
    optimizer="rmsprop",
    loss="mse"
)
```

## 自定义
```python
import keras.backend as K

def mean_pred(y_true, y_pred):    # 无论用没用到都必须要传入两个值，并且true在前pred在后
    return K.mean(y_pred)

model.compile(
    optimizer="rmsprop",
    loss="binary_crossentropy",
    metrics=["accuracy", mean_pred]
)
```
