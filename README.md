# 🏛️ Agora AI - 超级西方哲学 AI 平台

**创建时间**: 2026-02-25  
**维护者**: 勇哥 + 喵妹 🐱  
**愿景**: 让每个人都能与最伟大的思想家对话

---

## 🎯 项目愿景

Agora AI 是一个 AI 驱动的西方哲学研究与教育平台，整合：
- 🧠 哲学知识图谱 (PhilKG+) - 50 万 + 实体
- 🎭 苏格拉底 AI 导师 - 对话式学习
- 🗺️ 论证可视化 - 思想结构图谱
- 📚 文献智能管理 - AI 摘要 + 关联
- 🎓 教育课程 - 从入门到高阶

**名称寓意**: Agora (古希腊广场) - 思想交流的公共空间

---

## 🚀 快速开始

### 环境要求
- Python 3.10+
- Node.js 18+
- Neo4j 5+
- Docker (可选)

### 安装步骤

```bash
# 1. 克隆仓库
git clone https://github.com/leoxmrsh007/Agora-AI.git
cd Agora-AI

# 2. 安装后端依赖
cd backend
pip install -r requirements.txt

# 3. 安装前端依赖
cd ../frontend
npm install

# 4. 启动 Neo4j (Docker)
docker run -d --name neo4j \
  -p 7474:7474 -p 7687:7687 \
  -e NEO4J_AUTH=neo4j/agora2026 \
  neo4j:5

# 5. 启动后端
cd ../backend
python app.py

# 6. 启动前端
cd ../frontend
npm run dev
```

访问 http://localhost:3000

---

## 🏗️ 项目架构

```
Agora-AI/
├── backend/              # FastAPI 后端
│   ├── app.py           # 主应用
│   ├── services/        # 业务逻辑
│   ├── models/          # 数据模型
│   └── api/             # API 路由
│
├── frontend/            # Next.js 前端
│   ├── pages/          # 页面组件
│   ├── components/     # UI 组件
│   └── styles/         # 样式文件
│
├── data/               # 数据目录
│   ├── sep/           # 斯坦福哲学百科
│   ├── knowledge_graph/ # 知识图谱数据
│   └── papers/        # 论文数据
│
├── scripts/            # 工具脚本
│   ├── crawl_sep.py   # SEP 爬取
│   ├── build_graph.py # 图谱构建
│   └── ...
│
└── docs/              # 文档
    ├── architecture.md  # 架构设计
    ├── api.md          # API 文档
    └── ...
```

---

## 📊 核心功能

### 1. 哲学知识图谱 (PhilKG+)

**数据源**:
- Stanford Encyclopedia of Philosophy (1,722 篇)
- PhilPapers (300 万 + 文献索引)
- Perseus (古希腊罗马经典)
- Project Gutenberg (公版哲学著作)

**实体类型**:
- 📄 文献 (Document)
- 👤 哲学家 (Philosopher)
- 💡 概念 (Concept)
- 🎯 论点 (Argument)
- 🔗 引用 (Citation)

**关系类型**:
- authored (哲学家→文献)
- cites (文献→文献)
- influenced (哲学家→哲学家)
- belongs_to (哲学家→流派)
- opposes (论点→论点)

---

### 2. 苏格拉底 AI 导师

**特点**:
- 用提问引导学生思考
- 个性化学习路径
- 论证分析 + 逻辑漏洞识别
- 思想实验引导

**对话示例**:
```
学生：我认为功利主义是对的，因为它最大化幸福。

苏格拉底：有趣的观点。但让我问你：
1. "幸福"如何定义？每个人的幸福都一样吗？
2. 如果牺牲一个人能救 100 个人，应该这样做吗？
3. 权利和幸福，哪个更根本？
```

---

### 3. 论证可视化

**功能**:
- 可视化哲学论证结构
- 识别前提、结论、假设
- 标注逻辑谬误
- 对比不同哲学家的论证

**示例**:
```
     [前提 1]: 痛苦是坏的
     [前提 2]: 幸福是好的
          ↓
   [前提 3]: 道德行为最大化好、减少坏
          ↓
      [结论]: 应该最大化幸福
          ↓
   [反对意见]: 权利比结果更重要
        ↙              ↘
  [回应 1]          [回应 2]
 权利也是功利    有独立于功利的权利
```

---

## 🗺️ 开发路线图

### Phase 1: MVP (2 个月) 📅 03-04 月
- [ ] 知识图谱 v1 (SEP 数据)
- [ ] 基础 AI 对话 (苏格拉底模式)
- [ ] 前端 Demo
- [ ] 部署测试

### Phase 2: 功能完善 (3 个月) 📅 05-07 月
- [ ] 论证可视化
- [ ] 完整课程体系
- [ ] PhilPapers API 集成
- [ ] 用户系统 + 进度追踪

### Phase 3: 规模化 (6 个月) 📅 08-01 月
- [ ] 多语言支持 (中/英/法/德)
- [ ] API 开放平台
- [ ] 移动端 App
- [ ] 付费订阅

---

## 🤝 贡献指南

### 开发流程
1. Fork 仓库
2. 创建分支 (`git checkout -b feature/xxx`)
3. 提交更改 (`git commit -m 'Add xxx'`)
4. 推送分支 (`git push origin feature/xxx`)
5. 创建 Pull Request

### 代码规范
- Python: PEP 8
- JavaScript: ESLint + Prettier
- 提交信息：Conventional Commits

---

## 📚 参考资料

- [PhilKG 论文](https://openreview.net/forum?id=yvk5HRVGQr)
- [Stanford Encyclopedia](https://plato.stanford.edu/)
- [PhilPapers](https://philpapers.org/)
- [Perseus Digital Library](https://www.perseus.tufts.edu/)

---

## 📄 许可证

MIT License

---

## 🌟 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=leoxmrsh007/Agora-AI&type=Date)](https://star-history.com/#leoxmrsh007/Agora-AI&Date)

---

**Agora AI - 让每个人都能与最伟大的思想家对话** 🏛️✨
