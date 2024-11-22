# YabaiConfig
Mac平铺配置

## yabai 配置文件

> 文件保存在用户目录下，文件名称为 `.yabairc`

```bash
# 新建窗口显示在哪个显示器
# - default: 在新建窗口的显示器显示（mac的默认行为）
# - focused: 在当前聚焦的显示器出现
# - cursor: 在鼠标指针所在的显示器出现
yabai -m config window_origin_display  default

# 当前屏幕下，新窗口出现在屏幕的位置
yabai -m config window_placement  second_child

# 浮动窗口是否置顶
yabai -m config window_topmost    on

# 窗口不透明度效果
# - on: 启用透明效果
# - off: 关闭透明效果图 
yabai -m config window_opacity    off

# 激活窗口不透明度（需要上面的为 on 才有效）
yabai -m config active_window_opacity  1.0

# 未激活窗口不透明度（需要上面的为 on 有效）
yabai -m config normal_window_opacity  0.9

# 激活窗口和普通窗口切换时，不透明度的过度时间（需要上面的为 on 生效）
yabai -m config window_opacity_duration    0.2

# 窗口边框
# - on: 启用边框
# - off: 不启用
yabai -m config window_border    on

# 边框宽度
yabai -m config window_border_width  2

# 激活边框颜色
yabai -m config active_window_border_color    #ab4480
# yabai -m config normal_window_border_color    0xff

# 所有窗口使用相同比例的空间
yabai -m config auto_balance    off
# 分屏后新旧窗口比例，当 auto_balance off 时有效
yabai -m config split_ratio    0.50

# 窗口切换时，鼠标自动移动到使用的窗口中心
yabai -m config mouse_follows_focus    off

# 是否自动聚焦到鼠标所在的窗口
# - off: 关闭
# - autoraise
# - autofocus
yabai -m config focus_follows_mouse    off

# 按住对应修饰键时，yabai 不自动调整平铺
# 默认情况下调整大小时，yabai 会自适应调整平铺
# 配置时通常会关闭 focus_follows_mouse
yabai -m config mouse_modifier    fn

# modifier + 左键行为
# - move: 移动窗口
# - resize: 设置尺寸
yabai -m config mouse_action1    move

# modifier + 右键行为
# - move
# - resize
yabai -m config mouse_action2    resize

# 在平铺管理情况下，拖动窗口到另一个窗口位置时的操作
# - swap: 交换窗口位置
# - stack: 堆叠在旧窗口
yabai -m config mouse_drop_action    swap

# yabai 布局模式
# - bsp: 平铺
# - stack: 堆叠
# - float: 浮动
yabai -m config layout    bsp
# 窗口和屏幕边缘的距离
yabai -m config top_padding    08
yabai -m config bottom_padding    08
yabai -m config left_padding    08
yabai -m config right_padding    08
# 窗口之间的间距
yabai -m config window_gap    05

# manage: 是否使用 yabai 管理
# - on
# - off
# sticky: 是否总是置顶
# - on
# - off
# layer:
# - below
# - normal
# - above

yabai -m rule --add app="^System Preferences$" manage=off
yabai -m rule --add app="^System Information$" sticky=on layer=above manage=off
yabai -m rule --add app="^Activity Monitor$" sticky=on layer=above manage=off
yabai -m rule --add app="^Finder$" sticky=on layer=above manage=off
yabai -m rule --add app="^Alfred Preferences$" sticky=on layer=above manage=off
yabai -m rule --add app="^飞书$" sticky=on layer=above manage=off
yabai -m rule --add app="^Feishu$" sticky=on layer=above manage=off
yabai -m rule --add app="^Lark$" sticky=on layer=above manage=off
yabai -m rule --add app="^Lark Meetings$" sticky=on layer=above manage=off
yabai -m rule --add app="^AppCleaner$" sticky=off layer=above manage=off
yabai -m rule --add app="^WeChat$" manage=of
yabai -m rule --add app="^微信$" manage=off

echo "yabai config loaded"
```
