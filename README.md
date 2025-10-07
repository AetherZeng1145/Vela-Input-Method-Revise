## 更好用的Vela-InputMethod

基于NEORUAA的Vela_input_method修改

把渲染改成了336*480，可以直接在Xiaomi Smart Band Pro模拟器和实际上完美使用

事件和属性和原本NEORUAA的代码一样，并无任何改变

使用方法也和原版没有更改，将components文件夹拷贝到src目录下，就可以作为自定义组件进行使用

## 属性
| 名称 | 类型 | 默认值 | 必填 | 描述 |
| --------  | :----:  | :----:  | :----:  | :---- |
| hide | boolean | true | 是 | 是否显⽰键盘（开发者可以通过切换属性值隐藏或者唤醒键盘） |
| keyboardtype | string | "QWERTY" | 否 | 键盘布局，"QWERTY" 表⽰全键 |
| maxlength | number | 5 | 否 | 默认展⽰的拼⾳候选词数量， maxlength > 0 时有效；点击展开查看所有候选词 |
| vibratemode | string | "" | 否 | 振动模式，""表⽰输⼊时不振动，"long" 表⽰⻓振动，"short" 表⽰短振动。默认为 "" |
| screentype | string | "circle" | 否 | 设备屏幕类型，"rect" 表示方形屏布局（对应 designWidth ≥ 336），"circle" 表示圆形屏布局（对应 designWidth 为 480），"pill-shaped" 表示胶囊形屏布局（对应 designWidth ≥ 192） |

## 事件
| 名称 | 参数 | 描述 |
| --------  | :-----  | :---- |
| complete | { detail: { content: string } } | 键盘输出字符时触发（当切换为中⽂输⼊法时候，当选中拼⾳对应⽂字时触发；当切换为英⽂输⼊法时，与 keyDown 触发条件⼀致）|
| delete | - | 键盘点击删除按钮触发 |
| keyDown | { detail: { content: string } } | 键盘按钮按下时触发 |
| visibilityChange | { detail: { visible: boolean } } | 键盘显示或隐藏时触发，visible 表⽰显示状态 |

这里感谢NEORUAA的开源！非常感谢

该版本为圆屏全键版本，其他版本请去对应的分支查看！

更多信息请至这里查看[传送门](https://github.com/NEORUAA/Vela_input_method)
