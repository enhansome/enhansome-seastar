# Awesome Seastar with stars

A curated list of resources related to [Seastar](http://seastar.io), an industrial-grade C++ framework for building high-performance servers.

## News

* What's new in Seastar (infrequently released)
  * [Issue 1 - Apr '23](https://makedist.com/posts/2023/04/30/whats-new-in-seastar-issue-1/)
  * [Issue 2 - Dec '23](https://makedist.com/posts/2023/12/01/whats-new-in-seastar-issue-2/)
  * [Issue 3 - Apr '24](https://makedist.com/posts/2024/04/22/whats-new-in-seastar-issue-3/)
  * [Issue 4 - Sep '24](https://makedist.com/posts/2024/08/31/whats-new-in-seastar-issue-4/)

## Building with Bazel

The official build system of Seastar is CMake. But now Seastar can now be brought into a Bazel project using this <https://registry.bazel.build/modules/seastar>. It's as easy as adding this to your `MODULE.bazel`:

```
bazel_dep(name = "seastar", version = "25.08.0-20250807194611-1520326e6032")
```

You'll still need to install several system dependencies, but this set should reduce over time. This is receipe was contributed by [Redpanda](https://github.com/redpanda-data/redpanda) ⭐ 12,465 | 🐛 590 | 🌐 C++ | 📅 2026-08-22 which has now officially moved to a 100% Bazel build.

## Projects

*Systems and projects using Seastar*

* [Ceph](https://github.com/ceph/ceph) ⭐ 16,954 | 🐛 1,261 | 🌐 C++ | 📅 2026-08-22 - Distributed storage system for object, block, and file
  * The seastar-based storage engine is called [Crimson](https://github.com/ceph/ceph/tree/master/src/crimson) ⭐ 16,954 | 🐛 1,261 | 🌐 C++ | 📅 2026-08-22
* [Scylladb](https://github.com/scylladb/scylla) ⭐ 15,719 | 🐛 3,568 | 🌐 C++ | 📅 2026-08-22 - Replacement for Apache Cassandra and Amazon DynamoDB
* [Redpanda](https://github.com/redpanda-data/redpanda/) ⭐ 12,465 | 🐛 590 | 🌐 C++ | 📅 2026-08-22 - Replacement for Apache Kafka designed for modern hardware
* [Pedis/1store](https://github.com/fastio/1store) ⭐ 1,329 | 🐛 26 | 🌐 C++ | 📅 2019-10-02 - Replacement for Redis written in Seastar
* [SMF](https://github.com/smfrpc/smf) ⭐ 761 | 🐛 33 | 🌐 C++ | 📅 2023-04-12 - RPC framework built for microseconds latencies using Seastar
* [CPV](https://github.com/cpv-project/cpv-framework) ⭐ 121 | 🐛 17 | 🌐 C++ | 📅 2023-06-22 - Web framework written in C++ and Seastar
* [Hiactor](https://github.com/alibaba/hiactor) ⭐ 119 | 🐛 6 | 🌐 C++ | 📅 2024-06-14 - Hiactor is a distributed actor framework.
* [RageDB](https://github.com/ragedb/ragedb) ⭐ 51 | 🐛 22 | 🌐 C++ | 📅 2026-07-13 - In Memory Property Graph Server using the Shared Nothing design from Seastar
* [Chogori](https://github.com/futurewei-cloud/chogori-platform) ⚠️ Archived - Low-latency distributed OLTP database
* [Parquet4Seastar](https://github.com/michoecho/parquet4seastar) ⭐ 16 | 🐛 3 | 🌐 C++ | 📅 2020-07-31 - Parquet file format implementation for use in Seastar projects
* [Shredder](https://github.com/utah-scs/shredder) ⭐ 12 | 🐛 1 | 🌐 C++ | 📅 2020-07-10 - Research prototype for [SoCC '19 paper](https://www.cs.utah.edu/~lifeifei/papers/shredder.pdf) embedding v8 in Seastar
  * [nanoservices](https://github.com/utah-scs/nanoservices) ⭐ 8 | 🐛 7 | 🌐 C++ | 📅 2025-07-31 - Some relationship to [Shredder](https://github.com/utah-scs/shredder) ⭐ 12 | 🐛 1 | 🌐 C++ | 📅 2020-07-10
* [SpiderDB](https://github.com/chungphb/spiderdb) ⭐ 9 | 🐛 6 | 🌐 C++ | 📅 2021-07-06 - An on-disk key-value database based on a b-link tree
* [ministun](https://github.com/nguyenminh-phuc/ministun) ⭐ 3 | 🐛 0 | 🌐 C++ | 📅 2022-03-23 - RFC 8489 STUN server
* [mithril](https://github.com/salahsheikh/mithril) ⭐ 2 | 🐛 0 | 🌐 C++ | 📅 2021-04-05 Client-server framework inspired by Netty
* [Lightbits](https://www.youtube.com/watch?v=kWfhVaeY2BE) - Lightbits LightOS

## Learning

*Resources for learning Seastar*

* [Official tutorial](https://github.com/scylladb/seastar/blob/master/doc/tutorial.md) ⭐ 9,341 | 🐛 571 | 🌐 C++ | 📅 2026-08-19 - a comprehensive tutorial from the creators of Seastar
* [Seabrute](https://github.com/VictorDenisov/seabrute) ⭐ 3 | 🐛 0 | 🌐 C++ | 📅 2017-11-03 - a selfstudy project for learning seastar by implementing distributed password bruteforce
* [Seastar internals](https://makedist.com/projects/seastar-internals/) - is a series of deep dives into various Seastar components
* [Asynchronous Programming with Seastar](http://nadav.harel.org.il/seastar/) - is a series of tutorials covering Seastar compnents
* [Rolling your own MOM](https://dev.to/cppchedy/rolling-out-your-own-mom-or-how-i-did-it-general-introduction-3j20) - a series documenting the MOZA middleware

## Archived

These appear to no longer exist :(

* [seastar-kafka-client](https://github.com/haaawk/seastar-kafka-client) - A seastar-based kafka client

## Contributors

<!-- prettier-ignore-start -->

<!-- markdownlint-disable -->

<table>
  <tr>
    <td align="center"><a href="https://twitter.com/cppchedy"><img src="https://avatars.githubusercontent.com/u/18627131?s=100&v=3" width="100px;" alt=""/><br/><sub><b>Chedy Najjar</b></sub></a></td>
    <td align="center"><a href="https://twitter.com/dotnwat"><img src="https://avatars.githubusercontent.com/u/242417?s=100&v=3" width="100px;" alt=""/><br/><sub><b>Noah Watkins</b></sub></a></td>
  </tr>
</table>
<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-08-22._
