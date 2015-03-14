# 简介 #
  * 下载MediaWiki文章归档
  * 如何索引
  * 上传至iPhone/iPod touch.

# 详细内容 #

**下载MediaWiki文章归档**

归档文件包含了MediaWiki的文本信息和对图像的描述。

关键的问题是如何找到正确的文件。如Wikipedia这样的网站提供了不同形式的归档以利各种用途。一些文件包含了不必要的信息。你只需一个包含了当前版本的文章内容的文件(**"contains current versions of article content"**)，即 pages-articles.xml.bz2。

下载Wikipedia的详细方法请参考：

> http://download.wikimedia.org/backup-index.html

基于Wikia的站点也使用了MediaWiki系统，其归档可循 Special:Statistics 页面得到。(参考 http://www.wikia.com/wiki/Wikia:Database_download)

**用indexer生成索引**

Indexer程序的目的是扫描下载的 .bz2 文件，重组xml数据生成索引过的'articles.bin' 和包含图片名的文件'images.txt'。

命令：
> indexer your\_dump\_file.xml.bz2

其结果为当前目录下的articles.bin。需要注意的是：indexer并不对覆盖操作进行提示，故注意备份同目录下的原有articles.bin。

其他工具也可提供相似功能，及更加用户友好的GUI。

**上传至 iPhone/iPod touch**

目前，wiki2touch 只能运行于“已越狱”的 iPhoneOS 设备上（ WinCE 的移植版本不在此处讨论），故假设你已可以存取文件系统。

默认的位置是'/var/mobile/Media/Wikipedia/**xx**/'，其中 '**xx**' 表示两个字节的语言代码，例如 'en' 表示英语，'fr'表示法语，'de'表示德语，'zh'表示汉语，'ja'表示日语等。

目前，英文版 Wikipedia 已有 5GB 之大，其他语言也有数百 MB ，通过 Wifi 进行 SCP 拷贝将会十分缓慢耗时。一些软件支持通过 USB/Dock 的文件传输，如 PC 上的 iFunBox 或 Mac 上的 DiskAid 等。

如有疑问，可现行上传一个较小的文件进行测试。如下articles.bin，源自遗忘的国度Wiki(http://forgottenrealms.wikia.com/ )
> http://wiki2touch-standalone-ui.googlecode.com/files/articles.bin