# README
trilium-jsmind
--------------

![](README_image.png)

在trilium创建jsmind思维导图，可以编辑并实时保存 （Trilium 0.63.5）

使用了以下项目：

[hizzgdev/jsmind](https://github.com/hizzgdev/jsmind)

[allensunjian/jsmind.menu.js](https://github.com/allensunjian/jsmind.menu.js)

### 如何安装

1.  导入笔记，取消勾选安全导入选项（如果您不熟悉trilium的小部件，请谨慎操作）
2.  检查下列笔记是否已经添加标签（默认已经添加）
    1.  TriliumJsmindWidget笔记添加 `#widget` 标签
    2.  template添加 `#jsMindWidgetTemplate` 标签
    3.  css和jsmind.css添加 `#jsMindWidgetCss` 标签
    4.  jsMind笔记添加 `#template` 标签
3.  开始使用

### 使用说明

#### 如何创建jsMind笔记

![](1_README_image.png)

#### 如何进行图像引用

因trilium的api限制，本插件通过创建一个图像笔记间接实现图像引用。

![](2_README_image.png)

点击【Save image note】，会在jsMind笔记下生成一个jsMind-export图像子笔记。

![](3_README_image.png)

复制引用，插入到其他笔记。

![](4_README_image.png)

更新完思维导图后，点击【Save image note】会更新jsMind-export图像子笔记，可以看到其他笔记内的引用也更新了。

#### 如何启用/关闭右键菜单

在config笔记中，设置SHOW\_MENU=true启用右键菜单，设置SHOW\_MENU=false关闭右键菜单。

#### 如何添加图片节点

> 要添加图片节点，请先启用右键菜单

选中节点右键，点击【添加图片节点】

![](5_README_image.png)

![](7_README_image.png)

复制图片链接到输入框，点击【Save】

![](6_README_image.png)

### 正在实现的功能

> 或者待修复的bug

*   处理domtoimage生成图像模糊的问题
*   添加简单图片节点
*   右键菜单（jsmind.menu.js）
*   图像引用
*   全屏显示
*   记录jsMind主题颜色
*   jsMind渲染在笔记右侧

### 版本历史

**v1.1.1（当前版本）**

更新jsmind；添加jsmind.menu.js插件；实现简单图片节点添加，直接添加图片数据会导致页面卡死，目前只允许添加图片链接；处理domtoimage生成图像模糊的问题。

**v1.1.0**

渲染更改为显示在笔记右侧，更加适配trilium的操作逻辑；无需再配置笔记ID；生成图像子笔记，间接实现图像引用。

**v1.0.0**

验证版本，能够渲染和编辑jsmind。