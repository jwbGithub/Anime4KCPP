# Anime4KCPP
This is an implementation of Anime4K in C++. It based on the [bloc97's Anime4K](https://github.com/bloc97/Anime4K) algorithm version 0.9 and some optimizations have been made, it can process both image and video.
This project is for learning and the exploration task of algorithm course in SWJTU.  

***NOTICE: Thanks for the high performance of pointer, the C++ version will be very fast. It is about 6.5 times faster than [Go version](https://github.com/TianZerL/Anime4KGo), and 650 times faster than [Python version](https://github.com/TianZerL/Anime4KPython), but please understand, this is executed in CPU, for video preprocessing, it will be slower than your expecting. Therefore, if your graphic card is good enough, I recommend you to use the real-time process version by [bloc97](https://github.com/bloc97/Anime4K).***

# About Anime4K
Anime4K is a simple high-quality anime upscale algorithm for anime. it does not use any machine learning approaches, and can be very fast in real-time processing.

# Usage
Please install [OpenCV Library](https://opencv.org) before using.  

If you want to process video, please install [ffmpeg](https://ffmpeg.org) firstly, otherwise the output will be silent.  

For video processing, all you need do is to add a argument "**-v**", and waiting. For performance, I recommend only do one pass for video processing, and don't make "**zoomFactor**" to large.

This project uses [cmake](https://cmake.org) to build.

    options:
      -i, --input               File for loading (string [=./pic/p1.png])
      -o, --output              File for outputting (string [=output.png])
      -p, --passes              Passes for processing (int [=2])
      -c, --strengthColor       Strength for pushing color,range 0 to 1,higher for thinner (double [=0.3])
      -g, --strengthGradient    Strength for pushing gradient,range 0 to 1,higher for sharper (double [=1])
      -z, --zoomFactor          zoom factor for resizing (double [=2])
      -f, --fastMode            Faster but maybe low quality
      -v, --videoMode           Video process
      -s, --preview             Preview image
      -?, --help                print this message

# Other implementations
- Python
  - [TianZerL/Anime4KPython](https://github.com/TianZerL/Anime4KPython)
- Go
  - [TianZerL/Anime4KGo](https://github.com/TianZerL/Anime4KGo)
- C#
  - [shadow578/Anime4kSharp](https://github.com/shadow578/Anime4kSharp)
  - [net2cn/Anime4KSharp](https://github.com/net2cn/Anime4KSharp)
- Java
  - [bloc97/Anime4K](https://github.com/bloc97/Anime4K)
- Rust
  - [andraantariksa/Anime4K-rs](https://github.com/andraantariksa/Anime4K-rs)