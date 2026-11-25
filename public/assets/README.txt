frames/f001.webp ... f152.webp - the scroll animation (extracted from the original garlic video).
pack-500g.jpg  pack-1kg.jpg  pack-5kg.jpg  pack-10kg.jpg - photos of your packs.
To change the animation: ffmpeg -i new.mp4 -vf "select='not(mod(n\,4))',scale=960:-2" -vsync vfr -c:v libwebp -quality 70 frames/f%03d.webp
then set NF in public/index.html to the number of frames.
