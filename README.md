# Socfony 需求意见稿

## 终端计划

 - iOS（Flutter）
 - Android（Flutter）
 - 客户端 GraphQL 接口
 - SSR 管理后端？终端管理客户端？暂无计划！

## 业务需求

 - 全局用户无需登录即可进入应用，在例如发表内容，评论，点赞等情况下需要用户登录
 - 用户将账号资料、其他资料、安全资料进行分割。
 - MFA 暂定三种
    1. 用户密码
    2. 用户手机号
    3. TOTP 一次性密码
    > TOTP 不应该用于不验证密码的情况下进行登录
- 用户关注&联系人
    - 两个用户互相关注不等于是好友！内置 IM 好友需要用户单独添加为联系人！
    - 个人主页展示信息为用户个性资料的基本信息和可公开的用户信息，默认列表为用户动态列表
- 动态
    - 用户可以自主发布动态，动态为图文、纯文、纯图、视频配文、纯视频
    - 动态可以附带地理位置信息
    - 动态不仅用户可以自己发布，应用内必要活动也需要进行动态关联。
- 圈子
    - 用户可以加入或者自己创建圈子
    - 圈子存在私密和公开两种类型
    - 创建者默认为圈子的所有人，但是所有人可以转让给其他加入了该圈子的用户
    - 圈子可以设置管理员，具体数量可以使用系统配置表来进行限制
    - 管理员仅能管理圈内帖子和评论，以及移除圈内用户
    - 圈子所有人可以自定义帖子分类
    - 帖子存在标题和封面图，但是是可选的，仅编帖子内容可以成为类似动态的内容
    - 置顶，圈内帖子管理员可以置顶，置顶帖子数量未定。暂定为 5 吧

## 客户端布局

 - 底部导航栏
    0. 动态
    1. 发现
    3. 消息
    4. 我的
