# Release Notes

- 2.0.8
  - Bumped log4j-core from 2.17.0 to 2.17.1
  - Bumped netty from 4.1.71 to 4.1.72
  - Bumped slf4j from 1.7.30 to 1.7.32

- 2.0.7
  - Bumped log4j-core from 2.16.0 to 2.17.0

- 2.0.6
  - Use single Hamcrest dependency in tests
  - Improve logging performance
  - Bumped netty-codec from 4.1.63.Final to 4.1.68.Final
  - Bump netty-codec-http from 4.1.68.Final to 4.1.71.Final
  - Bumped log4j-core from 2.14.0 to 2.16.0
  - Added public key file

- 2.0.5
  - Bumped jetty-server from 9.4.34.v20201102 to 9.4.41.v20210516.

- 2.0.4
  - Android compatibility fix (PR #76)
  - Fix NoSuchElementException when switching protocols to WebSocket (PR #78)
  - Prevent NullPointerException in ProxyUtils::isHEAD (PR #79)
  - Fixes in ThrottlingTest, Upgrade to Netty 4.1.63.Final (PR #65)
  - Fix NPEs in getReadThrottle and getWriteThrottle when globalTrafficShapingHandler is null (PR #80)

- 2.0.3
  - Upgrade guava to 30.1
  - Threads are now set as daemon (not user, which is the default) threads so the JVM exits as expected when all other threads stop.
  - Close thread pool if proxy fails to start

- 2.0.2
  - Support for WebSockets with MITM in transparent mode
  - Support for per request conditional MITM

- 2.0.1
  - Removed beta tag from version
  - Updated various dependency versions
  - Re-ordered the release notes so the newest stuff is at the top

- 2.0.0-beta-6
  - Cleaned up old code to conform with newer version of Netty
  - Deprecated UDT support because it's deprecated in Netty
  - Removed performance test code because it seems to be confusing GitHub into thinking that this is a PHP project

- 2.0.0-beta-5
  - Treat an upstream SOCKS proxy as if it is the origin server
  - Fixed memoryLeak in ClientToProxyConnection

- 2.0.0-beta-4
  - Allow users to set their own sesrvergroup within the bootstrap helper
  - Added support for chained SOCKS proxies

- 2.0.0-beta-3
  - Upgraded Netty, guava, Hamcrest, Jetty, Selenium, Apache commons cli and lang3
  - Upgrade Maven plugins to the latest versions

- 2.0.0-beta-2
  - Added support for proxy protocol.  See https://www.haproxy.com/blog/haproxy/proxy-protocol/ and https://www.haproxy.org/download/1.8/doc/proxy-protocol.txt for protocol details.

- 2.0.0-beta-1
  - New Maven coordinates
  - Moved from Java 7 to 8
  - Updated dependency versions
  - **Breaking change:**  Made client details available to ChainedProxyManager
  - Refactored MITM manager to accept engine with user-defined parameters
  - Added ability to load keystore from classpath
