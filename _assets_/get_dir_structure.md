---
tags:
---

```shell
$includeFolders = @("_assets_", "概率论", "微积分", "线性代数", "Other")
$excludeFolders = @(".clinerules", ".obsidian", ".trash", ".vscode")

function Get-UnifiedFolderTree($path, $indent = "") {
    $currentFolder = Split-Path $path -Leaf
    if ($currentFolder -in $excludeFolders) { return }

    Write-Output "${indent}├── $currentFolder"
    $subFolders = Get-ChildItem -Path $path -Directory -ErrorAction SilentlyContinue | Sort-Object Name
    foreach ($folder in $subFolders) {
        Get-UnifiedFolderTree $folder.FullName "$indent    "
    }
}

# 获取当前目录
$currentDir = Get-Location

# 只显示包含的文件夹及其子结构
Write-Output "文件夹结构: $currentDir"
foreach ($folder in $includeFolders) {
    $fullPath = Join-Path $currentDir $folder
    if (Test-Path $fullPath -PathType Container) {
        Get-UnifiedFolderTree $fullPath -maxDepth 3
    }
}
```
