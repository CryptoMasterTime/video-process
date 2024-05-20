# video-process

for MacOS

brew install ffmpeg


ffmpeg -i 'ssvideo 2024-05-19 11.35.02.mov' -vf "scale=1920:1080" -c:v libx264 -c:a aac -b:a 192k encoded1.mp4
ffmpeg -i 'ssvideo 2024-05-19 14.06.13.mov' -vf "scale=1920:1080" -c:v libx264 -c:a aac -b:a 192k encoded2.mp4


echo "file 'encoded1.mp4'" > input.txt
echo "file 'encoded2.mp4'" >> input.txt


ffmpeg -f concat -safe 0 -i input.txt -c copy output.mp4



This way, video editing software is not needed, and it's also very fast.
