# ffmpeg基本使用

```shell
ffmpeg -i video.webm -crf 0 video.mp4

#封装mkv
ffmpeg -i video.mp4 -i audio.m4a -map 0:0 -c:v copy -map 1:0 -c:a copy output.mkv

ffmpeg -i movie.mkv -i sub2.ass -map 0:v -map 0:a -map 1:s -c copy output.mkv 

ffmpeg -i 文件名 -map 0:a 

# 从webm提取aac
ffmpeg -i Violet Evergarden - Best OST Covers.webm -map 0:a output.aac


# 去除片头
ffmpeg -ss 00:00:37 -i video.mp4 -c copy cut.mp4



```



