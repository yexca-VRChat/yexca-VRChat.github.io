Two Axis Puppet

# 动画

My Pan：[PC_Arm_Moving.unitypackage](https://pan.vrchat.yexca.xyz/Anim/PC_Arm_Moving.unitypackage)

# Arm_Rigth

*注：此演示退出不重置*

* 数值

Bool：Arm_Right_Toggle，Reset_Right

Float：Arm_1，Arm_2

* 图层

添加Avatar遮罩

`Default` - `Arm_Right_Toggle=True` - `BlendTree` - `Reset_Right=True` - `Resrt` - `Reset_Right=False` - `Default`

* BlendTree

Arm_1，Arm_2

2D Freeform Directional(二维自由定向)

6个Add Motion Field

| Motion         | Pos X | Pos Y |
| -------------- | ----- | ----- |
| ArmDefault     | 0     | 0     |
| ArmLeft        | -1    | 0     |
| ArmRight       | 1     | 0     |
| ArmUp          | 0     | 1     |
| ArmDown        | 0     | -1    |
| ArmRightUpLeft | -0.75 | 0.75  |

* 菜单

一、

Type：Two Axis Puppet

Parameter：Arm_Right_Toggle

Parameter Horizontal：Arm_1

Parameter Vertical：Arm_2

二、

Type：Button

Parameter：Reset_Right

# Arm_Both

*注：此演示退出即重置*

* 数值

Bool：Arm_Both_Toggle

Float：Arm_1，Arm_2

* 图层

添加Avatar遮罩

`Default` - `Arm_Both_Toggle=True` - `BlendTree`

`BlendTree` - `Arm_Both_Toggle=False` - `Default`

* BlendTree

Arm_1，Arm_2

2D Freeform Directional(二维自由定向)

7个Add Motion Field

| Motion          | Pos X | Pos Y |
| --------------- | ----- | ----- |
| ArmBothDefault  | 0     | 0     |
| ArmBothLeft     | -1    | 0     |
| ArmBothRight    | 1     | 0     |
| ArmBothUp       | 0     | 1     |
| ArmBothDown     | 0     | -1    |
| ArmBothUpLeft   | -0.5  | 0.5   |
| ArmBothLeftDown | -0.5  | -0.5  |

* 菜单

Type：Two Axis Puppet

Parameter：Arm_Both_Toggle

Parameter Horizontal：Arm_1

Parameter Vertical：Arm_2

