# 坦克大战游戏部署指南

## 📁 项目文件

- `tank-battle.html` - 完整的游戏文件（单文件，可直接部署）

## 🚀 部署选项

### 方案一：GitHub Pages（免费，推荐）

#### 步骤 1: 创建 GitHub 仓库
1. 访问 [GitHub](https://github.com) 并登录
2. 点击右上角 "+" → "New repository"
3. 填写仓库名称（如 `tank-battle-game`）
4. 选择 "Public"
5. 点击 "Create repository"

#### 步骤 2: 上传游戏文件
1. 在仓库页面点击 "uploading an existing file"
2. 将 `tank-battle.html` 文件拖拽到上传区域
3. 点击 "Commit changes"

#### 步骤 3: 启用 GitHub Pages
1. 进入仓库的 "Settings" 选项卡
2. 滚动到 "GitHub Pages" 部分
3. Source 选择 "main" 分支和 "/" root
4. 点击 "Save"
5. 等待 1-2 分钟，你的游戏将上线

#### 访问地址
```
https://你的用户名.github.io/tank-battle-game/tank-battle.html
```

---

### 方案二：Vercel（免费，高性能）

#### 步骤 1: 安装 Vercel CLI
```bash
npm install -g vercel
```

#### 步骤 2: 部署
```bash
# 进入项目目录
cd d:\CY\trae\project

# 登录 Vercel
vercel login

# 部署
vercel
```

#### 步骤 3: 配置
- Project name: `tank-battle`
- Directory: `.`（当前目录）
- Build Command: 无需
- Output Directory: `.`

#### 访问地址
部署完成后会提供访问链接

---

### 方案三：Netlify（免费）

#### 步骤 1: 创建 Netlify 账号
1. 访问 [Netlify](https://www.netlify.com)
2. 使用 GitHub 或邮箱注册

#### 步骤 2: 拖拽部署
1. 进入 Netlify Dashboard
2. 点击 "Sites" → "Add new site" → "Deploy manually"
3. 将整个项目文件夹拖拽到上传区域
4. 等待部署完成

#### 访问地址
Netlify 会自动生成一个子域名

---

### 方案四：使用免费的 HTTPS 文件托管服务

#### 1. surge.sh
```bash
npm install -g surge
cd d:\CY\trae\project
surge . tank-battle-game.surge.sh
```

#### 2. Cloudflare Pages
1. 注册 [Cloudflare](https://pages.cloudflare.com/)
2. 创建新项目
3. 上传文件
4. 自动生成 HTTPS 链接

---

## 📱 微信环境配置

### 微信分享配置（可选）

在你的 HTML 文件 `<head>` 中添加微信 JS-SDK 配置：

```html
<script src="https://res.wx.qq.com/open/js/jweixin-1.6.0.js"></script>
```

### 微信内置浏览器访问
1. 将部署后的 HTTPS 链接复制
2. 在微信中发送给好友或发到群聊
3. 点击链接即可直接打开游戏

### 注意事项
- ⚠️ 微信可能会提示"提示非微信官方网页"，点击"继续访问"即可
- 确保使用 HTTPS（Http Secure）协议
- 部分功能可能需要微信公众号授权

---

## 🔧 自定义域名（可选）

### 配置步骤
1. 购买域名（如阿里云、腾讯云）
2. 在托管平台设置自定义域名
3. 添加 DNS 解析记录
4. 等待 SSL 证书自动配置

### 微信白名单（如需要）
如果需要更稳定地访问，可以配置微信公众号白名单

---

## 📊 性能优化建议

### 已实现的优化
✅ 使用 Canvas 2D 渲染  
✅ 粒子系统优化（自动回收）  
✅ requestAnimationFrame 渲染循环  
✅ 响应式设计  
✅ 触摸事件优化  

### 可选优化
1. 启用 Gzip 压缩
2. 使用 CDN 加速
3. 添加 Service Worker 实现离线缓存
4. 图片资源懒加载

---

## 🐛 常见问题

### Q: 游戏加载慢？
A: 首次加载约 2-3 秒属正常现象，后续会有缓存

### Q: 微信中无法全屏？
A: 在微信中点击右上角"..."，选择"在浏览器中打开"

### Q: 触摸控制不灵敏？
A: 确保设备开启了触摸反馈

### Q: 如何分享给好友？
A: 直接复制 HTTPS 链接，通过微信发送即可

---

## 📈 数据统计

游戏已内置基础数据统计：
- 当前分数（实时显示）
- 当前关卡
- 剩余生命
- 本地最高分（localStorage）

### 可扩展的数据统计
如需更详细的统计，可以集成：
- Google Analytics
- 友盟+
- GrowingIO
- 自建统计后端

---

## 🎮 游戏特性

### 已实现功能
✅ 玩家坦克控制（方向键/WASD + 空格射击）  
✅ 移动端触摸控制（虚拟摇杆 + 射击按钮）  
✅ 敌方 AI 坦克  
✅ 多种地形（砖块、钢铁、水域、树林、冰面）  
✅ 5种道具（强化、炸弹、护盾、冻结、生命）  
✅ 粒子特效系统  
✅ 爆炸动画  
✅ 动态光影  
✅ 关卡递进  
✅ 分数系统  
✅ 本地最高分保存  

### 视觉效果
- 🎨 炫酷粒子爆炸效果
- 💫 坦克引擎尾焰
- 🔥 炮弹轨迹拖尾
- ✨ 动态光影照明
- 🌊 水面波纹动画
- 🌟 道具悬浮效果

---

## 📞 技术支持

如遇问题，请检查：
1. 浏览器控制台是否有错误信息
2. 网络连接是否正常
3. 是否使用 HTTPS 访问

---

## 📋 快速部署清单

- [x] 游戏代码开发完成
- [x] 视觉效果实现完成
- [x] 移动端适配完成
- [ ] 选择部署平台
- [ ] 上传文件到托管平台
- [ ] 获取访问链接
- [ ] 测试游戏功能
- [ ] 分享链接到微信

---

**祝你游戏愉快！🎮**
