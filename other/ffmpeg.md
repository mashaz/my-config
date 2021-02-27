## FFMPEG NOTE

### concat videos

```
ffmpeg -f concat -i file.txt -c copy output.mp4
```

### trim video

```
ffmpeg -ss 00:00:10 -i "$FILE" -vcodec copy -acodec copy "trim.$FILE"

ffmpeg -i $FILE -ss 00:00:03 -t 00:00:08 -async 1 $FILE.mp4

ffmpeg -i concat:"1.mp4|2.mp4" -c copy dest.mp4
```

### transcoding

```
ffmpeg -i $FILE -vcodec copy -acodec copy $FILE.mp4

ffmpeg -i $FILE -c:v libx264 -crf 23 $FILE.mp4
```

### merge

```
ffmpeg -i audio.m4a -i video.mp4  -y dest.mp4

```