## OmniRing 万能变焦环

把 Xiaomi 17 Ultra（含徕卡版）的**大师变焦环**当成通用旋钮用：像数码表冠那样跟手滚列表，
看视频时当进度环，也可以映射成音量 / 亮度 / 启动应用等动作。

### 怎么装
1. 手机需要 **root + LSPosed**（KernelSU / Magisk 均可）。
2. 装上本模块，在 LSPosed 管理器里启用它。
3. **作用域勾选「系统框架」（System Framework）**，然后重启系统界面 / 手机。
4. 打开 OmniRing App，首页会显示「技术路径」一行，看到 `sensor` 或 `input+sensor` 即已生效。

### 现在能干什么
- 顺时针 / 逆时针两个槽位，分别绑定动作（滚动、音量、亮度、视频进度、启动应用…）。
- 转速只影响**幅度**，不影响触发哪个动作。
- 全局 / 分应用 / 分场景三种生效范围。

### 支持的系统
- **HyperOS 4（Android 17）：已实测，在支持范围内。**
- **HyperOS 3（Android 16）及更低：不在支持范围内，不保证可用。**
  代码里保留了双入口互斥、租约兜底这些防护，所以装上不一定出问题，但不做任何承诺，
  也不收这类系统的适配反馈。**源码是公开的**（GPL-3.0），想在上面跑请自行修改编译、
  自测自用，由此产生的问题自行承担。

### 已知问题
- 与上游旧包 `xyz.nextalone.hyperzoomring` **互不覆盖**，两个都装会各自抢一次环，请先卸载旧包。
- 本模块改的是系统输入路径，属于有风险的系统级修改，请自行评估、自行刷机风险自担。
- 使用老版本 LSPosed 时，管理器里会出现「使用已废弃功能」的黄字提示，不影响功能。

### 署名与许可
本模块是 [NextAlone/HyperZoomRing](https://github.com/NextAlone/HyperZoomRing) 的 Fork，
按 **GPL-3.0** 发布，修改记录见源码仓库的 `MODIFICATIONS.md`。

源码与 changelog：https://github.com/TvTjiesen/OmniRing