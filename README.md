# [Python](https://bigjackson.us.kg/python)

## 微信轰炸1.0

### 注意：需要先下载pynput.keyboard库

### 代码 pip install -i https://pypi.tuna.tsinghua.edu.cn/simple pynput

```

from pynput.keyboard import Key, Controller
import time
keyboard = Controller()

a = input("请输入你要循环输出的内容：")
b = eval(input('请输入你想循环的次数：'))
print("数据已接收！请把光标移动到对话框")
time.sleep(2)
for i in range(3):
    print(r'距离程序运行还有%d秒! '%(3-i))
    time.sleep(1)
for i in range(b):
    keyboard.type(a)
    keyboard.press(Key.enter)
    keyboard.release(Key.enter)
    time.sleep(0.1)
print('消息发送完成！请关闭窗口')
```