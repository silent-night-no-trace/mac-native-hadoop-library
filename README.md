# mac-native-hadoop-library

## 本仓库提供了关于macos的native-hadoop-library 

## 用途
用于解决macos系统中 启动 hadoop 的 hdfs 时出现的错误 Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
详细错误如下

```java
> ./start-dfs.sh
Starting namenodes on [localhost]
Starting datanodes
Starting secondary namenodes [MacBook-Pro.local]
2024-01-13 17:04:00,232 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
```

### 使用方式
没有特殊说明的话 都是基于Intel芯片 如果使用m1 m2 m3 苹果系列的芯片可以先使用试试,如果不行的话 需要自行编译了
找到自己对应的版本 下载并解压然后 加lib/native下的文件  复制到 $HADOOP_HOME/lib/native下即可

然后可以 启动或者关闭 hdfs进行测试 或者start-all.sh / stop-all.sh

控制台没有报错 说明这个 native支持



### 说明
hadoop-2.7.3 fork from https://github.com/mingsquall/native-hadoop-library
hadoop-2.7.7 fork from https://github.com/janlle/mac-hadoop-native-lib
hadoop-2.8.5 fork from https://github.com/janlle/mac-hadoop-native-lib
hadoop-2.9.2 fork from https://github.com/janlle/mac-hadoop-native-lib
hadoop-3.1.3 fork from https://github.com/YosanHo/hadoop-native-macos
hadoop-3.2.1 fork from https://github.com/YosanHo/hadoop-native-macos



