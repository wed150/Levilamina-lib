# LevilaminaLib
a pre-compiled Levilamina sdk

不用担心本项目未更新导致编译错误,本项目会自动更新,并且就算有本项目未预编译的版本也会自动拉Levilamina仓库在本地编译
## Usage

1. 正常创建 `LeviLamina` 模组项目。
2. 在您项目中的 `xmake.lua` 中进行如下修改
```lua
...
在add_repositories("levimc-repo https://github.com/LiteLDev/xmake-repo.git")下方加入
add_repositories("groupmountain-repo https://github.com/GroupMountain/xmake-repo.git")
...
add_requires("levilamina x.xx.xx",{.....})
改成
add_requires("levilamina-lib x.xx.xx",{.....})
...
target("xxxx") -- 找到你Mod的这段内容
    ...
    add_packages("levilamina")
    改成
    add_packages("levilamina-lib")
    ...
```
3.执行xmake repo -u

