# Text generation web UI 汉化版

原仓库链接：<https://github.com/oobabooga/text-generation-webui>。

本项目对其进行了部分汉化和镜像站设置，有助于优化在 `github` 下载较慢的问题。  
注意：当前项目只进行了部分 `windows` 系统的汉化，其他系统将会陆续实现。

## 更改
### `start_windows.bat`
修改了 `anaconda` 的[下载链接](https://mirrors.tuna.tsinghua.edu.cn/anaconda/miniconda/Miniconda3-py310_23.3.1-0-Windows-x86_64.exe)。   
清华大学镜像站：<https://mirrors.tuna.tsinghua.edu.cn>。

### `requirements.txt` 即其他
将下载链接中的 `github` 改为 `kkgithub`。   
`kkgithub` 镜像站：<https://kkgithub.com>。

### `one_click.py`
修改了 `pip` 的下载链接：
```
python -m pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
```
修改 `git` 的访问方式，以防止 `git` 在 `HTTP/2` 情况下有可能出错：
```
git config --global http.version HTTP/1.1
```
同时对 `CPU/GPU` 选择部分进行了汉化。

## 安装方式
1. 下载并解压 `text-generation-webui-Chinese`，请注意路径中均为英文字母。
2. 选择你的系统，点击 `start_linux.sh/start_macos.sh/start_windows.bat` 并运行，请注意除 `start_windows.bat` 外并未设置镜像。
3. 待运行完毕后，点击 `update_linux.sh/update_macos.sh/update_windows.bat` 检测。
4. 使用时再次打开 `start_linux.sh/start_macos.sh/start_windows.bat`，访问网站。
5. 下载模型。对于无法访问 <https://huggingface.co/> 的情况，可以选择 <https://modelscope.cn/>。
6. Enjoy!
