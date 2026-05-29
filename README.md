# 🧊 绿联 NAS（UGOS PRO）图标一键更换脚本

![banner](https://github.com/zeyu8023/ugreen-icon-replacer/blob/main/icons/bana.jpg)

本项目是一个用于快速替换 UGOS PRO 系统图标的终端脚本工具，支持多套图标风格、联网自动下载、代理加速、自动解压和覆盖替换。适用于绿联 NAS 图标定制与美化。

> **当前由 [陈子疯（@zifeng-chen）](https://github.com/zifeng-chen) 迭代维护**，基于原作者 [zeyu8023](https://github.com/zeyu8023) 的优秀开源项目进行扩展和优化。感谢原作者的付出与贡献！🙏

---

## ⚠️ 权限说明

> **请务必在执行脚本前使用 `sudo -i` 切换为 root 用户，否则替换操作将失败！**

```bash
sudo -i
bash zt
```

---

## 🚀 快速使用

![演示图](https://github.com/zeyu8023/ugreen-icon-replacer/blob/main/icons/yanshi2.png)

### 方法一：一键运行（推荐）

#### GitHub 地址：

```bash
bash <(curl -s https://raw.githubusercontent.com/zifeng-chen/ugreen-icon-replacer/main/replace_icons.sh)
```

#### Gitee 地址（由 [@Dear-Chen](https://github.com/Dear-Chen) 制作及维护）：

```bash
bash <(curl -s https://gitee.com/Dear-Chen/ugreen-icon-replacer/raw/main/replace_icons.sh)
```

### 方法二：手动下载运行

```bash
git clone https://github.com/zifeng-chen/ugreen-icon-replacer.git
cd ugreen-icon-replacer
chmod +x replace_icons.sh
sudo ./replace_icons.sh
```

### 方法三：安装为命令（zt）

```bash
bash <(curl -s https://raw.githubusercontent.com/zifeng-chen/ugreen-icon-replacer/main/install_zt.sh)
```

安装后可直接运行：

```bash
zt
```

---

## ✨ 功能特色

- ✅ 图标风格选择：5 套风格任意切换
- ✅ 一键执行：自动拉取图标并完成覆盖替换
- ✅ 多源下载：支持 GitHub 主站、FastGit 镜像与代理兜底
- ✅ 代理记忆：首次输入代理后自动保存，下次运行自动加载
- ✅ 图标 ZIP 包永久缓存，存储目录可自定义
- ✅ 主菜单支持操作选择、查看缓存、清理缓存、修改路径
- ✅ 格式校验：代理地址格式检测，支持多次重输
- ✅ unzip 自动检测与安装提示
- ✅ 本地图标目录支持：无需联网也可本地替换
- ✅ 操作日志记录：自动生成 `/var/log/iconreplace*.log`
- ✅ 权限判断：无写权限时提示使用 `sudo -i` 后重新运行

---

## 🎨 图标主题支持

脚本内置以下图标风格，可在执行时自由选择：

| 编号 | 风格名称         | 说明                         |
|------|------------------|------------------------------|
| 1    | iOS 26 液态玻璃  | 乐小宇制作，高光玻璃质感     |
| 2    | 锤子 OS          | Sunny 整理，极简细腻         |
| 3    | 拟物毛玻璃       | Sunny 制作，冰感拟物         |
| 4    | 绿联毛玻璃       | Sunny 制作，更绿、更毛、更玻璃 |
| 5    | 官方默认图标     | 恢复原始图标样式             |

---

## ☁️ 支持代理访问 GitHub

- 下载失败时自动提示输入代理地址（支持 http 和 socks5h）
- 示例格式：

```bash
http://127.0.0.1:7890
socks5h://127.0.0.1:1080
```

- 代理配置将保存至 `~/.ugreen_icon_config`
- 下次运行时自动提示是否复用

---

## 📦 unzip 自动安装说明

- 脚本会自动检测系统是否安装 unzip
- 若未安装，则提示用户是否安装，并根据系统自动选择以下包管理器：

| 系统         | 包管理器 |
|--------------|-----------|
| Ubuntu/Debian | apt       |
| Fedora/CentOS | dnf       |
| Arch/Manjaro  | pacman    |

---

## 📁 示例目录结构

```
ugreen-icon-replacer/
├── replace_icons.sh
└── icons/
    ├── nav.png
    └── custom-logo.svg
```

---

## 🧩 注意事项

- 替换操作不可撤销，请确认图标内容无误后执行
- 不会修改未匹配的系统文件
- 系统更新后图标可能恢复默认，可重新执行本脚本
- 如需支持更多图片格式，可修改脚本中的文件过滤规则

---

## 📄 更新日志

当前版本：**v1.4.0**

### v1.4.0 (2026-05-29) by 陈子疯
- 🔧 Fork 并迁移仓库至 zifeng-chen/ugreen-icon-replacer
- ➕ 新增 25 个 com.ugreen.* 前缀图标支持（适配 UGOS PRO 新版应用）
- 🎨 锤子 OS 主题持续迭代更新中（安全管家、迅雷、帮助中心、UGREEN AI、回收站等自定义图标）
- 📝 更新 README，补充维护者信息与使用说明

查看完整更新记录：[CHANGELOG.md](https://github.com/zeyu8023/ugreen-icon-replacer/blob/main/CHANGELOG.md)

---

## 🙌 致谢与贡献

- 🏗️ **原作者 [zeyu8023](https://github.com/zeyu8023)**：创建了优秀的绿联 NAS 图标替换项目，感谢开源分享！
- 🎨 **乐小宇（@zeyu8023）**：iOS 26 玻璃风格
- 🧊 **Sunny**：SmartisanOS（整理）、玻璃拟物、绿联毛玻璃系列
- 👤 **陈子疯（@zifeng-chen）**：当前维护者，持续迭代锤子 OS 主题图标

欢迎提交 Issue 和 PR，持续完善脚本、扩展风格或优化执行体验！

---

## 📜 License

MIT License © 2025 zeyu8023
