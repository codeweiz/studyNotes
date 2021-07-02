- 安装 maven

  ```shell
  brew install maven
  ```

- 安装 openjdk@11

  ```shell
  brew install openjdk@11
  ```

- 替换 maven 的 JAVA_HOME

  ```shell
  cd /opt/homebrew/Cellar/maven/3.8.1/bin
  vim mvn
  ```

  - 替换JAVA_HOME

    ```shell
    JAVA_HOME:-/opt/homebrew/Cellar/openjdk@11/11.0.10/libexec/openjdk.jdk/Contents/Home
    ```

    按 esc 进入命令行模式，输入 :wq! 强制保存退出

    ```shell
    :wq!
    ```

- 查看 maven 的信息

    ```shell
    mvn -v
    ```

    Java Version 为 11.0.10 即可

    ```shell
    Apache Maven 3.8.1 (05c21c65bdfed0f71a2f2ada8b84da59348c4c5d)
    Maven home: /opt/homebrew/Cellar/maven/3.8.1/libexec
    Java version: 11.0.10, vendor: Oracle Corporation, runtime: /opt/homebrew/Cellar/openjdk@11/11.0.10/libexec/openjdk.jdk/Contents/Home
    Default locale: zh_CN_#Hans, platform encoding: UTF-8
    OS name: "mac os x", version: "11.4", arch: "aarch64", family: "mac"
    ```

- 安装 zookeeper

  ```shell
  brew install --build-from-source zookeeper
  ```

  一般卡在 mvn，稍作等待即可

- 安装 kafka

  ```shell
  brew install --build-from-source kafka
  ```

- 启动/关闭 zookeeper（background mode）推荐

  ```shell
  brew services start zookeeper
  
  brew services stop zookeeper
  ```

- 启动/关闭 zookeeper（session mode）

  ```shell
  zkServer start
  
  zkServer stop
  ```

- 启动/关闭 kafka（background mode）推荐

  ```shell
  brew services start kafka
  
  brew services stop kafka
  ```

- 启动/关闭 kafka（session mode）

  ```shell
  zookeeper-server-start -daemon /opt/homebrew/etc/kafka/zookeeper.properties & kafka-server-start /opt/homebrew/etc/kafka/server.properties
  
  zookeeper-server-stop -daemon /opt/homebrew/etc/kafka/zookeeper.properties & kafka-server-start /opt/homebrew/etc/kafka/server.properties
  ```

  