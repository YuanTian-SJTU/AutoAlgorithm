# 固定时间最大覆盖调度算法

## 项目背景
本项目基于Google DeepMind的Funsearch框架，解决卫星任务调度中的固定时间窗口最大覆盖问题。通过遗传算法和优先级评估模型，优化卫星对地面观测点的覆盖效率。

## 算法原理
### 核心优化模块
- **优先级函数**：`priority()` 通过多维度评估（覆盖点数、卫星索引、任务索引）动态选择最优任务
- 时间窗口冲突检测算法
- 多卫星资源分配策略

## 环境依赖
```bash
Python 3.10+
matplotlib==3.7.1
numpy==1.24.3
typing-extensions==4.7.1
```

## 运行方法
```bash
# 启动算法进化过程
python specification_new_5.py

# 运行测试用例
pytest specification_new_5_test.py -v
```

## 结果评估
算法迭代日志存储在/logs目录，包含：
- 每代最优个体适应度
- 覆盖率提升曲线
- 时间资源利用率分析

![算法进化曲线](./logs/coverage_progress.png)

## GitHub同步指南
```bash
git remote add origin [您的仓库URL]
git push -u origin main
```