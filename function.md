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

##### python中一共有五种参数
- 参数组合的顺序是 必选参数、默认参数、可变参数、命名关键字参数和关键字参数。

##### 默认参数
- 当使用可变对象的时候，默认参数会记住上一次的值。
- none是不可变对象

##### 可变参数
- 参数的个数可变
- 函数内部接受到的是一个tuple
```
def calc(*numbers):
    sum = 0
    for n in numbers:
        sum = sum + n * n
    return sum
```
- Python允许你在list或tuple前面加一个 * 号，把list或tuple的元素变成可变参数传进去

##### 关键字参数
- 关键字参数用 ** 表示
- 关键字参数的接受对象是字典
```
def person(name, age, **kw):
    print('name:', name, 'age:', age, 'other:', kw)
```


##### 命名关键字参数
```
def person(name, age, **kw):
    if 'city' in kw:
        # 有city参数
        pass
    if 'job' in kw:
        # 有job参数
        pass
    print('name:', name, 'age:', age, 'other:', kw)
```
