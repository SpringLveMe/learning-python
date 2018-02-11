##### 函数也是对象
- 数据类型检查可以用内置函数isinstance()实现
```
def my_abs(x):
    if not isinstance(x, (int, float)):
        raise TypeError('bad operand type')
    if x >= 0:
        return x
    else:
        return -x
```

- 返回多个值,返回的是一个tuple
```
x, y = move(100, 100, 60, math.pi / 6)
```
