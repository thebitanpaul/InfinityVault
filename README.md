<div align="center">

<a href="https://phiuture.com/tech">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://res.cloudinary.com/b0tb1mho/image/upload/v1794310202/ymqwl9jz0hpsmdoegmwx.png" />
    <img src="https://res.cloudinary.com/b0tb1mho/image/upload/b_black,r_24/v1794310202/ymqwl9jz0hpsmdoegmwx.png" alt="phiUture Tech" width="220" />
  </picture>
</a>

<em>Thoughtfully Engineered. Crafted for You.</em>

<br/><br/>

<img src="https://res.cloudinary.com/b0tb1mho/image/upload/v1784639185/bbuq4h2ifhnslgzeam65.webp" alt="InfinityVault icon" width="96" />

# InfinityVault

### *Transform ordinary YouTube videos into experimental cloud file storage.*

[![Watch the demo](https://img.shields.io/badge/Watch-the_demo-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtu.be/wsbZO4kmXFI)
[![Open on phiUture](https://img.shields.io/badge/Open_on-phiUture-000000?style=for-the-badge)](https://phiuture.com/tech/InfinityVault)

![status Research](https://img.shields.io/badge/status-Research-6E7781?style=flat-square)
[![license Apache 2.0](https://img.shields.io/badge/license-Apache_2.0-0A84FF?style=flat-square)](LICENSE)
![launched 2024](https://img.shields.io/badge/launched-2024-7C3AED?style=flat-square)

<br/>

<img src="https://res.cloudinary.com/b0tb1mho/image/upload/v1784634050/wceytjpwvty5jgzisr4j.webp" alt="InfinityVault — a phiUture Tech product" width="100%" />

</div>

---

## Overview

InfinityVault is a proof-of-concept research project that explores using YouTube as a large-scale file storage medium by encoding ZIP archives into video frames and reconstructing them back into their original files. It demonstrates how visual media platforms can be repurposed for unconventional data storage through binary encoding techniques.

---

## How to use

1. Install the requirements.
2. Zip everything you want to store into a single `.zip` archive, and keep only that one archive in
   the working directory.
3. Run the executable. It offers three modes: **file to video**, **video to file**, and
   **download video from YouTube**.
4. Choose *file to video*, then upload the resulting video to your YouTube channel — unlisted is a
   sensible default.
5. When you need the files back, use the download mode to fetch the video.
6. Choose *video to file* to rebuild the original archive from the downloaded video.

![InfinityVault in action](https://user-images.githubusercontent.com/86147453/221376499-1e7e894a-1d76-4d59-90ec-90ccf7fb6fd0.gif)

---

## Demo

[Watch the demo on YouTube](https://youtu.be/wsbZO4kmXFI)

<img src="https://res.cloudinary.com/b0tb1mho/image/upload/v1784634052/ul5ys2vdjzjwonctnuet.webp" alt="InfinityVault demo"/>

---

## How it works

Video platforms compress what they store, so binary mode writes each bit as a larger block of
pixels — typically 2×2 — to reduce the risk of corruption. The program is a small set of functions
that turn a file into binary, binary into video frames, and back again.

### `file_to_binary()`

Takes no parameters and returns a string of 0s and 1s representing the binary data of a `.zip`
file. It determines the file size, reads the file as binary, converts it to a string of 0s and 1s,
and returns it.

### `binary_to_video(bin_string, width=1920, height=1080, pixel_size=4, fps=24)`

<img src="https://res.cloudinary.com/b0tb1mho/image/upload/v1784634051/ybed78bbq1wporalxhh3.webp" alt="Binary data encoded as video frames"/>

Takes the binary string plus optional parameters for the size and frame rate of the video, and
returns an `.mp4` file. It calculates the total number of pixels the data needs and how many fit in
one image, then builds the frames row by row and column by column, colouring each pixel by its
binary digit. Finally the frames are written to disk as a video with MoviePy.

### `process_images(frames)`

Takes an array of frames and returns the binary string they contain. Each frame is converted to
grayscale, and each pixel's colour is read back as a binary digit; the digits are concatenated
into a single string.

### `imageToText()`

Takes no parameters, prompts for the name of the file to convert, calls `file_to_binary()`, and
stores the result in `binary.txt`.

### `binaryToFile(binary_filename)`

Takes the binary data and writes it back out as `output.zip`.

<img src="https://res.cloudinary.com/b0tb1mho/image/upload/v1784634052/ysvz0w6c16kpjl9mfflt.webp" alt="Rebuilding the original files from video"/>

Together these make a complete round trip: files to binary to video, and video back to binary to
files.

---

## Credits

InfinityVault is a Python implementation of the idea behind
[DvorakDwarf's Infinite-Storage-Glitch](https://github.com/DvorakDwarf/Infinite-Storage-Glitch),
which is written in Rust — the original is well worth a look.

---

## License

Licensed under the **Apache License 2.0** — see [`LICENSE`](LICENSE) and [`NOTICE`](NOTICE).

Copyright © 2024 Bitan Paul, phiUture. All Rights Reserved.

---

## About phiUture Tech

**InfinityVault** is built by **[phiUture Tech](https://phiuture.com/tech)** — *Thoughtfully Engineered. Crafted for You.*

phiUture Tech is the software half of **[phiUture](https://phiuture.com)** — *Technically Creative.* —
an independent studio with one vision: *Shaping the future for you through technology and creativity.*
The name is the philosophy: **φ**, the golden ratio, for craft and balance, and **U** for you — the
person every product is built around. *Thoughtfully Engineered.* means every product is designed
before it is built; *Crafted for You.* means the engineering exists so the experience feels effortless.

phiUture Tech builds AI & data products, agentic systems, automation, applications, research and
games. Its sister half, **[phiUture Studios](https://phiuture.com/studios)** — *Entertainment First.
Technology Follows.* — makes original music and film.

<div align="center">

[![Explore phiUture Tech](https://img.shields.io/badge/Explore-phiUture_Tech-000000?style=for-the-badge)](https://phiuture.com/tech)
[![YouTube @phiuture](https://img.shields.io/badge/YouTube-%40phiuture-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@phiuture)
[![GitHub thebitanpaul](https://img.shields.io/badge/GitHub-thebitanpaul-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/thebitanpaul)
[![Business email](https://img.shields.io/badge/Business-thephiuture%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:thephiuture@gmail.com)

</div>

<details>
<summary><b>Every phiUture link</b></summary>

<br/>

| Personal | Business | Artist |
|----------|----------|--------|
| [![GitHub](https://img.shields.io/badge/GitHub-thebitanpaul-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/thebitanpaul) | [![Website](https://img.shields.io/badge/Website-phiUture-000000?style=for-the-badge&logo=googlechrome&logoColor=white)](https://phiuture.com) | [![YouTube](https://img.shields.io/badge/YouTube-thebitanpaul-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@thebitanpaul) |
| [![LinkedIn](https://img.shields.io/badge/LinkedIn-thebitanpaul-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/thebitanpaul) | [![YouTube](https://img.shields.io/badge/YouTube-phiUture-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@phiuture) | [![Spotify](https://img.shields.io/badge/Spotify-1DB954?style=for-the-badge&logo=spotify&logoColor=white)](https://open.spotify.com/artist/6ghDcCBlKzJIgm3e586jpV) |
| [![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/thebitanpaul) [![Threads](https://img.shields.io/badge/Threads-000000?style=for-the-badge&logo=threads&logoColor=white)](https://www.threads.com/@thebitanpaul) | [![Google Play](https://img.shields.io/badge/Google_Play-Developer-34A853?style=for-the-badge&logo=googleplay&logoColor=white)](https://play.google.com/store/apps/dev?id=6358474525178045834&hl=en) | [![YouTube Music](https://img.shields.io/badge/YouTube_Music-FF0000?style=for-the-badge&logo=youtubemusic&logoColor=white)](https://music.youtube.com/playlist?list=OLAK5uy_km3cjEB2zl59Etcgv9UBKWw800O9G3NdE) |
| [![Facebook](https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white)](https://facebook.com/thebitanpaul) | [![Email](https://img.shields.io/badge/Business_Email-thephiuture%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:thephiuture@gmail.com) | [![Amazon Music](https://img.shields.io/badge/Amazon_Music-46C3D0?style=for-the-badge&logo=amazonmusic&logoColor=white)](https://music.amazon.com/albums/B0G52QMYDC) |
| [![X](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/thebitanpaul_) |  | [![Apple Music](https://img.shields.io/badge/Apple_Music-FA243C?style=for-the-badge&logo=applemusic&logoColor=white)](https://music.apple.com/us/artist/thebitanpaul/1858534880) |
| [![Snapchat](https://img.shields.io/badge/Snapchat-FFFC00?style=for-the-badge&logo=snapchat&logoColor=000000)](https://snapchat.com/t/UgO0Iywr) |  | [![JioSaavn](https://img.shields.io/badge/JioSaavn-2BC5B4?style=for-the-badge&logo=jiosaavn&logoColor=white)](https://www.jiosaavn.com/artist/thebitanpaul-songs/zuo0NgC65gQ_) |
| [![Email](https://img.shields.io/badge/Personal_Email-thebitanpaul%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:thebitanpaul@gmail.com) |  |  |

</details>

<br/>

<div align="center">

**phiUture Tech** · *Thoughtfully Engineered. Crafted for You.*

<sub>© 2024 phiUture · Apache License 2.0</sub>

</div>
