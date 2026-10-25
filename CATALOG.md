# 内容目录契约 v1

catalog.json 的 schemaVersion 为 1，resources 是作品数组。

每件作品有稳定 id、title、category（ADDON/TEXTURE/SHADER/SKIN/MAP）、summary、description、author、cover、page、requirements，以及 releases。

每次发布有 version、changelog、artifacts。每个文件包含 name、url（固定版本 HTTPS 资产）、size（字节）、sha256、minGameVersion 和 testedGameVersions。无游戏实测时 testedGameVersions 为 []。

图片与描述可独立更新，已经发布的成品文件使用新版本上传。发布成品并完成完整下载校验后再更新目录。目录变更在 App 手动刷新后显示。

“最低版本”是制作声明，不能单独证明兼容；只有确切运行验证过的游戏版本才能加入 testedGameVersions。
