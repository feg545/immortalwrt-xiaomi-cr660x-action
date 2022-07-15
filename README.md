## immortalwrt
https://github.com/immortalwrt/immortalwrt

#### 文件说明
cr660x.patch 是小米CR6606、CR6608、CR6609的机型补丁文件，主要是上游immortalwrt仓库里面还没更新。

#### 修改配置
执行命令`make menuconfig` 可以获得我们自己定义的.config
然后执行`./scripts/diffconfig.sh > diffconfig` 这样可以获取只包括修改项的配置文件。

这个项目中的.config仅包括变化的内容
合并配置到默认配置：
```bash
   cp diffconfig openwrt/.config
   make defconfig
```
