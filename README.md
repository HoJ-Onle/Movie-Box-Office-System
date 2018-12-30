![十三组](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1540476601004&di=1836db18b117c2fada5324c06d62d2de&imgtype=0&src=http%3A%2F%2Fp8.qhimg.com%2Fdmsmty%2F350_200_%2Ft01b59f3c80d947c82d.jpg)  

# 软件工程13组

|Number| Id | Name | English | Tasks |
| :-: | :-: | :-: | :-: | - |
| 1 | SZ160110224 | 姜昊 | jianghao | 服务器系统、环境的调配、配置，数据库管理，实现数据库中数据与网页的连接使用，登录注册模块 |
| 2 | SZ160110231 | 但远琦 | danyuanqi | 电影数据爬虫功能的实现、电影数据数据库的构建、存储与管理|
| 3 | SZ160110214 | 陈润泽 | chenrunze | 可视化相关界面、前端绘图、可视化&用户图表库数据交互 |
| 4 | SZ160110216 | 赵昕玥 | zhaoxinyue | 主页、登录界面、导航栏、报表图片导出为pdf |
| 5 | SZ160110205 | 许浚伟 | xujunwei | 服务器管理、数据库管理、可视化业务逻辑后台模块实现 |
- - -

## 项目的依赖环境、使用说明
### Server端
- - -
#### 硬件配置
|Item| Request |
| - | - |
| CPU核数 | 建议选择可以独占一核的CPU使用 |
| 系统位数 | 建议64位以上系统 |
| 操作系统要求 | 建议选用64位Linux系统 |
| 内存大小 | 建议内存大小在1GB以上 |
| 硬盘空间 | 建议40GB以上 |

#### 软件配置
|Item| Request |
| - | - |
| Python | 使用Python3.6以上的版本 |
| PHP | 使用PHP7.0+版本 |
| 数据库 | 建议使用MySQL5.7及更新的版本 |


### Client端
- - -
|Item| Request |
| - | - |
| CPU要求 | 建议CPU核数为双核或以上 |
| 内存大小要求 | 建议内存大小在1GB以上 |
| 网络协议 | 支持TCP/IP协议，以及HTTP协议 |
| 操作系统要求 | Windows版本：Windows 2000/XP/2003/Vista/7及以上 </br> Linux版本：内核要求Linux kernel - 2.2.14及以上，并且至少要安装glibc 2.2.4、gtk+ 2.0函数库 </br> Mac版本：Mac OS X 10.2.x 及以上
| 浏览器要求 | 使用Internet Explorer 6.0及以上版本，或使用Chrome或Firefox浏览器 |
- - -

## 实现功能与实现技术

|Number| Module | Implements | Remark | Files
| :-: | :-: | - | :-: | - |
| 1 | 登录 | js、php实现验证码，登录和密码加密 | 基础功能 | 前端： jawnho.xyz/log.html  </br>后台：logincheck.php、picture.php | 
| 2 | 注册 | js、php实现注册、密码加密，SMTP协议邮箱服务器进行注册邮件链接生成发送 | 基础功能、附加功能(邮箱注册验证) | 前端： jawnho.xyz/register.html  </br>后台：connect.php、register.php、active.php、SMTPclass.php |
| 3 | 电影数据可视化 | Ajax异步请求数据, 后台从MySQL中获取对应数据部分后递交给前端，前端使用`echarts.js` 插件绘图 | 基础功能 | 前端： jawnho.xyz/vis*.html, jawnho.xyz/style/js/paint_charts.js </br>后台： jawnho.xyz/ControllerPost.php, jawnho.xyz/service/model.php |
| 4 | 图表存储 | 前端进行base64编码, 服务器使用MySQL无重复地存储图片数据 | 附加功能 | 前端： jawnho.xyz/vis*.html </br>后台： jawnho.xyz/ControllerPost.php, jawnho.xyz/service/model.php: imageStore |
| 5 | 用户图表库展示 | Ajax异步请求图片，后台递交base64编码的图片，由前端进行动态展示 | 附加功能 | 前端： jawnho.xyz/report.html </br>后台： jawnho.xyz/ControllerGet.php, jawnho.xyz/service/model.php: imageLoad |
| 6 | 下载图片 | 使用 `echarts.js` 插件生成 | 基础功能 | 前端： jawnho.xyz/vis*.html |
| 7 | 生成报表 | 使用 `jsPdf.js` 插件生成 | 基础功能 | 前端： jawnho.xyz/report.html |
| 8 | 基本电影数据爬虫 | 使用scrapy框架构建爬虫对“猫眼专业版”影库进行爬取| 基础功能 | movie/movie/spiders/movie_spider.py |
| 9 | 电影数据更新爬虫 | 使用scrapy框架构建爬虫获取猫眼电影正在上映电影的数据 ，在服务器端编写脚本定时运行| 附加功能 | 服务器端: movie/runCrawl.sh 爬虫: movie_update/movie/spiders/movie_spider.py|
- - -
