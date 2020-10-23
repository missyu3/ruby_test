## Docker コマンド

- image 作成
  - docker pull ruby:3.0.0-preview1-alpine
- コンテナ作成
  - docker run -d -it IMAGE ID
- コンテナ実行
  - docker exec -it NAMES sh
- bash のインストール

  - apk add bash

- 削除
  - コンテナ一括削除
    - docker rm -f `docker ps -a -q`
  - image 一括削除
    - docker rmi `docker images -q`

## RBS コマンド

- https://github.com/ruby/rbs/blob/master/lib/rbs/cli.rb

## 試したこと

- rbs prototype rb test.rb

  - 表示

    ```
    class Test
    def main: () -> untyped

    def hoge: (untyped huga) -> untyped
    end
    ```

### test.rb

```
class Test
  def main: () -> untyped

  def hoge: (untyped huga) -> untyped
end
bash-5.0# cat test.rb
class Test
  def main
    hoge("1")
  end

  def hoge(huga)
    huga + huga
  end
end

a = Test.new
puts a.hoge("tes")
```
