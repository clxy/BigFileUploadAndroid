BigFileUploadAndroid
====================

### [☆ English](#english) ###
### [☆ 中文](#chinese) ###

<a id="english"></a>Basics
-----------------------------------
This is a example about how to use the [BigFileUploadJava](https://github.com/clxy/BigFileUploadJava) on Android.

### Preparation
Use BigFileUploadJava require a total of four jar package.
However, because Android built-in an old version of Apache HttpComponents, so we need rename all org.apache.http package names into repack.org.apache.http (or any name you like) to avoid the version conflict .

####  Here are the jars.
- repack-clxyupload.jar
- repack-httpclient-4.2.5.jar
- repack-httpcore-4.2.4.jar
- repack-httpmime-4.2.5.jar

http*.Jars are Apache HttpComponents need. repack-clxyupload.jar is BigFileUploadJava project generated.

#### If you want to make jars above by yourself.
1. Download latest HttpComponents(4.2+) from http://hc.apache.org.
2. Generate jar file from BigFileUploadJava project.
3. Amd you also need download [jarjar](https://code.google.com/p/jarjar/) too.

 Here is the jarjar rule：
```rule org.apache.http.** repack.org.apache.http.@1```
 
 Execute command(Windows) looks like：
```Batchfile
java -jar jarjar-1.4.jar process rules.txt httpclient-4.2.5.jar repack-httpclient-4.2.5.jar
java -jar jarjar-1.4.jar process rules.txt httpcore-4.2.4.jar repack-httpcore-4.2.4.jar
java -jar jarjar-1.4.jar process rules.txt httpmime-4.2.5.jar repack-httpmime-4.2.5.jar
java -jar jarjar-1.4.jar process rules.txt clxyupload.jar repack-clxyupload.jar```
  
Those content can also be found in the directory [RepackHttpClient](https://github.com/clxy/BigFileUploadAndroid/tree/master/RepackHttpClient).

* * ** * ** * ** * ** * ** * ** * ** * ** * *


<a id="chinese"></a>概要
-----------------------------------
这是个演示如何在Android上使用BigFileUploadJava的示例项目。

### 准备
使用BigFileUploadJava共需要4个jar包。
但是由于Android内置有旧版本的Apache HttpComponents，所以需要将所有org.apache.http的包名重新命名成repack.org.apache.http(或者你喜欢的任何名字)。

#### 下面是本项目中的jar包。
- repack-clxyupload.jar
- repack-httpclient-4.2.5.jar
- repack-httpcore-4.2.4.jar
- repack-httpmime-4.2.5.jar

其中，http*.jar是Apache HttpComponents所需要的。repack-clxyupload.jar是BigFileUploadJava项目生成的jar包

#### 如果你想自己制作上述jar包
1. 从hc.apache.org上自行下载最新版(4.2+)的HttpComponents。
2. 生成BigFileUploadJava项目生成的jar包。
3. 最后，还需要[jarjar](https://code.google.com/p/jarjar/)这个工具。

 jarjar的rule如下：
```rule org.apache.http.** repack.org.apache.http.@1```
 
  转换命令(Windows)如下：
```Batchfile
java -jar jarjar-1.4.jar process rules.txt httpclient-4.2.5.jar repack-httpclient-4.2.5.jar
java -jar jarjar-1.4.jar process rules.txt httpcore-4.2.4.jar repack-httpcore-4.2.4.jar
java -jar jarjar-1.4.jar process rules.txt httpmime-4.2.5.jar repack-httpmime-4.2.5.jar
java -jar jarjar-1.4.jar process rules.txt clxyupload.jar repack-clxyupload.jar```
  
上述内容也可以在目录[RepackHttpClient](https://github.com/clxy/BigFileUploadAndroid/tree/master/RepackHttpClient)中找到。