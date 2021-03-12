---
title: Linux常用命令之文件解/压缩
categories: DataScience
tags:
  - Linux
date: 2021-02-24  22:00:00
---

1. *.tar*

   ```Linux
   解包：tar xvf FileName.tar
   打包：tar cvf FileName.tar DirName
   ```

2. *.gz*

   ```javascript
   解压1：gunzip FileName.gz
   解压2：gzip -d FileName.gz
   压缩：gzip FileName
   ```

3. *.tar.gz///.tgz*

   ```javascript
   解压：tar zxvf FileName.tar.gz
   压缩：tar zcvf FileName.tar.gz DirName
   ```

4. *.bz2*

   ```javascript
   解压1：bzip2 -d FileName.bz2
   解压2：bunzip2 FileName.bz2
   压缩： bzip2 -z FileName
   ```

5. *.tar.bz2*

   ```javascript
   解压：tar jxvf FileName.tar.bz2
   压缩：tar jcvf FileName.tar.bz2 DirName
   ```

6. *.bz*

   ```javascript
   解压1：bzip2 -d FileName.bz
   解压2：bunzip2 FileName.bz
   ```

7. *.tar.bz*

   ```javascript
   解压：tar jxvf FileName.tar.bz
   ```

8. *.Z*

   ```javascript
   解压：uncompress FileName.Z
   压缩：compress FileName
   ```

9. *.tar.Z*

   ```javascript
   解压：tar Zxvf FileName.tar.Z
   压缩：tar Zcvf FileName.tar.Z DirName
   ```

10. *.zip*

    ```javascript
    解压：unzip FileName.zip
    压缩：zip FileName.zip DirName
    ```

11. *.rar*

    ```javascript
    解压：rar x FileName.rar
    压缩：rar a FileName.rar DirName
    ```

12. *.lha*

    ```javascript
    解压：lha -e FileName.lha
    压缩：lha -a FileName.lha FileName
    ```

13. *.rpm*

    ```javascript
    解包：rpm2cpio FileName.rpm | cpio -div
    ```

14. *.deb*

    ```javascript
    解包：ar p FileName.deb data.tar.gz | tar zxf -
    ```

    

