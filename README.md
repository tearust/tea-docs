
All these md files will be compiled into static html and showing under the documetn header in teaproject.org

# Compile md files
Go to the website repo, https://github.com/tearust/website readme file explain how to compile

# How to embed an image
First, all images should be under /res folder. sub folders are ok. Images under other folder won't be converted.
```
![](../res/measured-boot.png)
```
the code above shows the image. 

Suggest to put images in subfolders for easiler maintenance. 

The absolute path in full http url is ok too. Example `![snap2](https://github.com/tearust/tea-docs/blob/main/res/deploy-data2.png?raw=true)`

For those video or image with links, see example `[![](../res/start-demo-video.jpg)](http://www.youtube.com/watch?v=6GYwrITSfJo "")`

# TEA token sign
Use [/TEA]

# Obsidian links
All obsidian links are supported use [[]] 


