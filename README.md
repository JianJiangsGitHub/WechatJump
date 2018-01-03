工具介绍

  ● Python
  
  ● 手机或模拟器
  
  ● ADB驱动，可以到【https://adb.clockworkmod.com/】下载

  ● 相关依赖

如果你是iOS + MacOS，请参考下面的配置：

  ● 使用真机调试WDA，参考iOS真机如何安装WebDriverAgent · TesterHome
  
  ● 安装openatx/facebook-wda
  
  ● Python 3
  

如果你是 Android + MacOS，请参考下面的配置：

       
  ● Python 3
  
  ● 使用brew进行安装 brew cask install android-platform-tools
  
  ● clone 项目 cd 打开
  
  ● 安装完后插入安卓设备且安卓已打开USB调试模式（部分新机型可能需要再另外勾上 允许模拟点击 权限），终端输入adb devices ,显示如下表明设备已连接
       List of devices attached 6934dc33 device

      出现错误 mac ModuleNotFoundError: No module named 'PIL'
      解决：sudo pip install pillow 

如果你是 Android + Windows，请参考下面的配置：

  ● Python 3
  
  ● 安装ADB后，请在 环境变量 里将ADB的安装路径保存到PATH变量里，确保ADB命令可以被识别到。
  
  ● 同 Android + MacOS 测试连接
  

2

安卓手机操作步骤

  ● 安卓手机打开 USB 调试，设置--开发者选项--USB 调试
  
  ● 电脑与手机 USB 线连接，确保执行adb devices可以找到设备ID
  
  ● 界面转至微信跳一跳游戏，点击开始游戏
  
  ● 运行python wechat_jump_auto.py，如果手机界面显示USB授权，请点击确认
  
  ● 请按照你的手机分辨率从./config/文件夹找到相应的配置，拷贝到 *.py 同级目录./config.json（如果屏幕分辨率能成功探测，会直接调用 config目录的配置，不需要复制）

3

iOS 手机操作步骤

  ● 运行安装好的 WebDriverAgentRunner
  
  ● 将手机点击到《跳一跳》小程序界面
  
  ● 运行脚本。有两种模式可供选择：手动辅助跳 和 自动连续跳
  
  ● 拷贝./config/iPhone目录下对应的设备配置文件，重命名并替换到./config.json
  
  ● 命令行运行

python3 wechat_jump_auto_iOS.py

  ● 会自动计算坐标并连续起跳，根据起跳的精准情况更改./config.json中的press_coefficient参数，直到获得最佳取值
  
  ● 命令行运行

python3 wechat_jump_iOS_py3.py

  ● 依次点击弹出的窗口中的起始位置和目标位置，会自动计算距离后起跳
  
  ● 根据起跳的精准情况更改python3 wechat_jump_iOS_py3.py中的time_coefficient参数，直到获得最佳取值
  
  ● 手动辅助跳
  
  ● 自动连续跳
  
不得不承认，机器人比人更会玩游戏。
