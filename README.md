# SamsClub_buy

山姆会员店自动化抢购

## 更新内容

#### 4.26 更新

普通模式增加购物车轮询,用于及时更新缺货库存,详见 常规下单 操作步骤

#### 4.25 更新

执行 sam_buy_bao_gong.py

持续扫描是否有货,有货就加购物车并下单

如果持续上3个套餐,会都下单,最后取消你不需要的

加入barkid参数,如果要bark通知在一开始填入barkid

#### 4.24 更新
sam_buy_bao_gong.py 保供功能,加入购物车后动结算

#### 4.22 更新

加入保供套餐搜寻,并且自动加入购物车功能 sam_buy_bao_gong.py

直接运行即可

#### 4.19 更新 

加入动态加载order的request body参数,修改data.txt文件可以不用重启直接反应到order请求中,用于临时修改商品列表或者其他参数

如果想完全盲猜不调用getCapacityData接口,可以将guess置为True

修复极速达时间段太多导致线程过多的问题,现在默认只取最后2个

### 建议不要随意修改sleep时间!!! 并发太高被封ip!!!


## 第一件事: 抓包获取headers里的authtoken,网上搜索手机抓包,推荐charles
## 第二件事: 确保安装了 requests 组件
#### 引入 requests 组件
执行
```bash
pip install --index-url https://pypi.douban.com/simple/ requests
```
## 保供套餐 操作步骤

1: sam_buy_bao_gong.py 类里填写authtoken, barkid(选填)直接执行

## 常规下单 操作步骤

1: nomal文件夹下 getData.py 类里填写authtoken

2: 执行getData.py,选择相应地址和仓库

3: 等待提示"购物车加载完成"后,执行order.py即可开始下单

4: 可以不关闭getData.py让其一直运行以保持购物车持续更新


### 此工程参考 https://github.com/azhan1998/sam_buy 

感谢作者付出

## 版权说明

本项目为 GPL3.0 协议，请所有进行二次开发的开发者遵守 GPL3.0协议，并且不得将代码用于商用。

本项目仅供学习交流，严禁用作商业行为，特别禁止黄牛加价代抢等！

因违法违规等不当使用导致的后果与本人无关，如有任何问题可联系本人删除！
