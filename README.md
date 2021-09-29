# banana_blackmail
Golang写的勒索软件，仅供学习与交流勒索软件行为，切勿对真实目标操作，否则后果自负！

此项目用时三天完成的，较为粗糙，简单实现了勒索病毒文件加解密，以及删除卷影和备份等操作；
后续会添加新的功能以及代码优化。

## 文件介绍:
blackmail - 文件加密，以及删除卷影备份等;
blackmail_dec - 对加密的文件进行解密;
RSA - 生成RSA公私钥.

## 用法:
由于还在测试和添加新功能中，所以只递归加解密某个文件夹下的所有文件（在blackmail/blackmail_dec的 main.go 中可以写入要加解密的文件）。
### 勒索测试:
进入blackmail的main.go中，输入要加密的文件路径
进入blackmail中 go build 打包项目生成exe文件，以管理员运行。
### 解密文件:
进入blackmail_dec的main.go中，输入要解密的文件路径
进入blackmail_dec中 go build 打包项目生成exe文件运行即可。

## 补充
加密前的文件如果为1.txt,则加密后的文件为1.txt.banana;
1.txt.banana分为三部分:
  第一部分为RSA公钥加密的随机生成的AES key,
  第二部分为提示信息，提示你的文件已被加密,
  第三部分为文件加密后的内容。

## *重要:
此项目仅供学习与交流勒索软件行为，切勿对真实目标操作，否则后果自负！
