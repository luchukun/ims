# 创建云服务器\(Linux\)<a name="ZH-CN_TOPIC_0030713194"></a>

该任务指导用户使用未初始化的私有镜像创建云服务器。

## 前提条件<a name="zh-cn_topic_0029486610_zh-cn_topic_0029124475_section16323558145024"></a>

已准备未初始化的私有镜像。

## 操作步骤<a name="zh-cn_topic_0029486610_zh-cn_topic_0029124475_s3524cdcb025c4c3aa892d8c644fc677e"></a>

1.  登录管理控制台。
2.  单击“计算”下的“镜像服务”。
3.  在“镜像”列表页面，单击“私有镜像”进入对应的镜像列表。
4.  在私有镜像所在行的“操作”列下，单击“申请服务器”，创建云服务器。用户也可以单击镜像名称，在镜像详情页面单击“申请云服务器”，创建云服务器。由于此云服务器需要进行相关配置和删除，强烈建议您使用“按需付费”的方式创建云服务器。
5.  根据界面提示完成云服务器的创建。

    创建云服务器的相关操作请参见《弹性云服务器用户指南》。

    如果在镜像文件系统中已经安装并配置了Cloud-init工具，请按照界面提示设置密码方式登录云服务器。如果镜像文件系统中未安装Cloud-init工具，请使用镜像文件中包含登录该镜像所创建云服务器的密码或证书登录。

6.  执行以下步骤检查云服务器，验证私有镜像是否可用。

    1.  如果云服务器启动成功，证明云平台的自动化配置已为您安装云服务器正常运行依赖的XEN和KVM驱动。否，请请您在注册镜像前确保镜像已安装XEN和KVM驱动。

        建议您禁用任何防病毒软件或入侵检测软件，安装XEN和KVM驱动完成后，您可以再次重启上述服务。

        云服务器安装XEN和KVM驱动的具体操作请参考[优化过程\(Linux\)](优化过程(Linux).md)。

    2.  如果能够使用用户设置的密码/密钥登录云服务器，证明已安装Cloud-init工具。否，请使用原始密码/密钥登录云服务器，再请参考[安装Cloud-init工具](安装Cloud-init工具.md)安装Cloud-init。
    3.  请参考“[配置云服务器\(Linux\)](配置云服务器(Linux).md)”章节检查相关配置。

    如果满足以上条件，则私有镜像可用，请参考[清理环境\(可选）](清理环境-Linux.md)章节执行相关操作。


