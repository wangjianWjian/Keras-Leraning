# 优化器 Optimizer

---------------

SGD 随机梯度下降  
```python
keras.optimizers.SGD(lr=0.01, momentum=0.0, decay=0.0, nesterov=False)
```
参数
	* 
lr: float >= 0. 学习率。
	* 
momentum: float >= 0. 参数，用于加速 SGD 在相关方向上前进，并抑制震荡。
	* 
decay: float >= 0. 每次参数更新后学习率衰减值。
	* 
nesterov: boolean. 是否使用 Nesterov 动量。

