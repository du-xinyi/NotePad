# main函数中形参的用法
``` C++
int main(int argc, char** argv)
```
argc 表示命令行参数的数量,包括程序名称本身
argv 包含每个命令行参数的值。每个指针指向一个以null结尾的字符串
``` C++
./executable_file arg1 arg2 arg3

argv[0] -> "./executable_file"
argv[1] -> "arg1"
argv[2] -> "arg2"
argv[3] -> "arg3"
```