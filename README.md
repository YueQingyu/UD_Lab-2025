任务一
1.关于选择下载anaconda还是miniconda我首先进行了查阅，发现下载anaconda在以下方面对于新手更有优势：
（1）可以快速开启学习
（2）內部已经置有实用工具
（3）环境配置更简单
（4）学习上手更轻松
因此我选择下载anaconda

2.在检查完anaconda下载完成后开始进行创建python虚拟环境，我选择了python的3.10版本，既符合了考核的要求同时也考虑了最新版本3.12可能存在bug还不稳定的情况。在下载的过程中，我经历了网络连接失败，设置了清华源但仍连接在国外的服务器repo.anaconda.com而导致下载失败的过程，最终我改用了使用python自带的venv才成功进行创建该虚拟环境。使用该方法进行创建避开了网络问题，同时也成功创建了独立虚拟环境。而通过在cmd中输入dir也成功验证了venv该虚拟环境的成功建立。

3.关于选择安装pytorch，我选择了CPU版本。
理由：CPU版本适合没有NVIDIA显卡的电脑，而我经过硬件检查，命令行输出“False”（截图有说明），则说明我的电脑只能够下载CPU版本的pytorch。

4.通过Git的配置验证，根据截图相关显示，Git已安装成功且用户信息已正确配置，可与GitHub正常通信。

具体困难及解决过程

困难1：Conda网络连接失败（截图：images/conda_network_error.png）
问题描述：使用conda创建环境时出现HTTP连接失败，无法从官方服务器下载包
解决过程：
1. 尝试更换网络环境 → 问题依旧
2. 配置清华镜像源 → 配置复杂且仍有超时问题
3. 最终方案：放弃conda，改用Python自带的venv

困难2：虚拟环境创建与验证（截图：images/venv_structure.png  images/venv_activated.png）
项目文件夹结构，包含venv、images、README.md
虚拟环境激活成功，显示(venv)前缀，Python版本3.13.7
解决方案：
· 使用python -m venv venv成功创建虚拟环境
· 通过venv\Scripts\activate激活环境
· 验证Python版本，确保环境独立可用
