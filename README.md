# btlet

通过实现BT协议族中的部分协议来完成一些toolkit

* [DHT-Spider](#DHT-Spider)

## Install

```
$ go get -v github.com/neoql/btlet
```

## Dependences

* [willf/bloom](https://github.com/willf/bloom)

## Modules

### DHT-Spider

运行截图

![](./screenshot/btsniffer.png)

> Example

下面是一个简单的爬虫例子，[这里](./example/btsniffer)是完整的Demo

```go
package main

import (
    "github.com/neoql/btlet"
)

func main() {
    s := btlet.NewSniffer()
    s.Run()
    
    for meta := range s.MetaChan() {
        println(meta)
    }
}
```

## License

MIT, read more [here](./LICENSE).
