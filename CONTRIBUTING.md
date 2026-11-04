# 跨主机更新

本仓库是公开复习版。任意主机都可以匿名拉取和阅读；写入需要 GitHub 仓库权限。公网版只保留复习文字，其他项目的原稿、代码、未脱敏记录仍在原处。

```sh
git clone https://github.com/peropeng/interview-review.git
cd interview-review
git pull --ff-only
git switch -c notes/short-topic
# 修改 README.md 或对应分册
git diff --check
git add -- seckill.md
git commit -m "docs: clarify a project answer"
git push -u origin HEAD
gh pr create --fill --base main
```

已有副本从 `git switch main`、`git pull --ff-only` 开始；`git add` 换成实际修改的文件。小改也可在 GitHub 网页编辑并发起 PR。不依赖某台电脑的盘符、备份目录或自动监听。

更新时先判断内容放哪里：临场最短答案放 README，项目实现与数据口径放 bank.md、seckill.md 或 deepagent.md，projects.md 只做目录，通用八股放 java.md。新增本机材料时，先提取公开可用的文字，再补到对应章节；不要上传整份项目、个人资料、凭据或原始运行记录。专业术语首次出现用通行译名，可附英文；口语解释放在术语后。没有固定译名时保留英文，用一句话说明它在项目里的作用。正文尽量自洽，跨文件用相对链接。速读只留能直接说的答案。只保留能用项目例子说清的机制。每个技术点先问它能不能解释这次的设计或取舍，再决定是否放进正文。
