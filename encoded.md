##### encoded
- 在最新的Python 3版本中，字符串是以Unicode编码的，也就是说，Python的字符串支持多语言
- 对于单个字符的编码，Python提供了ord()函数获取字符的整数表示，chr()函数把编码转换为对应的字符
- 如果知道字符的整数编码，还可以用十六进制这么写str：`'\u4e2d\u6587'`
- 由于Python的字符串类型是str，在内存中以Unicode表示，一个字符对应若干个字节。如果要在网络上传输，或者保存到磁盘上，就需要把str变为以字节为单位的bytes  `x = b'ABC'`
- 以Unicode表示的str通过encode()方法可以编码为指定的bytes
- 反过来，如果我们从网络或磁盘上读取了字节流，那么读到的数据就是bytes。要把bytes变为str，就需要用decode()方法
```
#!/usr/bin/env python3
# -*- coding: utf-8 -*-
```
