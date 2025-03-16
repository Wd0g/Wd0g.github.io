---
date: '2025-02-02T22:06:36+08:00'
draft: false
title: 'Apache Module for Linux'
categories:
  - Code
tags:
  - Apache
---

## 目的

使用c/cpp开发linux平台下的apache模块，实现拦截任意请求，并返回自定义内容。

## 背景：apache运行和模块相关流程

## 实现
```cpp
#include "httpd.h"
#include "http_config.h"
#include "http_protocol.h"
#include "http_request.h"

static int my_handler(request_rec *r) {
    ap_set_content_type(r, "text/html");
    ap_rputs("Hello, World!", r);
    return OK;
}
```


## 总结