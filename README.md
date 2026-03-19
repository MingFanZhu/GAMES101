# GAMES101 课程作业
环境：Windows 10 + Visual Studio 2022 + vcpkg + CMake + VSCODE

## 配置CMake插件
配置vcpkg：

1. Ctrl + Shift + P 输入@ext:ms-vscode.cmake-tools
2. 找到cmake.configureArgs
3. 添加-DCMAKE_TOOLCHAIN_FILE=[vcpkg安装路径]/scripts/buildsystems/vcpkg.cmake

## 注意
因为环境与课程要求不一致，所以有cmake文件会和作业课件不一致