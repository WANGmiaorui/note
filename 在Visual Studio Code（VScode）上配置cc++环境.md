在Visual Studio Code（VScode）上配置c/c++环境

# 1.安装必要的插件和工具

## 1.1 安装 VSCode

安装 VSCode。可以前往 [Visual Studio Code 官方网站](https://code.visualstudio.com/) 下载并安装

## 1.2 安装编译器

参考 http://xhslink.com/a/G3SXK810ejaX这篇笔记安装MinGW

## 1.3 安装 VSCode的 C/C++ 扩展

![image-20241006100325612](D:\苗\笔记\实习笔记Typora\图片\image-20241006100325612.png)

### 1.3.1 c/c++插件

搜索C/C++ 安装第一个插件



![image-20241006100403926](D:\苗\笔记\实习笔记Typora\图片\image-20241006100403926.png)



### 1.3.2 Code Runner插件

再搜索安装Code Runner

![image-20241006100619681](D:\苗\笔记\实习笔记Typora\图片\image-20241006100619681.png)

### 1.3.3 中文插件(Chinese)

![image-20241006100732075](D:\苗\笔记\实习笔记Typora\图片\image-20241006100732075.png)

还有很多好用的插件，需要的可以自行下载

### 1.3.5 C/C++ Extension Pack

![image-20241006103409935](D:\苗\笔记\实习笔记Typora\图片\image-20241006103409935.png)



这个插件是一个预配置的扩展集合，包括了开发C/C++所需的基础工具。

![image-20241006103512404](D:\苗\笔记\实习笔记Typora\图片\image-20241006103512404.png)





# 2.配置调试功能

## 2.1 新建文件夹

在任意位置建一个文件夹（路径里不要有中文）

以后的C/C++代码文件都要放在这个文件夹里才可以正常调试。

![image-20241006101332193](D:\苗\笔记\实习笔记Typora\图片\image-20241006101332193.png)

## 2.2 打开文件夹，并信任文件夹



![image-20241006101546112](D:\苗\笔记\实习笔记Typora\图片\image-20241006101546112.png)





![image-20241006101645924](D:\苗\笔记\实习笔记Typora\图片\image-20241006101645924.png)

## 2.3 创建完成后再点击这个图标新建四个文件

```
//c_cpp_properties.json
//launch.json
//settings.json
//tasks.json
```

在这里面添加

![image-20241006102057869](D:\苗\笔记\实习笔记Typora\图片\image-20241006102057869.png)

### 2.3.1 c_cpp_properties.json

```
{
    "configurations": [
      {
        "name": "Win64",
        "includePath": ["${workspaceFolder}/**"],
        "defines": ["_DEBUG", "UNICODE", "_UNICODE"],
        "windowsSdkVersion": "10.0.18362.0",
        "compilerPath": "D:/workApp/x86_64-13.2.0-release-win32-seh-msvcrt-rt_v11-rev1/mingw64/bin/g++.exe",
        "cStandard": "c17",
        "cppStandard": "c++17",
        "intelliSenseMode": "gcc-x64"
      }
    ],
    "version": 4
  }

```



![image-20241006102637407](D:\苗\笔记\实习笔记Typora\图片\image-20241006102637407.png)

注意compilerPath这一项要把路径改成刚才g++的安装路径:找到刚刚的安装文件夹->MinGW->bin->g++,exe ，注意一下格式

### 2.3.2 launch.json

```
{
    "version": "0.2.0",
    "configurations": [
      {
        "name": "(gdb) Launch", 
        "type": "cppdbg", 
        "request": "launch", 
        "program": "${fileDirname}\\${fileBasenameNoExtension}.exe", 
        "args": [], 
        "stopAtEntry": false,
        "cwd": "${workspaceRoot}",
        "environment": [],
        "externalConsole": true, 
        "MIMode": "gdb",
        "miDebuggerPath": "D:\\workApp\\x86_64-13.2.0-release-win32-seh-msvcrt-rt_v11-rev1\\mingw64\\bin\\gdb.exe",
        "preLaunchTask": "g++",
        "setupCommands": [
          {
            "description": "Enable pretty-printing for gdb",
            "text": "-enable-pretty-printing",
            "ignoreFailures": true
          }
        ]
      }
    ]
  }
```

注意路径

![image-20241006102848828](D:\苗\笔记\实习笔记Typora\图片\image-20241006102848828.png)

### 2.3.3 settings.json

```
{
  "files.associations": {
    "*.py": "python",
    "iostream": "cpp",
    "*.tcc": "cpp",
    "string": "cpp",
    "unordered_map": "cpp",
    "vector": "cpp",
    "ostream": "cpp",
    "new": "cpp",
    "typeinfo": "cpp",
    "deque": "cpp",
    "initializer_list": "cpp",
    "iosfwd": "cpp",
    "fstream": "cpp",
    "sstream": "cpp",
    "map": "c",
    "stdio.h": "c",
    "algorithm": "cpp",
    "atomic": "cpp",
    "bit": "cpp",
    "cctype": "cpp",
    "clocale": "cpp",
    "cmath": "cpp",
    "compare": "cpp",
    "concepts": "cpp",
    "cstddef": "cpp",
    "cstdint": "cpp",
    "cstdio": "cpp",
    "cstdlib": "cpp",
    "cstring": "cpp",
    "ctime": "cpp",
    "cwchar": "cpp",
    "exception": "cpp",
    "ios": "cpp",
    "istream": "cpp",
    "iterator": "cpp",
    "limits": "cpp",
    "memory": "cpp",
    "random": "cpp",
    "set": "cpp",
    "stack": "cpp",
    "stdexcept": "cpp",
    "streambuf": "cpp",
    "system_error": "cpp",
    "tuple": "cpp",
    "type_traits": "cpp",
    "utility": "cpp",
    "xfacet": "cpp",
    "xiosbase": "cpp",
    "xlocale": "cpp",
    "xlocinfo": "cpp",
    "xlocnum": "cpp",
    "xmemory": "cpp",
    "xstddef": "cpp",
    "xstring": "cpp",
    "xtr1common": "cpp",
    "xtree": "cpp",
    "xutility": "cpp",
    "stdlib.h": "c",
    "string.h": "c"
  },
  "editor.suggest.snippetsPreventQuickSuggestions": false,
  "aiXcoder.showTrayIcon": true
}
```

### 2.3.4 tasks.json

```
{
    "version": "2.0.0",
    "tasks": [
      {
        "label": "g++",
        "command": "g++",
        "args": [
          "-g",
          "${file}",
          "-o",
          "${fileDirname}/${fileBasenameNoExtension}.exe"
        ],
        "problemMatcher": {
          "owner": "cpp",
          "fileLocation": ["relative", "${workspaceRoot}"],
          "pattern": {
            "regexp": "^(.*):(\\d+):(\\d+):\\s+(warning|error):\\s+(.*)$",
            "file": 1,
            "line": 2,
            "column": 3,
            "severity": 4,
            "message": 5
          }
        },
        "group": {
          "kind": "build",
          "isDefault": true
        }
      }
    ]
  }
```



# 3.打出第一个程序

新建.c/.cpp文件

![image-20241006104820164](D:\苗\笔记\实习笔记Typora\图片\image-20241006104820164.png)

在里面写代码然后运行

![image-20241006104912406](D:\苗\笔记\实习笔记Typora\图片\image-20241006104912406.png)

![image-20241006104736069](D:\苗\笔记\实习笔记Typora\图片\image-20241006104736069.png)