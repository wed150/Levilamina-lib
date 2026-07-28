# LevilaminaLib
a pre-compiled Levilamina sdk
## Usage

1. 正常创建 `LeviLamina` 模组项目。
2. 在您项目中的 `xmake.lua` 中进行如下修改
```lua
...
在add_repositories("levimc-repo https://github.com/LiteLDev/xmake-repo.git")下方加入
add_repositories("wed15-repo https://github.com/wed150/xmake-repo.git")
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

