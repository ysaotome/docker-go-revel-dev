Dockerfile for Development using Revel Framework
=====

## Build Image

* git clone

```zsh
git clone https://github.com/ysaotome/docker-go-revel-dev
```

* docker build

```zsh
docker build --rm -t ysaotome/go-revel-dev docker-go-revel-dev
```

## Example usage

### run Development mode

```zsh
docker run -it -p 9000:9000 -v /path/to/dev:/root/go/src/dev ysaotome/go-revel-dev zsh
5ad219bfca52# revel new dev/sample
~
~ revel! http://revel.github.io
~
Your application is ready:
   /root/go/src/dev/sample

You can run it with:
   revel run dev/sample
5ad219bfca52# 
5ad219bfca52# revel run dev/sample
~
~ revel! http://revel.github.io
~
INFO  2015/05/30 09:00:28 revel.go:329: Loaded module testrunner
INFO  2015/05/30 09:00:28 revel.go:329: Loaded module static
INFO  2015/05/30 09:00:28 revel.go:206: Initialized Revel v0.12.0 (2015-03-25) for >= go1.3
INFO  2015/05/30 09:00:28 run.go:57: Running sample (dev/sample) in dev mode
INFO  2015/05/30 09:00:28 harness.go:165: Listening on :9000

```

### run Test mode

```zsh
docker run -it -p 9000:9000 -v /path/to/dev:/root/go/src/dev ysaotome/go-revel-dev zsh -c 'revel run dev/sample'
~
~ revel! http://revel.github.io
~
INFO  2015/05/30 09:04:40 revel.go:329: Loaded module testrunner
INFO  2015/05/30 09:04:40 revel.go:329: Loaded module static
INFO  2015/05/30 09:04:40 revel.go:206: Initialized Revel v0.12.0 (2015-03-25) for >= go1.3
INFO  2015/05/30 09:04:40 run.go:57: Running sample (dev/sample) in dev mode
INFO  2015/05/30 09:04:40 harness.go:165: Listening on :9000

```


* This software is released under the MIT License, see LICENSE.txt.


