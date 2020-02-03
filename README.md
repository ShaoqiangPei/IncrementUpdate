## IncrementUpdate(增量更新库)


[![](https://jitpack.io/v/ShaoqiangPei/IncrementUpdate.svg)](https://jitpack.io/#ShaoqiangPei/IncrementUpdate)

### 简介
这是一个用于做增量更新的库，服务于apk文件的下载。主要包含 `生成差量文件` 和 `合成新文件` 两个方法。

### 使用说明
#### 库引用
在你项目的`project`对应的`build.gradle`中添加如下代码：
```
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```
然后在你要使用的`module`对应的`build.gradle`中添加库依赖(以0.0.1版本为例)：
```
	dependencies {
	        implementation 'com.github.ShaoqiangPei:IncrementUpdate:0.0.1'
	}
```
#### 主要方法介绍
本库主要包含两个方法： `生成差量文件`的方法 和 `合成新文件` 的方法。
##### 1.生成差量文件
```
        /***
         * 生成差分文件的方法(生成成功返回true)
         * 
         * oldPath：旧版本apk文件路径,如：https://xxxx/xx/test_1.0.0.apk
         * newPath：新版本apk文件路径,如：https://xxxx/xx/test_2.0.0.apk
         * patchPath：生成差分文件路径,如：https://xxxx/xx/test.patch
         * 
         */
        BigNews.diff(String oldPath,String newPath,String patchPath);
```
##### 2.合成新文件
```
        /***
         * 合成新文件的方法(合成成功返回true)
         *
         * oldPath：旧版本apk文件路径,如：https://xxxx/xx/test_1.0.0.apk
         * newPath：新版本apk文件路径,如：https://xxxx/xx/test_2.0.0.apk
         * patchPath：生成差分文件路径,如：https://xxxx/xx/test.patch
         *
         */
        BigNews.make(String oldPath,String newPath,String patchPath);
```



