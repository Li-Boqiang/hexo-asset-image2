# 中文说明（English Follows)

使用`hexo-asset-image`插件同时使用`hexo-abbrlink`时，会导致图片路径错误。

这个插件基于`hexo-asset-image`修改，以兼容`hexo-abbrlink`插件

## 安装

```shell
npm install https://github.com/littlesevenmo/hexo-asset-image2.git --save
```

## 使用方法

与`hexo-abbrlink`一起使用，修改Hexo配置文件`__config.yml`

```yaml
post_asset_folder: true
root: /
permalink: posts/:abbrlink.html
abbrlink:
  alg: crc32  # 算法：crc16(default) and crc32
  rep: hex    # 进制：dec(default) and hex
```

目录结构

```shell
YourBlogDoc
├── image.jpg
YourBlogDoc.md
```

使用`![image description](YourBlogDoc/image.jpg)`或`![image description](D:/<Absolute_Addr>/YourBlogDoc/image.jpg)`插入图片`image.jpg`。

# English

When you use `hexo-asset-image` with `hexo-abbrlink`,  it will cause the image path to be wrong.

This plugin modified based on `hexo-asset-image` to be compatible with `hexo-abbrlink`.

## Install

```shell
npm install https://github.com/littlesevenmo/hexo-asset-image2.git --save
```

## Usage

For use with `hexo-abbrlink`, modify the Hexo configuration file `__config.yml`

```
post_asset_folder: true
root: /
permalink: posts/:abbrlink.html
abbrlink:
  alg: crc32  # Algorithm：crc16(default) and crc32
  rep: hex    # base：dec(default) and hex
```

File directory structure

```shell
YourBlogDoc
├── image.jpg
YourBlogDoc.md
```

Insert image `image.jpg` using `![image description](YourBlogDoc/image.jpg)` or `![image description](D:/<Absolute_Addr>/YourBlogDoc/image.jpg)`.
