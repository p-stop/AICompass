# 贡献指南

- 欢迎
### 贡献方式

**发邮件给热心网友** 

- 如果你对github不熟悉，或者你有不会挂载的大文件，可以将你要挂的文件、写好的markdown文件或者一些想法，打包发邮件到**cuikq&#64;mail2&#46;sysu&#46;edu&#46;cn**，几位热心网友可以帮你代为修改。
- 还是很推荐通过github贡献（下面的方法）！这样可以学习github的使用，并成为贡献者显示在仓库右侧！


**Pull Request（推荐）**

推荐通过PR（即Pull Request）的形式来进行贡献，具体流程：

- 在GitHub[网页端](https://github.com/SYSU-SAIA/AICompass)点击右上角的fork，将本仓库fork到自己的账号下
- 在自己账号的对应仓库中进行修改
- 修改完成后，点击New pull request，提交一个PR
- 等待其他人审核、修改，然后合并到本repo中
### 如何上传文件？
- 试试huggingface上创建存储库来创建下载链接！(huggingface创建的下载链接墙内不可访问，可以将下载网址中的huggingface.co转变为hf-mirror.com)即可成功
## 1. 本地构建项目

本项目基于 Python 构建，请确保您的系统已安装 Python 环境。


### 1.1 克隆仓库
```shell
git clone https://github.com/SYSU-SAIA/AICompass.git
cd AICompass
```

创建虚拟环境
```shell
python -m venv venv
```

激活虚拟环境
```shell
# Windows

venv\Scripts\activate

# Linux/MacOS

source venv/bin/activate

```

安装项目依赖
```shell
pip install -r requirements.txt
```
### 1.2 本地运行
```shell
#启动开发服务器

mkdocs serve
```

此时可以访问http://127.0.0.1:8000 在本机查看文档

## 2. 贡献内容

### 2.1 网站结构
目前本站内容根据开课时间进行分组，然后再根据课程单独分页，每页内记录关于该课程的介绍、学习资料、学习技巧等。

在源代码层面，使用 markdown 进行编写，每一学期是一个文件夹，路径和网站链接路径保持一致，整体结构在 `mkdocs.yml` 文件中的 `nav` 部分定义。

`mkdocs.yml`是网站的配置文件，可修改网站的风格、添加拓展等。
```text
.
├── .github/                # GitHub 相关配置
├── docs/                   # 文档主目录
│   ├── FirstYear_1/       # 大一上学期
│   ├── FirstYear_2/       # 大一下学期
│   ├── SecondYear_1/      # 大二上学期
│   ├── stylesheets/       # 样式文件
│   ├── ContributionGuidelines.md    # 贡献指南
│   ├── important-source.md          # 重要资源
│   └── index.md                     # 主页
├── .gitignore            # Git 忽略配置
├── mkdocs.yml            # MkDocs 配置文件
├── model.md              # 模型文档
├── README.md             # 项目说明
└── requirements.txt      # Python 依赖清单

```

### 2.2 如何贡献

欢迎为本网站做出贡献！您可以

- 完善或更新页面内容
- 添加新的课程页面
- 改进网站样式
#### a. 贡献方式
**Pull Request（推荐）**
推荐通过 PR（即 Pull Request）的形式来进行贡献，具体流程：

- 在 GitHub 网页端点击右上角的 fork，将本仓库 fork 到自己的账号下
- 在自己账号的对应仓库中进行修改
- 修改完成后，点击 New pull request，提交一个 PR
- 等待其他人审核、修改，然后合并到本 repo 中

**发邮件给热心网友** 
如果你对github不熟悉,或者你有不会挂载的大文件,可以将你要挂的文件、写好的markdown文件或者一些想法，打包发邮件到**cuikq&#64;mail2&#46;sysu&#46;edu&#46;cn**,几位热心网友可以帮你代为修改
#### b. 添加新页面

1. 在 `docs` 目录下创建 markdown 文件
2. 在 `mkdocs.yml` 的 `nav` 部分添加页面路径，例如：
```yaml
nav:
  - 课程:
    - 大一上:
      - 高等数学1上: 'FirstYear_1/calculus1.md'
```

#### c. 内容规范

- 保持客观性，理性介绍课程内容，请不要在本网站出现对老师本人的负面评价

#### d. 文件处理
- 课程笔记等请上传 PDF，建议多个文件打包整理
- **略大的文件(>1MB)请勿直接上传仓库** 这样可以避免仓库体积过大，保持克隆和访问速度


#### e.大文件处理方法

- 你可以将文件通过邮箱(主页有)发送给维护者来上传文件
- 对于小文件(<10MB)，你可以将其上传到自己的github存储库然后创建下载链接

- 如何上传大文件(>10MB)？
- 在**huggingface.co**上创建自己的公开仓库->在仓库中上传大文件->对这份文件的下载按钮右击->复制链接地址->将这个链接插入到你的指南文件中，这样就可以做到点击即下载
- huggingface创建的下载链接墙内不可访问，可以将下载网址中的huggingface.co转变为hf-mirror.com

#### e. 资源引用
- 优先使用外部资源链接
- 避免上传有版权内容（如课件）
!!! note
    新页面可以参考我们提供的[模板]()。
