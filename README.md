# discord-movie-bot
Discord bot to organize movie nights

temporary thoughts:
 ffmpeg -re -i MOVIE_FILE -preset ultrafast -vcodec h264_omx -tune zerolatency -b 4000k -acodec mp3 -f flv rtmp://host:port/rtmploc/streamkey
 
 Still need to maintain aspect, omx works for rpi based streaming for hardware accel
 
aspect: -vf scale=320:-1, set width, height is autocalculated

ffmpeg -re -i MOVIE_FILE -vcodec h264_omx -b 4000k -acodec libfdk_aac -ac 2 -vf scale=1280:-2 -f flv rtmp://localhost/live
-need to use aac, flv.js doesnt properly support mp3 current, notice some artifacts, scaling params work
