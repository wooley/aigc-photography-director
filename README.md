# AIGC Photography Director

摄影导演型 Skill。

## 简介

AIGC Photography Director 不是普通提示词生成器，而是一个面向 AI 图片与视频创作的摄影导演系统。

很多 AIGC 图片失败，并不是模型不会生成漂亮画面，而是缺少摄影师的空间思维：

- 摄影机在哪里？
- 人物和摄影机距离是多少？
- 镜头从什么方向观察？
- 人物在画面中占多少比例？
- 前景如何制造空间层次？

本 Skill 将真实摄影语言转换为 AI 可理解的结构化提示。

## 核心公式

```
Camera Position
× Camera Height
× Distance
× Direction
× Shot Size
× Foreground
× Subject Placement
```

## 功能

- AI 写真系列规划
- 摄影机空间推理
- 参考图片摄影语言反推
- 人物一致性控制
- 电影级分镜生成
- 图片 Prompt 工程
- 视频镜头设计

# 中文使用说明

## 适用场景

适用于：

- 人像写真
- 古风摄影
- 时尚街拍
- 体育摄影
- 电影角色设计
- 老照片修复
- AI 视频分镜

## 工作流程

输入：

```
主题 + 人物 + 场景 + 风格 + 数量
```

Skill 自动执行：

```
创意分析
 ↓
摄影定位
 ↓
镜头设计
 ↓
系列分镜
 ↓
Prompt生成
 ↓
一致性检查
```

# Reference Image Reverse Engineering

图片反推摄影导演模块。

输入一张参考图片时，不只描述图片内容，而分析：

- 摄影机位置
- 镜头高度
- 焦段推测
- 景别
- 构图方式
- 光线方向
- 色彩系统
- 前景关系
- 空间层次

输出：

```
Photography Analysis
Camera Setup
Composition
Lighting Design
Color Science
Reusable Prompt
```

# Codex 使用方式

## 安装 Skill

将仓库加入 Codex 工作目录：

```
skills/aigc-photography-director
```

Codex 可以通过读取 SKILL.md 自动理解能力。

## 调用示例

### 示例1：生成系列写真

```
Use aigc-photography-director.

Create a 10-image series:
A Chinese girl wearing traditional Hanfu in an ancient Chinese garden.
Style: cinematic oriental photography.
```

输出应该包含：

- 系列主题
- 每张照片摄影机位置
- 镜头参数
- 构图说明
- 完整 Prompt

## 示例2：分析参考图片

```
Use aigc-photography-director.

Reverse engineer this image as a professional photographer.
Analyze camera position, lens, lighting and composition.
```

## 示例3：视频分镜

```
Use aigc-photography-director.

Convert this photo concept into cinematic video shots.
```

# Examples

## Example 1: 中式古风公园

主题：

江南园林中的汉服少女写真。

摄影方向：

- 摄影机位于石桥另一侧
- 50mm 镜头
- 人物占画面30%
- 前景使用竹叶虚化
- 柔和晨雾光
- 中国高级人像摄影色彩

关键词：

```
oriental cinematic portrait
soft morning light
traditional garden
natural elegance
```

---

## Example 2: 美式运动现场

主题：

篮球比赛现场运动写真。

摄影方向：

- 摄影机贴近场边地面
- 24mm 广角
- 低机位仰拍
- 球鞋进入前景
- 动作瞬间捕捉
- 高速运动摄影

关键词：

```
sports documentary photography
dynamic perspective
motion freeze
stadium atmosphere
```

---

## Example 3: 时尚日系街拍

主题：

东京街头女性时尚写真。

摄影方向：

- 摄影机位于人物侧后方3米
- 35mm 胶片镜头
- 跟拍视角
- 商店玻璃反射作为前景
- 自然路人环境
- Fuji 胶片色彩

关键词：

```
Japanese street fashion
35mm film photography
urban documentary
natural moment
```

# 设计原则

不要堆叠：

```
cinematic
masterpiece
high quality
beautiful
```

优先描述真实摄影决策：

```
Where is the camera?
How does the camera see?
What is the spatial relationship?
```

# Roadmap

- V0.1 Prompt structure
- V0.2 Photography director system
- V0.3 Reference Image Reverse Engineering
- V0.4 Video storyboard director
