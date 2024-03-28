# golang-unicorn-sample
在Golang中使用unicorn-engine进行汇编指令模拟执行的测试样例，静态库已编译配置好(基于unicorn-2.0.1.post1版本编译)，开箱即用
# 编译运行
```shell
go build
```
# 自己编译静态库
若不想使用unicorn-2.0.1.post1版本的静态库，可以自己编译其他版本的，以下命令基于unicorn-2.0.1.post1版本进行编译的，仅供参考
## Linux
linux很简单，基本没啥坑
```shell
mkdir build; cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make
```
## Window
Window环境比较乱，不建议使用基于MSVC的编译，坑很多，建议使用MSYS2编译，打开MSYS2的命令行窗口，输入以下命令即可编译
```shell
pacman -S mingw-w64-x86_64-toolchain mingw-w64-x86_64-cmake mingw-w64-x86_64-ninja
export PATH=/mingw64/bin:$PATH
mkdir build; cd build
/mingw64/bin/cmake .. -G "Ninja"
ninja -C .
```
