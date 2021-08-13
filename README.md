# [Hackintosh] OMEN_by_HP_Laptop_15-ce0xx
### 系统：macOS Big Sur 11.2.3
- 👌EFI基本完美，有新突破欢迎反馈！！
- 🤪qq群：<a href="https://jq.qq.com/?_wv=1027&k=qxSfoaw7">639131732</a> （验证：暗影精灵黑苹果）

### 对EFI改进 (原EFI：<a href="https://github.com/t-shao">t-shao</a>)
- 注入显示屏信息，修复屏闪、裂屏
- 修复暗影精灵3的有线网卡驱动
- 注入序列号，使appleID正常登入（可以使用<a href="https://github.com/ic005k/QtOpenCoreConfig/releases">OCAuxiliaryTools</a>进行更换序列号，避免冲突）

OpenCore 版本: 0.6.7

![](images/screenshot.png)

## 配置
| 产品名称暗影精灵3 | OMEN by HP Laptop 15-ce0xx                |
| ----------------- | ----------------------------------------- |
| BIOS              | F.23 / F.19                               |
| 处理器            | Intel(R) Core(TM) i5-7300HQ / i7-7700HQ   |
| 独立显卡          | NVIDIA GeForce GTX 1050ti                 |
| 显卡              | Intel(R) HD Graphics 630                  |
| 声卡              | Realtek ALC295                            |
| 硬盘              | SSD KIOXIA 512G、SSD WD 500G               |
| 网卡              | Realtek RTL8111 + Intel AX200（自选）      |

EFI兼容以上配置


## 硬件功能
#### Fn热键
| 全部功能键 |✅|

#### 电源管理
| 特征 | 状态 | 其他 |
| --- | --- | --- |
|电量百分比显示|✅| 前提：bios要设置充电至80%。若充至80%以上的电量，macOS电量会冻结在93% |
| CPU动态频率 |✅| |
| NVMe 硬盘休眠 |✅| |
| 睡眠、唤醒 |✅| 合上盖子再打开也正常 |

#### 显示
| 特征 | 状态 | 其他 |
| --- | --- | --- |
|内部显示和亮度调整|✅| 通过系统偏好设置或Fn热键 |
|USB-C 端口外接显示器|✅|未测试，USB-C测试：ipad pro能充电，但插入不能扩展屏（USB端口均可以扩展屏） |
|HiDPI|✅| 需自己注入|
| 独立显卡 |❌|  |
| 外接显示器的数字音频 |❌|  |

#### 声音
| 特征 | 状态 | 其他 |
| --- | --- | --- |
|模拟音频|✅| 包括扬声器、耳机和内部麦克风阵列（插入耳机自动切换音频正常） |
|USB-C 端口提供数字音频|✅|未测试 |
| 外置麦克风 |❌| 未测试 |

#### 网络
| 特征 | 状态 | 其他 |
| --- | --- | --- |
|有线以太网|✅|  |
|USB有线以太网|✅||
|Intel WiFi和BT|✅|相当稳定，目前支持系统wifi管理界面和部分Continuity功能，包括Handoff和Universal Clipboard）（应该指的是AX200网卡，但我用的是博通BCM94352z免驱卡）|
|蓝牙适配器|❌|应该指的是AX200网卡|

#### I/O
| 特征 | 状态 | 其他 |
| --- | --- | --- |
|USB 端口|✅|  |
|Type-C|✅|自己测试过Type-c好像只能充电 |
|触摸板|✅| 支持多指手势和 ForceTouch 模拟，4指都能识别出来|
|读卡器 |✅|  未测试|
| miniDP, HDMI 端口 (via dGPU) |❌| 主要原因应该是：端口走的是独显 |

## 说明书
- 前提：bios关闭安全启动模式

1. 用黑果小兵的镜像安装，直至进入新系统页面（镜像一般不会出现错误，中途会出现“block”字眼会卡很久，最终还是会加载进去的，给点耐心，祝你成功）
2. 关机，复制OC和BOOT到你的EFI文件，进行替换
3. 拔掉u盘，按F9开机，选OpenCore.efi启动

## 链接
- 镜像下载
  - <a href="https://blog.daliansky.net/macOS-BigSur-11.2.3-20D91-Release-version-with-OC-0.6.7-and-Clover-5131-and-PE-original-image.html">黑果小兵macOS Big Sur 11.2.3 20D91 Installer for OpenCore 0.6.7 and CLOVER 5131 and PE</a>
  - `BaiDuCloud link`: <https://pan.baidu.com/s/1ILCN29bhHypIjNfwU5EjuQ> `Extraction code`: `49vz`
  - MD5 (macOS Big Sur 11.2.3 20D91 Installer for OpenCore 0.6.7 and CLOVER 5131 and PE.dmg) = 9a1b44e8038e8c416a8ba5f99ed553f6
- <a href="https://www.acutesystems.com/tmac/tmsetup.zip">u盘刷写工具transmac</a>（建议，个人感觉比etcher稳太多了）
- <a href="https://github.com/Howardnm/HP-OMEN-3-Hackintosh-Bigsur/releases/tag/EFI">EFI Downloads</a>
