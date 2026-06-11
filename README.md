# 西江月数据包

这个仓库用于发布西江月 App 的离线诗词数据。

Git 仓库中只保存轻量级元数据：

- `README.md`
- `manifest.json`

完整数据包请放在 GitHub Releases 中，不要直接提交到 Git。

## 当前数据包

- 版本：`1.0.0`
- 文件名：`poetry_data_v1.0.0.zip`
- 解压根目录：`category-offline-xjy`
- SHA256：`CFC3A6F7B93784B30C228BA27716FAECF98B55930FD2A010C33126BC11F7A95C`
- 大小：`214498906` bytes

## 发布流程

1. 在本仓库创建 Release，标签建议使用 `v1.0.0`。
2. 上传 `poetry_data_v1.0.0.zip` 到 Release assets。
3. 获取 Release asset 下载地址。
4. 更新 `manifest.json` 中对应包的 `url` 字段。

App 同步数据时读取 `manifest.json`，下载 zip 后校验 SHA256，再解压到 App 本地私有目录。
