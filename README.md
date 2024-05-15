# SPDX-FileCopyrightText: 2015 - 2024 Rime community
#
# SPDX-License-Identifier: GPL-3.0-or-later

# Trime default style settings
# encoding: utf-8

config_version: "3.0"
name: 預設 #方案名稱
author: osfans #作者資訊

style:
  auto_caps: false #自動句首大寫:true|false|ascii
  background_dim_amount: 0.5
  candidate_font: han.ttf #候選字型
  candidate_padding: 5 #候選項內邊距
  candidate_spacing: 0.5 #候選間距
  candidate_text_size: 22 #候選字號
  candidate_use_cursor: true #高亮候選項
  candidate_view_height: 28 #候選區高度
  color_scheme: default #配色方案
  comment_font: comment.ttf #編碼提示字型
  comment_height: 12 #編碼提示區高度
  comment_on_top: true #編碼提示在上方或右側
  comment_text_size: 12 #編碼提示字號
  hanb_font: hanb.ttf #擴充字型
  horizontal: true #水平模式
  horizontal_gap: 1 #鍵水平間距
  keyboard_padding: 0 #竖屏模式下，屏幕左右两侧与键盘的距离（曲面屏减少误触）
  keyboard_padding_left: 0 #竖屏屏模式下，左手键盘布局，屏幕左侧与键盘的距离
  keyboard_padding_right: 40 #竖屏屏模式下，左手键盘布局，屏幕右侧与键盘的距离
  keyboard_padding_bottom: 0 #竖屏模式下，屏幕下边缘与键盘的距离（避免误触发全面屏手势）
  keyboard_padding_land: 40 #横屏模式下，屏幕左右两侧与键盘的距离（避免横屏按键过度拉伸变形）
  keyboard_padding_land_bottom: 0 #横屏模式下，屏幕下侧与键盘的距离
  layout: #懸浮窗口設置
    position: fixed #位置：left|right|left_up|right_up|fixed|bottom_left|bottom_right|top_left|top_right(left、right需要>=Android5.0)
    min_length: 5 #最小詞長
    max_length: 10 #超過字數則換行
    sticky_lines: 0 #固頂行數
    sticky_lines_land: 0 #横屏模式下的固顶行数
    max_entries: 1 #最大詞條數
    min_check: 3 #只要前n个候选词有长度大于等于min_length的词，就会把长度符合以及之前的词全部加到悬浮窗内。
    all_phrases: false #所有滿足條件的詞語都顯示在窗口
    border: 2 #邊框寬度
    max_width: 230 #最大寬度，超過則自動換行
    max_height: 400 #最大高度
    min_width: 40 #最小寬度
    min_height: 0 #最小高度
    margin_x: 5 #水平邊距 NOTE: margin_{x, y, bottom} 实际为 padding
    margin_y: 5 #豎直邊距
    margin_bottom: 0 #底部边距 （用于适配特定背景图）
    line_spacing: 0 #候选詞的行間距(px)
    line_spacing_multiplier: 1.2 #候选詞的行間距(倍數)
    real_margin: 3 #屏幕左右边缘和悬浮窗之间的距离 TODO: 在 4.0 时给 real_margin 与 spacing 换一个更适合的名字
    spacing: 1 #屏幕上下边缘或预编辑上下边缘和悬浮窗之间的距离
    round_corner: 8 #窗口圓角
    alpha: 0xdd #透明度(0-255)
    elevation: 5 #陰影(>=Android5.0)
    movable: once #是否可移動窗口，或僅移動一次 true|false|once
  window: #懸浮窗口組件
    - {start: "", move: 'ㄓ ', end: ""}
    - {start: "", composition: "%s", end: "", letter_spacing: 0} #letter_spacing需要>=Android5.0。TODO: 不爲0時，會導致不換行的問題
    - {start: "\n", label: "%s.", candidate: "%s", comment: " %s", end: "", sep: " "}
  key_font: symbol.ttf #鍵盤字型
  key_height: 44 #鍵高
  key_long_text_size: 14 #長標籤字號
  key_text_size: 22 #鍵字號
  key_width: 10.0 #鍵寬，佔螢幕寬的百分比
  keyboards: [.default, letter, number, symbols, mini] #鍵盤配置：自動鍵盤、字母、數字、符號、精简（供插入实体键盘使用）
  label_text_size: 22 #標籤字號
  label_font: label.ttf #編標籤字型
  latin_font: latin.ttf #西文字型
  latin_locale: en_US #西文語言
  locale: zh_TW #預設語言 zh_TW,zh_CN,zh_HK,""
  keyboard_height: 250 #锁定键盘高度，避免切换时键盘高度变化而造成闪烁
  keyboard_height_land: 200 #锁定横屏下键盘高度，避免切换时键盘高度变化而造成闪烁
  preview_font: latin.ttf #按鍵提示字型
  preview_height: 60 #按鍵提示高度
  preview_offset: -12 #按鍵提示縱向偏移
  preview_text_size: 40 #按鍵提示字號
  proximity_correction: true #按鍵糾錯
  reset_ascii_mode: false #顯示鍵盤時重置爲中文狀態
  round_corner: 8 #按鍵圓角半徑
  shadow_radius: 0.0 #按鍵陰影半徑
  speech_opencc_config: s2t.json #語音輸入簡繁轉換
  symbol_font: symbol.ttf #符號字型
  symbol_text_size: 10 #符號字號
  text_font: latin.ttf #編碼字型
  #text_height: 22 #編碼區高度
  text_size: 16 #編碼區字號
  vertical_correction: -10
  vertical_gap: 1 #鍵盤行距
  long_text_font: comment.ttf #剪贴板等可能包含大段文本使用的字体
  #background_folder: #背景图保存在background目录下的哪个子目录
  key_long_text_border: 1
  enter_label_mode: 0  #是否使用App提供的ActionLabel内容作为Enter键的文本（由于多数App没有适配ActionLable，实际影响不大）。0不使用，1只使用actionlabel，2优先使用，3当其他方式没有获得label时才读取actionlabel
  enter_labels:  # 定义Enter键的文本
    go: 前往
    done: 完成
    next: 下个
    pre:  上个
    search: 搜索
    send: 发送
    default: Enter   # 定义默认Enter键的文本

# 最好保留一项，防止其他主题使用 __include 时无法加载
fallback_colors:
  candidate_text_color: text_color
# 以下值是程序内置的，你也可以在这里自定义，这会覆盖默认值
#
#  comment_text_color: candidate_text_color
#  border_color: back_color
#  candidate_separator_color: border_color
#  hilited_text_color: text_color
#  hilited_back_color: back_color
#  hilited_candidate_text_color: hilited_text_color
#  hilited_candidate_back_color: hilited_back_color
#  hilited_label_color: hilited_candidate_text_color # 高亮候选序号 颜色
#  hilited_comment_text_color: comment_text_color
#  hilited_key_back_color: hilited_candidate_back_color
#  hilited_key_text_color: hilited_candidate_text_color
#  hilited_key_symbol_color: hilited_comment_text_color
#  hilited_off_key_back_color: hilited_key_back_color
#  hilited_on_key_back_color: hilited_key_back_color
#  hilited_off_key_text_color: hilited_key_text_color
#  hilited_on_key_text_color: hilited_key_text_color
#  key_back_color: back_color
#  key_border_color: border_color
#  key_text_color: candidate_text_color
#  key_symbol_color: comment_text_color
#  label_color: candidate_text_color
#  off_key_back_color: key_back_color
#  off_key_text_color: key_text_color
#  on_key_back_color: hilited_key_back_color
#  on_key_text_color: hilited_key_text_color
#  preview_back_color: key_back_color
#  preview_text_color: key_text_color
#  shadow_color: border_color
#  root_background: back_color # 整个键盘区+候选栏的背景图/色
#  candidate_background: back_color #候选栏的整体背景图/色
#  keyboard_back_color: border_color #键盘区的背景图/色
#  liquid_keyboard_background: keyboard_back_color # liquidKeyboard的背景图/色
#  text_back_color: back_color #编码区背景，即悬浮窗背景
#  long_text_back_color: key_back_color #长文本按键的背景(剪贴板）

preset_color_schemes:
  default:
    name: 預設／default #方案名稱
    author: osfans #作者資訊
    back_color: 0xe4e7e9 #候選區背景
    border_color: 0xc1c7ca #邊框
    candidate_separator_color: 0xc1c7ca #候選分割背景
    candidate_text_color: 0x5a676e #候選文字
    comment_text_color: 0x7b868c #提示
    hilited_back_color: 0xccd3d7da #標明編碼背景
    hilited_candidate_back_color: 0xd3d7da #標明候選背景
    hilited_candidate_text_color: 0x000000 #標明候選文字
    hilited_comment_text_color: 0x000000 #標明提示
    hilited_key_back_color: 0xd3d7da #標明按鍵背景
    hilited_key_symbol_color: 0x000000 #標明按鍵符號
    hilited_key_text_color: 0x000000 #標明按鍵文字
    hilited_off_key_back_color: 0xd3d7da #標明按鍵關閉狀態背景
    hilited_off_key_text_color: 0x000000 #標明按鍵關閉狀態文字
    hilited_on_key_back_color: 0xd3d7da #標明按鍵打開狀態背景
    hilited_on_key_text_color: 0x000000 #標明按鍵打開狀態文字
    hilited_text_color: 0x23948e #標明編碼
    key_back_color: 0xeceff1 #按鍵背景
    #key_border_color: 0xeceff1 #按鍵邊框
    key_symbol_color: 0x5f6b73 #按鍵符號
    key_text_color: 0x37474f #按鍵文字
    keyboard_back_color: 0xffffff #鍵盤背景
    label_color: 0x000000 #標籤
    off_key_back_color: 0xd3d7da #按鍵關閉狀態背景
    off_key_text_color: 0x000000 #按鍵關閉狀態文字
    on_key_back_color: 0x23948e #按鍵打開狀態背景
    on_key_text_color: 0x37474f #按鍵打開狀態文字
    preview_back_color: 0x55bfbfbf #按鍵提示背景
    preview_text_color: 0x23948e #按鍵提示文字
    shadow_color: 0x000000 #按鍵文字陰影
    text_color: 0x5a676e #編碼
    text_back_color: 0xcce4e7e9 #編碼區背景

  aqua:
    name: 碧水／Aqua
    author: 佛振 <chen.sst@gmail.com>
    text_color: 0x000000
    back_color: 0xeeeeec
    border_color: 0xe0e0e0
    hilited_text_color: 0x000000
    hilited_back_color: 0xd4d4d4
    hilited_candidate_text_color: 0xffffff
    hilited_candidate_back_color: 0x0a3afa

  azure:
    name: 青天／Azure
    author: 佛振 <chen.sst@gmail.com>
    text_color: 0xcae8ff
    candidate_text_color: 0xeef8ff
    back_color: 0x014e8b
    border_color: 0x014e8b
    hilited_text_color: 0xeef8ff
    hilited_back_color: 0x014e8b
    hilited_candidate_text_color: 0xfffe7f
    hilited_candidate_back_color: 0x015ea9
    comment_text_color: 0x6496c6

  luna:
    name: 明月／Luna
    author: 佛振 <chen.sst@gmail.com>
    text_color: 0x000000
    back_color: 0xffffff
    border_color: 0xcccccc
    hilited_text_color: 0x000000
    hilited_back_color: 0xffff7f
    hilited_candidate_text_color: 0xffffff
    hilited_candidate_back_color: 0x000000

  ink:
    name: 墨池／Ink
    author: 佛振 <chen.sst@gmail.com>
    text_color: 0x000000
    back_color: 0xffffff
    border_color: 0x000000
    hilited_text_color: 0x000000
    hilited_back_color: 0xdddddd
    hilited_candidate_text_color: 0xffffff
    hilited_candidate_back_color: 0x000000

  lost_temple:
    name: 孤寺／Lost Temple
    author: 佛振 <chen.sst@gmail.com>, based on ir_black
    text_color: 0xf6f3e8
    back_color: 0x444444
    border_color: 0x444444
    hilited_text_color: 0xcae682
    hilited_back_color: 0x222222
    hilited_candidate_text_color: 0x000000
    hilited_candidate_back_color: 0xcae682

  dark_temple:
    name: 暗堂／Dark Temple
    author: 佛振 <chen.sst@gmail.com>, based on ir_black
    text_color: 0xdaf692
    candidate_text_color: 0xe6e3d8
    back_color: 0x222222
    border_color: 0x222222
    hilited_text_color: 0x9acfff
    hilited_back_color: 0x222222
    hilited_candidate_text_color: 0xdaf692
    hilited_candidate_back_color: 0x333333
    comment_text_color: 0xff6c60

  starcraft:
    name: 星際我爭霸／StarCraft
    author: Contralisk <contralisk@gmail.com>, original artwork by Blizzard Entertainment
    text_color: 0x88aacc
    candidate_text_color: 0x55bb30
    back_color: 0x000000
    border_color: 0xa01010
    hilited_text_color: 0x96cbfe
    hilited_back_color: 0x000000
    hilited_candidate_text_color: 0xa8ff60
    hilited_candidate_back_color: 0x000000

  google:
    name: 谷歌／Google
    author: skoj <skoj@qq.com>
    text_color: 0x666666
    candidate_text_color: 0x000000
    back_color: 0xFFFFFF
    border_color: 0xE2E2E2
    hilited_text_color: 0x000000
    hilited_back_color: 0xFFFFFF
    hilited_candidate_text_color: 0xFFFFFF
    hilited_candidate_back_color: 0x3975CE

  solarized_rock:
    name: 曬經石／Solarized Rock
    author: "Aben <tntaben@gmail.com>, based on Ethan Schoonover's Solarized color scheme"
    back_color: 0x002b36
    border_color: 0x002b36
    text_color: 0x859900
    hilited_text_color: 0x2aa198
    candidate_text_color: 0x839496
    hilited_candidate_text_color: 0xffffff
    hilited_candidate_back_color: 0xd33682

  tintin:
    name: "丁丁／ Tintin"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0xffffff
    back_color: 0x0095d9
    border_color: 0x0095d9
    label_color: 0xffffff
    candidate_text_color: 0xffffff
    comment_text_color: 0xffffff
    hilited_text_color: 0x91d8f7
    hilited_back_color: 0x0095d9
    hilited_candidate_text_color: 0xffffff
    hilited_comment_text_color: 0xffffff
    hilited_candidate_back_color: 0xf16421

  dota_2:
    name: "DOTA 2"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0xffffff
    back_color: 0x100f12
    border_color: 0x100f12
    label_color: 0x8f755c
    hilited_text_color: 0xdd4118
    hilited_back_color: 0x100f12
    candidate_text_color: 0x8f755c
    comment_text_color: 0x8f755c
    hilited_candidate_text_color: 0xffffff
    hilited_comment_text_color: 0xffffff
    hilited_candidate_back_color: 0xdd4118

  brasil:
    name: "笆悉／Brasil"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0xffffff
    back_color: 0x119355
    border_color: 0x119355
    label_color: 0xffffff
    hilited_text_color: 0xffffff
    hilited_back_color: 0x17367d
    candidate_text_color: 0xffffff
    comment_text_color: 0xffffff
    hilited_candidate_text_color: 0xffffff
    hilited_comment_text_color: 0xffffff
    hilited_candidate_back_color: 0xf7c716

  doraemon:
    name: "銅鑼衛門／Doraemon"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0xe50012
    back_color: 0xffffff
    border_color: 0x009fe8
    label_color: 0x009fe8
    hilited_text_color: 0xffffff
    hilited_back_color: 0xe50012
    candidate_text_color: 0x009fe8
    comment_text_color: 0x009fe8
    hilited_candidate_text_color: 0xffffff
    hilited_comment_text_color: 0xffffff
    hilited_candidate_back_color: 0x009fe8

  espagna:
    name: "埃斯巴尼亞／España"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0xffffff
    back_color: 0xc30d23
    border_color: 0xc30d23
    label_color: 0xffffff
    hilited_text_color: 0xffffff
    hilited_back_color: 0xf7b52c
    candidate_text_color: 0xffffff
    comment_text_color: 0xffffff
    hilited_candidate_text_color: 0xffffff
    hilited_comment_text_color: 0xffffff
    hilited_candidate_back_color: 0xf7b52c

  gholabok:
    name: "胡蘿菔／Gholabok"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0xffffff
    back_color: 0xe83929
    border_color: 0xe83929
    label_color: 0xffffff
    hilited_text_color: 0xffffff
    hilited_back_color: 0x007b43
    candidate_text_color: 0xffffff
    comment_text_color: 0xffffff
    hilited_candidate_text_color: 0xffffff
    hilited_comment_text_color: 0xffffff
    hilited_candidate_back_color: 0xed6d3d

  kuma_shuzboz:
    name: "熊出沒／Kuma Shuzboz"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0x000000
    back_color: 0xf8b62d
    border_color: 0xf8b62d
    label_color: 0xffffff
    hilited_text_color: 0xf8b62d
    hilited_back_color: 0xffffff
    candidate_text_color: 0xffffff
    comment_text_color: 0xffffff
    hilited_candidate_text_color: 0xffffff
    hilited_comment_text_color: 0xffffff
    hilited_candidate_back_color: 0x000000

  kuon:
    name: "琨／Kuon"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0xffffff
    back_color: 0x3eb370
    border_color: 0x3eb370
    label_color: 0xffffff
    hilited_text_color: 0x3eb370
    hilited_back_color: 0xffffff
    candidate_text_color: 0xffffff
    comment_text_color: 0xffffff
    hilited_candidate_text_color: 0x3eb370
    hilited_comment_text_color: 0x3eb370
    hilited_candidate_back_color: 0xffffff

  macau:
    name: "澳門／Macau"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0xffd900
    back_color: 0x00a381
    border_color: 0x00a381
    label_color: 0xffffff
    hilited_text_color: 0xffffff
    hilited_back_color: 0xffd900
    candidate_text_color: 0xffffff
    comment_text_color: 0xffffff
    hilited_candidate_text_color: 0xffd900
    hilited_comment_text_color: 0xffd900
    hilited_candidate_back_color: 0xffffff

  nba:
    name: "NBA"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0xffffff
    back_color: 0x006ab7
    border_color: 0x006ab7
    label_color: 0xffffff
    hilited_text_color: 0xd71e54
    hilited_back_color: 0xffffff
    candidate_text_color: 0xffffff
    comment_text_color: 0xffffff
    hilited_candidate_text_color: 0xffffff
    hilited_comment_text_color: 0xffffff
    hilited_candidate_back_color: 0xd71e54

  ps4:
    name: "遊驛四／PS4"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0xffffff
    back_color: 0x000000
    border_color: 0x000000
    label_color: 0xffffff
    hilited_text_color: 0xffffff
    hilited_back_color: 0x595757
    candidate_text_color: 0xffffff
    comment_text_color: 0xffffff
    hilited_candidate_text_color: 0xffffff
    hilited_comment_text_color: 0xffffff
    hilited_candidate_back_color: 0x009fe8

  skype:
    name: "斯蓋普／Skype"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0xffffff
    back_color: 0x00adef
    border_color: 0x00adef
    label_color: 0xffffff
    hilited_text_color: 0x00adef
    hilited_back_color: 0xffffff
    candidate_text_color: 0xffffff
    comment_text_color: 0xffffff
    hilited_candidate_text_color: 0x00adef
    hilited_comment_text_color: 0x00adef
    hilited_candidate_back_color: 0xffffff

  xbox_silver:
    name: "銀色叉盒／Xbox Silver"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0x8dc21f
    back_color: 0xeeeeef
    border_color: 0xeeeeef
    label_color: 0xb5f05b
    hilited_text_color: 0xffffff
    hilited_back_color: 0xb5f05b
    candidate_text_color: 0x8dc21f
    comment_text_color: 0x8dc21f
    hilited_candidate_text_color: 0xffffff
    hilited_comment_text_color: 0xffffff
    hilited_candidate_back_color: 0x288c44

  youtube:
    name: "YouTube"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0x000000
    back_color: 0xdedede
    border_color: 0xdedede
    label_color: 0x000000
    hilited_text_color: 0xc30d23
    hilited_back_color: 0xffffff
    candidate_text_color: 0x000000
    comment_text_color: 0x000000
    hilited_candidate_text_color: 0xffffff
    hilited_comment_text_color: 0xffffff
    hilited_candidate_back_color: 0xc30d23

  so_young:
    name: "致青春／So Young"
    author: "五磅兔 <zcunlin@foxmail.com>"
    text_color: 0xd33682
    back_color: 0xfdf6e3
    border_color: 0xeee8d5
    label_color: 0x93a1a1
    candidate_text_color: 0x657b83
    comment_text_color: 0x268bd2
    hilited_text_color: 0x839496
    hilited_back_color: 0xeee8d5
    hilited_candidate_text_color: 0xeee8d5
    hilited_comment_text_color: 0xeee8d5
    hilited_candidate_back_color: 0x2aa198

  smurfs:
    name: "藍精靈／Smurfs"
    author: "skoj <skoj@qq.com>"
    text_color: 0xffffff
    back_color: 0x1778bf
    border_color: 0xe0edf5
    label_color: 0x1778bf
    hilited_text_color: 0x6dbcdb
    hilited_back_color: 0x1778bf
    candidate_text_color: 0xf6f6f6
    comment_text_color: 0xf6f6f6
    hilited_candidate_text_color: 0xf6f6f6
    hilited_comment_text_color: 0xf6f6f6
    hilited_candidate_back_color: 0x6dbcdb

  wii:
    name: "Wii"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0x595757
    back_color: 0xefefef
    border_color: 0xefefef
    label_color: 0xc8c9ca
    hilited_text_color: 0x33ccff
    hilited_back_color: 0xefefef
    candidate_text_color: 0x595757
    comment_text_color: 0xc8c9ca
    hilited_candidate_text_color: 0xffffff
    hilited_comment_text_color: 0xffffff
    hilited_candidate_back_color: 0x33ccff

  android:
    name: "安卓／Android"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0xffffff
    back_color: 0x1c7399
    border_color: 0x1c7399
    label_color: 0x3588c1
    hilited_text_color: 0xa8c450
    hilited_back_color: 0x1c7399
    candidate_text_color: 0xffffff
    comment_text_color: 0xffffff
    hilited_candidate_text_color: 0xffffff
    hilited_comment_text_color: 0xffffff
    hilited_candidate_back_color: 0xa8c450

  cool_breeze:
    name: "清風／Cool Breeze"
    author: "skoj <skoj@qq.com>"
    text_color: 0xFF0000
    back_color: 0xFBFBFF
    border_color: 0xAAAAFF
    hilited_text_color: 0xCE0000
    hilited_back_color: 0xFBFBFF
    candidate_text_color: 0x009100
    hilited_candidate_text_color: 0x3A006F
    hilited_candidate_back_color: 0xACD6FF

  google_plus:
    name: "Google+"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0xc8c9ca
    back_color: 0xffffff
    border_color: 0xdd4b39
    label_color: 0xc8c9ca
    hilited_text_color: 0xdd4b39
    hilited_back_color: 0xffffff
    candidate_text_color: 0xdd4b39
    comment_text_color: 0xc8c9ca
    hilited_candidate_text_color: 0xffffff
    hilited_comment_text_color: 0xffffff
    hilited_candidate_back_color: 0xdd4b39

  modern_warfare:
    name: "現代戰爭／Modern Warfare"
    author: P1461
    text_color: 0x70bc14
    back_color: 0x0d1b0a
    border_color: 0x83ad4b
    hilited_text_color: 0xfcfdfb
    hilited_back_color: 0x060e03
    candidate_text_color: 0xdcfeab
    comment_text_color: 0xfbfdfc
    hilited_candidate_text_color: 0xdcfeab
    hilited_candidate_back_color: 0x636f67

  brisk:
    name: "輕盈／Brisk"
    author: "skoj <skoj@qq.com>"
    text_color: 0xdc3822
    back_color: 0xffffff
    border_color: 0x333333
    hilited_text_color: 0xdc3822
    hilited_back_color: 0xffffff
    candidate_text_color: 0x575757
    hilited_candidate_text_color: 0xdc3822
    hilited_candidate_back_color: 0xffffff

  starcraft_ii:
    name: "星際爭霸Ⅱ／StarCraft Ⅱ"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0xffffff
    back_color: 0x0a1929
    border_color: 0x464b53
    label_color: 0xffffff
    hilited_text_color: 0xffffff
    hilited_back_color: 0x0a1017
    candidate_text_color: 0xffffff
    comment_text_color: 0xffffff
    hilited_candidate_text_color: 0xffffff
    hilited_comment_text_color: 0xffffff
    hilited_candidate_back_color: 0x1eadef

  steam:
    name: "Steam"
    author: "Patricivs <ipatrickmac@me.com>"
    text_color: 0x528ccd
    back_color: 0x171614
    border_color: 0x383635
    label_color: 0xffffff
    hilited_text_color: 0xd1cfc9
    hilited_back_color: 0x171614
    candidate_text_color: 0xffffff
    comment_text_color: 0xa9a7a7
    hilited_candidate_text_color: 0xffffff
    hilited_comment_text_color: 0xa9a7a7
    hilited_candidate_back_color: 0x314259

  flypy:
    # description: |
    #   小鶴飛揚：白底藍字，紅色標明。
    #   根據小鶴雙拼官網圖片製作
    #   http://www.flypy.com/images/mr.png
    name: "小鶴飛揚／flypy"
    author: "Pal.lxk <Pal.lxk@gmail.com>"
    text_color: 0x000000
    back_color: 0xffffff
    border_color: 0xc6c6c6
    label_color: 0x0080ff
    hilited_text_color: 0x0080ff
    hilited_back_color: 0xffffff
    candidate_text_color: 0x0080ff
    comment_text_color: 0x0080ff
    hilited_candidate_text_color: 0xb00000
    hilited_comment_text_color: 0xb00000
    hilited_candidate_back_color: 0xffffff
  tantsing:
    name: 丹青
    author: Mijiag
    back_color: 0xe3e3e3
    border_color: 0x000000
    text_color: 0x000000
    hilited_text_color: 0xe3e3e3
    hilited_back_color: 0x91071a
    hilited_candidate_text_color: 0xe3e3e3
    hilited_candidate_back_color: 0x730b6f
    candidate_text_color: 0x000000
    comment_text_color: 0x474747
  yygc:
    author: "小辛"
    back_color: 0xffffff
    border_color: 0xffffff
    candidate_text_color: 0x7f7f7f
    comment_text_color: 0x7f7f7f
    hilited_back_color: 0xffffff
    hilited_candidate_back_color: 0xffffff
    hilited_candidate_text_color: 0x7f7f7f
    hilited_comment_text_color: 0x7f7f7f
    hilited_key_text_color: 0x7f7f7f
    hilited_off_key_back_color: 0xffffff
    hilited_off_key_text_color: 0x7f7f7f
    hilited_on_key_back_color: 0xffffff
    hilited_on_key_text_color: 0x7f7f7f
    hilited_text_color: 0x7f7f7f
    key_text_color: 0x7f7f7f
    label_color: 0x7f7f7f
    name: "一葉孤城"
    off_key_text_color: 0x7f7f7f
    text_color: 0x7f7f7f

liquid_keyboard:
  # 目前只能直接写参数，不支持变量或者fallback机制。
  # 缺少参数时，自动从style中加载参数。除非需要指定liquid_keyboard使用与主键盘不同的背景色、背景图，否则不应设置被注释掉的参数。
  author: "tumuyan"
  row: 6              #每屏最多显示多少行按键
  row_land: 5         #横屏每屏最多显示多少行按键
  key_height: 40      #按键高度
  key_height_land: 40 #横屏模式按键高度
  single_width: 60    #single类型的按键宽度
  vertical_gap: 1     #纵向按键间隙
  margin_x: 0.5         #左右按键间隙的1/2
  keyboards: [emoji, math, ascii, cn, history, clipboard, collection, draft, symbollist, list, ids, symbol, tabs, pinyin, script_symbols, jp, grease, rusa, korea, lation, yinbiao, unit, yanwenzi, combing, emoji_full, candidate]  #tab列表
  tabs:
    name: 更多
    type: TABS
  candidate:
    name: 候选
    type: CANDIDATE
  history:
    name: 常用
    type: HISTORY
  emoji:
    type: SINGLE
    keys: "🙂😂🤣😆🙃😅🥺😎👀🙈🙉🙊☹😑😄🤐😨😱🌚🌝🤔❤💔🌹💣👌👍😣😥😮🙄😏😕😯😪😫😴😌🤑😉😋😎😍😘😚😛😜😝😒😓😔😲😷🤒😇🤓🤗🤕🙁😖😞😟😤😢😭😦😧😨😩😬😰😳😵😡😠☝✌🖕👎🙏🤘👏💪💋☘🍀🌸☕🍵🍺🍻🍦🍬🍚🍜🍲🍖🎂💤"
  emoji_full:
    type: SINGLE
    name: 全emoji
    keys: "😀😃😄😁😆😅🤣😂🙂🙃🫠😉😊😇🥰😍🤩😘😗☺😚😙🥲😋😛😜🤪😝🤑🤗🤭🫢🫣🤫🤔🫡🤐🤨😐😑😶🫥😏😒🙄😬🤥😌😔😪🤤😴😷🤒🤕🤢🤮🤧🥵🥶🥴😵🤯🤠🥳🥸😎🤓🧐😕🫤😟🙁☹😮😯😲😳🥺🥹😦😧😨😰😥😢😭😱😖😣😞😓😩😫🥱😤😡😠🤬😈👿💀☠💩🤡👹👺👻👽👾🤖😺😸😹😻😼😽🙀😿😾🙈🙉🙊💌💘💝💖💗💓💞💕💟❣💔❤🧡💛💚💙💜🤎🖤🤍💋💯💢💥💫💦💨🕳💬🗨🗯💭💤👋🤚🖐✋🖖🫱🫲🫳🫴👌🤌🤏✌🤞🫰🤟🤘🤙👈👉👆🖕👇☝🫵👍👎✊👊🤛🤜👏🙌🫶👐🤲🤝🙏✍💅🤳💪🦾🦿🦵🦶👂🦻👃🧠🫀🫁🦷🦴👀👁👅👄🫦👶🧒👦👧🧑👱👨🧔👩🧓👴👵🙍🙎🙅🙆💁🙋🧏🙇🤦🤷👮🕵💂🥷👷🫅🤴👸👳👲🧕🤵👰🤰🫃🫄🤱👼🎅🤶🦸🦹🧙🧚🧛🧜🧝🧞🧟🧌💆💇🚶🧍🧎🏃💃🕺🕴👯🧖🧗🤺🏇⛷🏂🏌🏄🚣🏊⛹🏋🚴🚵🤸🤼🤽🤾🤹🧘🛀🛌👭👫👬💏💑👪🗣👤👥🫂👣🏻🏼🏽🏾🏿🦰🦱🦳🦲🐵🐒🦍🦧🐶🐕🦮🐩🐺🦊🦝🐱🐈🦁🐯🐅🐆🐴🐎🦄🦓🦌🦬🐮🐂🐃🐄🐷🐖🐗🐽🐏🐑🐐🐪🐫🦙🦒🐘🦣🦏🦛🐭🐁🐀🐹🐰🐇🐿🦫🦔🦇🐻🐨🐼🦥🦦🦨🦘🦡🐾🦃🐔🐓🐣🐤🐥🐦🐧🕊🦅🦆🦢🦉🦤🪶🦩🦚🦜🐸🐊🐢🦎🐍🐲🐉🦕🦖🐳🐋🐬🦭🐟🐠🐡🦈🐙🐚🪸🐌🦋🐛🐜🐝🪲🐞🦗🪳🕷🕸🦂🦟🪰🪱🦠💐🌸💮🪷🏵🌹🥀🌺🌻🌼🌷🌱🪴🌲🌳🌴🌵🌾🌿☘🍀🍁🍂🍃🪹🪺🍄🍇🍈🍉🍊🍋🍌🍍🥭🍎🍏🍐🍑🍒🍓🫐🥝🍅🫒🥥🥑🍆🥔🥕🌽🌶🫑🥒🥬🥦🧄🧅🥜🫘🌰🍞🥐🥖🫓🥨🥯🥞🧇🧀🍖🍗🥩🥓🍔🍟🍕🌭🥪🌮🌯🫔🥙🧆🥚🍳🥘🍲🫕🥣🥗🍿🧈🧂🥫🍱🍘🍙🍚🍛🍜🍝🍠🍢🍣🍤🍥🥮🍡🥟🥠🥡🦀🦞🦐🦑🦪🍦🍧🍨🍩🍪🎂🍰🧁🥧🍫🍬🍭🍮🍯🍼🥛☕🫖🍵🍶🍾🍷🍸🍹🍺🍻🥂🥃🫗🥤🧋🧃🧉🧊🥢🍽🍴🥄🔪🫙🏺🌍🌎🌏🌐🗺🗾🧭🏔⛰🌋🗻🏕🏖🏜🏝🏞🏟🏛🏗🧱🪨🪵🛖🏘🏚🏠🏡🏢🏣🏤🏥🏦🏨🏩🏪🏫🏬🏭🏯🏰💒🗼🗽⛪🕌🛕🕍⛩🕋⛲⛺🌁🌃🏙🌄🌅🌆🌇🌉♨🎠🛝🎡🎢💈🎪🚂🚃🚄🚅🚆🚇🚈🚉🚊🚝🚞🚋🚌🚍🚎🚐🚑🚒🚓🚔🚕🚖🚗🚘🚙🛻🚚🚛🚜🏎🏍🛵🦽🦼🛺🚲🛴🛹🛼🚏🛣🛤🛢⛽🛞🚨🚥🚦🛑🚧⚓🛟⛵🛶🚤🛳⛴🛥🚢✈🛩🛫🛬🪂💺🚁🚟🚠🚡🛰🚀🛸🛎🧳⌛⏳⌚⏰⏱⏲🕰🕛🕧🕐🕜🕑🕝🕒🕞🕓🕟🕔🕠🕕🕡🕖🕢🕗🕣🕘🕤🕙🕥🕚🕦🌑🌒🌓🌔🌕🌖🌗🌘🌙🌚🌛🌜🌡☀🌝🌞🪐⭐🌟🌠🌌☁⛅⛈🌤🌥🌦🌧🌨🌩🌪🌫🌬🌀🌈🌂☂☔⛱⚡❄☃⛄☄🔥💧🌊🎃🎄🎆🎇🧨✨🎈🎉🎊🎋🎍🎎🎏🎐🎑🧧🎀🎁🎗🎟🎫🎖🏆🏅🥇🥈🥉⚽⚾🥎🏀🏐🏈🏉🎾🥏🎳🏏🏑🏒🥍🏓🏸🥊🥋🥅⛳⛸🎣🤿🎽🎿🛷🥌🎯🪀🪁🎱🔮🪄🎮🕹🎰🎲🧩🧸🪅🪩🪆♠♥♦♣♟🃏🀄🎴🔫🎭🖼🎨🧵🪡🧶🪢👓🕶🥽🥼🦺👔👕👖🧣🧤🧥🧦👗👘🥻🩱🩲🩳👙👚👛👜👝🛍🎒🩴👞👟🥾🥿👠👡🩰👢👑👒🎩🎓🧢🪖⛑📿💄💍💎🔇🔈🔉🔊📢📣📯🔔🔕🎼🎵🎶🎙🎚🎛🎤🎧📻🎷🪗🎸🎹🎺🎻🪕🥁🪘📱📲☎📞📟📠🔋🪫🔌💻🖥🖨⌨🖱🖲💽💾💿📀🧮🎥🎞📽🎬📺📷📸📹📼🔍🔎🕯💡🔦🏮🪔📔📕📖📗📘📙📚📓📒📃📜📄📰🗞📑🔖🏷💰🪙💴💵💶💷💸💳🧾💹✉📧📨📩📤📥📦📫📪📬📭📮🗳✏✒🖋🖊🖌🖍📝💼📁📂🗂📅📆🗒🗓📇📈📉📊📋📌📍📎🖇📏📐✂🗃🗄🗑🔒🔓🔏🔐🔑🗝💣🔨🪓⛏⚒🛠🗡⚔🪃🏹🛡🪚🔧🪛🔩⚙🗜⚖🦯🔗⛓🪝🧰🧲🪜⚗🧪🧫🧬🔬🔭📡💉🩸💊🩹🩼🩺🩻🚪🛗🪞🪟🛏🛋🪑🚽🪠🚿🛁🪤🪒🧴🧷🧹🧺🧻🪣🧼🫧🪥🧽🧯🛒🧿🪬🚬⚰🪦⚱🗿🪧🪪🏧🚮🚰♿🚹🚺🚻🚼🚾🛂🛃🛄🛅⚠🚸⛔🚫🚳🚭🚯🚱🚷📵🔞☢☣⬆↗➡↘⬇↙⬅↖↕↔↩↪⤴⤵🔃🔄🔙🔚🔛🔜🔝🛐⚛🕉✡☸☯✝☦☪☮🕎🔯♈♉♊♋♌♍♎♏♐♑♒♓⛎🔀🔁🔂▶⏩⏭⏯◀⏪⏮🔼⏫🔽⏬⏸⏹⏺⏏🎦🔅🔆📶📳📴♀♂⚧✖➕➖➗🟰♾‼⁉❓❔❕❗〰💱💲⚕♻⚜🔱📛🔰⭕✅☑✔❌❎➰➿〽✳✴❇©®™🔟🔠🔡🔢🔣🔤🅰🆎🅱🆑🆒🆓ℹ🆔Ⓜ🆕🆖🅾🆗🅿🆘🆙🆚🈁🈂🈷🈶🈯🉐🈹🈚🈲🉑🈸🈴🈳㊗㊙🈺🈵🔴🟠🟡🟢🔵🟣🟤⚫⚪🟥🟧🟨🟩🟦🟪🟫⬛⬜◼◻◾◽▪▫🔶🔷🔸🔹🔺🔻💠🔘🔳🔲🏁🚩🎌🏴🏳"
  clipboard:
    type: CLIPBOARD
    name: 剪贴
  collection:
    type: COLLECTION
    name: 收藏
  draft:
    type: DRAFT
    name: 草稿
  math:   #tab名称
    type: SINGLE
    name: 数学
    keys: "≈＝≠≌<>≤≥≡()[]{}-+±×*/÷&∥%‰‱°′″∫∮∯∬∭∰∞∑∧∏∈∵∴⊥∝∨∪•√〒∝∽∈∩∧⊙⌒∥∟∣∂∆∞≌∉∪∨⊕⊿⊥∠∫∬∭"  #tab中的按键列表
  cn:
    type: SINGLE
    name: 中文
    keys:  #keys列表可以使用多种格式混合书写。
      - ，
      - 。
      - ？
      - ！
      - ：
      - 、
      - “
      - ”
      - ‘
      - ···
      - ……
      - { click: "-" }
      - { click: "——", label: "破折" }
      - { click: "" } # 内容为空可以强制令键盘从此处新起一行
      - （
      - ）
      - 【
      - 】
      - 《
      - 》
      - ［
      - ］
      - ｛
      - ｝
      - 「
      - 」
      - 『
      - 』
      - ～
  symbol:
    name: 特殊
    type: SINGLE
    keys: "△▽○◇□☆▲▼●◆■★▷◁▶◀♻♲†⚝✡⚹✦✸✹￼�×⌫☑☒✅❎✔✘✓✗☀☼☽☾◑◐㏂㏘☭♀♂☹☻☠☜☝☞☚☟☛▪•‥…∷※♩♪♫♬§°♭♯♮‖¶№◎¤۞℗®©卍卐℡™㏇Φ⇦⇧⇨⇩⇪↖↑↗←↔→↙↓↘⇄⇅⇆⇤↩⇥▸◂▴▾◤◥◣◢㊤㊧㊥㊨㊦❏❐◲〼▢▣↶✁↷✍⏍ϟ📝✎✆☱☰☴⚿⛮⚙☲☯☵⛶☩☐☳☷☶💬🗨⟲ღ✈☂🎤🌐🔍"
  unit:
    name: 单位
    type: SINGLE
    keys: "℃¥$€฿￡㎡m³℉￥£￠₠¹²³⁴⁵ⁿ⁶⁷⁸⁹⁰ˣ⁺⁻⁼⁽⁾½⅓¼⅔¾₁₂₃₄₅ₙ₆₇₈₉₀ₓ₊₋₌₍₎℅"
  list:
    name: 列表
    type: SINGLE
    keys: "①②③④⑤⑥⑦⑧⑨⑩⒈⒉⒊⒋⒌⒍⒎⒏⒐⒑⒒⒓⒔⒕⒖⒗⒘⒙⒚⒛⑴⑵⑶⑷⑸⑹⑺⑻⑼⑽⑾⑿⒀⒁⒂⒃⒄⒅⒆⒇㈠㈡㈢㈣㈤㈥㈦㈧㈨㈩➊➋➌➍➎➏➐➑➒➓㊀㊁㊂㊃㊄㊅㊆㊇㊈㊉ⅰⅱⅲⅳⅴⅵⅶⅷⅸⅹⅠⅡⅢⅣⅤⅥⅦⅧⅨⅩ"
  pinyin:
    name: 拼音
    type: SINGLE
    keys: "āáǎàōóēéěèǒòīíǐìūúǖǘǚǜǔùêüńňㄚㄛㄜㄧㄨㄩㄝㄞㄟㄠㄡㄢㄣㄤㄥㄦㄅㄆㄇㄈㄉㄊㄋㄌㄍㄎㄏㄐㄑㄒㄓㄔㄕㄖㄗㄘㄙ"
  script_symbols:
    name: 𝒶𝒜
    type: SINGLE
    keys: "𝒶𝒷𝒸𝒹ℯ𝒻ℊ𝒽𝒾𝒿𝓀𝓁𝓂𝓃ℴ𝓅𝓆𝓇𝓈𝓉𝓊𝓋𝓌𝓍𝓎𝓏𝒜ℬ𝒞𝒟ℰℱ𝒢ℋℐ𝒥𝒦ℒℳ𝒩𝒪𝒫𝒬ℛ𝒮𝒯𝒰𝒱𝒲𝒳𝒴𝒵"
  grease:
    type: SINGLE
    name: 希腊
    keys: "ΑΒΓΔΕΖΗΘΙΚΛΜΝΞΟΠΡΣΤΥΦΧΨΩαβγδεζηθικλμνξοπρστυφχψω"
  rusa:
    name: 俄语
    type: SINGLE
    keys: "АБВГДЕЁЖЗИЙКЛМНОПРСТУФХЦЧШЩЪЫЬЭЮЯабвгдеёжзийклмнопрстуфхцчшщъыьэюя"
  lation:
    name: 拉丁
    type: SINGLE
    keys: "ÀÁÂÃÄÅÆÇÈÉÊËÌÍÎÏÐÑÒÓÔÕÖØÙÚÛÜÝÞŠŸŒàáâãäåæçèéêëìíîïðñòóõôöøùúûüýþšÿœ"
  korea:
    type: SINGLE
    name: "韩文"
    keys: "dㅏㅑㅓㅕㅗㅛㅜㅠㅡㅣㅐㅒㅔㅖㅘㅙㅚㅝㅞㅟㅢㄱㄴㄷㄹㅁㅂㅅㅇㅈㅊㅋㅌㅍㅎㄲㄸㅚㅆㅉ㉠㉡㉢㉣㉤㉥㉦㉧㉨㉩㉪㉫㉬㉭㉮㉯㉰㉱㉲㉳㉴㉵㉶㉷㉸㉹㉺㉻㈀㈁㈂㈃㈄㈅㈆㈇㈈㈉㈊㈋㈌㈍㈎㈏㈐㈑㈒㈓㈔㈕㈖㈗㈘㈙㈚㈛"
  yinbiao:
    type: SINGLE
    name: "音标"
    keys: ["a:", "ɔ:", "ɜː", "i:", "u:", "ʌ", "ɒ", "ə", "ɪ", "ʊ", "e", "æ", "eɪ", "aɪ", "ɔɪ", "ɪə", "eə", "ʊə", "əʊ", "aʊ", "p", "t", "k", "f", "θ", "s", "b", "d", "g", "v", "ð", "z", "ʃ", "h", "ts", "tʃ", "j", "tr", "ʒ", "r", "dz", "dʒ", "dr", "w", "m", "n", "ŋ", "l"]
  yanwenzi:
    type: VAR_LENGTH
    name: "颜文字"
    keys: ["⎛⎝≥⏝⏝≤⎠⎞", "^_^", "^ω^", "^o^", "~\\(≧▽≦)/~", "*^_^*", "↖(^ω^)↗", "(^o^)／", "(=^▽^=)", "=^_^=", "(*^ω^*)", "٩(๑^o^๑)۶", "o(￣▽￣)o", "Y(^_^)Y", "٩( 'ω' )و", "╰(*´︶`*)╯", "*罒▽罒*", "ヾ ^_^♪", "=￣ω￣=", "︿(￣︶￣)︿", "(´▽｀)ノ♪", "乁( ˙ ω˙乁)", "✧*｡٩(ˊωˋ*)و✧*｡", "～(￣▽￣～)(～￣▽￣)～", "QwQ", "(●—●)", "(๑• . •๑)", "ヾ(≧O≦)〃嗷~", "罒ω罒", "(｡ì _ í｡)", "(๑•ี_เ•ี๑)", "ㄟ(≧◇≦)ㄏ", "(*/ω＼*)", "●▽●", "٩(๑òωó๑)۶", "✺◟(∗❛ัᴗ❛ั∗)◞✺", "( σ'ω')σ", "♡＾▽＾♡", "(๑•̀ㅂ•́)و✧", "(ง •̀_•́)ง", "(｡･ω･｡)ﾉ♡", "(☆_☆)", "(๑°3°๑)", "_(•̀ω•́ 」∠)_", "♪～(´ε｀　)", "～(^з^)-☆", "(´∀｀)♡", "ლ(´ڡ`ლ)", "(＞﹏＜)", "T_T", "⊙︿⊙", "〒▽〒", "⊙﹏⊙", "π_π", "(｡•́︿•̀｡)", "(ToT)/~~~", "╯﹏╰", "ಥ_ಥ", "(╥╯^╰╥)", "(〃′o`)", "●﹏●", "( •̥́ ˍ •̀ू )", "(つд⊂)", "心塞(´-ωก`)", "(╥﹏╥)", "┭┮﹏┭┮", "（；´д｀）ゞ", "(´;︵;`)", "(。﹏。)", "┗( T﹏T )┛", "QAQ", "ヘ(_ _ヘ)", "╰（‵□′）╯", "(*￣︿￣)", ">o<", "(-`ェ´-怒)", "ヽ(‘⌒´メ)ノ", "(*｀Ω´*)v", "(｡•ˇ‸ˇ•｡)", "(怒｀Д´怒)", "٩(๑`^´๑)۶", "(;｀O´)o", "╰_╯", "(#｀皿´)<怒怒怒!!!", "<(｀^´)>", "（｀Δ´）！", "ψ(｀∇´)ψ", "(；′⌒`)", "s(・｀ヘ´・;)ゞ", "(▼皿▼#)", "￣へ￣", "←_←", "（╯‵□′）╯︵┴─┴", "（▼へ▼メ）", "☄ฺ(◣д◢)☄ฺ", "→_→", "⊙_⊙", "d(ŐдŐ๑)", "Σ( ° △ °|||)︴", "(((φ(◎ロ◎;)φ)))", "⊙▽⊙", "(๑ŐдŐ)b", "╭(°A°`)╮", "(๑òᆺó๑)", "⊙ω⊙", "Σ(っ °Д °;)っ", " (ﾟДﾟ≡ﾟдﾟ)!?", "( *・ω・)✄╰ひ╯", "(⊙x⊙;)", "┌(。Д。)┐", "(°ー°〃)", "︽⊙_⊙︽", "!!!∑(°Д°ノ)ノ", "(๑ŐдŐ)b☆d(ŐдŐ๑)", "Σ⊙▃⊙川", "ヽ(*。>Д<)o゜", "━((*′д｀)爻(′д｀*))━!!!!", "=_=", "╮(╯_╰)╭", "（︶︿︶）", "_(:з」∠)_", "@_@", "╮(╯▽╰)╭", "(＠￣ー￣＠)", "_(:3」∠❀)_", "눈_눈", "╭(╯ε╰)╮", "(ー_ー)!!", "_(:D)∠)_", "o_O", "╭(╯^╰)╮", "(；一_一)", "´_>`", "-_-#", "┑(￣Д ￣)┍", "≡￣﹏￣≡", "○|￣|_", "-_-||", "ㄟ( ▔, ▔ )ㄏ", "( ＿ ＿)ノ｜壁", "▄█▀█●"]
  combing:
    type: SINGLE
    name: "组合" #combing character
    keys: ["⃢", "꯭", "̣", "̲"  ]
  ascii:
    type: SINGLE
    name: 英文
    keys: ",.?!:;/\\|*-+=^$`'\"^~@#%&()[]{}_"
  ids:
    type: SINGLE
    name: IDS
    keys: "⿰⿱⿲⿳⿴⿵⿶⿷⿸⿹⿺⿻↷↔"
  jp:
    type: SINGLE
    name: 假名
    keys: "あいうえおかがきぎくぐけげこごさざしじすずせぜそぞただちぢつづてでとどなにぬねのはばぱひびぴふぶぷへべぺほぼぽまみむめもゃやゅゆょよらりるれろわをんアィイウェエオカガキギクグケゲコゴサザシジスズセゼソゾタダチヂツヅテデトドナニヌネノハバパヒビピフブプヘベペホボポマミムメモャヤュユョヨラリルレロワヲン"
  symbollist:
    type: SYMBOL
    name: 符号表
    keys: [ 符号: '/fh', 电脑: '/dn', 象棋: '/xq', 麻将: '/mj', 骰子: '/sz', 扑克: '/pk', 天气: '/tq', 音乐: '/yy', 八卦: '/bg', 易经: '/lssg', 天体: '/tt',  星座: '/xz',  星号: '/xh',  方块: '/fk',  几何: '/jh',  箭头: '/jt',  数学: '/sx',  上标: '/sb',  下标: '/xb',  单位: '/dw',  货币: '/hb',  拼音: '/py',  注音: '/zy',  假名: '/jm',  片假: '/pjm',  韩文: '/hw',  希腊: '/xl',  希大: '/xld', 罗马:   '/lm',  罗大:   '/lmd', 俄语:   '/ey',  俄大:   '/eyd', 表情:  '/bq',  一: '/1',  二: '/2',  三: '/3',  四: '/4',  五: '/5',  六: '/6',  七: '/7',  八: '/8',  九: '/9',  零: '/0',  十: '/10',  分数: '/fs',  标点: '/bd',  偏旁: '/pp',  竖标:  '/bdz'  ]
  

android_keys:
  # 仅供编辑键盘时参考，实际不产生任何效果
  when:
    ascii: 西文標籤
    paging: 翻頁標籤
    has_menu: 選單標籤
    composing: 輸入狀態標籤
    #always: 始終
    #hover: 滑過
    combo: 並擊
    click: 單按
    long_click: 長按
    #double_click: 雙按
    swipe_left: 左滑
    swipe_right: 右滑
    swipe_up: 上滑
    swipe_down: 下滑
  property:
    width: 寬度
    height: 高度
    gap: 間隔
    preview: 預覽
    hint: 提示
    label: 標籤
    states: 狀態標籤
    repeatable: 連續按鍵
    functional: 功能鍵
    shift_lock: Shift鎖定 #ascii_long: 英文長按中文單按鎖定, long: 長按鎖定, click: 單按鎖定
  action:
    command: 命令
    option: 參數
    select: 選擇
    toggle: 狀態
    send: 按鍵
    text: 文字
    commit: 上屏

preset_keys:
  # 安卓
  BRIGHTNESS_DOWN: {label: 亮度-, send: BRIGHTNESS_DOWN}
  BRIGHTNESS_UP: {label: 亮度+, send: BRIGHTNESS_UP}
  CALCULATOR: {label: 計算機, send: CALCULATOR}
  CALENDAR: {label: 日曆, send: CALENDAR}
  CONTACTS: {label: 電話簿, send: CONTACTS}
  ENVELOPE: {label: 信箱, send: ENVELOPE}
  EXPLORER: {label: 瀏覽器, send: EXPLORER}
  MUSIC: {label: 音樂, send: MUSIC}
  POWER: {label: 電源, send: POWER}
  SEARCH: {label: 搜尋, send: Find}
  SLEEP: {label: 休眠, send: SLEEP}
  VOICE_ASSIST: {label: 語音, send: VOICE_ASSIST}
  VOLUME_DOWN: {label: 音量-, send: VOLUME_DOWN}
  VOLUME_UP: {label: 音量+, send: VOLUME_UP}
  VOLUME_MUTE: {label: 靜音, send: VOLUME_MUTE}
  # 編輯
  Shift_L: {label: Shift, send: Shift_L, shift_lock: ascii_long}
  Return: {label: enter_labels, send: Return}
  Return1: {label: Enter, send: Return }
  Hide: {label: 隱藏, send: BACK}
  BackSpace: {label: 退格, repeatable: true, send: BackSpace}
  space: {repeatable: false, functional: false, send: space}
  Escape: {label: Esc, send: Escape}
  Home: {label: 行首, send: Home}
  Insert: {label: 插入, send: Insert}
  Delete: {label: 刪除, send: Delete}
  End: {label: 行尾, send: End}
  Page_Up: {label: 上頁, send: Page_Up}
  Page_Down: {label: 下頁, send: Page_Down}
  Left: {label: '←', send: Left}
  Down: {label: '↓', send: Down}
  Up: {label: '↑', send: Up}
  Right: {label: '→', send: Right}
  select_all: {label: 全選, send: Control+a}
  Clear: {label: 清除, text: "{Control+a}{BackSpace}"} #全選並刪除
  cut: {label: 剪下, send: Control+x}
  cut_all: {label: 全挪, text: "{Control+a}{Control+x}"} #全選並剪切
  copy: {label: 複製, send: Control+c}
  copy_all: {label: 全謄, text: "{Control+a}{Control+c}"} #全選並複製
  paste: {label: 貼上, send: Control+v}
  paste_text: {label: 貼上文本, send: Control+Shift+Alt+v} #>=Android 6.0
  share_text: {label: 分享文本, send: Control+Alt+s} #>=Android 6.0
  redo: {label: 重做, send: Control+Shift+z} #>=Android 6.0
  undo: {label: 撤銷, send: Control+z} #>=Android 6.0
  # rime組合鍵
  F4: {label: 方案選單, send: F4}
  BackToPreviousSyllable: {label: 刪音節, send: Control+BackSpace}
  CommitRawInput: {label: 編碼, send: Control+Return}
  CommitScriptText: {label: 編碼, send: Shift+Return}
  CommitComment: {label: 編碼, send: Control+Shift+Return}
  DeleteCandidate: {label: 刪詞, send: Control+Delete}
  # rime狀態
  Mode_switch: {toggle: ascii_mode, send: Mode_switch, states: [ 中文, 西文 ]}
  Zenkaku_Hankaku: {toggle: full_shape, send: Mode_switch, states: [ 半角, 全角 ]}
  Henkan: {toggle: simplification, send: Mode_switch, states: [ 漢字, 汉字 ]}
  Charset_switch: {toggle: extended_charset, send: Mode_switch, states: [ 常用, 增廣 ]}
  Punct_switch: {toggle: ascii_punct, send: Mode_switch, states: [ 。，, ．， ]}
  #切换键盘
  Keyboard_symbols: {label: 符號, send: Eisu_toggle, select: symbols}
  Keyboard_number: {label: 數字, send: Eisu_toggle, select: number}
  Keyboard_mini: {label: 迷你, send: Eisu_toggle, select: mini}
  Keyboard_letter: {label: 字母, send: Eisu_toggle, select: default}
  Keyboard_default: {label: 返回, send: Eisu_toggle, select: .default}
  Keyboard_switch: {label: 鍵盤, send: Eisu_toggle, select: .next}
  liquid_keyboard_switch: { label: 更多, send: function, command: liquid_keyboard, option: "符号表" }
  liquid_keyboard_exit: {label: 返回, send: function, command: liquid_keyboard, option: "-1"}  #退出liquidkeyboard
  liquid_keyboard_emoji: { label: 🙂, send: function, command: liquid_keyboard, option: "emoji" }
  liquid_keyboard_clipboard: { label: 剪贴, send: function, command: liquid_keyboard, option: "剪贴" }
  set_color_ink: { label: 切换到ink配色, send: function, command: set_color_scheme, option: "ink" }
  # trime設定
  IME_switch: { label: 🌐, send: LANGUAGE_SWITCH } #彈出對話框選擇輸入法
  IME_last: { label: 上一輸入法, send: LANGUAGE_SWITCH, select: .last } #直接切換到上一輸入法
  IME_next: { label: 下一輸入法, send: LANGUAGE_SWITCH, select: .next } #直接切換到下一輸入法
  Schema_switch: {label: 下一方案, send: Control+Shift+1}
  one_hand_switch_1: {toggle: _one_hand_mode_1, send: Mode_switch, states: [ 左手, 普通 ]}
  one_hand_switch_2: {toggle: _one_hand_mode_2, send: Mode_switch, states: [ 右手, 普通 ]}
  one_hand_switch_3: {toggle: _one_hand_mode_3, send: Mode_switch, states: [ 左手, 右手 ]}
  Color_switch: {label: 配色, send: PROG_RED}
  Help: {label: 說明, send: Help}
  Info: {label: 關於, send: INFO}
  Menu: {label: 方案, send: Menu}
  Settings: {label: 設定, send: SETTINGS}
  Color_settings: {label: 配色, send: SETTINGS, option: "color"}
  Theme_settings: {label: 主題, send: SETTINGS, option: "theme"}
  Schema_settings: {label: 方案, send: SETTINGS, option: "schema"}
  Candidate_switch: {toggle: _hide_candidate, send: Mode_switch, states: [ 有候選, 無候選]}
  Comment_switch: {toggle: _hide_comment, send: Mode_switch, states: [ 有註釋, 無註釋]}
  Hint_switch: {toggle: _hide_key_hint, send: Mode_switch, states: [ 有助記, 無助記]}
  # trime命令
  Date: {label: 日期, command: date, option: "yyyy-MM-dd"}
  ChineseDate: {label: 農曆, command: date, option: "zh_CN@calendar=chinese"} #農曆等日期(>=Android 7.0)：date 語言@calendar=曆法 格式。具體參見https://developer.android.com/reference/android/icu/util/Calendar.html
  Time: {label: 時間, command: date, option: "HH:mm:ss"} #時間： date 格式
  TrimeApp: {label: 同文, command: run, option: "com.osfans.trime"} #運行程序: run 包名
  TrimeCmp: {label: 同文組件, command: run, option: "com.osfans.trime/.Pref"} #運行程序指定組件: run 包名/組件名
  Homepage: {label: 同文主頁, command: run, option: "https://github.com/osfans/trime"} #查看網頁: run 網址
  CommitHomepage: {label: 同文網址, commit: https://github.com/osfans/trime} #直接上屏
  Wiki: {label: 維基, command: run, option: "https://zh.wikipedia.org/wiki/%s"} #搜索網頁: %s或者%1$s爲當前字符
  Google: {label: 谷歌, command: run, option: "https://www.google.com/search?q=%s"} #搜索網頁: %s或者%1$s爲當前字符
  MoeDict: {label: 萌典, command: run, option: "https://www.moedict.tw/%3$s"} #搜索網頁: %3$s爲光標前字符
  Baidu: {label: 百度搜索, command: run, option: "https://www.baidu.com/s?wd=%4$s"} #搜索網頁: %4s爲光標前所有字符
  Zdic: {label: 漢典, command: run, option: "http://www.zdic.net/sousuo/?q=%1$s"} #搜索網頁: %s或者%1$s爲當前字符
  Zdic2: {label: 漢典, command: run, option: "http://www.zdic.net/sousuo/?q=%2$s"} #搜索網頁: %2$s爲當前輸入的編碼
  WebSearch: {label: 搜索網頁, command: web_search, option: "%4$s"} #搜索，其他view、dial、edit、search等intent，參考安卓的intent文檔：https://developer.android.com/reference/android/content/Intent.html
  Search: {label: 搜索, command: search, option: "%1$s"} #搜索短信、字典等
  Share: {label: 分享, command: send, option: "%s"} #分享指定文本: %s或者%1$s爲當前字符
  Deploy: {label: 部署, command: broadcast, option: "com.osfans.trime.deploy"}
  Sync: {label: 同步, command: broadcast, option: "com.osfans.trime.sync"}
  RepeatCommit: { label: 重复,  command: commit, option: "%1$s" } #重复输入刚上屏的内容

preset_keyboards:
  default:
    name: 預設40鍵
    author: "osfans <waxaca@163.com>"
    ascii_mode: 0
    width: 10
    height: 44
    lock: true #切換程序時記憶鍵盤
    keys:
      - {click: '1', long_click: '!'}
      - {click: '2', long_click: '@'}
      - {click: '3', long_click: '#'}
      - {click: '4', long_click: '$'}
      - {click: '5', long_click: '%'}
      - {click: '6', long_click: '^'}
      - {click: '7', long_click: '&'}
      - {click: '8', long_click: '*'}
      - {click: '9', long_click: '('}
      - {click: '0', long_click: ')'}
      - {click: 'q', long_click: '_'}
      - {click: 'w', long_click: '-'}
      - {click: 'e', long_click: '+'}
      - {click: 'r', long_click: '='}
      - {click: 't', long_click: '|'}
      - {click: 'y', long_click: '\'}
      - {click: 'u', long_click: '['}
      - {click: 'i', long_click: ']'}
      - {click: 'o', long_click: '{'}
      - {click: 'p', long_click: '}'}
      - {click: 'a', long_click: select_all }
      - {click: 's', long_click: Home}
      - {click: 'd', long_click: End}
      - {click: 'f', long_click: Page_Up}
      - {click: 'g', long_click: Page_Down}
      - {click: 'h', long_click: Left}
      - {click: 'j', long_click: Down}
      - {click: 'k', long_click: Up}
      - {click: 'l', long_click: Right}
      - {click: ';', long_click: ':'}
      - {click: 'z', long_click: '`'}
      - {click: 'x', long_click: cut}
      - {click: 'c', long_click: copy}
      - {click: 'v', long_click: paste}
      - {click: 'b', long_click: '~'}
      - {click: 'n', long_click: Insert}
      - {click: 'm', long_click: Delete}
      - {click: ',', long_click: '<'}
      - {click: '.', long_click: '>'}
      - {click: '/', long_click: '?'}
      - {click: Shift_L}
      - {click: Keyboard_symbols, long_click: Keyboard_number}
      - {click: Mode_switch, long_click: Menu}
      - {click: space, width: 30}
      - {click: "'", long_click: '"'}
      - {click: BackSpace, width: 15}
      - {click: Return, composing: Return1, long_click: CommitComment, width: 15}
  mini:
    name: 精简键盘
    author: "tumuyan"
    ascii_mode: 0
    width: 10
    height: 44
    keyboard_height: 120
    lock: true #切換程序時記憶鍵盤
    keys:
      - {click: '1', long_click: '!'}
      - {click: '2', long_click: '@'}
      - {click: '3', long_click: '#'}
      - {click: '4', long_click: '$'}
      - {click: '5', long_click: '%'}
      - {click: '6', long_click: '^'}
      - {click: '7', long_click: '&'}
      - {click: '8', long_click: '*'}
      - {click: '9', long_click: '('}
      - {click: '0', long_click: ')'}
      - {click: Shift_L}
      - {click: Keyboard_symbols, long_click: Keyboard_number}
      - {click: "'", long_click: '"'}
      - {click: '-', long_click: '_'}
      - {click: '=', long_click: '+'}
      - {click: ',', long_click: '<'}
      - {click: '.', long_click: '>'}
      - {click: '/', long_click: '?'}
      - {click: Mode_switch, long_click: Menu}
      - {click: Return, composing: Return1, long_click: CommitComment}
  letter:
    __include: /preset_keyboards/default
    ascii_mode: 1
    reset_ascii_mode: true  #显示键盘时重置为ascii_mode指定的状态
    lock: false
  qwerty0:
    name: 預設36鍵
    author: "osfans <waxaca@163.com>"
    ascii_mode: 0
    width: 10
    height: 44
    label_transform: uppercase #uppercase|none 中文模式下的字母標籤自動大寫
    lock: true
    keys:
    - {click: '1', long_click: '!'}
    - {click: '2', long_click: '@'}
    - {click: '3', long_click: '#'}
    - {click: '4', long_click: '$'}
    - {click: '5', long_click: '%'}
    - {click: '6', long_click: '^'}
    - {click: '7', long_click: '&'}
    - {click: '8', long_click: '*'}
    - {click: '9', long_click: '('}
    - {click: '0', long_click: ')'}
    - {click: 'q', long_click: '_'}
    - {click: 'w', long_click: '-'}
    - {click: 'e', long_click: '+'}
    - {click: 'r', long_click: '='}
    - {click: 't', long_click: '|'}
    - {click: 'y', long_click: '\'}
    - {click: 'u', long_click: '['}
    - {click: 'i', long_click: ']'}
    - {click: 'o', long_click: '{'}
    - {click: 'p', long_click: '}'}
    - {width: 5}
    - {click: 'a', long_click: select_all }
    - {click: 's', long_click: Home}
    - {click: 'd', long_click: End}
    - {click: 'f', long_click: Page_Up}
    - {click: 'g', long_click: Page_Down}
    - {click: 'h', long_click: Left}
    - {click: 'j', long_click: Down}
    - {click: 'k', long_click: ':'}
    - {click: 'l', long_click: ';'}
    - {width: 5}
    - {click: Shift_L, has_menu: "'", width: 15}
    - {click: 'z', long_click: '`'}
    - {click: 'x', long_click: cut}
    - {click: 'c', long_click: copy}
    - {click: 'v', long_click: paste}
    - {click: 'b', long_click: '~'}
    - {click: 'n', long_click: '"'}
    - {click: 'm', long_click: "MoeDict"}
    - {click: BackSpace, width: 15}
    - {click: Mode_switch, long_click: Menu, width: 15}
    - {click: Keyboard_symbols, long_click: Keyboard_number}
    - {click: ',', long_click: '<'}
    - {click: space, width: 30}
    - {click: '.', long_click: '>'}
    - {click: '/', long_click: '?'}
    - {click: Return, composing: Return1, long_click: CommitComment, width: 15}
  qwerty_:
    name: 預設30鍵
    author: "osfans <waxaca@163.com>"
    ascii_mode: 0
    width: 10
    height: 55
    lock: true
    keys:
    - {click: 'q', long_click: '!', swipe_up: 1}
    - {click: 'w', long_click: '@', swipe_up: 2}
    - {click: 'e', long_click: '#', swipe_up: 3}
    - {click: 'r', long_click: '$', swipe_up: 4}
    - {click: 't', long_click: '%', swipe_up: 5}
    - {click: 'y', long_click: '^', swipe_up: 6}
    - {click: 'u', long_click: '&', swipe_up: 7}
    - {click: 'i', long_click: '*', swipe_up: 8}
    - {click: 'o', long_click: '(', swipe_up: 9}
    - {click: 'p', long_click: ')', swipe_up: 0}
    - {click: 'a', long_click: select_all, swipe_left: Left, swipe_right: Right, swipe_up: Up, swipe_down: Down}
    - {click: 's', long_click: '~', swipe_left: Home, swipe_right: End, swipe_up: Page_Up, swipe_down: Page_Down}
    - {click: 'd', long_click: '-', swipe_down: '_'}
    - {click: 'f', long_click: '+', swipe_down: '='}
    - {click: 'g', long_click: '\', swipe_down: '|'}
    - {click: 'h', long_click: '[]{Left}', swipe_left: '[', swipe_right: ']'}
    - {click: 'j', long_click: '{}{Left}', swipe_left: '{', swipe_right: '}'}
    - {click: 'k', long_click: '"'}
    - {click: 'l', long_click: "'"}
    - {click: ';', long_click: ':'}
    - {click: 'z', long_click: '`'}
    - {click: 'x', long_click: cut}
    - {click: 'c', long_click: copy}
    - {click: 'v', long_click: paste}
    - {click: 'b', long_click: Time, swipe_up: Date}
    - {click: 'n', long_click: Insert}
    - {click: 'm', long_click: Delete}
    - {click: ',', long_click: '<'}
    - {click: '.', long_click: '>'}
    - {click: '/', long_click: '?'}
    - {click: Shift_L}
    - {click: Keyboard_symbols, long_click: Keyboard_number}
    - {click: Mode_switch, long_click: Menu}
    - {click: space, width: 40}
    - {click: BackSpace, width: 15}
    - {click: Return, composing: Return1, long_click: CommitComment, width: 15}
  qwerty:
    name: 預設26鍵
    author: "osfans <waxaca@163.com>"
    ascii_mode: 0
    columns: 10 #鍵盤列數，超過則自動換行，默認30列
    width: 10
    height: 55
    lock: true
    key_symbol_offset_x: 0
    key_symbol_offset_y: 0
    key_text_offset_x: 0
    key_text_offset_y: 0
    key_hint_offset_x: 0
    key_hint_offset_y: 0
    key_press_offset_x: 2
    key_press_offset_y: 2
    keys:
    - {click: 'q', long_click: '!', swipe_up: 1}
    - {click: 'w', long_click: '@', swipe_up: 2}
    - {click: 'e', long_click: '#', swipe_up: 3}
    - {click: 'r', long_click: '$', swipe_up: 4}
    - {click: 't', long_click: '%', swipe_up: 5}
    - {click: 'y', long_click: '^', swipe_up: 6}
    - {click: 'u', long_click: '&', swipe_up: 7}
    - {click: 'i', long_click: '*', swipe_up: 8}
    - {click: 'o', long_click: '(){Left}', swipe_up: 9}
    - {click: 'p', long_click: 'Hide', swipe_up: 0}
    - {width: 5}
    - {click: 'a', long_click: select_all, swipe_left: Left, swipe_right: Right, swipe_up: Up, swipe_down: Down}
    - {click: 's', long_click: '~', swipe_left: Home, swipe_right: End, swipe_up: Page_Up, swipe_down: Page_Down}
    - {click: 'd', long_click: '-', swipe_down: '_'}
    - {click: 'f', long_click: '+', swipe_down: '='}
    - {click: 'g', long_click: '\', swipe_down: '|'}
    - {click: 'h', long_click: '[]{Left}', swipe_left: '[', swipe_right: ']'}
    - {click: 'j', long_click: '{}{Left}', swipe_left: '{', swipe_right: '}'}
    - {click: 'k', long_click: ':'}
    - {click: 'l', long_click: ';'}
    - {width: 5}
    - {click: Shift_L, send_bindings: false, width: 15}
    - {click: 'z', long_click: '`'}
    - {click: 'x', long_click: cut}
    - {click: 'c', long_click: copy}
    - {click: 'v', long_click: paste}
    - {click: 'b', long_click: Time, swipe_up: Date}
    - {click: 'n', long_click: '"'}
    - {click: 'm', long_click: "'"}
    - {click: BackSpace, swipe_left: Escape, width: 15}
    - {click: Mode_switch, long_click: Menu, width: 15}
    - {click: Keyboard_symbols, long_click: Keyboard_number}
    - {click: ',', long_click: '<'}
    - {click: space, width: 30}
    - {click: '.', long_click: '>'}
    - {click: '/', long_click: '?'}
    - {click: Return, composing: Return1, long_click: CommitComment, width: 15}
  us_intl:
    name: 美式國際
    author: "Terry Tsang <archerindigo@gmail.com>"
    ascii_mode: 1
    width: 10
    height: 44
    lock: true
    keys:
    - {click: '1', long_click: '!', swipe_up: '¡', swipe_down: '¹'}
    - {click: '2', long_click: '@', swipe_up: '²'}
    - {click: '3', long_click: '#', swipe_up: '³'}
    - {click: '4', long_click: '$', swipe_up: '¤', swipe_down: '£'}
    - {click: '5', long_click: '%', swipe_up: '€'}
    - {click: '6', long_click: '^', swipe_up: '¼'}
    - {click: '7', long_click: '&', swipe_up: '½'}
    - {click: '8', long_click: '*', swipe_up: '¾'}
    - {click: '9', long_click: '(){Left}', swipe_left: '(', swipe_right: ')', swipe_up: '‘'}
    - {click: '0', long_click: '-', swipe_down: '_', swipe_up: '’', swipe_left: '¥'}
    - {click: 'q', long_click: '~', swipe_up: 'ä'}
    - {click: 'w', long_click: '+', swipe_up: 'å'}
    - {click: 'e', long_click: '=', swipe_up: 'é'}
    - {click: 'r', long_click: '×', swipe_up: '®'}
    - {click: 't', long_click: '÷', swipe_up: 'þ'}
    - {click: 'y', long_click: '«»{Left}', swipe_left: '«', swipe_right: '»', swipe_up: 'ü'}
    - {click: 'u', long_click: '[]{Left}', swipe_left: '[', swipe_right: ']', swipe_up: 'ú'}
    - {click: 'i', long_click: '{}{Left}', swipe_left: '{', swipe_right: '}', swipe_up: 'í'}
    - {click: 'o', long_click: '\', swipe_up: 'ó'}
    - {click: 'p', long_click: '|', swipe_up: 'ö', swipe_down: '¬', swipe_left: '¦'}
    - {click: 'a', long_click: '`', swipe_up: 'á'}
    - {click: 's', swipe_up: 'ß', swipe_down: '§'}
    - {click: 'd', swipe_up: 'ð'}
    - {click: 'f', long_click: Left, swipe_left: Home, swipe_right: End, swipe_up: Page_Up, swipe_down: Page_Down}
    - {click: 'g', long_click: Up, swipe_left: Home, swipe_right: End, swipe_up: Page_Up, swipe_down: Page_Down}
    - {click: 'h', long_click: Down, swipe_left: Home, swipe_right: End, swipe_up: Page_Up, swipe_down: Page_Down}
    - {click: 'j', long_click: Right, swipe_left: Home, swipe_right: End, swipe_up: Page_Up, swipe_down: Page_Down}
    - {click: 'k'}
    - {click: 'l', swipe_up: 'ø'}
    - {click: ';', long_click: ':', swipe_up: '¶', swipe_down: '°'}
    - {click: 'z', long_click: select_all, swipe_up: 'æ'}
    - {click: 'x', long_click: cut}
    - {click: 'c', long_click: copy, swipe_up: '©', swipe_down: '¢'}
    - {click: 'v', long_click: paste}
    - {click: 'b', long_click: Insert}
    - {click: 'n', long_click: undo, swipe_up: 'ñ'}
    - {click: 'm', long_click: redo, swipe_up: 'µ'}
    - {click: ',', long_click: '<', swipe_up: 'ç'}
    - {click: '.', long_click: '>'}
    - {click: '/', long_click: '?', swipe_up: '¿'}
    - {click: Shift_L}
    - {click: Keyboard_symbols, long_click: Keyboard_number}
    - {click: Mode_switch, long_click: Menu}
    - {click: space, long_click: VOICE_ASSIST, width: 30}
    - {click: "'", long_click: '"'}
    - {click: BackSpace, swipe_right: Delete, swipe_left: Escape, width: 15}
    - {click: Return, long_click: CommitComment, width: 15}
  number:
    name: 預設數字
    author: "osfans <waxaca@163.com>"
    width: 20
    height: 44
    keys:
    - {click: '+'}
    - {click: 'KP_1'}
    - {click: 'KP_2'}
    - {click: 'KP_3'}
    - {click: '#'}
    - {click: '-'}
    - {click: 'KP_4'}
    - {click: 'KP_5'}
    - {click: 'KP_6'}
    - {click: '%'}
    - {click: '*'}
    - {click: 'KP_7'}
    - {click: 'KP_8'}
    - {click: 'KP_9'}
    - {click: ':'}
    - {click: '/'}
    - {click: '±'}
    - {click: 'KP_0'}
    - {click: '.'}
    - {click: ','}
    - {click: '='}
    - {click: Keyboard_default, long_click: Keyboard_symbols}
    - {click: space}
    - {click: BackSpace}
    - {click: Return}
  symbols:
    name: 符號
    author: "天真可愛的滿滿"
    ascii_mode: 1
    width: 10
    height: 44
    keys:
    - {click: '1'}
    - {click: '2'}
    - {click: '3'}
    - {click: '4'}
    - {click: '5'}
    - {click: '6'}
    - {click: '7'}
    - {click: '8'}
    - {click: '9'}
    - {click: '0'}
    - {click: '~',long_click: '`'}
    - {click: '!'}
    - {click: '@'}
    - {click: '#'}
    - {click: '$'}
    - {click: '￥'}
    - {click: '%'}
    - {click: '^'}
    - {click: '&'}
    - {click: '*'}
    - {click: '(', long_click: '{'}
    - {click: ')', long_click: '}'}
    - {click: '[', long_click: '【'}
    - {click: ']', long_click: '】'}
    - {click: '「', long_click: '『'}
    - {click: '」', long_click: '』'}
    - {click: '、', ascii: '\', long_click: '|'}
    - {click: '/', long_click: '√'}
    - {click: ':'}
    - {click: ';'}
    - {click: '+'}
    - {click: '-', long_click: '_'}
    - {click: '='}
    - {click: '〈', long_click: '《', ascii: '<'}
    - {click: '〉', long_click: '》', ascii: '>'}
    - {click: '“', ascii: '"', long_click: '‘'}
    - {click: '”', ascii: "'", long_click: '’'}
    - {click: '，', ascii: ',', long_click: one_hand_switch_1}
    - {click: '？', ascii: '?', long_click: one_hand_switch_3}
    - {click: BackSpace, long_click: Escape}
    - {click: Keyboard_default, long_click: Menu, width: 15}
    - {click: Keyboard_number, long_click: Color_switch}
    - {click: Keyboard_mini, long_click: Theme_settings}
    - {click: space, width: 30}
    - {click: '。', ascii: '.'}
    - {click: liquid_keyboard_switch, long_click: Delete}
    - {click: Return, long_click: select_all, width: 15}
  bopomofo:
    name: 註音鍵盤
    author: "皛筱晓小笨鱼"
    ascii_mode: 0
    ascii_keyboard: letter
    width: 10
    height: 44
    keys:
    - {label: 'ㄅ', long_click: '!', click: '1'}
    - {label: 'ㄉ', long_click: '@', click: '2'}
    - {label: 'ˇ', long_click: '#', click: '3'}
    - {label: 'ˋ', long_click: '$', click: '4'}
    - {label: 'ㄓ', long_click: '%', click: '5'}
    - {label: 'ˊ', long_click: '^', click: '6'}
    - {label: '˙', long_click: '&', click: '7'}
    - {label: 'ㄚ', long_click: '*', click: '8'}
    - {label: 'ㄞ', long_click: '(', click: '9'}
    - {label: 'ㄢ', long_click: ')', click: '0'}
    - {label: 'ㄆ', long_click: '_', click: q}
    - {label: 'ㄊ', long_click: '-', click: w}
    - {label: 'ㄍ', long_click: '+', click: e}
    - {label: 'ㄐ', long_click: '=', click: r}
    - {label: 'ㄔ', long_click: '|', click: t}
    - {label: 'ㄗ', long_click: '\', click: y}
    - {label: 'ㄧ', long_click: '[', click: u}
    - {label: 'ㄛ', long_click: ']', click: i}
    - {label: 'ㄟ', long_click: '{', click: o}
    - {label: 'ㄣ', long_click: '}', click: p}
    - {label: 'ㄇ', long_click: '`', click: a}
    - {label: 'ㄋ', long_click: Up, click: s}
    - {label: 'ㄎ', long_click: '~', click: d}
    - {label: 'ㄑ', long_click: '!', click: f}
    - {label: 'ㄕ', click: g, long_click: select_all}
    - {label: 'ㄘ', click: h, long_click: Home}
    - {label: 'ㄨ', click: j, long_click: End}
    - {label: 'ㄜ', click: k, long_click: Page_Up}
    - {label: 'ㄠ', click: l, long_click: Page_Down}
    - {label: 'ㄤ', long_click: ':', click: ';'}
    - {label: 'ㄈ', click: z, long_click: Left}
    - {label: 'ㄌ', click: x, long_click: Down}
    - {label: 'ㄏ', click: c, long_click: Right}
    - {label: 'ㄒ', click: v, long_click: cut}
    - {label: 'ㄖ', click: b, long_click: copy}
    - {label: 'ㄙ', click: n, long_click: paste}
    - {label: 'ㄩ', click: m, long_click: Insert}
    - {label: 'ㄝ', long_click: '<', click: ','}
    - {label: 'ㄡ', long_click: '>', click: '.'}
    - {label: 'ㄥ', long_click: '?', click: '/'}
    - {click: Shift_L, label: 換檔, send_bindings: false}
    - {click: Mode_switch, long_click: Menu}
    - {click: Keyboard_symbols, long_click: Keyboard_number}
    - {click: space, width: 30}
    - {label: 'ㄦ', long_click: '"', click: "-"}
    - {long_click: '。', click: '，'}
    - {click: BackSpace, long_click: Escape, width: 10}
    - {click: Return, composing: Return1, long_click: CommitComment, width: 10}
  cangjie5:
    name: 倉頡五代鍵盤
    author: "皛筱晓小笨鱼"
    ascii_mode: 0
    width: 10
    height: 55
    keys:
    - {label: '手', long_click: '_', click: q}
    - {label: '田', long_click: '-', click: w}
    - {label: '水', long_click: '+', click: e}
    - {label: '口', long_click: '=', click: r}
    - {label: '廿', long_click: '|', click: t}
    - {label: '卜', long_click: '\', click: y}
    - {label: '山', long_click: '[', click: u}
    - {label: '戈', long_click: ']', click: i}
    - {label: '人', long_click: '{', click: o}
    - {label: '心', long_click: '}', click: p}
    - {long_click: ':', click: ';'}
    - {label: '日', long_click: '`', click: a}
    - {label: '尸', long_click: Up, click: s}
    - {label: '木', long_click: '~', click: d}
    - {label: '火', long_click: '!', click: f}
    - {label: '土', long_click: '@', click: g}
    - {label: '竹', long_click: '#', click: h}
    - {label: '十', long_click: '$', click: j}
    - {label: '大', long_click: '%', click: k}
    - {label: '中', long_click: '^', click: l}
    - {long_click: '?', click: '/'}
    - {label: '符', click: z, long_click: Left}
    - {label: '難', click: x, long_click: Down}
    - {label: '金', click: c, long_click: Right}
    - {label: '女', long_click: '&', click: v}
    - {label: '月', long_click: '*', click: b}
    - {label: '弓', long_click: '(', click: n}
    - {label: '一', long_click: ')', click: m}
    - {long_click: '<', click: ','}
    - {click: BackSpace, long_click: Escape, width: 10}
    - {click: Hide}
    - {click: Shift_L, send_bindings: false}
    - {click: Keyboard_symbols, long_click: Keyboard_number}
    - {click: space, width: 40}
    - {click: Mode_switch, long_click: Menu}
    - {long_click: '>', click: '.'}
    - {click: Return, composing: Return1, long_click: CommitComment, width: 10}
  cangjie6:
    ascii_mode: 0
    name: 倉頡六代
    author: 吴琛11
    height: 44
    width: 9.7
    keys:
    - {width: 3}
    - {click: 1, long_click: "!"}
    - {click: 2, long_click: "@"}
    - {click: 3, long_click: "#"}
    - {click: 4, long_click: "$"}
    - {click: 5, long_click: "%"}
    - {click: 6, long_click: "^"}
    - {click: 7, long_click: "&"}
    - {click: 8, long_click: "*"}
    - {click: 9, long_click: "("}
    - {click: 0, long_click: ")"}
    - {width: 3}
    - {click: q, label: "手", long_click: _}
    - {click: w, label: "田", long_click: "-"}
    - {click: e, label: "水", long_click: "+"}
    - {click: r, label: "口", long_click: "="}
    - {click: t, label: "廿", long_click: "|"}
    - {click: y, label: "卜", long_click: "\\"}
    - {click: u, label: "山", long_click: "["}
    - {click: i, label: "戈", long_click: "]"}
    - {click: o, label: "人", long_click: "{"}
    - {click: p, label: "心", long_click: "}"}
    - {width: 7}
    - {click: a, label: "日", long_click: select_all}
    - {click: s, label: "尸", long_click: Home}
    - {click: d, label: "木", long_click: End}
    - {click: f, label: "火", long_click: Page_Up}
    - {click: g, label: "土", long_click: Page_Down}
    - {click: h, label: "的", long_click: Left}
    - {click: j, label: "十", long_click: Down}
    - {click: k, label: "大", long_click: Up}
    - {click: l, label: "中", long_click: Right}
    - {width: 6}
    - {width: 3}
    - {click: Shift_L, width: 13.8}
    - {click: z, label: "片", long_click: "`"}
    - {click: x, label: "止", long_click: cut}
    - {click: c, label: "金", long_click: copy}
    - {click: v, label: "女", long_click: paste}
    - {click: b, label: "月", long_click: "~"}
    - {click: n, label: "弓", long_click: '"'}
    - {click: m, label: "一", long_click: Delete}
    - {click: BackSpace, width: 13.8}
    - {width: 2}
    - {width: 3}
    - {click: Menu, long_click: Color_switch, width: 14}
    - {click: Keyboard_symbols, long_click: Keyboard_number, width: 11.5}
    - {click: ",", long_click: .}
    - {click: space, width: 25}
    - {click: "'", long_click: "?"}
    - {click: Return, composing: Return1, long_click: CommitComment, width: 25.5}
  scj6:
    __include: /preset_keyboards/cangjie5
  stroke:
    name: 五筆畫鍵盤
    author: 皛筱晓小笨鱼
    ascii_mode: 0
    width: 20
    height: 75
    keys:
    - {click: '?', long_click: '!'}
    - {click: h, label: '一'}
    - {click: s, label: '丨'}
    - {click: p, label: '丿'}
    - {click: BackSpace, long_click: Escape}
    - {click: ';', long_click: ':'}
    - {click: n, label: '丶'}
    - {click: z, label: '乙'}
    - {click: "'", label: '詞組'}
    - {click: ',', long_click: '.'}
    - {click: Hide, width: 10}
    - {click: '/', long_click: '^', width: 10}
    - {click: Keyboard_symbols, long_click: Keyboard_number, width: 10}
    - {click: space, width: 40}
    - {click: Keyboard_letter, long_click: Menu, width: 10}
    - {click: Return, composing: Return1, long_click: CommitComment, width: 20}
  telegraph:
    name: 電碼
    author: 熊貓阿Bo
    ascii_mode: 0
    width: 20
    keys:
    - {click: '@'}
    - {click: '7'}
    - {click: '8'}
    - {click: '9'}
    - {click: '、'}
    - {click: '!', label: '！'}
    - {click: '4'}
    - {click: '5'}
    - {click: '6'}
    - {click: ';', label: '；'}
    - {click: '?', label: '？'}
    - {click: '1'}
    - {click: '2'}
    - {click: '3'}
    - {click: ',', label: '，'}
    - {click: '"', label: '“”{Left}'}
    - {click: ':', label: '：'}
    - {click: '0'}
    - {click: '.', label: '。'}
    - {click: BackSpace}
    - {click: Keyboard_letter, long_click: Menu}
    - {click: space, width: 60}
    - {click: Return, composing: Return1}
  terra_pinyin:
    name: 地球拼音鍵盤
    author: 默默ㄇㄛˋ
    ascii_mode: 0
    width: 10
    height: 55
    keys:
    - {click: 'q', long_click: '_'}
    - {click: 'w', long_click: '-'}
    - {click: 'e', long_click: '+'}
    - {click: 'r', long_click: '='}
    - {click: 't', long_click: '|'}
    - {click: 'y', long_click: '^'}
    - {click: 'u', long_click: '['}
    - {click: 'i', long_click: ']'}
    - {click: 'o', long_click: '{'}
    - {click: 'p', long_click: '}'}
    - {click: 'a', long_click: '`' }
    - {click: 's', long_click: Time, swipe_up: Date}
    - {click: 'd', long_click: '~'}
    - {click: 'f', long_click: '!'}
    - {click: 'g', long_click: '@'}
    - {click: 'h', long_click: '#'}
    - {click: 'j', long_click: '$'}
    - {click: 'k', long_click: '%'}
    - {click: 'l', long_click: '>'}
    - {click: ';', long_click: ':', composing: 'ˉ', send_bindings: false}  #一聲
    - {click: 'z', long_click: cut}
    - {click: 'x', long_click: copy}
    - {click: 'c', long_click: paste}
    - {click: 'v', long_click: '&'}
    - {click: 'b', long_click: '*'}
    - {click: 'n', long_click: '('}
    - {click: 'm', long_click: ')'}
    - {click: '/', long_click: '?', composing: 'ˊ', send_bindings: false}  #二聲
    - {click: ',', long_click: '<', composing: 'ˇ', send_bindings: false}  #三聲
    - {click: BackSpace, long_click: Escape}
    - {click: Mode_switch, long_click: Menu}
    - {click: Shift_L}
    - {click: Keyboard_symbols, long_click: Keyboard_number}
    - {click: space, width: 40}
    - {click: ".", long_click: '"'}
    - {click: '\', long_click: '.', composing: 'ˋ', send_bindings: false}  #四聲
    - {click: Return, composing: Return1, long_click: CommitComment}
  array30:
    name: 行列30配美式國際
    author: "Terry Tsang <archerindigo@gmail.com>"
    ascii_mode: 1
    width: 10
    height: 44
    lock: true
    keys:
    - {click: '1', long_click: '!', swipe_up: '¡', swipe_down: '¹'}
    - {click: '2', long_click: '@', swipe_up: '²'}
    - {click: '3', long_click: '#', swipe_up: '³'}
    - {click: '4', long_click: '$', swipe_up: '¤', swipe_down: '£'}
    - {click: '5', long_click: '%', swipe_up: '€'}
    - {click: '6', long_click: '^', swipe_up: '¼'}
    - {click: '7', long_click: '&', swipe_up: '½'}
    - {click: '8', long_click: '*', swipe_up: '¾'}
    - {click: '9', long_click: '(){Left}', swipe_left: '(', swipe_right: ')', swipe_up: '‘'}
    - {click: '0', long_click: '-', swipe_down: '_', swipe_up: '’', swipe_left: '¥'}
    - {click: 'q', label: "1^", long_click: '~', swipe_up: 'ä'}
    - {click: 'w', label: "2^", long_click: '+', swipe_up: 'å'}
    - {click: 'e', label: "3^", long_click: '=', swipe_up: 'é'}
    - {click: 'r', label: "4^", long_click: '×', swipe_up: '®'}
    - {click: 't', label: "5^", long_click: '÷', swipe_up: 'þ'}
    - {click: 'y', label: "6^", long_click: '«»{Left}', swipe_left: '«', swipe_right: '»', swipe_up: 'ü'}
    - {click: 'u', label: "7^", long_click: '[]{Left}', swipe_left: '[', swipe_right: ']', swipe_up: 'ú'}
    - {click: 'i', label: "8^", long_click: '{}{Left}', swipe_left: '{', swipe_right: '}', swipe_up: 'í'}
    - {click: 'o', label: "9^", long_click: '\', swipe_up: 'ó'}
    - {click: 'p', label: "0^", long_click: '|', swipe_up: 'ö', swipe_down: '¬', swipe_left: '¦'}
    - {click: 'a', label: "1-", long_click: '`', swipe_up: 'á'}
    - {click: 's', label: "2-", swipe_up: 'ß', swipe_down: '§'}
    - {click: 'd', label: "3-", swipe_up: 'ð'}
    - {click: 'f', label: "4-", long_click: Left, swipe_left: Home, swipe_right: End, swipe_up: Page_Up, swipe_down: Page_Down}
    - {click: 'g', label: "5-", long_click: Up, swipe_left: Home, swipe_right: End, swipe_up: Page_Up, swipe_down: Page_Down}
    - {click: 'h', label: "6-", long_click: Down, swipe_left: Home, swipe_right: End, swipe_up: Page_Up, swipe_down: Page_Down}
    - {click: 'j', label: "7-", long_click: Right, swipe_left: Home, swipe_right: End, swipe_up: Page_Up, swipe_down: Page_Down}
    - {click: 'k', label: "8-"}
    - {click: 'l', label: "9-", swipe_up: 'ø'}
    - {click: ';', label: "0-", long_click: ':', swipe_up: '¶', swipe_down: '°'}
    - {click: 'z', label: "1v", long_click: select_all, swipe_up: 'æ'}
    - {click: 'x', label: "2v", long_click: cut}
    - {click: 'c', label: "3v", long_click: copy, swipe_up: '©', swipe_down: '¢'}
    - {click: 'v', label: "4v", long_click: paste}
    - {click: 'b', label: "5v", long_click: Insert}
    - {click: 'n', label: "6v", long_click: undo, swipe_up: 'ñ'}
    - {click: 'm', label: "7v", long_click: redo, swipe_up: 'µ'}
    - {click: ',', label: "8v", long_click: '<', swipe_up: 'ç'}
    - {click: '.', label: "9v", long_click: '>'}
    - {click: '/', label: "0v", long_click: '?', swipe_up: '¿'}
    - {click: Shift_L}
    - {click: Keyboard_symbols, long_click: Keyboard_number}
    - {click: Mode_switch, long_click: Menu}
    - {click: space, long_click: VOICE_ASSIST, width: 30}
    - {click: "'", long_click: '"'}
    - {click: BackSpace, swipe_right: Delete, swipe_left: Escape, width: 15}
    - {click: Return, long_click: CommitComment, width: 15}
  quick5:
    ascii_mode: 0
    name: 速成
    height: 44
    width: 9.7
    keys:
    - {width: 3}
    - {click: 1, long_click: "!"}
    - {click: 2, long_click: "@"}
    - {click: 3, long_click: "#"}
    - {click: 4, long_click: "$"}
    - {click: 5, long_click: "%"}
    - {click: 6, long_click: "^"}
    - {click: 7, long_click: "&"}
    - {click: 8, long_click: "*"}
    - {click: 9, long_click: "("}
    - {click: 0, long_click: ")"}
    - {width: 3}
    - {click: q, label: "手", long_click: _}
    - {click: w, label: "田", long_click: "-"}
    - {click: e, label: "水", long_click: "+"}
    - {click: r, label: "口", long_click: "="}
    - {click: t, label: "廿", long_click: "|"}
    - {click: y, label: "卜", long_click: "\\"}
    - {click: u, label: "山", long_click: "["}
    - {click: i, label: "戈", long_click: "]"}
    - {click: o, label: "人", long_click: "{"}
    - {click: p, label: "心", long_click: "}"}
    - {width: 7}
    - {click: a, label: "日", long_click: select_all}
    - {click: s, label: "尸", long_click: Home}
    - {click: d, label: "木", long_click: End}
    - {click: f, label: "火", long_click: Page_Up}
    - {click: g, label: "土", long_click: Page_Down}
    - {click: h, label: "竹", long_click: Left}
    - {click: j, label: "十", long_click: Down}
    - {click: k, label: "大", long_click: Up}
    - {click: l, label: "中", long_click: Right}
    - {width: 6}
    - {width: 3}
    - {click: Shift_L, width: 13.8}
    - {click: z, label: "重", long_click: "`"}
    - {click: x, label: "難", long_click: cut}
    - {click: c, label: "金", long_click: copy}
    - {click: v, label: "女", long_click: paste}
    - {click: b, label: "月", long_click: "~"}
    - {click: n, label: "弓", long_click: '"'}
    - {click: m, label: "一", long_click: Delete}
    - {click: BackSpace, width: 13.8}
    - {width: 2}
    - {width: 3}
    - {click: Menu, long_click: Color_switch, width: 14}
    - {click: Keyboard_symbols, long_click: Keyboard_number, width: 11.5}
    - {click: ",", long_click: .}
    - {click: space, width: 25}
    - {click: "'", long_click: "?"}
    - {click: Return, long_click: CommitComment, width: 25.5}

