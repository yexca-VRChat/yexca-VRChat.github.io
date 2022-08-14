***

# 公告  <!-- {docsify-ignore} -->

**最后修改-2022.08.08**  

此部分所有的文件应该都是我的网盘网站的链接  
查看所有文件请访问<https://pan.vrchat.yexca.xyz>  

~~所有图片均使用Github外链，如加载不出，可能是网络问题 (当然，能访问这里应该没啥问题了)~~  
所有图片已替换为Staticaly的CDN链接  
另外我VRChat的ID为[yexca](https://vrchat.com/home/user/usr_16490da9-3083-4d90-baab-f19d939c2732)  

# 说明/目录 <!-- {docsify-ignore} -->

~~原本只是说明，考虑到手机端不是太方便观看便加上目录~~  
鉴于想要侧边栏简洁，此处添加说明

* [VRC Avatar Descriptor](/div/VRC_Avatar_Descriptor.md) *VRChat描述文件的介绍*
* [PhysBones](/dynamics/PhysBones.md) *VRChat动骨的介绍*
* [Contacts](/dynamics/Contacts.md) *VRChat交互的介绍*
* [State Behaviors](/div/State_Behaviors.md) *VRChat提供的状态机脚本的介绍*
* [Cloth](/div/Cloth.md) *Unity布料简介*
* [Particle System](/div/Particle_System.md) *Unity粒子系统简介*
* [Animation](/Summary/Anime.md) *动画的制作*
* [Parameters](/Summary/Parameters) *数值的类型与官方数值*
* [Animator Layers](/Summary/Layers.md) *Unity动画器的图层*
* [VRChat Menu](/Summary/Menu.md) *VRChat的菜单*
* 上传：*这部分是模型的上传*
    * [上传前准备](/Upload/Prepare.md)
    * [成品模型上传](/Upload/Upload.md)
    * [MMD模型转为FBX](/Upload/mmd_to_fbx.md)
    * [MMD模型上传](/Upload/mmd_upload.md)
    * [SDK2转为SDK3](/Upload/sdk2_to_sdk3.md)
* 修改：*这部分是简单的修改*
    * [添加默认图层与菜单](/editing/Playable_Layers.md)
    * [Base层-蹲姿，趴姿](/editing/Base.md)
    * [Action层-AFK](/editing/afk.md)
    * [FX层-物品开关](/editing/switch.md)
* 附加：*修改的附加部分*
    * [物体绑骨](/additional/tied_bones.md)
    * [换衣服](/additional/change_clothes.md)
    * [固定世界物品](/additional/set_object.md)
    * [固定世界MMD](/additional/set_MMD.md)
    * [手势开关](/additional/gesture.md)
* 表情：*表情制作相关*
    * [添加手势表情](/emote/emote_anim.md)
    * [Blender添加形态键](/emote/Add_BlenderShapes.md)
    * [一键复制](/emote/Pumkin_Tools.md)
* 脚本：*此部分修改使用了VRC的脚本*
    * [自身跳MMD舞蹈](/script/self_MMD.md)
    * [随机播放音乐](/script/Shuffle_Playback.md)
    * [顺序播放音乐](/script/play_in_order.md)
    * [出场动画](/script/Start.md)
* 其他：*其他修改*
    * [添加一个可以写字的笔](/other/VRLabs_Marker.md)
    * [Blender换头](/other/Blender_change_head.md)
    * [PC下移动手](/other/PC_Arm_Moving.md)
* [参考资料](/References.md)

# 待办 <!-- {docsify-ignore} -->
以下是通过评论或私信或其他渠道希望我做的相关内容，说实话与其等我写出来不如自己去研究 ~~(等我做出来自己早就精通了)~~  
按照时间顺序排列，已经做好就不放链接了，左上角有搜索

* [x] SDK描述文件(VRC Avatar Descriptor)的介绍
* [x] 修改/制作表情动画
* [X] Blender换头
* [X] 粒子系统（这个因个人能力有限，可能不会做视频）
* [X] 顺序播放音乐
* [X] 按手势 拔出和发射武器
* [X] 更改自身亮度
* [ ] 制作动作动画
* [X] 出场动画
* [ ] 换头发(我好像没有相关物品，可能做不了)
* [ ] 换颜色
* [ ] 多个头手势与嘴型
* [ ] 挥动武器显示特效
* [ ] 摇尾巴

***

# 关于网站vrchat.yexca.xyz  <!-- {docsify-ignore} -->
我从接触VRChat到做出网站[yexca'VRChat入门教程](https://vrchat.yexca.xyz)其实只有大概一个半月的时间，肯定会有许多问题我没有遇到或无法解决，请见谅  
~~然后就是里面的文章可能就那样不会去修改了吧~~  
目前已经更换网站系统，文章 ~~(如果有)~~ 将继续发布，原有文章链接替换完毕，不再更新

# 关于此网站  <!-- {docsify-ignore} -->
这个网站是部署在Github上的，主要是在做网盘网站时接触了Markdown觉得很好用，又得知可以直接使用Markdown进行建网站便尝试了一下，~~以后更新应该会在这里吧~~，毕竟WordPress打开写文章太难受了 ~~(我本可以忍受WordPress，如果我不曾遇见Markdown)~~  
~~现在两网站将一起更新，但此网站会更快点？~~  
考虑到网站<https://vrchat.yexca.xyz>修改，形式或者说功能？与此网站冲突，特修改侧边样式，将模块放到前面  
产生了将此网站改模相关文章删除的想法-2022.08.08

# 记录  <!-- {docsify-ignore} -->
这里是我为什么做这些，仅记录使用  

* 起因  
和朋友开玩笑式说自己要去做教程，然后他很支持  
不过说实话当时知道的还很少，就想着随便写写吧，反正没人看

* 文章  
然后我就去做了网站[yexca‘VRChat入门教程](https://vrchat.yexca.xyz/)，这个网站刚开始名字是`VRChat教程`，在制作过程查阅资料时发现自己知道的其实非常有限，于是~~连夜~~更改网站名称

* 视频  
起初只是想写文章，但有些东西是文章无法表现出来的，于是便去试着做了视频  
令我没想到的是居然有人会看我的视频(doge)，然后后面的文章写的也不是特别随意了  
在看到很多人的评论之类的东西后感觉 ~~(自己遇到的问题好少啊)~~ 挺开心的  
然后也渐渐看到了一些更深入的视频，再次意识到了自己的弱小  

# 其他  <!-- {docsify-ignore} -->
这边就是我个人的东西啦，写到这里突然感觉还是应该和我的博客隔离开来比较好啊  
好啦，现在已经分离啦

> All about me

<https://a.yexca.xyz>

> 文章

写文章是爱好，得益于学习了Markdown更喜欢记录东西啦~  

> 视频

我**可能**还会把自己的学习的东西做成视频吧  

~~我说了那么多次Markdown，这不得挂个我自己写的文章：~~  
[Markdown简述(github)](https://git.yexca.xyz/#/Markdown/Markdown_Guide)  
[Markdown简述(博客)](https://yexca.xyz/index.php/2022/05/28/markdown%e7%ae%80%e6%98%93%e5%85%a5%e9%97%a8%e5%ad%a6%e4%b9%a0%e7%ac%94%e8%ae%b0/)