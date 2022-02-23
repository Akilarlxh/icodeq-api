### `Weibo` 直链转换 `API`

🚀 仓库地址：https://github.com/zkeq/icodeq-api/tree/main/api/weibo_307_video

🚀 示例地址：https://api.icodeq.com/api/weibo_307_video/

🚀 本项目由两部分组成，并且数据库基于 `redis`

🚀 `/api/weibo_307_video` 目录下的 `index.py` 是主要文件

🚀 它会去读取 `redis` 上面的 `video` 的值。

🚀 `/api/weibo_307_video/get-new-url` 则复制传递 `video` 的值，每次访问都会传递。

🚀 所以需要将 `SCF_30_min_fresh.py` 部署至云函数，设置半小时刷新一次

🚀 使用说明为修改成自己的 `redis`，修改自己的视频 ID 定位。

#### 具体操作
1. 修改 `redis`
2. 修改 微博获取列表 `url`
3. 修改 视频定位 `id`
4. 将 `SCF_30_min_fresh.py` 上传至云函数并且设定半小时执行一次（替换成你自己的链接）
4. 测试 `https://api.icodeq.com/api/weibo_307_video/get-new-url`
5. 测试 `https://api.icodeq.com/api/weibo_307_video`
