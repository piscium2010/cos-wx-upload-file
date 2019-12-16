# cos-wx-upload-file
微信小程序上传文件到腾讯云v5

## Demo
<p align='center'>
<img src='https://public-1256264454.cos.ap-shanghai.myqcloud.com/cos-wx-upload-file/live-demo.gif' width='600' alt=''>
</p>

微信小程序仅支持https请求上传文件，所以我们选择了腾讯云作为文件服务器。此外腾讯云提供了配套小程序开发的[SDK](https://github.com/tencentyun/cos-wx-sdk-v5)，方便微信上传文件时调用。

`为了例子的简洁性，这里没有使用服务器鉴权，而采用了前端鉴权`

## 前提
我们假设（哥们儿/妹子）你已经[入门微信小程序开发](https://mp.weixin.qq.com/debug/wxadoc/dev/)

## 准备工作
注册[腾讯云](https://cloud.tencent.com/)

到[COS对象存储控制台](https://console.cloud.tencent.com/cos5) 创建存储桶，

<p align='center'>
<img src='https://public-1256264454.cos.ap-shanghai.myqcloud.com/cos-wx-upload-file/create-bucket.png' width='600' alt=''>
</p>

填入存储桶名称等基本信息。为了方便测试，选择公有读私有写
<p align='center'>
<img src='https://public-1256264454.cos.ap-shanghai.myqcloud.com/cos-wx-upload-file/create-bucket-II.png' width='600' alt=''>
</p>

为存储桶添加跨域访问规则（重要）
<p align='center'>
<img src='https://public-1256264454.cos.ap-shanghai.myqcloud.com/cos-wx-upload-file/create-bucket-III.png' width='600' alt=''>
</p>

如果你不熟悉跨域访问设置，可参考以下配置
<p align='center'>
<img src='https://public-1256264454.cos.ap-shanghai.myqcloud.com/cos-wx-upload-file/create-bucket-IV.png' width='600' alt=''>
</p>

获取你的 Bucket（存储桶名称), Region（地域名称) 和访问域名
<p align='center'>
<img src='https://public-1256264454.cos.ap-shanghai.myqcloud.com/cos-wx-upload-file/create-bucket-V.png' width='600' alt=''>
</p>

到[控制台密钥管理](https://console.cloud.tencent.com/cam/capi) 获取你的 SecretId 和 SecretKey

<p align='center'>
<img src='https://public-1256264454.cos.ap-shanghai.myqcloud.com/cos-wx-upload-file/create-bucket-VI.png' width='600' alt=''>
</p>

登录[微信公众平台](https://mp.weixin.qq.com/) 设置 --> 开发设置，将你刚才得到的访问域名填入服务器域名
<p align='center'>
<img src='https://public-1256264454.cos.ap-shanghai.myqcloud.com/cos-wx-upload-file/add-domain.png' width='600' alt=''>
</p>

至此，准备工作全部完成

## 运行项目

```sh
git clone https://github.com/piscium2010/cos-wx-upload-file.git
```

编辑cos-wx-upload-file\pages\index\config.js，替换你的 Bucket, Region, SecretId, SecretKey
<p align='center'>
<img src='https://public-1256264454.cos.ap-shanghai.myqcloud.com/cos-wx-upload-file/config.png' width='600' alt=''>
</p>

运行小程序
<p align='center'>
<img src='https://public-1256264454.cos.ap-shanghai.myqcloud.com/cos-wx-upload-file/live-demo.gif' width='600' alt=''>
</p>


### 万一这篇文章对各位客官有些许帮助的话，劳烦右上角打赏个星星，阿里阿多




#### 羞耻广告位
[designare-table: 企业级react table组件, IE11 下性能完胜Ant Design](https://piscium2010.github.io/designare-table)

[Form 表单联级校验 适配任意UI库：Antd，Office UI fabric， Material ui...](https://github.com/piscium2010/v-form)

[React Proptypes 转 React Typescript 工具](https://github.com/piscium2010/react-proptypes-to-typescript)

[React 轻量级前端控件实例 - 打造你自己的前端控件](https://piscium2010.github.io/lime)



