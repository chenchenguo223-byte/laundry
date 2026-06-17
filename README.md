# 🧺 校园洗衣房预约系统 · Campus Laundry Booking System

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.0-blue" alt="version">
  <img src="https://img.shields.io/badge/license-MIT-green" alt="license">
  <img src="https://img.shields.io/badge/vanilla-js-yellow" alt="vanilla js">
  <img src="https://img.shields.io/badge/i18n-中文%2FEnglish-orange" alt="i18n">
</p>

<p align="center">
  <b>智能预约 · 随时随地</b> &nbsp;|&nbsp; <b>Smart Booking · Anytime</b>
</p>

---

## 📖 简介 | Introduction

**校园洗衣房预约系统**是一个面向高校学生的智能洗衣房管理平台。它提供洗衣机/烘干机状态实时监控、在线预约、衣物取送互助等一站式服务，内置 AI 助手 WashBot，并支持中英双语无缝切换。

**Campus Laundry Booking System** is a smart laundry management platform for university students. It provides real-time washer/dryer status monitoring, online booking, peer-to-peer laundry pickup & delivery, a built-in AI assistant WashBot, and seamless Chinese-English bilingual switching.

当前版本专为 **澳门科技大学 (MUST)** 设计，可轻松适配其他高校场景。

---

## ✨ 核心功能 | Core Features

### 🏠 首页 · Home
- **设备状态总览**：按楼座（A/B/C/D/P）和楼层（1-5）筛选，实时查看洗衣机和烘干机的空闲/使用中/即将空闲状态
- **正在使用追踪**：进度条显示当前洗衣/烘干剩余时间，预估完成时间
- **快捷入口**：一键跳转预约、我的预约、报修、统计

### 📅 预约 · Booking
- **7 天滚动日期选择**：今天、明天及未来一周可选
- **楼座 + 楼层二级筛选**：精准定位目标洗衣房
- **设备卡片 + 时间段视图**：每台设备的每小时可用状态一目了然
- **预约确认弹窗**：提交前二次确认设备、位置、日期、时段等详情

### 🛵 取送服务 · Delivery
- **帮我取**：发布取衣订单，消耗 1 积分，由其他同学接单帮你把洗好的衣服送到烘干机或宿舍
- **我要帮取**：浏览待接订单，接单赚取 1 积分
- **送达类型灵活**：支持「送去烘干」和「送回宿舍」两种模式
- **二维码门禁**：接单后生成门禁二维码（仿真），便于进入对应楼栋
- **人脸验证**：接单前需人脸识别（仿真动画）

### 🤖 AI 助手 · WashBot
- **浮层聊天面板**：点击底部中央 AI 按钮呼出
- **快捷指令**：预约洗衣、查机器状态、剩余时间、我的预约
- **自然语言交互**：支持中文/英文输入
- **语音输入**：支持语音输入 & 录音动画反馈

### 👤 我的 · Profile
- **个人中心**：姓名、学号、积分、累计使用次数、违约次数
- **积分系统**：发布订单 -1 积分，接单完成 +1 积分，激励互助参与
- **我的帮取子页**：「帮我取记录」和「送货记录」两个 Tab 分类管理
- **预约历史**：进行中 / 已完成 / 已取消三种状态

### 📋 注册 & 规则
- **学号绑定注册**：限定澳门科技大学学生
- **使用须知弹窗**：包含爽约警告、多次爽约封号等规则说明

### 🌐 国际化 · i18n
- **中英双语**：页面内一键切换，覆盖全部文案、日期格式、问候语
- **无运行时依赖**：纯 JavaScript 字典实现，轻量高效

---

## 🛠 技术栈 | Tech Stack

| 技术 | 说明 |
|------|------|
| **HTML5** | 语义化结构，单文件架构 |
| **CSS3** | 纯手写，移动端优先，使用 CSS 变量 + Flexbox + Grid |
| **JavaScript (Vanilla)** | 零依赖，纯原生 JS，无框架 |
| **i18n** | 自建国际化字典，支持全文案中英切换 |

> 📌 **零依赖、零构建**：整个项目就是一个 `index.html` 文件，下载即用，无需安装任何依赖或工具链。

---

## 🚀 快速开始 | Quick Start

### 方式一：直接打开
```bash
# 克隆仓库
git clone https://github.com/your-username/campus-laundry.git

# 用浏览器直接打开
open campus-laundry/index.html   # macOS
start campus-laundry/index.html  # Windows
```

### 方式二：本地服务器（推荐）
```bash
# 使用 Python 内置服务器
cd campus-laundry
python3 -m http.server 8080

# 浏览器访问 http://localhost:8080
```

### 方式三：部署到 GitHub Pages
1. 将仓库推送到 GitHub
2. 在仓库 Settings → Pages 中，选择分支和根目录
3. 几秒钟后即可通过 `https://your-username.github.io/campus-laundry` 访问

---

## 📂 项目结构 | Project Structure

```
campus-laundry/
├── index.html          # 🎯 主文件，包含全部 HTML / CSS / JS
├── README.md           # 📖 项目说明
└── LICENSE             # ⚖️ 开源协议
```

---

## 🎯 使用流程 | User Journey

```
注册绑定学号
    │
    ▼
阅读使用须知 → 同意进入
    │
    ├─ 📅 预约洗衣 ──→ 选日期 → 选楼座楼层 → 选设备 → 选时间段 → 确认预约
    │
    ├─ 🛵 发布取衣 ──→ 选取衣地点 → 选送达地点 → 消耗积分 → 发布订单
    │            └──→ 等待同学接单 → 确认收货
    │
    ├─ 🏃 接单帮取 ──→ 浏览待接订单 → 人脸验证 → 接单成功 → 获积分
    │
    ├─ 🏠 查看状态 ──→ 实时设备状态 → 筛选楼座楼层
    │
    └─ 🤖 问 WashBot ──→ 快捷指令 / 自然语言 / 语音输入
```

---

## 📐 数据结构 | Data Structure

### 设备数据 (DB)
```javascript
DB[building][floor] = {
  washers: [
    { id: "W-A101", type: "washer", slots: [...], status: "free"|"busy"|"soon" }
  ],
  dryers: [
    { id: "D-A101", type: "dryer", slots: [...], status: "free"|"busy"|"soon" }
  ]
}
```

### 预约记录 (records)
```javascript
{
  icon: "🫧",          // 设备图标
  id: "W-P503",        // 设备编号
  type: "washer",      // washer | dryer
  b: "P", f: 5,        // 楼座、楼层
  date: "06/17",       // 预约日期
  slot: "09:00",       // 时间段
  st: "ongoing"        // ongoing | done | cancelled
}
```

### 取送订单 (deliveryOrders)
```javascript
{
  id: "order_001",
  pickupBuilding: "P", pickupFloor: "5",
  pickup: "P座5楼洗衣房",        // 中文显示
  pickupEn: "Bldg P F5 Laundry",  // 英文显示
  machineNum: "W-P501",
  destType: "dry",               // "dry" | "dorm"
  dest: "任意烘干机",
  pointsCost: 1,
  status: "pending",             // pending | accepted | completed
  isMyOrder: false,
  acceptedByMe: false,
  postedAt: 1234567890
}
```

---

## 🔧 自定义适配 | Customization

### 适配其他学校
1. **修改学校列表**：在注册页 `reg-school` 下拉菜单中添加你的学校
2. **调整楼座楼层**：修改 `BUILDINGS` 和 `FLOORS` 数组
3. **更换设备数据**：修改 `DB` 初始化和 `sRand` 随机种子逻辑
4. **替换文案**：修改 `I18N` 字典中的品牌名称和描述

### 对接真实后端
- 将 `DB`、`records`、`deliveryOrders` 等内存数据替换为 API 调用
- 设备状态和数据量小，可直接使用前端状态管理或 sync 到后端

---

## 📝 版本规划 | Roadmap

- [ ] 接入真实后端 API，支持多用户实时数据同步
- [ ] 微信小程序版本
- [ ] 推送通知（洗衣完成、订单状态变更）
- [ ] 支付集成（洗衣费用、取送服务费）
- [ ] 数据统计面板（使用频率、高峰时段热力图）
- [ ] 暗色模式

---

## 📄 开源协议 | License

本项目采用 [MIT License](https://opensource.org/licenses/MIT) 开源，欢迎 Star ⭐、Fork 和 PR！

---

## 🙏 致谢 | Acknowledgments

- 澳门科技大学的同学们提供的需求反馈
- 所有为开源社区贡献力量的开发者们

---

<p align="center">
  Made with ❤️ for MUST students
  <br>
  如果这个项目对你有帮助，请给一个 ⭐ Star！
</p>
