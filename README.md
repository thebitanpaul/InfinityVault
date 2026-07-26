# InfinityValut

 <img src="https://res.cloudinary.com/b0tb1mho/image/upload/v1784634050/wceytjpwvty5jgzisr4j.webp"/>

 YouTube as Cloud Storage: Store Any Files You Want

![ezgif-1-0299af809c](https://user-images.githubusercontent.com/86147453/221376499-1e7e894a-1d76-4d59-90ec-90ccf7fb6fd0.gif)

How to use
-------------
Install Requirments


1. Archive to zip all the files you will be uploading
2. Run the executable
3. It will give you three options file to video , video to file , download video from youtube select option you need and program will start executing 
4. Upload the video to your YouTube channel. You probably want to keep it up as unlisted
5. Use the download option to get the video back
6. Use the dislodge option to get your files back from the downloaded video
7. PROFIT
 

input file should be zipped (.zip) file 

keep only one zip file in same directery 



This program inspired from DvorakDwarf Infinite-Storage-Glitch 
https://github.com/DvorakDwarf/Infinite-Storage-Glitch check out his project

I dont know rust so I recreated the same project in python 

# Demo 
 [YouTube Link](https://youtu.be/wsbZO4kmXFI)

 <img src="https://res.cloudinary.com/b0tb1mho/image/upload/v1784634052/ul5ys2vdjzjwonctnuet.webp"/>

To reduce the risk of corruption, the program uses larger pixel blocks in binary mode, typically 2x2 blocks.

This program consists of several functions that allow for the conversion of files to binary format, and for the creation of videos from a file.

## file_to_binary()
This function takes no parameters and returns a string of 0's and 1's representing the binary data of a file with a .zip extension. It does this by first determining the file size and reading the file as binary data. The binary data is then converted to a string of 0's and 1's and returned.

## binary_to_video(bin_string, width=1920, height=1080, pixel_size=4, fps=24)

 <img src="https://res.cloudinary.com/b0tb1mho/image/upload/v1784634051/ybed78bbq1wporalxhh3.webp"/>

This function takes a string of binary data as bin_string and several optional parameters that determine the size and framerate of the resulting video. It returns a video file in .mp4 format. The function first calculates the total number of pixels needed to represent the binary data and the number of pixels that can fit in one image. It then creates an array of frames, each of which corresponds to one image that contains the binary data. The frames are created by iterating through each row and column of binary digits and determining the color of each pixel based on the binary digit. The frames are then added to the array of frames. Finally, the frames are used to create a video file using the MoviePy library and written to disk.

## process_images(frames)
This function takes an array of frames as input and returns a string of 0's and 1's representing the binary data contained in the frames. It does this by iterating through each frame and converting it to grayscale. It then iterates through each row and column of pixels and determines the binary digit based on the color of each pixel. The binary digits are concatenated into a single string and returned.

## imageToText()
This function takes no parameters and prompts the user to enter the name of a file to convert to binary format. It then calls the file_to_binary() function and stores the resulting binary data in a file named binary.txt.

## binaryToFile(binary_filename)
This function takes a string of binary data as binary_filename and writes it to a file named output.zip. It does this by first converting the binary data to binary format and then writing the binary data to the output file.

 <img src="https://res.cloudinary.com/b0tb1mho/image/upload/v1784634052/ysvz0w6c16kpjl9mfflt.webp"/>

Overall, this program provides a simple way to convert files to binary format and create videos from binary data, as well as convert binary data back to files.


---

## License

This project is licensed under the [Apache-2.0](LICENSE).
See the LICENSE file for full license text.

---

## About phiUture


Welcome to phiUture — Beautiful Technology. Centered Around You. Shaping Tomorrow.

Inspired by the Golden Ratio (φ), our name represents beautiful, intelligent engineering, while the "U" stands for You—placing people at the center of every solution we build.

phiUture is an AI-first software company creating intelligent products, automation systems, and modern digital experiences. This channel documents the journey of building practical AI solutions, from concept to deployment.

```text
Here you'll find:
• AI applications and product demos
• AI agents and automation workflows
• Web and mobile app showcases
• Machine Learning and Data Engineering projects
• Product launches and development insights
• UI/UX and software engineering content
• Tutorials, experiments, and future innovations
```

| Personal | Business | Artist |
|----------|----------|--------|
| [![GitHub](https://img.shields.io/badge/GitHub-thebitanpaul-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/thebitanpaul) | [![Website](https://img.shields.io/badge/Website-phiUture-000000?style=for-the-badge&logo=googlechrome&logoColor=white)](https://phiuture.com) | [![YouTube](https://img.shields.io/badge/YouTube-thebitanpaul-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@thebitanpaul) |
| [![LinkedIn](https://img.shields.io/badge/LinkedIn-thebitanpaul-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/thebitanpaul) | [![YouTube](https://img.shields.io/badge/YouTube-phiUture-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@phiuture) | [![Spotify](https://img.shields.io/badge/Spotify-1DB954?style=for-the-badge&logo=spotify&logoColor=white)](https://open.spotify.com/artist/6ghDcCBlKzJIgm3e586jpV) |
| [![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/thebitanpaul) | [![Google Play](https://img.shields.io/badge/Google_Play-Developer-34A853?style=for-the-badge&logo=googleplay&logoColor=white)](https://play.google.com/store/apps/dev?id=6358474525178045834&hl=en) | [![YouTube Music](https://img.shields.io/badge/YouTube_Music-FF0000?style=for-the-badge&logo=youtubemusic&logoColor=white)](https://music.youtube.com/playlist?list=OLAK5uy_km3cjEB2zl59Etcgv9UBKWw800O9G3NdE) |
| [![Facebook](https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white)](https://facebook.com/thebitanpaul) | [![Email](https://img.shields.io/badge/Business_Email-thephiuture%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:thephiuture@gmail.com) | [![Amazon Music](https://img.shields.io/badge/Amazon_Music-46C3D0?style=for-the-badge&logo=amazonmusic&logoColor=white)](https://music.amazon.com/albums/B0G52QMYDC) |
| [![X](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/thebitanpaul_) |  | [![Apple Music](https://img.shields.io/badge/Apple_Music-FA243C?style=for-the-badge&logo=applemusic&logoColor=white)](https://music.apple.com/us/artist/thebitanpaul/1858534880) |
| [![Snapchat](https://img.shields.io/badge/Snapchat-FFFC00?style=for-the-badge&logo=snapchat&logoColor=000000)](https://snapchat.com/t/UgO0Iywr) |  | [![JioSaavn](https://img.shields.io/badge/JioSaavn-2BC5B4?style=for-the-badge&logo=jiosaavn&logoColor=white)](https://www.jiosaavn.com/artist/thebitanpaul-songs/zuo0NgC65gQ_) |
| [![Email](https://img.shields.io/badge/Personal_Email-thebitanpaul%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:thebitanpaul@gmail.com) |  |  |



<div align="center">

**2024 · © phiUture · All Rights Reserved**

</div>
