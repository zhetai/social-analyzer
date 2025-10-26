# Social Analyzer 项目概述

Social Analyzer 是一个用于分析和跨超过1000个社交媒体网站查找个人资料的工具，提供 API、CLI 和 Web 应用程序三种使用方式。它包含多种分析和检测模块，用户可以在调查过程中选择使用哪些模块。

该工具的主要功能包括：
- 字符串和名称分析（排列组合）
- 使用多种技术查找个人资料（HTTPS 库和 Webdriver）
- 多资料搜索（用于关联 - 任何用逗号分隔的组合）
- 多层检测（OCR、正常、高级和特殊）
- 使用 Ixora 可视化个人资料信息（元数据和模式）
- 元数据和模式提取
- 元数据的力导向图（需要 ExtractPatterns）
- 按排名或国家搜索（Alexa 排名）
- 按类型搜索（成人、音乐等）
- 个人资料统计和静态信息
- 跨元数据统计
- 自动 flirtation 以减少不必要的输出
- 搜索引擎查找（Google API - 可选）
- 自定义搜索查询（Google API 和 DuckDuckGo API - 可选）
- 个人资料截图、标题、信息和网站描述
- 查找姓名来源、姓名相似性和按语言的常用词
- 查找可能的个人资料/年龄（有限分析）
- 自定义用户代理、代理、超时和隐式等待
- Python CLI 和 NodeJS CLI（限于 FindUserProfilesFast 选项）
- 检测到的个人资料截图（必须安装最新版本的 Chrome）
- 更快检查的网格选项（限于 docker-compose）
- 将日志转储到文件夹或终端（美化）
- 调整查找/获取个人资料的工作线程（默认 15）
- 重新检查失败的个人资料选项
- 按好、可能和坏过滤个人资料
- 将分析结果保存为 JSON 文件
- 简化的 Web 界面和 CLI

## 项目结构

该项目包含以下主要部分：
- `app.js`：Node.js 的主要入口点，处理 CLI 和 Web 应用程序。
- `app.py`：Python 的主要入口点，处理 CLI。
- `modules/`：包含核心功能模块，如检测、分析和可视化。
- `data/`：包含网站列表、语言和其他数据文件。
- `public/`：包含 Web 应用程序的静态文件。
- `readme/`：包含项目的说明和截图。

## 安装和运行

### Node.js Web 应用程序
```bash
npm install
npm start
```

### Node.js CLI
```bash
node app.js --username "johndoe"
```

### Python 包
```bash
pip install social-analyzer
python -m social-analyzer --username "johndoe"
```

### Python 脚本
```bash
pip install -r requirements.txt
python app.py --username "johndoe"
```

## 开发约定

- 项目使用 Node.js 和 Python 编写。
- 使用 `eslint` 进行 JavaScript 代码检查。
- 使用 `prettier` 进行代码格式化。
- 使用 `yargs` 处理 Node.js CLI 参数。
- 使用 `argparse` 处理 Python CLI 参数。
- 使用 `requests` 和 `selenium-webdriver` 进行网络请求。
- 使用 `cheerio` 和 `BeautifulSoup` 进行 HTML 解析。