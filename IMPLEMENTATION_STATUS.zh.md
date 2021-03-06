
# IPFS实现状态

> 状态说明:: **青苹果🍏: 完成 : 柠檬🍋: 进展中 : 番茄🍅: 不见了 : 栗子🌰: 没有计划**

# 目录

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [API](#api)
  - [比特交换](#%E6%AF%94%E7%89%B9%E4%BA%A4%E6%8D%A2)
      - [CLI](#cli)
      - [HTTP](#http)
      - [核心](#%E6%A0%B8%E5%BF%83)
  - [块`ipfs block`](#%E5%9D%97ipfs-block)
      - [CLI](#cli-1)
      - [HTTP](#http-1)
      - [核心](#%E6%A0%B8%E5%BF%83-1)
  - [引导](#%E5%BC%95%E5%AF%BC)
      - [CLI](#cli-2)
      - [HTTP](#http-2)
      - [核心](#%E6%A0%B8%E5%BF%83-2)
  - [配置](#%E9%85%8D%E7%BD%AE)
      - [CLI](#cli-3)
      - [HTTP](#http-3)
      - [核心](#%E6%A0%B8%E5%BF%83-3)
  - [DAG](#dag)
      - [CLI](#cli-4)
      - [HTTP](#http-4)
      - [核心](#%E6%A0%B8%E5%BF%83-4)
  - [统计和诊断](#%E7%BB%9F%E8%AE%A1%E5%92%8C%E8%AF%8A%E6%96%AD)
      - [CLI](#cli-5)
      - [HTTP](#http-5)
      - [核心](#%E6%A0%B8%E5%BF%83-5)
  - [DHT](#dht)
      - [CLI](#cli-6)
      - [HTTP](#http-6)
      - [核心](#%E6%A0%B8%E5%BF%83-6)
  - [档](#%E6%A1%A3)
      - [CLI](#cli-7)
      - [HTTP](#http-7)
      - [核心](#%E6%A0%B8%E5%BF%83-7)
  - [文件存储 (IPFS包)](#%E6%96%87%E4%BB%B6%E5%AD%98%E5%82%A8-ipfs%E5%8C%85)
      - [CLI](#cli-8)
      - [HTTP](#http-8)
      - [核心](#%E6%A0%B8%E5%BF%83-8)
  - [密钥管理](#%E5%AF%86%E9%92%A5%E7%AE%A1%E7%90%86)
      - [CLI](#cli-9)
      - [HTTP](#http-9)
      - [核心](#%E6%A0%B8%E5%BF%83-9)
  - [杂](#%E6%9D%82)
      - [CLI](#cli-10)
      - [HTTP](#http-10)
      - [核心](#%E6%A0%B8%E5%BF%83-10)
  - [命名](#%E5%91%BD%E5%90%8D)
      - [CLI](#cli-11)
      - [HTTP](#http-11)
      - [核心](#%E6%A0%B8%E5%BF%83-11)
  - [目的`ipfs object`](#%E7%9B%AE%E7%9A%84ipfs-object)
      - [CLI](#cli-12)
      - [HTTP](#http-12)
      - [核心](#%E6%A0%B8%E5%BF%83-12)
  - [p2p (libp2p暴露的API)](#p2p-libp2p%E6%9A%B4%E9%9C%B2%E7%9A%84api)
      - [CLI](#cli-13)
      - [HTTP](#http-13)
      - [核心](#%E6%A0%B8%E5%BF%83-13)
  - [消瘦](#%E6%B6%88%E7%98%A6)
      - [CLI](#cli-14)
      - [HTTP](#http-14)
      - [核心](#%E6%A0%B8%E5%BF%83-14)
  - [PubSub的](#pubsub%E7%9A%84)
      - [CLI](#cli-15)
      - [HTTP](#http-15)
      - [核心](#%E6%A0%B8%E5%BF%83-15)
  - [回购](#%E5%9B%9E%E8%B4%AD)
      - [CLI](#cli-16)
      - [HTTP](#http-16)
      - [核心](#%E6%A0%B8%E5%BF%83-16)
  - [一群](#%E4%B8%80%E7%BE%A4)
      - [CLI](#cli-17)
      - [HTTP](#http-17)
      - [核心](#%E6%A0%B8%E5%BF%83-17)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# API

## 比特交换

#### CLI

| 命令                          |  Go Impl  | JS Impl |
| --------------------------- | :-----: | :-----: |
| **`ipfs ledger`**           | : 青苹果:  |  : 柠檬:  |
| `peer`                      | : 青苹果:  |  : 柠檬:  |
| **`ipfs reprovide`**        | : 青苹果:  |  : 番茄:  |
| **`ipfs bitswap stat`**     | : 青苹果:  | : 青苹果:  |
| **`ipfs bitswap unwant`**   | : 青苹果:  | : 青苹果:  |
| `key`                       | : 青苹果:  | : 青苹果:  |
| **`ipfs bitswap wantlist`** | : 青苹果:  | : 青苹果:  |
| `peer`                      | : 青苹果:  | : 青苹果:  |

#### HTTP

| 端点                                  |  Go Impl  | JS Impl |
| ----------------------------------- | :-----: | :-----: |
| **`GET /api/v0/bitswap/ledger`**    | : 青苹果:  |  : 柠檬:  |
| `arg=`                              | : 青苹果:  |  : 柠檬:  |
| **`GET /api/v0/bitswap/reprovide`** | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/bitswap/stat`**      | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/bitswap/unwant`**    | : 青苹果:  | : 青苹果:  |
| `arg=`                              | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/bitswap/wantlist`**  | : 青苹果:  | : 青苹果:  |
| `peer=`                             | : 青苹果:  | : 青苹果:  |

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## 块`ipfs block`

#### CLI

| 命令                    |  Go Impl  | JS Impl |
| --------------------- | :-----: | :-----: |
| **`ipfs block get`**  | : 青苹果:  | : 青苹果:  |
| `key`                 | : 青苹果:  | : 青苹果:  |
| **`ipfs block put`**  | : 青苹果:  | : 青苹果:  |
| `data`                | : 青苹果:  | : 青苹果:  |
| `format`              | : 青苹果:  | : 青苹果:  |
| `mhtype`              | : 青苹果:  | : 青苹果:  |
| `mhlen`               | : 青苹果:  | : 青苹果:  |
| **`ipfs block rm`**   | : 青苹果:  |  : 柠檬:  |
| `hash`                | : 青苹果:  |  : 柠檬:  |
| `force`               | : 青苹果:  |  : 柠檬:  |
| **`ipfs block stat`** | : 青苹果:  | : 青苹果:  |
| `key`                 | : 青苹果:  | : 青苹果:  |

#### HTTP

| 端点                           |  Go Impl  | JS Impl |
| ---------------------------- | :-----: | :-----: |
| **`GET /api/v0/block/get`**  | : 青苹果:  | : 青苹果:  |
| `arg=`                       | : 青苹果:  | : 青苹果:  |
| **`POST /api/v0/block/put`** | : 青苹果:  | : 青苹果:  |
| `arg=`                       | : 青苹果:  | : 青苹果:  |
| `format=`                    | : 青苹果:  | : 青苹果:  |
| `mhtype=`                    | : 青苹果:  | : 青苹果:  |
| `mhlen=`                     | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/block/rm`**   | : 青苹果:  |  : 柠檬:  |
| `arg=`                       | : 青苹果:  |  : 柠檬:  |
| `force=`                     | : 青苹果:  |  : 柠檬:  |
| **`GET /api/v0/block/stat`** | : 青苹果:  | : 青苹果:  |
| `arg=`                       | : 青苹果:  | : 青苹果:  |

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## 引导

#### CLI

| 命令                        |  Go Impl  | JS Impl |
| ------------------------- | :-----: | :-----: |
| **`ipfs bootstrap add`**  | : 青苹果:  | : 青苹果:  |
| `arg=`                    | : 青苹果:  | : 青苹果:  |
| `default=`                | : 青苹果:  | : 青苹果:  |
| **`ipfs bootstrap list`** | : 青苹果:  | : 青苹果:  |
| **`ipfs bootstrap rm`**   | : 青苹果:  | : 青苹果:  |
| `arg=`                    | : 青苹果:  | : 青苹果:  |
| `all=`                    | : 青苹果:  | : 青苹果:  |

#### HTTP

| 端点                                      |  Go Impl  | JS Impl |
| --------------------------------------- | :-----: | :-----: |
| **`GET /api/v0/bootstrap/add`**         | : 青苹果:  | : 青苹果:  |
| `arg=`                                  | : 青苹果:  | : 青苹果:  |
| `default=`                              | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/bootstrap/add/default`** | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/bootstrap/list`**        | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/bootstrap/rm`**          | : 青苹果:  | : 青苹果:  |
| `arg=`                                  | : 青苹果:  | : 青苹果:  |
| `all=`                                  | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/bootstrap/rm/all`**      | : 青苹果:  |  : 番茄:  |

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## 配置

#### CLI

| 命令                        |  Go Impl  | JS Impl |
| ------------------------- | :-----: | :-----: |
| **`ipfs config edit`**    | : 青苹果:  |  : 栗子:  |
| **`ipfs config`**         | : 青苹果:  |  : 栗子:  |
| `key`                     | : 青苹果:  | : 青苹果:  |
| `value`                   | : 青苹果:  | : 青苹果:  |
| `bool=`                   | : 青苹果:  | : 青苹果:  |
| `json=`                   | : 青苹果:  | : 青苹果:  |
| **`ipfs config replace`** | : 青苹果:  | : 青苹果:  |
| `file`                    | : 青苹果:  | : 青苹果:  |
| **`ipfs config show`**    | : 青苹果:  | : 青苹果:  |
| **`ipfs log level`**      | : 青苹果:  |  : 栗子:  |
| `subsystem`               | : 青苹果:  |  : 栗子:  |
| `level`                   | : 青苹果:  |  : 栗子:  |
| **`ipfs log ls`**         | : 青苹果:  |  : 栗子:  |
| **`ipfs log tail`**       | : 青苹果:  |  : 栗子:  |

#### HTTP

| 端点                                |  Go Impl  | JS Impl |
| --------------------------------- | :-----: | :-----: |
| **`GET /api/v0/config/edit`**     | : 青苹果:  |  : 栗子:  |
| **`POST /api/v0/config`**         | : 青苹果:  |  : 栗子:  |
| `arg1=`                           | : 青苹果:  | : 青苹果:  |
| `arg2=`                           | : 青苹果:  | : 青苹果:  |
| `bool=`                           | : 青苹果:  | : 青苹果:  |
| `json=`                           | : 青苹果:  | : 青苹果:  |
| **`POST /api/v0/config/replace`** | : 青苹果:  | : 青苹果:  |
| `arg=`                            | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/config/show`**     | : 青苹果:  | : 青苹果:  |
| **`POST /api/v0/log/level`**      | : 青苹果:  |  : 栗子:  |
| `arg1=`                           | : 青苹果:  |  : 栗子:  |
| `arg2=`                           | : 青苹果:  |  : 栗子:  |
| **`GET /api/v0/log/ls`**          | : 青苹果:  |  : 栗子:  |
| **`GET /api/v0/log/tail`**        | : 青苹果:  |  : 栗子:  |

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## DAG

> **阻止,直到以下解决: **
>
> -   <https://github.com/ipfs/js-ipfs-api/pull/534>
> -   <https://github.com/ipfs/go-ipfs/issues/3771#issue-213068794>

#### CLI

#### HTTP

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## 统计和诊断

#### CLI

| 命令                            |  Go Impl  | JS Impl |
| ----------------------------- | :-----: | :-----: |
| **`ipfs stats bitswap`**      | : 青苹果:  |  : 番茄:  |
| **`ipfs stats bw`**           | : 青苹果:  |  : 番茄:  |
| `peer`                        | : 青苹果:  |  : 番茄:  |
| `proto`                       | : 青苹果:  |  : 番茄:  |
| `poll`                        | : 青苹果:  |  : 番茄:  |
| `interval`                    | : 青苹果:  |  : 番茄:  |
| **`ipfs stats repo`**         | : 青苹果:  |  : 番茄:  |
| **`ipfs diag cmds`**          | : 青苹果:  |  : 栗子:  |
| **`ipfs diag cmds clear`**    | : 青苹果:  |  : 栗子:  |
| **`ipfs diag cmds set-time`** | : 青苹果:  |  : 栗子:  |
| `time`                        | : 青苹果:  |  : 栗子:  |
| **`ipfs diag sys`**           | : 青苹果:  |  : 栗子:  |

#### HTTP

| 端点                                   |  Go Impl  | JS Impl |
| ------------------------------------ | :-----: | :-----: |
| **`GET /api/v0/stats/bitswap`**      | : 青苹果:  |  : 番茄:  |
| **`POST /api/v0/stats/bw`**          | : 青苹果:  |  : 番茄:  |
| `peer=`                              | : 青苹果:  |  : 番茄:  |
| `proto=`                             | : 青苹果:  |  : 番茄:  |
| `poll=`                              | : 青苹果:  |  : 番茄:  |
| `interval=`                          | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/stats/repo`**         | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/diag/cmds`**          | : 青苹果:  |  : 栗子:  |
| **`GET /api/v0/diag/cmds/clear`**    | : 青苹果:  |  : 栗子:  |
| **`GET /api/v0/diag/cmds/set-time`** | : 青苹果:  |  : 栗子:  |
| `arg=`                               | : 青苹果:  |  : 栗子:  |
| **`GET /api/v0/net`**                | : 青苹果:  |  : 栗子:  |
| `vis`                                | : 青苹果:  |  : 栗子:  |
| **`GET /api/v0/sys`**                | : 青苹果:  |  : 栗子:  |

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## DHT

> **注意: **这被DHT本身的核心实施所阻止. 跟随<https://github.com/ipfs/js-ipfs/pull/856>

#### CLI

| 命令                       |  Go Impl  | JS Impl |
| ------------------------ | :-----: | :-----: |
| **`ipfs dht findpeer`**  | : 青苹果:  |  : 番茄:  |
| `peer ID`                | : 青苹果:  |  : 番茄:  |
| `verbose=`               | : 青苹果:  |  : 番茄:  |
| **`ipfs dht findprovs`** | : 青苹果:  |  : 番茄:  |
| `key`                    | : 青苹果:  |  : 番茄:  |
| `verbose=`               | : 青苹果:  |  : 番茄:  |
| `num-providers=`         | : 青苹果:  |  : 番茄:  |
| **`ipfs dht get`**       | : 青苹果:  |  : 番茄:  |
| `key`                    | : 青苹果:  |  : 番茄:  |
| `verbose=`               | : 青苹果:  |  : 番茄:  |
| **`ipfs dht provide`**   | : 青苹果:  |  : 番茄:  |
| `key`                    | : 青苹果:  |  : 番茄:  |
| `verbose=`               | : 青苹果:  |  : 番茄:  |
| `recursive=`             | : 青苹果:  |  : 番茄:  |
| **`ipfs dht put`**       | : 青苹果:  |  : 番茄:  |
| `key`                    | : 青苹果:  |  : 番茄:  |
| `value`                  | : 青苹果:  |  : 番茄:  |
| `verbose=`               | : 青苹果:  |  : 番茄:  |
| **`ipfs dht query`**     | : 青苹果:  |  : 番茄:  |
| `peer ID`                | : 青苹果:  |  : 番茄:  |
| `verbose=`               | : 青苹果:  |  : 番茄:  |

#### HTTP

| 端点                              |  Go Impl  | JS Impl |
| ------------------------------- | :-----: | :-----: |
| **`GET /api/v0/dht/findpeer`**  | : 青苹果:  |  : 番茄:  |
| `arg=`                          | : 青苹果:  |  : 番茄:  |
| `verbose=`                      | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/dht/findprovs`** | : 青苹果:  |  : 番茄:  |
| `arg=`                          | : 青苹果:  |  : 番茄:  |
| `verbose=`                      | : 青苹果:  |  : 番茄:  |
| `num-providers=`                | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/dht/get`**       | : 青苹果:  |  : 番茄:  |
| `arg=`                          | : 青苹果:  |  : 番茄:  |
| `verbose=`                      | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/dht/provide`**   | : 青苹果:  |  : 番茄:  |
| `arg=`                          | : 青苹果:  |  : 番茄:  |
| `verbose=`                      | : 青苹果:  |  : 番茄:  |
| `recursive=`                    | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/dht/put`**       | : 青苹果:  |  : 番茄:  |
| `arg1=`                         | : 青苹果:  |  : 番茄:  |
| `arg2=`                         | : 青苹果:  |  : 番茄:  |
| `verbose=`                      | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/dht/query`**     | : 青苹果:  |  : 番茄:  |
| `arg=`                          | : 青苹果:  |  : 番茄:  |
| `verbose=`                      | : 青苹果:  |  : 番茄:  |

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## 档

#### CLI

| 命令                     |  Go Impl  | JS Impl |
| ---------------------- | :-----: | :-----: |
| **`ipfs add`**         | : 青苹果:  |  : 柠檬:  |
| `file`                 | : 青苹果:  | : 青苹果:  |
| `recursive`            | : 青苹果:  | : 青苹果:  |
| `quiet`                | : 青苹果:  | : 青苹果:  |
| `quieter`              | : 青苹果:  | : 青苹果:  |
| `silent`               | : 青苹果:  | : 青苹果:  |
| `progress`             | : 青苹果:  | : 青苹果:  |
| `trickle`              | : 青苹果:  | : 青苹果:  |
| `only-hash`            | : 青苹果:  | : 青苹果:  |
| `wrap-with-directory`  | : 青苹果:  | : 青苹果:  |
| `hidden`               | : 青苹果:  |  : 番茄:  |
| `chunker`              | : 青苹果:  |  : 番茄:  |
| `pin`                  | : 青苹果:  |  : 柠檬:  |
| `raw-leaves`           | : 青苹果:  |  : 番茄:  |
| `nocopy`               | : 青苹果:  |  : 番茄:  |
| `fscache`              | : 青苹果:  |  : 番茄:  |
| `cid-version`          | : 青苹果:  |  : 番茄:  |
| `hash`                 | : 青苹果:  |  : 番茄:  |
| **`ipfs cat`**         | : 青苹果:  | : 青苹果:  |
| `arg`                  | : 青苹果:  | : 青苹果:  |
| **`ipfs ls`**          | : 青苹果:  |  : 柠檬:  |
| `arg`                  | : 青苹果:  |  : 柠檬:  |
| `headers`              | : 青苹果:  |  : 柠檬:  |
| `resolve-type`         | : 青苹果:  |  : 柠檬:  |
| **`ipfs file ls`**     | : 青苹果:  |  : 栗子:  |
| `path`                 | : 青苹果:  |  : 栗子:  |
| **`ipfs files cp`**    | : 青苹果:  |  : 番茄:  |
| `src`                  | : 青苹果:  |  : 番茄:  |
| `dst`                  | : 青苹果:  |  : 番茄:  |
| `flush`                | : 青苹果:  |  : 番茄:  |
| **`ipfs files flush`** | : 青苹果:  |  : 番茄:  |
| `path`                 | : 青苹果:  |  : 番茄:  |
| **`ipfs files ls`**    | : 青苹果:  |  : 番茄:  |
| `path`                 | : 青苹果:  |  : 番茄:  |
| `level`                | : 青苹果:  |  : 番茄:  |
| `flush`                | : 青苹果:  |  : 番茄:  |
| **`ipfs files mkdir`** | : 青苹果:  |  : 番茄:  |
| `path`                 | : 青苹果:  |  : 番茄:  |
| `parents`              | : 青苹果:  |  : 番茄:  |
| `flush`                | : 青苹果:  |  : 番茄:  |
| **`ipfs files mv`**    | : 青苹果:  |  : 番茄:  |
| `src`                  | : 青苹果:  |  : 番茄:  |
| `dst`                  | : 青苹果:  |  : 番茄:  |
| `flush`                | : 青苹果:  |  : 番茄:  |
| **`ipfs files read`**  | : 青苹果:  |  : 番茄:  |
| `path`                 | : 青苹果:  |  : 番茄:  |
| `offset`               | : 青苹果:  |  : 番茄:  |
| `count`                | : 青苹果:  |  : 番茄:  |
| `flush`                | : 青苹果:  |  : 番茄:  |
| **`ipfs files rm`**    | : 青苹果:  |  : 番茄:  |
| `path`                 | : 青苹果:  |  : 番茄:  |
| `recursive`            | : 青苹果:  |  : 番茄:  |
| `flush`                | : 青苹果:  |  : 番茄:  |
| **`ipfs files stat`**  | : 青苹果:  |  : 番茄:  |
| `path`                 | : 青苹果:  |  : 番茄:  |
| `flush`                | : 青苹果:  |  : 番茄:  |
| **`ipfs files write`** | : 青苹果:  |  : 番茄:  |
| `path`                 | : 青苹果:  |  : 番茄:  |
| `data`                 | : 青苹果:  |  : 番茄:  |
| `offset`               | : 青苹果:  |  : 番茄:  |
| `create`               | : 青苹果:  |  : 番茄:  |
| `truncate`             | : 青苹果:  |  : 番茄:  |
| `count`                | : 青苹果:  |  : 番茄:  |
| `flush`                | : 青苹果:  |  : 番茄:  |
| **`ipfs get`**         | : 青苹果:  | : 青苹果:  |
| `path`                 | : 青苹果:  | : 青苹果:  |
| `archive`              | : 青苹果:  |  : 番茄:  |
| `compress`             | : 青苹果:  |  : 番茄:  |
| `compression-level`    | : 青苹果:  |  : 番茄:  |

#### HTTP

| 端点                             |  Go Impl  | JS Impl |
| ------------------------------ | :-----: | :-----: |
| **`POST /api/v0/add`**         | : 青苹果:  |  : 柠檬:  |
| `arg=`                         | : 青苹果:  | : 青苹果:  |
| `recursive=`                   | : 青苹果:  | : 青苹果:  |
| `quiet=`                       | : 青苹果:  |  : 番茄:  |
| `quieter=`                     | : 青苹果:  |  : 番茄:  |
| `silent=`                      | : 青苹果:  |  : 番茄:  |
| `progress=`                    | : 青苹果:  | : 青苹果:  |
| `trickle=`                     | : 青苹果:  | : 青苹果:  |
| `only-hash=`                   | : 青苹果:  | : 青苹果:  |
| `wrap-with-directory`          | : 青苹果:  | : 青苹果:  |
| `hidden`                       | : 青苹果:  |  : 番茄:  |
| `chunker`                      | : 青苹果:  |  : 番茄:  |
| `pin`                          | : 青苹果:  |  : 柠檬:  |
| `raw-leaves`                   | : 青苹果:  |  : 番茄:  |
| `nocopy`                       | : 青苹果:  |  : 番茄:  |
| `fscache`                      | : 青苹果:  |  : 番茄:  |
| `cid-version`                  | : 青苹果:  |  : 番茄:  |
| `hash`                         | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/cat`**          | : 青苹果:  | : 青苹果:  |
| `arg=`                         | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/ls`**           | : 青苹果:  |  : 柠檬:  |
| `arg=`                         | : 青苹果:  |  : 柠檬:  |
| `headers=`                     | : 青苹果:  |  : 柠檬:  |
| `resolve-type=`                | : 青苹果:  |  : 柠檬:  |
| **`GET /api/v0/file/ls`**      | : 青苹果:  |  : 栗子:  |
| `arg=`                         | : 青苹果:  |  : 栗子:  |
| **`GET /api/v0/files/cp`**     | : 青苹果:  |  : 番茄:  |
| `arg=`                         | : 青苹果:  |  : 番茄:  |
| `arg2=`                        | : 青苹果:  |  : 番茄:  |
| `flush=,f=`                    | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/files/flush`**  | : 青苹果:  |  : 番茄:  |
| `arg=`                         | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/files/ls`**     | : 青苹果:  |  : 番茄:  |
| `arg=`                         | : 青苹果:  |  : 番茄:  |
| `l=`                           | : 青苹果:  |  : 番茄:  |
| `flush=,f=`                    | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/files/mkdir`**  | : 青苹果:  |  : 番茄:  |
| `arg=`                         | : 青苹果:  |  : 番茄:  |
| `parents=,p=`                  | : 青苹果:  |  : 番茄:  |
| `flush=,f=`                    | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/files/mv`**     | : 青苹果:  |  : 番茄:  |
| `arg=`                         | : 青苹果:  |  : 番茄:  |
| `arg2=`                        | : 青苹果:  |  : 番茄:  |
| `flush=,f=`                    | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/files/read`**   | : 青苹果:  |  : 番茄:  |
| `arg=`                         | : 青苹果:  |  : 番茄:  |
| `offset=,o=`                   | : 青苹果:  |  : 番茄:  |
| `count=,n=`                    | : 青苹果:  |  : 番茄:  |
| `flush=,f=`                    | : 青苹果:  |  : 番茄:  |
| **`POST /api/v0/files/rm`**    | : 青苹果:  |  : 番茄:  |
| `arg=`                         | : 青苹果:  |  : 番茄:  |
| `recursive=,r=`                | : 青苹果:  |  : 番茄:  |
| `flush=,f=`                    | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/files/stat`**   | : 青苹果:  |  : 番茄:  |
| `arg=`                         | : 青苹果:  |  : 番茄:  |
| `flush=,f=`                    | : 青苹果:  |  : 番茄:  |
| **`POST /api/v0/files/write`** | : 青苹果:  |  : 番茄:  |
| `arg=`                         | : 青苹果:  |  : 番茄:  |
| `arg2=`                        | : 青苹果:  |  : 番茄:  |
| `offset=,o=`                   | : 青苹果:  |  : 番茄:  |
| `create=,e=`                   | : 青苹果:  |  : 番茄:  |
| `truncate=,t=`                 | : 青苹果:  |  : 番茄:  |
| `count=,n=`                    | : 青苹果:  |  : 番茄:  |
| `flush=,f=`                    | : 青苹果:  |  : 番茄:  |
| **`POST /api/v0/get`**         | : 青苹果:  | : 青苹果:  |
| `arg=`                         | : 青苹果:  | : 青苹果:  |
| `archive=`                     | : 青苹果:  |  : 番茄:  |
| `compress=`                    | : 青苹果:  |  : 番茄:  |
| `compression-level=-1`         | : 青苹果:  |  : 番茄:  |
| `compression-level=0`          | : 青苹果:  |  : 番茄:  |
| `compression-level=1`          | : 青苹果:  |  : 番茄:  |
| `compression-level=2`          | : 青苹果:  |  : 番茄:  |
| `compression-level=3`          | : 青苹果:  |  : 番茄:  |
| `compression-level=4`          | : 青苹果:  |  : 番茄:  |
| `compression-level=5`          | : 青苹果:  |  : 番茄:  |
| `compression-level=6`          | : 青苹果:  |  : 番茄:  |
| `compression-level=7`          | : 青苹果:  |  : 番茄:  |
| `compression-level=8`          | : 青苹果:  |  : 番茄:  |
| `compression-level=9`          | : 青苹果:  |  : 番茄:  |

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## 文件存储 (IPFS包) 

> **注意: **目前还没有计划在js-ipfs中实现. 

#### CLI

#### HTTP

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## 密钥管理

#### CLI

| 命令                    |  Go Impl  | JS Impl |
| --------------------- | :-----: | :-----: |
| **`ipfs key gen`**    | : 青苹果:  |  : 栗子:  |
| `name`                | : 青苹果:  |  : 栗子:  |
| `type=`               | : 青苹果:  |  : 栗子:  |
| `size=`               | : 青苹果:  |  : 栗子:  |
| **`ipfs key list`**   | : 青苹果:  |  : 栗子:  |
| `l=`                  | : 青苹果:  |  : 栗子:  |
| **`ipfs key rename`** | : 青苹果:  |  : 栗子:  |
| `name`                | : 青苹果:  |  : 栗子:  |
| `newName`             | : 青苹果:  |  : 栗子:  |
| `force=`              | : 青苹果:  |  : 栗子:  |
| **`ipfs key rm`**     | : 青苹果:  |  : 栗子:  |
| `name`                | : 青苹果:  |  : 栗子:  |
| `l=`                  | : 青苹果:  |  : 栗子:  |

#### HTTP

| 端点                           |  Go Impl  | JS Impl |
| ---------------------------- | :-----: | :-----: |
| **`GET /api/v0/key/gen`**    | : 青苹果:  |  : 栗子:  |
| `arg=`                       | : 青苹果:  |  : 栗子:  |
| `type=`                      | : 青苹果:  |  : 栗子:  |
| `size=`                      | : 青苹果:  |  : 栗子:  |
| **`GET /api/v0/key/list`**   | : 青苹果:  |  : 栗子:  |
| `l=`                         | : 青苹果:  |  : 栗子:  |
| **`GET /api/v0/key/rename`** | : 青苹果:  |  : 栗子:  |
| `arg=`                       | : 青苹果:  |  : 栗子:  |
| `arg=`                       | : 青苹果:  |  : 栗子:  |
| `force=`                     | : 青苹果:  |  : 栗子:  |
| **`GET /api/v0/key/rm`**     | : 青苹果:  |  : 栗子:  |
| `arg=`                       | : 青苹果:  |  : 栗子:  |
| `l=`                         | : 青苹果:  |  : 栗子:  |

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## 杂

#### CLI

| 命令                  |  Go Impl  | JS Impl |
| ------------------- | :-----: | :-----: |
| **`ipfs ping`**     | : 青苹果:  |  : 柠檬:  |
| `peer ID`           | : 青苹果:  |  : 番茄:  |
| `count`             | : 青苹果:  |  : 番茄:  |
| **`ipfs update`**   |  : 栗子:  |  : 栗子:  |
| **`ipfs version`**  | : 青苹果:  | : 青苹果:  |
| **`ipfs commands`** | : 青苹果:  | : 青苹果:  |
| **`ipfs id`**       | : 青苹果:  | : 青苹果:  |
| `peerid`            | : 青苹果:  |  : 番茄:  |
| `aver`              | : 青苹果:  |  : 番茄:  |
| `pver`              | : 青苹果:  |  : 番茄:  |
| `pubkey`            | : 青苹果:  |  : 番茄:  |
| `addrs`             | : 青苹果:  |  : 番茄:  |
| **`ipfs mount`**    | : 青苹果:  |  : 栗子:  |
| `ipfs-path=`        | : 青苹果:  |  : 栗子:  |
| `ipns-path=`        | : 青苹果:  |  : 栗子:  |
| **`ipfs mount`**    | : 青苹果:  |  : 栗子:  |

#### HTTP

| 端点                         |  Go Impl  | JS Impl |
| -------------------------- | :-----: | :-----: |
| **`GET /api/v0/ping`**     | : 青苹果:  |  : 柠檬:  |
| `arg=`                     | : 青苹果:  |  : 番茄:  |
| `count=`                   | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/update`**   |  : 栗子:  |  : 栗子:  |
| **`GET /api/v0/version`**  | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/commands`** | : 青苹果:  | : 青苹果:  |
| **`POST /api/v0/id`**      | : 青苹果:  | : 青苹果:  |
| `arg=`                     | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/mount`**    | : 青苹果:  |  : 栗子:  |
| `ipfs-path=`               | : 青苹果:  |  : 栗子:  |
| `ipns-path=`               | : 青苹果:  |  : 栗子:  |
| **`GET /api/v0/mount`**    | : 青苹果:  |  : 栗子:  |

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## 命名

> **注意: **在DHT完成之前,js-ipfs中的实现将被阻止. 

#### CLI

| 命令                      |  Go Impl  | JS Impl |
| ----------------------- | :-----: | :-----: |
| **`ipfs name publish`** | : 青苹果:  |  : 番茄:  |
| `ipfs-path`             | : 青苹果:  |  : 番茄:  |
| `resolve=`              | : 青苹果:  |  : 番茄:  |
| `lifetime=`             | : 青苹果:  |  : 番茄:  |
| `ttl=`                  | : 青苹果:  |  : 番茄:  |
| `key=`                  | : 青苹果:  |  : 番茄:  |
| **`ipfs name resolve`** | : 青苹果:  |  : 番茄:  |
| `name`                  | : 青苹果:  |  : 番茄:  |
| `recursive=`            | : 青苹果:  |  : 番茄:  |
| `nocache=`              | : 青苹果:  |  : 番茄:  |
| **`ipfs resolve`**      | : 青苹果:  |  : 番茄:  |
| `name`                  | : 青苹果:  |  : 番茄:  |
| `recursive=`            | : 青苹果:  |  : 番茄:  |
| **`ipfs dns`**          | : 青苹果:  |  : 番茄:  |
| `domain`                | : 青苹果:  |  : 番茄:  |
| `recursive=`            | : 青苹果:  |  : 番茄:  |

#### HTTP

| 端点                              |  Go Impl  | JS Impl |
| ------------------------------- | :-----: | :-----: |
| **`POST /api/v0/name/publish`** | : 青苹果:  |  : 番茄:  |
| `arg=`                          | : 青苹果:  |  : 番茄:  |
| `resolve=`                      | : 青苹果:  |  : 番茄:  |
| `lifetime=`                     | : 青苹果:  |  : 番茄:  |
| `ttl=`                          | : 青苹果:  |  : 番茄:  |
| `key=`                          | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/name/resolve`**  | : 青苹果:  |  : 番茄:  |
| `arg=`                          | : 青苹果:  |  : 番茄:  |
| `recursive=`                    | : 青苹果:  |  : 番茄:  |
| `nocache=`                      | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/resolve`**       | : 青苹果:  |  : 番茄:  |
| `arg=`                          | : 青苹果:  |  : 番茄:  |
| `recursive=`                    | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/dns`**           | : 青苹果:  |  : 番茄:  |
| `arg=`                          | : 青苹果:  |  : 番茄:  |
| `recursive=`                    | : 青苹果:  |  : 番茄:  |

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## 目的`ipfs object`

#### CLI

| 端点                                         |  Go Impl  | JS Impl |
| ------------------------------------------ | :-----: | :-----: |
| **`ipfs object data`**                     | : 青苹果:  | : 青苹果:  |
| `key`                                      | : 青苹果:  | : 青苹果:  |
| **`ipfs object diff`**                     | : 青苹果:  |  : 番茄:  |
| `key1`                                     | : 青苹果:  |  : 番茄:  |
| `key2`                                     | : 青苹果:  |  : 番茄:  |
| **`ipfs object/get`**                      | : 青苹果:  | : 青苹果:  |
| `key`                                      | : 青苹果:  | : 青苹果:  |
| `encoding`                                 | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/object/links`**             | : 青苹果:  | : 青苹果:  |
| `key`                                      | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/object/new`**               | : 青苹果:  | : 青苹果:  |
| `template`                                 | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/object/patch/append-data`** | : 青苹果:  | : 青苹果:  |
| `root`                                     | : 青苹果:  | : 青苹果:  |
| `data`                                     | : 青苹果:  | : 青苹果:  |
| **`POST /api/v0/object/patch/add-link`**   | : 青苹果:  | : 青苹果:  |
| `root`                                     | : 青苹果:  | : 青苹果:  |
| `name`                                     | : 青苹果:  | : 青苹果:  |
| `ref`                                      | : 青苹果:  |  : 柠檬:  |
| `create`                                   | : 青苹果:  |  : 番茄:  |
| **`POST /api/v0/object/patch/rm-link`**    | : 青苹果:  | : 青苹果:  |
| `root`                                     | : 青苹果:  | : 青苹果:  |
| `link`                                     | : 青苹果:  | : 青苹果:  |
| **`POST /api/v0/object/patch/set-data`**   | : 青苹果:  | : 青苹果:  |
| `root`                                     | : 青苹果:  | : 青苹果:  |
| `data`                                     | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/object/put`**               | : 青苹果:  | : 青苹果:  |
| `data`                                     | : 青苹果:  | : 青苹果:  |
| `inputenc`                                 | : 青苹果:  | : 青苹果:  |
| `datafieldenc`                             | : 青苹果:  |  : 番茄:  |
| `pin`                                      | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/object/stat`**              | : 青苹果:  | : 青苹果:  |
| `root`                                     | : 青苹果:  | : 青苹果:  |

#### HTTP

| 端点                                         |  Go Impl  | JS Impl |
| ------------------------------------------ | :-----: | :-----: |
| **`GET /api/v0/object/data`**              | : 青苹果:  | : 青苹果:  |
| `arg=`                                     | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/object/diff`**              | : 青苹果:  |  : 番茄:  |
| `arg1=`                                    | : 青苹果:  |  : 番茄:  |
| `arg2=`                                    | : 青苹果:  |  : 番茄:  |
| **`POST /api/v0/object/get`**              | : 青苹果:  | : 青苹果:  |
| `arg=`                                     | : 青苹果:  | : 青苹果:  |
| `encoding=json,enc=json`                   | : 青苹果:  | : 青苹果:  |
| `encoding=protobuf,enc=protobuf`           | : 青苹果:  | : 青苹果:  |
| `encoding=xml,enc=xml`                     | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/object/links`**             | : 青苹果:  | : 青苹果:  |
| `arg=`                                     | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/object/new`**               | : 青苹果:  | : 青苹果:  |
| `arg=unixfs-dir`                           | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/object/patch/append-data`** | : 青苹果:  | : 青苹果:  |
| `arg1=`                                    | : 青苹果:  | : 青苹果:  |
| `arg2=`                                    | : 青苹果:  | : 青苹果:  |
| **`POST /api/v0/object/patch/add-link`**   | : 青苹果:  | : 青苹果:  |
| `arg1=`                                    | : 青苹果:  | : 青苹果:  |
| `arg2=`                                    | : 青苹果:  | : 青苹果:  |
| `arg3=`                                    | : 青苹果:  | : 青苹果:  |
| `create=`                                  | : 青苹果:  | : 青苹果:  |
| **`POST /api/v0/object/patch/rm-link`**    | : 青苹果:  | : 青苹果:  |
| `arg1=`                                    | : 青苹果:  | : 青苹果:  |
| `arg2=`                                    | : 青苹果:  | : 青苹果:  |
| **`POST /api/v0/object/patch/set-data`**   | : 青苹果:  | : 青苹果:  |
| `arg1=`                                    | : 青苹果:  | : 青苹果:  |
| `arg2=`                                    | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/object/put`**               | : 青苹果:  | : 青苹果:  |
| `arg=`                                     | : 青苹果:  | : 青苹果:  |
| `inputenc`                                 | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/object/stat`**              | : 青苹果:  | : 青苹果:  |
| `arg=`                                     | : 青苹果:  | : 青苹果:  |

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## p2p (libp2p暴露的API) 

> **在被正式化之前,这将被阻止`interface-libp2p`**. 目前,js-ipfs直接暴露libp2p,而go-ipfs暴露了使用libp2p的命令子集. 

#### CLI

#### HTTP

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## 消瘦

#### CLI

| 命令                    |  Go Impl  | JS Impl |
| --------------------- | :-----: | :-----: |
| **`ipfs pin add`**    | : 青苹果:  |  : 柠檬:  |
| `hash`                | : 青苹果:  |  : 柠檬:  |
| `recursive`           | : 青苹果:  |  : 柠檬:  |
| `progress`            | : 青苹果:  |  : 番茄:  |
| **`ipfs pin ls`**     | : 青苹果:  |  : 柠檬:  |
| `type`                | : 青苹果:  |  : 柠檬:  |
| `quiet`               | : 青苹果:  |  : 柠檬:  |
| **`ipfs pin rm`**     | : 青苹果:  |  : 柠檬:  |
| `hash`                | : 青苹果:  |  : 柠檬:  |
| `recursive`           | : 青苹果:  |  : 柠檬:  |
| **`ipfs pin update`** | : 青苹果:  |  : 番茄:  |
| `hash`                | : 青苹果:  |  : 番茄:  |
| `unpin`               | : 青苹果:  |  : 番茄:  |
| **`ipfs pin verify`** | : 青苹果:  |  : 番茄:  |
| `verbose`             | : 青苹果:  |  : 番茄:  |
| **`ipfs refs`**       | : 青苹果:  |  : 番茄:  |
| `hash`                | : 青苹果:  |  : 番茄:  |
| `format`              | : 青苹果:  |  : 番茄:  |
| `edges`               | : 青苹果:  |  : 番茄:  |
| `unique`              | : 青苹果:  |  : 番茄:  |
| `recursive`           | : 青苹果:  |  : 番茄:  |
| **`ipfs refs local`** | : 青苹果:  |  : 番茄:  |

#### HTTP

| 端点                            |  Go Impl  | JS Impl |
| ----------------------------- | :-----: | :-----: |
| **`GET /api/v0/pin/add`**     | : 青苹果:  |  : 柠檬:  |
| `arg=`                        | : 青苹果:  |  : 柠檬:  |
| `recursive=`                  | : 青苹果:  |  : 柠檬:  |
| **`POST /api/v0/pin/ls`**     | : 青苹果:  |  : 柠檬:  |
| `type=`                       | : 青苹果:  |  : 番茄:  |
| `quiet=`                      | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/pin/rm`**      | : 青苹果:  |  : 番茄:  |
| `arg=`                        | : 青苹果:  |  : 番茄:  |
| `recursive=`                  | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/pin/update`**  | : 青苹果:  |  : 番茄:  |
| `arg=`                        | : 青苹果:  |  : 番茄:  |
| `unpin=`                      | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/pin/verify`**  | : 青苹果:  |  : 番茄:  |
| `verbose=`                    | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/refs`**        | : 青苹果:  |  : 番茄:  |
| `arg=`                        | : 青苹果:  |  : 番茄:  |
| `format=`                     | : 青苹果:  |  : 番茄:  |
| `edges=`                      | : 青苹果:  |  : 番茄:  |
| `unique=`                     | : 青苹果:  |  : 番茄:  |
| `recursive=`                  | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0//refs/local`** | : 青苹果:  |  : 番茄:  |

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## PubSub的

#### CLI

| 命令                      |  Go Impl  | JS Impl |
| ----------------------- | :-----: | :-----: |
| **`ipfs pubsub ls`**    | : 青苹果:  | : 青苹果:  |
| **`ipfs pubsub peers`** | : 青苹果:  | : 青苹果:  |
| `topic`                 | : 青苹果:  | : 青苹果:  |
| **`ipfs pubsub pub`**   | : 青苹果:  | : 青苹果:  |
| `topic`                 | : 青苹果:  | : 青苹果:  |
| `data`                  | : 青苹果:  | : 青苹果:  |
| **`ipfs pubsub sub`**   | : 青苹果:  | : 青苹果:  |
| `topic`                 | : 青苹果:  | : 青苹果:  |
| `discover`              | : 青苹果:  |  : 番茄:  |

#### HTTP

| 端点                             |  Go Impl  | JS Impl |
| ------------------------------ | :-----: | :-----: |
| **`GET /api/v0/pubsub/ls`**    | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/pubsub/peers`** | : 青苹果:  | : 青苹果:  |
| `arg=`                         | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/pubsub/pub`**   | : 青苹果:  | : 青苹果:  |
| `arg=`                         | : 青苹果:  | : 青苹果:  |
| `arg=`                         | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/pubsub/sub`**   | : 青苹果:  | : 青苹果:  |
| `arg=`                         | : 青苹果:  | : 青苹果:  |
| `discover=`                    | : 青苹果:  | : 青苹果:  |

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## 回购

#### CLI

| 命令                      |  Go Impl  | JS Impl |
| ----------------------- | :-----: | :-----: |
| **`ipfs repo fsck`**    | : 青苹果:  |  : 栗子:  |
| **`ipfs repo gc`**      | : 青苹果:  |  : 番茄:  |
| **`ipfs repo stat`**    | : 青苹果:  |  : 番茄:  |
| **`ipfs repo verify`**  | : 青苹果:  |  : 栗子:  |
| **`ipfs repo version`** | : 青苹果:  | : 青苹果:  |

#### HTTP

| 端点                             |  Go Impl  | JS Impl |
| ------------------------------ | :-----: | :-----: |
| **`GET /api/v0/repo/fsck`**    | : 青苹果:  |  : 栗子:  |
| **`GET /api/v0/repo/gc`**      | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/repo/stat`**    | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/repo/verify`**  | : 青苹果:  |  : 栗子:  |
| **`GET /api/v0/repo/version`** | : 青苹果:  | : 青苹果:  |

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *

## 一群

#### CLI

| 命令                            |  Go Impl  | JS Impl |
| ----------------------------- | :-----: | :-----: |
| **`ipfs swarm addrs`**        | : 青苹果:  | : 青苹果:  |
| **`ipfs swarm addrs listen`** | : 青苹果:  |  : 番茄:  |
| **`ipfs swarm addrs local`**  | : 青苹果:  | : 青苹果:  |
| `id=`                         | : 青苹果:  |  : 番茄:  |
| **`ipfs swarm connect`**      | : 青苹果:  | : 青苹果:  |
| `arg=`                        | : 青苹果:  | : 青苹果:  |
| **`ipfs swarm disconnect`**   | : 青苹果:  | : 青苹果:  |
| `arg=`                        | : 青苹果:  | : 青苹果:  |
| **`ipfs swarm filters`**      | : 青苹果:  |  : 番茄:  |
| **`ipfs swarm filters add`**  | : 青苹果:  |  : 番茄:  |
| `arg=`                        | : 青苹果:  |  : 番茄:  |
| **`ipfs swarm filters rm`**   | : 青苹果:  |  : 番茄:  |
| `arg=`                        | : 青苹果:  |  : 番茄:  |
| **`ipfs swarm peers`**        | : 青苹果:  | : 青苹果:  |
| `verbose=`                    | : 青苹果:  |  : 番茄:  |
| `latency=`                    | : 青苹果:  |  : 番茄:  |
| `streams=`                    | : 青苹果:  |  : 番茄:  |

#### HTTP

| 端点                                   |  Go Impl  | JS Impl |
| ------------------------------------ | :-----: | :-----: |
| **`GET /api/v0/swarm/addrs`**        | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/swarm/addrs/listen`** | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/swarm/addrs/local`**  | : 青苹果:  | : 青苹果:  |
| `id=`                                | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/swarm/connect`**      | : 青苹果:  | : 青苹果:  |
| `arg=`                               | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/swarm/disconnect`**   | : 青苹果:  | : 青苹果:  |
| `arg=`                               | : 青苹果:  | : 青苹果:  |
| **`GET /api/v0/swarm/filters`**      | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/swarm/filters/add`**  | : 青苹果:  |  : 番茄:  |
| `arg=`                               | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/swarm/filters/rm`**   | : 青苹果:  |  : 番茄:  |
| `arg=`                               | : 青苹果:  |  : 番茄:  |
| **`GET /api/v0/swarm/peers`**        | : 青苹果:  | : 青苹果:  |
| `verbose=`                           | : 青苹果:  |  : 番茄:  |
| `latency=`                           | : 青苹果:  |  : 番茄:  |
| `streams=`                           | : 青苹果:  |  : 番茄:  |

#### 核心

看到[接口IPF问题核心](https://github.com/ipfs/interface-ipfs-core). 

* * *
