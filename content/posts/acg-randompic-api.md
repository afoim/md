
# API端点

门户： https://pic.072103.xyz

门户里面的API端点： https://hpic.072103.xyz https://vpic.072103.xyz （CF Worker）

博客用的API端点： https://eopageapi.2x.nz/pic?img=ua （EdgeOne Pages Functions）

*什么？你问为什么这么乱？你先别急*

# 详细实现

图源全部存在 **Cloudflare R2**，全部采用 **Webp** 格式，仅分类为 **横屏、竖屏** ，如图

![](../assets/images/2025-08-31-04-13-08-image.png)

![](../assets/images/2025-08-31-04-13-17-image.png)

API就拿我正投入使用的 https://eopageapi.2x.nz/pic?img=ua 来说

看域名也可以看出来，这是一个 **EdgeOne Pages Functions** 服务（下文简称 **eopf** ），什么？你问为什么用这个？那当然是因为！ **目前所有功能完全免费！**

![](../assets/images/2025-08-31-04-18-45-image.png)

源码在 [afoim/EdgeOne_Function_PicAPI: 适用于EdgeOne边缘函数的随机图API](https://github.com/afoim/EdgeOne_Function_PicAPI)

原理为让 **eopf** 连接上 **Cloudflare R2** 然后随机拿一张图出来。没错！就这么简单！

*上文提到的另一个CF Worker端点原理也一样，只不过CF内部连接R2就不用手搓S3鉴权了*
