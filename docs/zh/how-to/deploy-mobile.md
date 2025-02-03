# 移动应用发布指南
**TODO**

本指南涵盖了将 AI 生成的移动应用发布到 App Store（iOS）和 Google Play Store（Android）的过程。

## 前置要求

- 完成的移动应用
- 开发者账号
  - Apple 开发者账号（每年 99 美元）
  - Google Play 开发者账号（一次性 25 美元）
- 应用签名证书
- 隐私政策和服务条款

## iOS App Store 发布

### 1. 准备工作

```bash
# 安装最新的 Xcode
xcode-select --install

# 安装 CocoaPods（如果使用）
sudo gem install cocoapods
```

### 2. App Store Connect 设置

1. 在 App Store Connect 创建应用
2. 配置应用信息
   - 应用名称
   - Bundle ID
   - SKU
   - 隐私政策 URL

### 3. 构建配置

```bash
# 更新版本和构建号
/usr/libexec/PlistBuddy -c "Set :CFBundleShortVersionString 1.0.0" Info.plist
/usr/libexec/PlistBuddy -c "Set :CFBundleVersion 1" Info.plist
```

### 4. 打包和上传

1. 在 Xcode 中：
   - 选择"Generic iOS Device"
   - Product > Archive
   - 验证应用
   - 上传到 App Store

## Google Play Store 发布

### 1. 准备工作

```bash
# 生成签名的 APK/Bundle
./gradlew bundleRelease
```

### 2. Play Console 设置

1. 在 Play Console 创建应用
2. 配置应用信息
   - 应用名称
   - 包名
   - 类别
   - 内容分级

### 3. 发布类型

1. **内部测试**
   - 限定特定测试者
   - 快速审核流程
   - 即时更新

2. **封闭测试**
   - 私有群组测试
   - 有限公开测试
   - Beta 反馈

3. **开放测试**
   - 公开 beta 测试
   - 分阶段发布
   - 功能测试

4. **生产发布**
   - 完全公开发布
   - 分阶段推出
   - 监控指标

## 应用商店优化（ASO）

### 1. 元数据优化

```yaml
title:
  length:
    ios: "30个字符"
    android: "50个字符"
  keywords: "相关的, 可搜索的, 关键词"

description:
  length:
    ios: "4000个字符"
    android: "7000个字符"
  structure:
    - 功能特点
    - 产品优势
    - 社会证明
    - 行动号召
```

### 2. 视觉资产

- 应用图标
- 截图
- 预览视频
- 特色图片（Android）

## 合规性和安全

### 1. iOS 要求

- 应用隐私详情
- IDFA 声明
- 出口合规性
- 内容版权

### 2. Android 要求

- 数据安全表单
- 内容分级
- 目标 API 级别
- Play Protect

## 发布清单

### 1. 提交前
- [ ] 应用完全测试
- [ ] Crashlytics 配置
- [ ] 分析工具实现
- [ ] 深度链接验证
- [ ] 推送通知测试

### 2. 商店列表
- [ ] 截图准备
- [ ] 描述优化
- [ ] 隐私政策更新
- [ ] 支持 URL 可访问
- [ ] 营销 URL 就绪

### 3. 技术
- [ ] 签名证书安全
- [ ] API 端点生产就绪
- [ ] 第三方 SDK 更新
- [ ] 性能优化
- [ ] 安全审查

## 常见问题

### 1. 拒绝原因
- 缺少隐私政策
- 启动崩溃
- 元数据不完整
- 性能问题
- 内容违规

### 2. 解决方案
- 仔细审查指南
- 全面测试
- 清晰记录功能
- 及时响应
- 必要时申诉

## 最佳实践

1. **版本管理**
   - 语义化版本
   - 清晰的更新日志
   - Beta 测试
   - 分阶段发布

2. **质量保证**
   - 自动化测试
   - 手动测试
   - 设备兼容性
   - 网络条件测试

3. **用户反馈**
   - 监控评论
   - 回应反馈
   - 定期更新
   - 清晰沟通

## 相关资源

- [Web 应用部署](./deploy-web.md)
- [小程序发布](./deploy-miniprogram.md)
- [自定义模板](./custom-templates.md)
