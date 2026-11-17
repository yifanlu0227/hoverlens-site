# HoverLens · Mac 鼠标悬停翻译与离线查词

把鼠标移到单词上，轻按并松开 **Option（⌥）**，在浮窗中查看释义、翻译与发音。HoverLens 是原生 macOS 菜单栏应用，支持屏幕取词、离线英汉词典和可选的 AI 句子翻译。

**[官网与下载](https://hoverlens.app/#download)** · [使用演示](https://hoverlens.app/#how-it-works) · [最新版本与安装包](https://github.com/yifanlu0227/hoverlens-site/releases/latest) · [English website](https://hoverlens.app/en/) · [English below](#english)

## 能做什么

- **鼠标悬停查词**：指向单词、轻按 Option，也可选择自定义快捷键或自动悬停，无需复制文字或切换窗口。
- **离线词典**：ECDICT 提供英汉释义、音标与词形信息，首次下载约 52 MB 后可离线查询；也可使用 macOS 系统词典。
- **屏幕取词与 OCR**：优先读取应用提供的文字，无法直接读取时尝试 OCR。支持图片、PDF 和暂停视频中的单词；Apple 本机、百度、Google Cloud Vision OCR 可按单词与句子分别配置。
- **单词与句子翻译**：可选 Apple 本机单词翻译，或使用自己的 OpenAI 兼容服务。AI 句子翻译默认关闭，开启后在词典结果之后逐步显示所在句子的译文。
- **本机发音**：使用 Apple 语音朗读单词，可选美式或英式英语，并调整语速。
- **应用内更新**：自动检查正式新版本，也可手动检查；在应用内下载后安装并重启，保留已有配置与词典。

## 安装与首次使用

1. 从[官网下载页](https://hoverlens.app/#download)或[最新 Release](https://github.com/yifanlu0227/hoverlens-site/releases/latest)下载 `.dmg` 安装包。Release 中的源码归档是网站文件，不是 Mac 安装包。
2. 打开 DMG，将 HoverLens 拖入「应用程序」，再从那里启动。正式应用和 DMG 均使用 Developer ID 签名并经过 Apple 公证。
3. 按应用引导授予「辅助功能」和「屏幕录制」权限；如果系统要求重启应用，请退出后重新打开。不同 macOS 版本中的权限名称可能有所不同。
4. 在「词典与翻译」下载 ECDICT，或启用所需词典、翻译服务。使用 Apple 本机翻译前，先准备支持的语言包。
5. 把鼠标放到英文单词上，轻按并松开 Option。按 Esc 或点击浮窗外部即可关闭。

在设置窗口左下角点击「检查新版本」可手动检查更新；应用也会每 24 小时自动检查一次。升级时可查看更新内容、下载，再点击「安装并重启」。请将应用放在可写的本机应用目录中，也可随时从 Releases 手动下载。

## 系统要求与费用

| 项目 | 要求或说明 |
| --- | --- |
| Mac | Apple Silicon（M 系列芯片），macOS 14 或更新版本；当前未提供 Intel 安装包 |
| 本机词典、OCR 与发音 | 无需 API Key；ECDICT 需首次下载，系统词典与声音需在本机准备 |
| Apple 本机翻译 | 另需 macOS 26 或更新版本及支持的语言包 |
| AI 翻译 | 自备 OpenAI 兼容服务的地址、模型与凭证 |
| 云端 OCR | 百度 OCR 或 Google Cloud Vision OCR 需自备对应凭证；Google Cloud 项目还需启用 Cloud Vision API 与结算 |
| 费用 | HoverLens 可免费下载，无需注册 HoverLens 账户；云服务的额度和费用由对应服务商决定 |

## 数据与功能边界

使用本机词典、Apple OCR 和本机语音时，相关查询在 Mac 上处理。启用云端 OCR 会向所选服务发送识别用的截图；使用云端翻译会发送待译文字，以及按设置启用的附近文字或句子。服务凭证保存在 Mac 上权限受限的本地文件中，目前未加密，也未使用钥匙串。

HoverLens 以单词快查与可选的所在句子翻译为主，不提供整篇文章翻译、实时视频字幕翻译或生词本。OCR 效果取决于画面清晰度及应用是否允许截图；视频建议先暂停。句子未能完整读取时，只翻译已取得的上下文片段。

## 反馈与下载校验

遇到问题请[邮件联系开发者](mailto:yif.lu@mail.utoronto.ca?subject=HoverLens%20feedback)，附上 HoverLens 版本、macOS 版本、触发方式与复现步骤。请勿在反馈中包含 API Key 或其他凭证。

每个正式 Release 都附有 `SHA256SUMS`；[官网下载区](https://hoverlens.app/#download)也提供当前安装包的 SHA-256 校验值。

## English

**HoverLens is a native Mac hover translation and offline dictionary app.** Point at a word, tap and release **Option**, and read definitions and translations in a floating panel without copying text or switching windows.

**[Website and download](https://hoverlens.app/en/#download)** · [Interactive demo](https://hoverlens.app/en/#how-it-works) · [Latest release](https://github.com/yifanlu0227/hoverlens-site/releases/latest)

### Features

- Offline ECDICT English–Chinese lookup and macOS system dictionaries.
- Screen text lookup in apps, PDFs, images, and paused videos. Choose Apple on-device OCR, Baidu OCR, or Google Cloud Vision OCR independently for words and sentences.
- Apple on-device word translation and optional OpenAI-compatible word or sentence translation. Sentence translation is off by default and streams after dictionary results.
- On-device pronunciation, configurable shortcuts, automatic hover, and saved translation service configurations.
- In-app update checks, downloads, installation, and relaunch, preserving settings and local dictionaries.

### Install and get started

1. Download the `.dmg` from the website or latest release, drag HoverLens into Applications, and open it there. The app and DMG are Developer ID signed and Apple notarized.
2. Grant the requested Accessibility and Screen Recording permissions. Restart the app if macOS asks you to.
3. Download ECDICT or enable your preferred dictionary and translation services. Apple translation needs supported language packs.
4. Point at a word and tap Option. Press Esc or click outside the panel to close it.

Requires **Apple Silicon and macOS 14+**. Apple on-device translation additionally requires **macOS 26+**. No Intel download is currently provided. ECDICT needs an initial download of about 52 MB before offline use.

HoverLens is free to download and requires no HoverLens account. Local dictionaries, OCR, and speech need no API key. Cloud translation and OCR require your own credentials and may incur provider charges; Google Cloud Vision also requires an enabled API and billing. Cloud OCR sends lookup screenshots to the selected provider; cloud translation sends the requested text and any context enabled in your settings. Credentials are stored in a permission-restricted local file, currently without encryption or Keychain.

The app checks for stable updates every 24 hours, with a manual check next to the version number in settings. Review release notes, download, then install and relaunch. Keep the app in a writable local application directory. Manual downloads and SHA-256 checksums are available in Releases.

HoverLens does not provide full-article translation, live video subtitle translation, or a vocabulary notebook. OCR depends on image quality and capture permissions. Incomplete sentences are labeled as context fragments. For help, [email the developer](mailto:yif.lu@mail.utoronto.ca?subject=HoverLens%20feedback) with your app version, macOS version, and reproduction steps; omit credentials.

## 关于此仓库 / About this repository

此公开仓库用于维护 HoverLens 官网与分发正式安装包，**不包含应用源码**。GitHub 自动生成的源码归档仅包含网站文件。

This public repository contains the product website and distributes stable app downloads. **The application source is private.** GitHub's generated source archives contain website files only.

网站从 `main` 分支根目录通过 GitHub Pages 发布，`CNAME` 绑定 `hoverlens.app`。中英文文案分别位于 `index.html` 和 `en/index.html`；版本、下载链接与校验值由发布流程同步，编辑时请保留其结构。Google 与 Bing 的所有权验证文件需持续保留。
