# DSO2O


## 关于DSO2O
DSO2O系统是长沙德尚网络科技有限公司推出的一款O2O外卖系统，DSO2O系统是一款专业的O2O本地商圈线上线下源码系统，
包含同城跑腿、外卖送餐、上门服务、等最贴近社区居民的功能特性。
DSO2O包含移动端、微信端，是一款全平台的本地生活/智慧城市创业利器！

## DSO2O技术评价
1、B/S架构
2、MVC编码架构，wap端采用vue.js框架
3、支持Compser
4、支持阿里云存储
5、支持负载均衡
6、支持Mysql读写分离 
7、支持Redis/Memcached
8、支持Linux/Unix/Windows服务器，支持Apache/IIS/Nginx等
9、支持电脑PC端、手机端（微信端）、小程序

## DSO2O后台功能清单
(1)设置: 站点设置、账号同步、上传设置、SEO设置、邮箱关心、支付方式、权限设置、地区管理、数据备份、操作日志
(2)会员：会员管理、会员级别、经验值管理、会员通知、积分管理、预存款、会员相册、会员标签
(3)商品：商品分类、品牌管理、商品管理、类型管理、规格管理、空间管理
(4)店铺：店铺管理、店铺资金、店铺保证金、店铺等级、店铺分类、店铺帮助、开店首页、自营店铺
(5)交易：实物订单、退款管理、订单结算、咨询管理、举报管理、评价管理、投诉管理
(6)网站: 文章分类、文章管理、会员协议、导航管理、广告管理、友情链接
(7)营销：限时折扣、满即送、代金券、分销、吸粉红包、刮刮卡、幸运大抽奖、幸运砸金蛋、生肖翻翻看、礼品管理、礼品兑换、积分奖励、签到、充值卡
(8)统计：行业分析、会员统计、店铺统计、销量分析、商品分析、市场分析、售后分析
(9)公众号：公众号配置、微信菜单、关键词回复、绑定列表、消息推送
(10)平台配送：配送设置、配送员管理、配送结算、配送投诉
(11)跑腿：跑腿设置、跑腿类目、跑腿订单
(12)服务：服务分类、服务机构、服务列表、服务订单、服务资金


## 相关依赖SDK安装
	1.阿里云OSS  composer require aliyuncs/oss-sdk-php   
	介绍地址：https://help.aliyun.com/document_detail/32099.html?spm=5176.87240.400427.47.eaLg1R
	2.phpmailer  composer require phpmailer/phpmailer
  3.阿里云短信  composer require alibabacloud/client

	
## 安装教程
1、将源码解压到服务器空间
2、域名应该指向到public目录，因为应用入口文件位于public/index.php。
比如我的DSMALL项目在  D:\www\dso2o  域名应该指向到 D:\www\dso2o\public
3、进行安装 http://域名/install/install.php
4、后台地址：http://域名/index.php/admin
5、前台地址：http://域名/index.php/home

如果还有什么不懂的到DSMALL论坛(http://bbs.csdeshang.com)进行提问，以及下载最新版本。


## APIDOC 生成API
apidoc -i application/api/controller -o public/apidoc/

V3.2.6
免费版更新 
1.修改配送员保证金保存失败
2.修复只有跑腿订单时不生成配送员结算单的bug
3.修复配送员结算没有计算跑腿订单金额
4.修复支付宝、微信退款原账号 部分退款、不同店铺退款BUG
5.修复百度地图的引用版本，1.2版本无法兼容https  2.0可以
6.新增微信消息模板的功能
7.修复商品规格名称如果带有单引号的话  商品编辑页面会报错
8.新增手机短信发送测试及错误信息提示、格式
9.修复用户在非登录的状态下 访问继承BaseMember  没有做限制
10.规范语言包
11.修复手机注册不登陆
12.删除邮箱必填项
13.店铺中心分销模块 新增分销商品页面，新增如果后台开启分销员返佣 则显示一个提示，提示店铺主后台开启分销员返佣后 分销员购买商品会额外获得一份一级返佣佣金
14.新增初始数据配送员 密码123456
15.修复空间管理权限
16.新增阿里云短信
17.后台新增 手机端访问PC端  是否自动跳转 H5
18.修复微博API接口调用不了类的问题


授权版更新
1.配送员注册页去掉判断是否已登录
2.处理IOS手机 商品详情页面滑动卡顿的问题
3.修复登录页面返回按钮失效的BUG
4.新增手机端卖家验证收货码
5.申请提现页面如果没有提现账号 新增一个提示和跳转到新增提现账号页面的链接
6.商家中心添加商品搜索页
7.添加用户时，新增默认的支付密码
8.新增商品详情页面骨架屏
9.优化实名认证页面的显示
10.去除没有规格值的规格名称显示
11.新增我的浏览记录页面
12.新增手机端上传商品
13.新增手机端入驻
14.修复第一个规格没有设置库存 那么手机端点击商品后就无法切换该商品的其他规格
15.修复推广链接注册不显示推荐员是谁
16.修正手机端定位不准的问题
17.新增H5支付中间页面
18.新增手机端卖家验证收货码


V3.2.5
1. 修复系统发生的短信未记录到短信日志中，且未做限制的bug
2. 修复时间插件没有显示中文的bug
3. 修复店铺删除图片后的默认图片显示不出来的bug
4. 商品列表新增规格编辑
5. 更新后台权限列表
6. 修复只有一级分类时发布商品提示未绑定分类的bug
7. 店铺资金表店铺保证金表将seller_id改成store_id
8. 新增后台跑腿订单可以进行导出EXCEL
9. 新增用户可以对跑腿订单进行评价
10.新增跑腿订单可以显示接单人员信息以及电话号码，方便联系
11.新增后台管理员可以给跑腿订单指派配送员
12.修复发送全员消息时不显示的bug
13.修复手机端微信支付调用不出的bug
14.新增实名认证功能


V3.2.3
1. 新增红包活动
2. 新增刮刮卡活动
3. 新增大转盘活动
4. 新增砸金蛋活动
4. 新增生肖翻翻看活动


V3.2.2
1. 新增签到送积分
2. 店铺管理新增聊天
3. 发布商品添加事务
4. 修复营业执照验证


V3.2.1
1. 新增PC端家政服务
2. 修复投诉 需要平台审核通过之后卖家才能查看
3. 新增服务机构后台审核
4. 修复微信支付必须开启微信扫码支付的优化


V3.1.4
1. 新增自动拒单
2. 修复后台配送员结算
3. 修复配送员投诉
4. 修复搜索页品牌的bug


V3.1.3
1. 公共头部尾部优化
2. 新增配送端百度地图
3. 新增自动派单功能
4. 优化店铺列表


V3.1.1
1. PC端新增配送员管理
2. 修复下单判断处理
3. 新增配送员接单socket接口
4. 新增分销比例范围
5. 语言包更新