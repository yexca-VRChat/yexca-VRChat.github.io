## 前言

交互系统(Contacts)允许角色检测与自己或其他人的信号，然后可以使用这些信号产生的参数来触发动画

**注意：交互系统和动骨系统是不同的**(我刚开始看搞混了)

交互系统分为发送端(VRCContactSender)和接收端(VRCContactReceiver)。发送端是为了被检测而存在，即一直在广播自己的参数(Collision Tags)，接收端检测发送端，如果和发送端参数(Collision Tags)相同，则更新参数

## 添加交互系统的组件

在物体或骨骼上添加组件搜索“vrc”，找到相应组件点击即可

## VRC Contact Sender(发送端)

定义发送信号的体积和参数(Collision Tags)

![img](https://cdn.jsdelivr.net/gh/yexca/image_hosting@master/20220427/image.ebh40gdczco.webp)

### Root Transform

此组件所在位置，若为空则为组件所在物品

### Shape(形状)

**Shape Type**：形状类型，可选“球体”和“胶囊”

**半径、位置、高度**(“胶囊”)：字面意思

**Rotation**：旋转

### Filtering(过滤)

调整和定义发送端如何与接收端交互

**Collision Tags**：指定该发送端可以影响/受其影响的字符串列表，为了成功实现碰撞(被接收端成功检测)，发送端和接收端都需要至少一对匹配的字符串

此处可选择默认的一些参数或者自定义参数，**注意：字母区分大小写**

### 个人浅析

在“VRC Avatar Descriptor”里有“Collidees”会设置头部、身体、手部和脚部的一些碰撞，这些设置默认是会有发送端的，发送参数为名字，例如“头部”为“Head”，因此无需将这些部位设置上发送端

## VRC Contact Receiver(接收端)

定义接受信号的体积与参数(Collision Tags)，然后输出相应参数

![img](https://cdn.jsdelivr.net/gh/yexca/image_hosting@master/20220427/image.4zfxznntlkg0.webp)

### Root Transform

此组件所在位置，若为空则为组件所在物品

### Shape(形状)

**Shape Type**：形状类型，可选“球体”和“胶囊”

**半径、位置、高度**(“胶囊”)：字面意思

**Rotation**：旋转

### Filtering(过滤)

定义如何与发送端交互

**Allow Self**：允许自己触发，勾选即可以自己与自己交互

**Allow Others**：允许他人触发，勾选即他人可以与自己交互

**Local Only**：仅在本地客户端上运行

**Collision Tags**：指定可以接受的字符串列表/触发此交互的参数列表，为了成功实现碰撞(成功检测到发送端)，发送端和接收端都需要至少一对匹配的字符串

### Receiver

![img](https://cdn.jsdelivr.net/gh/yexca/image_hosting@master/20220427/image.66905l2pgso0.webp)

定义接受到信号后所改变的参数，参数后填入名字即为要改变的参数

| Receiver Type(类型) | 描述                                                    | 数值                                          |
| ------------------- | ------------------------------------------------------- | --------------------------------------------- |
| 常量(Constant)      | 发生交互则改变参数                                      | 建议Bool，触发时为True 其他Float为1.0，Int为1 |
| OnEnter             | 当进入速度大于Min Velocity时触发                        | 建议Bool，触发时为True 其他Float为1.0，Int为1 |
| Proximity           | 发送端到接收端中心的接近程度 如果多个发送端，值为最近的 | Float，0.0~1.0                                |

第三种“Proximity”如需要很高精准度，需要将发送端半径调到非常小

## 个人浅析

发送端和接收端比作俩人，发送端卖“冰糖葫芦”(Collision Tags处自定义参数“冰糖葫芦”)，接收端只买”冰糖葫芦”(Collision Tags处自定义参数“冰糖葫芦”)，发送端在一定范围内说自己卖“冰糖葫芦”(Shape内)，接收端只能听到一定范围内的声音(Shape内)，当接收端接受范围和发送端发送给范围有重合时，即接收端听到有卖“冰糖葫芦”的时候，就会去购买(改变Receiver里参数)

当然，发送端不仅可以卖“冰糖葫芦”，也可以卖“玩具”等(Collision Tags处添加多个自定义参数)，接收端也不仅可以买“冰糖葫芦”，还可以买“饮料”等(Collision Tags处添加多个自定义参数)，只要卖的东西和买的东西有重合的，接收端就会去买(只要发送端和接收端的Collision Tags处有完全相同的参数，就会触发接收端的Receiver的参数改变)

以上为“常量(Constant)”，接触即触发改变参数

## 应用

比如锤子上添加接收端，Collision Tags添加头部(Head)，Receiver选择“常量(Constant)”，然后设置一个参数名为“锤头音效”，然后添加一个音频录制打开动画，在动画器添加Bool参数“锤头音效”，图层为默认到动画条件为“垂头音效”为true

这样在VRChat里，拿这个锤子去锤别人的头就会触发动画播放音频