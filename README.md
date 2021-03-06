# ffmpeg-video-joiner-script

## Description:
Batch script for searching and joining video segments into a single video. Developed for **itleague.kharkov.ua** needs.

## How it works
The script uses a source path as a starting point. It goes through folders inside the source path, searches all video files inside that folders, sets them in time order, join them into single video (each folder - separate video) and save the result into an output folder.

## Dependencies:
ffmpeg - https://ffmpeg.org/download.html

Download the library, unpack it whereever you want and add the path to the `ffmpeg/bin` directory to the **PATH** variable.

## Usage:
`ffmpeg-video-joiner path/to/source/folder` - uses passed path as a source

`ffmpeg-video-joiner .` - (dot in the end) uses current folder as a source

You can add the path to the `ffmpeg-video-joiner-script.bat` file to the PATH variable, then copy the `join.bat` file to your source folder, and then just run it there.

## Example:
There is a source folder with 3 other folders:

![](https://github.com/sergeyvdovareize/ffmpeg-video-joiner-script/blob/master/screens/screen1.png)

Each folder has video parts:

![](https://github.com/sergeyvdovareize/ffmpeg-video-joiner-script/blob/master/screens/screen2.png)

Run the scipt with the source folder as a parameter:

![](https://github.com/sergeyvdovareize/ffmpeg-video-joiner-script/blob/master/screens/screen3.png)

As a result we have 3 joined videos inside an output folder:

![](https://github.com/sergeyvdovareize/ffmpeg-video-joiner-script/blob/master/screens/screen4.png)

## Known issues:

ffmpeg doesn't work with some specific symbols in names, for example `'`.
