# 更新日志

## 0.1.6

修复游戏内命令使用后失效的问题

## 0.1.5

**特性：**

实现伤害 Trigger

引入钩子，需要在编译时提供条件`hooks`

**重构：**

1. 事件转发系统重构，支持定向转发和广播（旧系统只支持广播）
2. logger 实现优化，打印日志等级和模块名
3. Context 上下文共享模式更改，使用智能指针共享

## 0.1.4

修复 in 和 nin 比较模式总是生效的问题。

回到据点和集会时，自动重置 sequential_one 的计数器。

新增插件临时启用和禁用的开关命令 `!mas enable` 和 `!mas disable`。每次启动游戏默认启用。

## 0.1.3

支持自定义单个触发器的冷却时间。

修复sequence_one模式下，最后一个行为结束后数组越界错误。

优化debug提示。

## 0.1.2

减少debug日志长度。

## 0.1.1

首次支持游戏内命令功能。

支持热重载配置 通过游戏内输入框输入 `!mas reload` 进行重载。

新触发器：使用特定道具（包括衣装）。

日志可以打印当前Fsm状态，通过修改 `loader-config.json`，将日志等级设为 `DEBUG` 即可启用。

## 0.1.0

支持基本功能。

- 通用
  - 动作
  - 任务状态
- 武器专有
  - 太刀：开刃等级
  - 虫棍：红白黄三灯时间
  - 盾斧：
      - 红盾时间
      - 红剑时间
      - 电锯时间
      - 瓶子数量
      - 剑能量（瓶子外框）
