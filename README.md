# GoSearch

Search the Go packages for [pkg.go.dev](https://pkg.go.dev/) via command-line. It supports all search options in [Search Help](https://pkg.go.dev/search-help).

## Installation

```
go get github.com/mingrammer/gosearch
```

## Usage

Basic search.

```
$ gosearch fastjson
```

You can query with multiple search words.

```
$ gosearch logging zero alloc
```

Use `-n` option to see more. (default: 10)

```
$ gosearch -n 20 redis
```

Use `-e` option to search for an exact match.

```
$ gosearch -e go cloud
```

Use `-o` option to combine searches. It will search for each word and combine their results.

```
$ gosearch -o json yaml
```

## Example

Search the mux packages with `gosearch mux`.

```shell
$ gosearch mux
mux (v1.8.0)
├ github.com/gorilla/mux
├ Package mux implements a request router and dispatcher.
└ Published: Jul 11, 2020 | Imported by: 37,568 | License: BSD-3-Clause

mux (v0.27.2)
├ k8s.io/apiserver/pkg/server/mux
├ Package mux contains abstractions for http multiplexing of APIs.
└ Published: May 18, 2023 | Imported by: 214 | License: Apache-2.0

grace (v1.12.3)
├ github.com/astaxie/beego/grace
├ Package grace use to hot reload Description: http://grisha.org/blog/2014/06/03/graceful-restart-in-golang/ Usage: import( "log" "net/http" "os" "github.com/astaxie/beego/grace" ) func handler(w http.ResponseWriter, r *http.Request) { w.Write([]byte("WORLD!")) } func main() { mux := http.NewServeMux() mux.HandleFunc("/hello", handler) err := grace.ListenAndServe("localhost:8080", mux) if err != nil { log.Println(err) } log.Println("Server on 8080 stopped") os.Exit(0) }
└ Published: Nov  3, 2020 | Imported by: 201 | License: Apache-2.0

mux (v0.0.0-...-b2dd784)
├ github.com/containous/mux
├ Package mux implements a request router and dispatcher.
└ Published: Jun 27, 2022 | Imported by: 656 | License: BSD-3-Clause

web (v1.0.1)
├ github.com/zenazn/goji/web
├ Package web provides a fast and flexible middleware stack and mux.
└ Published: Jun  2, 2019 | Imported by: 856 | License: MIT

otelmux (v0.42.0)
├ go.opentelemetry.io/contrib/instrumentation/github.com/gorilla/mux/otelmux
├ Package otelmux instruments the github.com/gorilla/mux package.
└ Published: May 23, 2023 | Imported by: 91 | License: Apache-2.0

traffic (v0.5.3)
├ github.com/pilu/traffic
├ Package traffic - a Sinatra inspired regexp/pattern mux for Go.
└ Published: Jul 11, 2014 | Imported by: 208 | License: MIT

mux (v2.2.8)
├ github.com/luraproject/lura/v2/router/mux
├ Package mux provides some basic implementations for building routers based on net/http mux
└ Published: today | Imported by: 22 | License: Apache-2.0

mux (v1.51.0)
├ gopkg.in/DataDog/dd-trace-go.v1/contrib/gorilla/mux
├ Package mux provides tracing functions for tracing the gorilla/mux package (https://github.com/gorilla/mux).
└ Published: May 24, 2023 | Imported by: 24 | License: Apache-2.0, BSD-3-Clause

mux (v2.9.1)
├ github.com/micro/go-micro/v2/util/mux
├ Package mux provides proxy muxing
└ Published: Jul  3, 2020 | Imported by: 6 | License: Apache-2.0
```
