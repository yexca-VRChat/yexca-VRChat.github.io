## 一、导入相关

不用导入SDK2，导入上传SDK3模型需要的东西即可

## 二、去SDK2的描述

将模型放进场景后(拖入prefab文件或双击场景文件)，点击模型

在右边将其余组件删除（一般最后俩个），仅保留“Transform”和“Animator”两个组件即可

## 三、添加SDK3描述文件

### 1）调整视角球

”VRC Avatar Descriptor“第一个为”View“，即我们要调整的视角球，点击”Edit“即可在Unity调整，大概放在额头前，然后回到脚本点击”Return“即可

### 2）添加”Viseme“

”VRC Avatar Descriptor“第二个为”LipSync“，点击“Auto Detect”即可自动识别

如未能自动识别，一般将“Body”拖入相应位置即可
有些模型有“Body”和“Face”，请将“Mode”换成“Viseme Blend Shape”，然后将“Face”拖入“Face Mesh”即可（注意检查是否有错误）

## 四、上传

上传参考[成品模型上传第四步](/Upload/Upload.md#四、上传模型)

关于”VRC Avatar Descriptor“其他部分将在后续文章描述