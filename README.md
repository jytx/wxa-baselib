# wxa-baselib

[wxa-runner](https://github.com/open-wxa/wxa-runner) 的内置基础库。本机没有微信开发者工具（如 Linux、CI）时，wxa-runner 用这里的基础库运行小程序。

## 版权

这里的文件是**微信官方小程序基础库**，版权归腾讯所有，不适用 wxa-runner 的 MIT 协议。本仓库只为 wxa-runner 在没有开发者工具的环境中运行而保存，不做任何修改。

## 目录

每个版本一个目录，只放 wxa-runner 运行时会加载的文件：

```
3.7.0/
  WAService.js     逻辑层
  WAWebview.js     渲染层
  WAWorker.js      Worker（wx.createWorker）
  WAVersion.json   版本信息
```

## 来源与更新

文件取自微信开发者工具下载的 `WeappVendor/<版本>.wxvpkg`，用 wxa-runner 解包后原样复制：

```bash
wxa-runner baselib extract 3.7.0        # 解包到 ~/.wxa-runner/baselib/3.7.0
mkdir 3.7.0
cp ~/.wxa-runner/baselib/3.7.0/{WAService.js,WAWebview.js,WAWorker.js,WAVersion.json} 3.7.0/
```

wxa-runner 目前最高支持 3.7.0，高于它的版本放进来也不会默认使用。
