# build NFT lootbox and quiz website

- 说明：第一次开发Web3的项目，第一次接触NFT，总的开发时间约为三天，在这里记录一下大体的过程，主要复盘一下踩到的坑
- 学习了Pointer上面的项目https://www.pointer.gg/tutorials/thirdweb-nft-lootbox/feda78d2-d35c-4b77-a1d3-182aa16070d9

- 做了什么
    - 构建全栈的回答问题app，答对时奖励用户NFT Pack，用户open pack的时候随机获取一个NFT
- **请大家谨慎学习这个项目，因为thirdWeb升级到了v2版本，这个教程里面的SDK基本全都不支持了，所以在配置的过程中踩了很多坑**
- 如何打开
    - 在.env文件中添加私钥
    - 修改
    - npm run dev
- 怎么做的
    - 智能合约代码是在thirdWeb上生成的，采用了Polygon Mumbai测试网络
    - 使用脚本生成Pack、生成NFT
    - 使用TypeScript编写前端并调用thirdWeb SDK接口
- 踩到的坑
    - 这个教程项目中，使用了早期版本的thirdWeb SDK接口，目前已经不维护了，前thirdWeb网站中维护的文档也是乱七八糟，有新版有旧版。在最初修改脚本的过程中遇到了很多报错的困难，经常显示xxx不是一个function。
    - 关于thirdweb dashboard,请使用v2版本的https://thirdweb.com/dashboard/contracts，无需构建项目
    - 停用npm install @3rdweb/sdk ethers dotenv，使用https://portal.thirdweb.com/typescript中的npm install @thirdweb-dev/sdk ethers^5
    - import { ThirdwebSDK } from "@thirdweb/sdk"; 调用的函数也需要对应修改。
- 网页图片
![图片](/pic/1.png)
![图片](/pic/2.png)
![图片](/pic/3.png)
![图片](/pic/4.png)