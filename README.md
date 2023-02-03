# KukajTo Downloader - get a direct url to a video or subtitle file

This program can find the direct url of a video or subtitle file from `film.kukaj.io` or `serial.kukaj.io`, which can be used for downloading the video or opening the vlc network stream.

## How to use

- Clone repository `git clone https://github.com/jurajhonsch/kukajto-downloader.git`
- Download chrome latest version
- Install requirements (`selenium4`, `argparse`) `python3 -m pip install -r requirements.txt`
- Go to https://kukaj.io/ and find film or episode.
- Copy url (e.g https://film.kukaj.io/matrix) and paste into program.
- Run `python3 kukajto-downloader.py https://film.kukaj.io/matrix`
- The results are in format `<url of video>,<url of subtitles if any>`

## Examples

Get the direct url of a video and subtitle file (if any) of Matrix

`python3 kukajto-downloader.py https://film.kukaj.io/matrix`

Specify language (english) by copying the link from flag icon (make sure you are on streamtape source)

`python3 kukajto-downloader.py https://film.kukaj.io/matrix/1?lng=EN`

Specify language (english) and subtitle (english) by combinig the url params from flag icon and subtitle button (make sure you are on streamtape source)

`python3 kukajto-downloader.py https://film.kukaj.io/avatar/1?subs=1&lng=EN`

Get multiple urls of video and subtitle files (if any) at once.

`python3 kukajto-downloader.py https://film.kukaj.io/matrix/1?lng=EN https://film.kukaj.io/avatar/1?subs=1&lng=EN`

You can output the results to the file.

`python3 kukajto-downloader.py https://film.kukaj.io/matrix > output.txt`

Special arguments to chrome driver

`python3 kukajto-downloader.py https://film.kukaj.io/matrix -a="start-maximized" -a="--disable-extensions"`

## TODO

- Support other sources (netu.tv, mixdrop.co)

## License

This program is released under MIT License.

## Credits

In my project I used following icons:
 - [kukajto](https://kukaj.io) favicon 228x228 [icon](https://kukaj.io/img/icons/228x228.png)
 - [flaticon](https://flaticon.com) icons [download file icon](https://www.flaticon.com/free-icons/download-file)