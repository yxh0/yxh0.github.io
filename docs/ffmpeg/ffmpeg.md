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
ffmpeg -ss 00:02:34 -i input.mp4 -c copy cut.mp4
ffmpeg -ss 00:04:26 -i input.mp4 -c copy cut.mp4
ffmpeg -ss 00:04:26 -i input.mp4 -t 821 -c:v copy -c:a copy output.mp4

ffmpeg -i "01 - 1.mp4" -i "01 - 1.m4a" -map 0:0 -c:v copy -map 1:0 -c:a copy "01 - 1output.mp4"

ffmpeg -i "02 - 2.mp4" -i "02 - 2.m4a" -map 0:0 -c:v copy -map 1:0 -c:a copy "02 - 2output.mp4"

ffmpeg -i "03 - 3.mp4" -i "03 - 3.m4a" -map 0:0 -c:v copy -map 1:0 -c:a copy "03 - 3output.mp4"

ffmpeg -i "04 - 4.mp4" -i "04 - 4.m4a" -map 0:0 -c:v copy -map 1:0 -c:a copy "04 - 4output.mp4"

ffmpeg -i "05 - 5.mp4" -i "05 - 5.m4a" -map 0:0 -c:v copy -map 1:0 -c:a copy in.mp4


ffmpeg -i in.mp4 -i in.ass -c copy -c:s mov_text output.mp4


```



