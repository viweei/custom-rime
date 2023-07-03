# 中州韵-输入法配置

## 包含功能
1. 五笔拼音 
2. emoji 
3. 反查


## fcitx5 配置目录
```sh
~/.local/share/fcitx5/rime
```

## 安装
```sh
git clone git@github.com:viweei/rime-custom.git && cd rime-custom
mv AppleColorEmoji.ttf ~/.local/share/fonts
cp -f * ~/.local/share/fcitx5/rime

# 更新字体
fc-cache -f -v
```


## 文件结构
```sh
# 主定义文件，配置输入方案
default.custom.yaml

# emoji 输入方案
emoji_category.txt
emoji.json
emoji_word.txt

# 拼音方案-用于反查与混输
pinyin_simp.dict.yaml
pinyin_simp.schema.yaml

# 五笔方案
wubi86_jidian.custom.yaml 		# 增加 emoji
wubi86_jidian.dict.yaml			# 五笔字典
wubi86_jidian.schema.yaml		# 方案定义文件
wubi86_jidian_user.dict.yaml	# 用户字典

# 同步文件
installation.yaml
# 外观文件
weasel.custom.yaml

# emoji 字体
# 来源 https://github.com/samuelngs/apple-emoji-linux
AppleColorEmoji.ttf
```

## 参考
https://github.com/rime/home/wiki/RimeWithSchemata#rime-with-schemata
https://github.com/rime/rime-emoji/tree/master
https://github.com/KyleBing/rime-wubi86-jidian
