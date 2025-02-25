# matplotlib

## 绘制图表

### 基本结构

~~~python
import numpy as np  
import matplotlib.pyplot as plt  # 导入pyplot模块  
data = np.array([1, 2, 3, 4, 5])  # 准备数据  
plt.plot(data)  # 在当前画布的绘图区域中绘制图表  
plt.show()  # 展示图表
~~~