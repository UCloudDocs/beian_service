# APP特征信息填写指导



## 基础概念

| 概念                       | 解释                                                         |
| -------------------------- | ------------------------------------------------------------ |
| 包名（安卓应用标识符）     | APK包名是Android应用程序的唯一标识符。                       |
| Bundle ID（iOS应用标识符） | Bundle ID是iOS应用程序的唯一标识符。                         |
| 数字摘要                   | 数字摘要又称数字指纹，是使用Hash函数将待加密明文转化得到的一串固定长度密文。常见的摘要算法有 MD5、SHA-1、SHA-256等。 |



## 安卓应用获取App特征信息指导

公钥和MD5值可以通过安卓开发工具、keytool、Jadx-GUI等多种工具获取，本文以使用JadxGUI工具获取为例。

1、下载JadxGUI工具：下载安装完成后，使用此工具打开apk包。

2、公钥与签名MD5值获取：查找文件APK signature中模数（公钥）和MD5签名。

![](https://www-s.ucloud.cn/2023/10/3c6b6eccfeb583445a0ae5a227e046f4_1696669586145.jpg)



3、包名获取：查找资源文件下AnddroidManifest.xml中的package属性对应信息。

![](https://www-s.ucloud.cn/2023/10/38d07c145aababdc5bad60091a3d4fbd_1696669828405.jpg)



## iOS应用获取App特征信息指导

1、使用APP对应的iOS开发者账号登录Developer控制台，找到下图标识符(英文)，单击进入Certificates,ldentifiers&Profiles页面。

2、Bundle ID获取：在Certificates,ldentifiers&Profiles页面，单击ldentifiers，其中IDENTIFIER列对应的就是Bundle ID。

![](https://www-s.ucloud.cn/2023/10/170caee1236c76aa8ba9f7c01a78116f_1696669850098.png)

![](https://www-s.ucloud.cn/2023/10/28a5c38b010a2e718401fab6c83f84b8_1696669867387.png)



3、公钥与签名SHA1值获取：在计划资源中，单击证书（英文），进入Certificates页面，可查看证书详情，并下载 APP对应的证书。通过查看证书详细信息，可获取公钥和签名SHA1值。

![](https://www-s.ucloud.cn/2023/10/58df103383e7bf3001a03d4dab43ffb3_1696669882906.png)

![](https://www-s.ucloud.cn/2023/10/5e7b4bb27ab536d2d4a2d0ad49808cbe_1696669898469.png)



**公钥（公共密钥）**:如果公共密钥显示不完整，您可先单击省略号，如果省略号仍然打不开或不显示，直接复制公共密钥省略号前面显示出的数据进行填写即可。

![](https://www-s.ucloud.cn/2023/10/78c5b472758985bc2cd4804e1af519c8_1696669912048.png)



**签名SHA1值（SHA-1）**

![](https://www-s.ucloud.cn/2023/10/b05c7a7bede3c83c1e0a61d7414b58f3_1696669926343.png)



## 鸿蒙应用获取App特征信息指导

1. 使用App对应的鸿蒙应用开发者账号登录[AppGallery Connect](https://developer.huawei.com/consumer/cn/service/josp/agc/index.html#/)。
2. 在**我的项目**页面，选择需要查询特征信息的应用项目。
3. 在应用项目页面的**应用**区域查看包名，即为所需要的App包名。
4. 获取公钥和MD5值。
   1. 选择**我的项目 > 用户与访问**。
   2. 在**用户与访问**页面中，单击左侧**证书管理**，并下载需要备案鸿蒙应用开发者证书。
   3. 下载**应用开发者证书**后，用文本编辑器（如记事本、VSCode），编辑证书，删除证书链部分并保存。
   4. 打开已保存的证书，选择**详细信息 > 公钥**，获取App的公钥信息。
   5. 选择**详细信息 > 指纹**，获取App的签名MD5值信息。
