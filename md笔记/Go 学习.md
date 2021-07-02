## Go 环境安装

- Homebrew 安装

  ```shell
  brew install go
  ```

  查看 go 版本信息

  ```shell
  go version
  ```

  简单测试 Go 功能

  ```shell
  mkdir GoProjects
  cd GoProjects
  touch test.go
  vim test.go
  ```

  按 i 进行输入模式，输入以下代码

  ```go
  package main
  import "fmt"
  func main() {
    fmt.Println("Hello, World!")
  }
  ```

  按 esc 进入命令模式，输入 :wq 保存并退出

  ```shell
  :wq
  ```

  使用 go 命令执行 test.go 文件

  ```shell
  go run test.go
  ```

  输出

  ```shell
  Hello, World!
  ```

  使用 go build 命令生成二进制文件 test

  ```shell
  go build test.go
  ```

  ./test 即可执行二进制文件

  ```shell
  ./test
  ```

  输出

  ```shell
  Hello, World!
  ```

  表示 go 环境正常！

  