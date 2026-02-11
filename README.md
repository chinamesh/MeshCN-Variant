# MeshCN-Variant
Meshtastic 中国地区专属变体库

## 项目介绍
MeshCN-Variant是契合中国地区使用场景的 Meshtastic 延伸项目，由 MeshCN 组织维护，专注提供独属于中国地区设备的变体固件库。

## 核心特性
- 定时自动拉取 Meshtastic 官方最新固件代码，完成全量构建
- 内置适配中国地区实际使用需求的补丁
  - 功率上限解除
  - 中文字符完整支持
  - ESP32C3的省电arduino依赖库
- 统一构建规范，保证固件稳定性与兼容性
-固定了官方仓库的git版本，确保补丁的持久可用性（现固定提交哈希于a092f6bb22f6fae223acf50e3306a9063f790fbd）
## 个人使用方式
1. Fork 本仓库
2. 修改或创建属于自己的设备变体
3. 等待 GitHub Action 自动运行构建，或手动执行单一目标构建 Workflow

## patch开发
1. Fork 官方固件库
2. 切换至指定提交版本（提交哈希：a092f6bb22f6fae223acf50e3306a9063f790fbd）
3. 修改代码制作成patch，移动至/patch目录
4. 运行**build from commit**工作流以验证更改正常

## PR 提交规范
- 支持提交**设备变体**与**功能补丁**类 PR
- 所有变体与补丁必须**通过项目构建测试（特指“build from commit”）**
- PR 描述中需清晰说明补丁作用、修改内容、适用设备等信息

## 鸣谢
- 深圳-派派(github:ssp97)提供了功率解锁，中文字符显示和针对ESP32c3省电的arduino依赖库与特调的补丁

## 维护组织
MeshCN
