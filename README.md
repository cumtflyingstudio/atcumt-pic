# atcumt-pic (GitHub 图床)
> 文档分析：Claude Sonnet 4.5
> 生成日期：2025-11-08

一个用于存放并托管图片的静态仓库，用作 GitHub 图床。

### 使用 Git LFS 管理大文件

如果仓库将长期存放高分辨率图片或视频，推荐使用 Git LFS（Git Large File Storage）来避免仓库膨胀。

快速启用（在你的本地环境里执行）：

```bash
# 在全局安装并初始化 Git LFS（如未安装，请先安装 git-lfs，例如 macOS: brew install git-lfs）
git lfs install

# 在仓库中跟踪常见图片/视频类型（此命令会生成 .gitattributes）
git lfs track "*.png" "*.jpg" "*.jpeg" "*.gif" "*.mp4" "*.mov"

# 提交 .gitattributes 并推送（示例）
git add .gitattributes
git commit -m "chore: track images/videos with Git LFS"
git push origin <branch>
```

注意：如果仓库中已有大文件已被提交到 Git 历史中，需使用 `git lfs migrate` 或其他工具迁移历史（此操作有风险，请先备份仓库）。