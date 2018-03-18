# cos-wx-upload-file
微信小程序上传文件到腾讯云v5；Wechat mini program upload file to tencent cos v5

微信小程序仅支持https请求上传文件，所以我们选择了腾讯云作为文件服务器。此外腾讯云提供了配套小程序开发的[SDK](https://github.com/tencentyun/cos-wx-sdk-v5)，方便微信调用

## 前提
我们假设您已经[入门微信小程序开发](https://mp.weixin.qq.com/debug/wxadoc/dev/)

## 准备工作
注册[腾讯云](https://cloud.tencent.com/)

到[COS对象存储控制台](https://console.cloud.tencent.com/cos5) 创建存储桶，

<p align='center'>
<img src='https://public-1256264454.cos.ap-shanghai.myqcloud.com/cos-wx-upload-file/create-bucket.png' width='600' alt=''>
</p>

得到 Bucket（存储桶名称） 和 Region（地域名称)
到[控制台密钥管理](https://console.cloud.tencent.com/cam/capi) 获取您的 SecretId 和 SecretKey


