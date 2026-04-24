# 广雅生存手册（GY-Guide）
广雅校园非官方实用指南，由学生共同维护，助力每一位广雅学子快速适应校园生活。
**所有人均可参与编辑，所有内容均经过审核求证后收录。**

![Stone Badge](https://stone.professorlee.work/api/stone/kuqilin/GY-Guide)

## 📋 项目简介
- 覆盖校园生活、学习、食宿、设施、常见问题等全场景指南
- 内容持续更新，真实、准确、易用
- 完全开源，欢迎每一位同学参与共建

## 🤝 如何贡献内容（How To Contribute）
欢迎通过以下两种方式为手册添砖加瓦：

### 方法一：提交 Issue（最简单）
无需修改代码，直接提出建议或反馈。
- 新增章节/内容
- 修正错误信息
- 提出优化建议
- 报告问题

操作：进入仓库 → 点击 **Issues** → **New issue**，清晰描述需求或者在内容中填写你想加入的内容即可。

示例标题：
- 新增：章节「广雅火星校区」
- 修正：校区中午作息时间更新

---

### 方法二：Fork + Pull Request（自己动手）

> [!WARNING]
> 本方法适合高级用户，对于普通人过于难了……

1. 点击仓库右上角 **Fork**，将项目复制到你的 GitHub 账号
2. 克隆你 Fork 的仓库到本地
    ```bash
    git clone https://github.com/你的账户名/GY-Guide
    ```

    值得注意的是，现在 GitHub 不能用 HTTPS 进行推送了，得用 SSH 来推送~~（不然我也不会说适合高级用户了）~~，所以克隆你的仓库得用
    ```bash
    git clone git@github.com:你的账户名/GY-Guide.git
    ```

3. **从 main 分支新建分支（切勿直接在 main 修改）**
   ```bash
   git checkout -b feature/你的功能名
   ```

4. 在新分支上完成修改
5. 提交并推送至你的远程仓库
6. 向本仓库提交 **Pull Request (PR)**
7. 等待审核、反馈与合并
8. 合并后，你可以用下方命令来删除本地的分支
```bash
# 先切换回 main 分支
git checkout main

# 再删除本地已合并分支
git branch -d 分支
```


### 重要规范
- 一个分支只做一件事（一个功能 / 一处修正）
- 内容真实有效，不造谣、不误导
- 语言友好、格式清晰
- PR 标题简明，说明修改内容

## 📌 内容规范
- 信息真实、准确、有效
- 语言文明、积极、实用
- 结构清晰，便于阅读与维护
- 不包含违法、违规、攻击性或不实信息




### Git 常用命令

#### 一、git clone 克隆

```bash
# 基础
git clone <仓库地址>

# 指定克隆到某个文件夹名
git clone <url> <文件夹名>

# 只克隆单个分支（不拉全部分支）
git clone -b 分支名 <url>

# 浅克隆（只拉最近一次提交，速度超快）
git clone --depth=1 <url>
```

#### 二、git checkout 分支切换 & 恢复文件

```bash
# 切换已有分支
git checkout 分支名

# 创建并切换新分支
git checkout -b 新分支名

# 从某个提交/分支拉出新分支
git checkout -b 新分支名 提交ID/分支名

# 丢弃工作区文件改动（恢复成原版）
git checkout -- 文件名
```

#### 三、git status 查看状态

```bash
# 普通查看
git status

# 精简模式（最常用）
git status -s
```

#### 四、git branch 分支管理

```bash
# 查看本地分支
git branch

# 查看本地 + 远程所有分支
git branch -a

# 创建分支（不切换）
git branch 新分支名

# 删除本地已合并分支
git branch -d 分支名

# 强制删除本地分支（未合并也删）
git branch -D 分支名
```

#### 五、git add 暂存

```bash
# 单个文件
git add 文件名

# 所有改动文件
git add .

# 只跟踪修改过的文件，不新增未追踪文件
git add -u
```

#### 六、git commit 提交

```bash
# 带描述提交
git commit -m "提交说明"

# 修改上一次提交（不新增提交记录）
git commit --amend
```

#### 七、git push 推送

```bash
# 普通推送
git push origin 分支名

# 第一次推送并绑定上游
git push -u origin 分支名

# 强制推送（危险！慎用）
git push -f

# 删除远程分支
git push origin :远程分支名
```

#### 八、git pull 拉取合并

```bash
# 拉取并合并
git pull origin 分支名

# 允许合并无关历史（偶尔用到）
git pull --allow-unrelated-histories
```

#### 九、git log 查看提交历史

```bash
# 完整日志
git log

# 单行精简日志
git log --oneline

# 看分支图形
git log --oneline --graph

# 最近 n 条记录
git log -n 5
```

#### 十、git remote 远程仓库管理

```bash
# 查看远程别名
git remote

# 查看详细地址
git remote -v

# 添加新远程
git remote add 别名 地址

# 删除远程
git remote remove 别名
```

#### 十一、git diff 对比改动

```bash
# 工作区和暂存区对比
git diff

# 暂存区和本地仓库对比
git diff --staged
```

#### 十二、git fetch 拉取远程信息（不合并）

```bash
# 拉取所有远程更新
git fetch

# 拉取指定远程
git fetch origin
```

