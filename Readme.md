# 百度的 php sdk

https://cloud.baidu.com/doc/CDN/s/ejwvyfgw1

运行环境

PHP SDK 包要求运行环境至少为 PHP 5.3.2 版本 (暂不支持 PHP 8 及以上版本)，如 5.4、5.5、5.6、7.0、7.1、7.2、7.3。

安装步骤

在 官方网站下载 PHP SDK 压缩工具包。
解压 ZIP 包之后有三个文件，如下：

    1. BaiduBce.phar                    //PHP SDK
    2. CdnClientSample.php         //示例
    3. CdnSampleConf.php                //参考配置文件，具体内容见下文
在脚本文件中添加以下代码，即可以使用 SDK 包：

    1. include BaiduBce.phar;
    2. require YourConf.php;
SDK 目录结构

 1. BaiduBce.phar
 2. ├──src
 3. │   └──BaiduBce
 4. │       ├──Auth                //BCE签名相关
 5. │       ├── **Exception**           //BCE客户端的异常
 6. │       ├──Http                //BCE的Http通信相关
 7. │       ├── **Log**                 //BCE日志
 8. │       ├──Services
 9. │       │   └──Cdn                   //Cdn主目录，此目录必须保留
10. │       │       ├──CdnClient.php     //Cdn操作类，所有操作可以通过CdnClient类可以完成
11. │       └──Util                //BCE公用工具
12. └──vendor                       //第三方库