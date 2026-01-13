# termux-python-wheels


# Termux Python Wheels

Pre-compiled Python wheels for **Termux (Android aarch64)**.
Build time saved: ~15 minutes per package.

## Included Packages
- **pydantic-core 2.41.5** (Python 3.12)
- **pymongo 4.16.0** (Python 3.12)

## Installation Guide / 安装指南

This repository provides two sets of wheels to support both `pip` and `uv` workflows.
本仓库提供两套文件名，分别兼容 `pip` 和 `uv`。

### Option A: Using `pip`
Pip works best with the `linux_aarch64` naming convention in Termux.
Termux 自带的 pip 识别 Linux 标签，请使用以下命令：

```bash
# Install pydantic-core
pip install https://github.com/Future-404/termux-python-wheels/raw/main/wheels/pydantic_core-2.41.5-cp312-cp312-linux_aarch64.whl

# Install pymongo
pip install https://github.com/Future-404/termux-python-wheels/raw/main/wheels/pymongo-4.16.0-cp312-cp312-linux_aarch64.whl
```

### Option B: Using `uv`
`uv` strictly checks for Android platform tags.
uv 严格检查 Android 平台标签，请下载对应的包：

```bash
# 1. Download the android version wheels
wget https://github.com/Future-404/termux-python-wheels/raw/main/wheels/pydantic_core-2.41.5-cp312-cp312-android_24_arm64_v8a.whl
wget https://github.com/Future-404/termux-python-wheels/raw/main/wheels/pymongo-4.16.0-cp312-cp312-android_24_arm64_v8a.whl

# 2. Install using uv pip
uv pip install ./pydantic_core-*-android_*.whl
uv pip install ./pymongo-*-android_*.whl
```

## Disclaimer
These binaries are provided "as is", without warranty of any kind. Use at your own risk.

## License & Disclaimer

This repository provides pre-compiled wheels for convenience.
- **pydantic-core** is licensed under the MIT License.
- **pymongo** is licensed under the Apache License 2.0.

This repository itself is licensed under the MIT License.

**Disclaimer:** These binaries are provided "as is", without warranty of any kind. Use at your own risk. I am not affiliated with the Pydantic or MongoDB teams.
