![bc5c7a34fee614e08839b511a5840873.jpg](https://i.loli.net/2020/01/30/fOFvI2o9KXqEkJr.jpg)
# Magisk Module 模板

`这是Magisk模块最基础的结构`
```
module.zip
│
├── META-INF
│   └── com
│       └── google
│           └── android
│               ├── update-binary      <--- 这个文件你可以通过下载 module_installer.sh 得到
│               └── updater-script     <--- 这个文件应仅包含字符串 "#MAGISK"
│
├── tools/*                            <---  一些必要的工具类文件
│
├── customize.sh                       <---  这个文件包含 "SKIPUNZIP=0" 如需更改权限 请把0改为1 
│                                           这个文件由 update-binary 执行(sourced)
├── module.prop
├── ...  /* 模块文件的其余部分 */
|
```
**这意味着除了以上重要文件 其他的文件如果您不需要的话 可以删掉**

### 请不要 fork, 推荐使用Github Template功能

#### 支持在recovery模式中刷入, 包括第一次开机前

#### 有关模块和存储库的更多信息 请查看 [Magisk 官方文档](https://topjohnwu.github.io/Magisk/guides.html)
