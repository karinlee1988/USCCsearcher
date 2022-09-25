# USCCsearcher
用于在企查查网站上批量查询企业的统一社会信用代码


### 特性
使用`selenium`库，在企查查网站上进行查询并获取统一社会信用代码。

`class UnifiedSocialCreditCodeSearcher(object)`类提供了批量查询统一社会信用代码的功能。其中可以设置`isscreenshot=True` ，查询时同时会对查询结果界面进行截图，以备后续手工核验。

`company.xlsx`用于添加多个企业名称以供查询，运行后程序会生成`company_finished.xlsx`文件保存查询结果。



经个人测试，一次大约批量查询60-80个就会出现人机验证；每天一个账号只能查询不到100个。


### 开始使用

#### step 1

将需要查询的多个企业名称放入`company.xlsx`的A列中，从第2行开始。

#### step 2

运行`uscc_searcher.py` 。程序运行后，生成浏览器实例并自动最大化。此时有30s时间用于扫码登录企查查账号。登录后将那些广告之类的弹窗全部关闭，等待30s后程序的自动化处理。

#### step 3

程序自动运行，输出结果。程序结束后，`company_finished.xlsx`文件的B列将会填写查询到的统一社会信用代码；设置`isscreenshot=True` 后会在程序的路径下保存格式为`{row}_{company_name}.png`的截图；IDE亦会print相应的查询结果。

### 免责声明

代码仅供学习测试，切勿用于非法用途！





