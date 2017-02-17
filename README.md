# Xiami Music Preview Downloader
test git
A simple tool for downloading music previews from [Xiami.com][1]

second 

Note: this script requires Python 2

## Dependencies

* Optionally depends on `mutagen` module for ID3 tag support.

## Usage

    python -m xiami_downloader.cli [options]

    # Install via pip (Currently not on PyPI, so you have to download this first)
    pip install .    # Install
    xiami [options]  # Run

## Options

* `-a <album id>` Adds all songs in an album to download list.
* `-p <playlist id>` Adds all songs in a playlist to download list.
* `-s <song id>` Adds a single song to download list.
* `-f` Force mode: overwrite existing files without prompting.
* `-t urllib2|wget` Change the download tool.
* `-h` Displays usage.
* `--no-tag` Do not add ID3 tags to the downloaded files.
* `--directory` Specifies the download directory.
* `--name-template` Path for the filename template file.
* `--no-lrc-timetag` Do not add the timetag in lyrics.
* `-un <email>` Vip account email.
* `-pw <password>` Vip account password.

`<song id>`, `<playlist id>` and `<album id>` can be retrived from URLs of Xiami.

For downloading on Windows, this script will use the built-in urllib2-library. On all other OSes, it will use wget. 

The default template for the filename is set to `{id} - {title} - {artist}`. The arguments are:

* `{id}` ID
* `{title}` Title of the track
* `{artist}` Artist of the track

If you have a Vip account, the script will download tracks in 320K. Remember to set the `-un` and `-pw` arguments accordingly.
Note that Xiami has a limits the downloads. If you are downloading lots of tracks, make sure to pause between downloads.

## Example

To download the album _Mahōtsukai no Yoru OST_, first obtain the album's ID from the url:  <http://www.xiami.com/album/511682> (__511682__). Then use the following command to download the album:

    python -m xiami_downloader.cli -a 511682

## License

This software is distributed under the [MIT License][2].


---

# 虾米音乐试听下载器

从[虾米网][1]上下载音乐试听的小工具。

注：这是一个 Python 2 脚本

## 依赖

* 可选择依赖于 `mutagen` 模块，由其提供 ID3 支持。

## 使用方法

    python -m xiami_downloader.cli [options]

    # 使用 pip 安装（尚未提交 PyPI，所以需要先手动下载源码）
    pip install .    # 安装
    xiami [options]  # 运行

## 选项

* `-a <专辑ID>` 下载该专辑中的所有歌曲。
* `-p <精选集ID>` 下载该精选集中的所有歌曲。
* `-s <歌曲ID>` 下载该歌曲。
* `-f` 强制模式：不经确认直接覆盖重名文件。
* `-t urllib2|wget` 修改下载工具。
* `-h` 显示用法。
* `--no-tag` 不添加 ID3 Tag。
* `--directory` 将下载到的文件放入该文件夹中。
* `--name-template` 文件名模版。
* `--no-lrc-timetag` 去除歌词中的时间标签。
* `-un <email>` Vip账号。
* `-pw <password>` Vip账号密码。

`<歌曲ID>`、`<精选集ID>` 及 `<专辑ID>` 都可以从对应虾米页面的 URL 中找出。

默认下载工具在 Windows 上是内置的 urllib2，其它平台则是 wget。

文件名模版默认值为 `{id} - {title} - {artist}`，可选参数如下：

* `{id}` 编号
* `{title}` 该音轨的标题
* `{artist}` 该音轨的作者

如果有VIP账号，可以下载高品质320K的歌曲
虾米有高音质音乐下载限制，所以不要短时间内下一大堆歌

## 示例

例如要下载专辑《魔法使いの夜 オリジナルサウンドトラック》，首先从其 URL <http://www.xiami.com/album/511682> 中找出专辑 ID： __511682__。然后使用如下命令下载：

    python -m xiami_downloader.cli -a 511682

## 许可

Xiami Music Preview Downloader 使用 [MIT License][2] 发布。

[1]: http://www.xiami.com "虾米"
[2]: http://opensource.org/licenses/MIT "The MIT License"
