# 在命令行下C/C++编译
编译使用`clang`, 调试使用`lldb`

写完代码后,假设文件名为`test.cpp`

## 编译

`clang test.cpp -lstdc++ -std=c++11 -g -o test.out`

选项说明:

选项|说明
---|----
`-lstdc++`|使用stdc++ lib
`-std=c++11`|使用c++11标准
`-g`| 生成的文件可以**调试**
`-o test.out`| 生成的文件输出名字为`test.out`,如果不设置这一项,默认为`a.out`

## 执行

已生成的文件`test.out` 或者`a.out`

执行`./test.out`

## 调试

基本的调试命令与gdb,pdb,ipdb相同,其他命令可以网上再搜索

`lldb test.out`

调试命令:


命令|作用
---|----
`l`|list code
`r`| run code
`c`| continue
`s`|step in
`b number`| 在第number行设置代码
`p var`| 打印 var这个变量
`n`| next