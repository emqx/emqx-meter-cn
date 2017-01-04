
.. _overview:

============
测试环境说明
============

--------
测试工具
--------

`XMeter`_ 在线性能测试服务，国内专业的性能测试服务提供商

`JMeter-MQTT`_ 测试插件实现

`JMeter`_ 3.0

`fusesource-1.14`_ MQTT客户端

--------
测试环境
--------

EMQ版本: `emqttd-ubuntu16.04-v2.0.zip`_

测试机: 青云8核CPU，28GB内存，Ubuntu-16.04.1

压力机：青云8核CPU，8GB，CentOS 7

压力机与被测系统之间的网络连接：青云北京三区内网基础网络，节点间带宽约500Mbps

--------
测试场景
--------

本次测试主要包括并发连接测试和消息吞吐测试，共计27个测试场景。相关的具体测试报告请参见每个测试用例的详细描述。并发连接测试有TCP、SSL单向认证和SSL双向认证三种，共计9个测试场景。消息吞吐测试有多SUB、少PUB，少SUB、多PUB，峰值测试，共享主题，收发和延时测试6大类型。

由于测试组合众多，测试场景的设计考虑了覆盖度和易于测试结果比较等因素，设计了这些测试场景。

--------
测试报告
--------

在本报告中有一些到www.xmeter.net的链接，用户可以直接在线查看这些报告。这些共享报告包含了从客户端监测到的一些基本测试指标，EMQ服务器端的测试指标都已经随本报告提供。如果想查看这些报告，用户只需要在xmeter.net注册一个账户，点击这些报告链接就可以了。

在查看Sub的测试报告的时候，请注意：由于Sub是异步调用和JMeter的实现机制等限制，无法准确知道响应时间和吞吐量等信息，目前Sub相关的报告只有虚拟用户数、返回成功率和下载的bytes等有效的指标。XMeter近期将对JMeter的Sub插件进行增强，将会取得准确的响应时间和吞吐量等信息。

.. _XMeter: http://xmeter.net
.. _JMeter-MQTT: https://github.com/XMeterSaaSService/mqtt-jmeter/tree/master/src/main/java/net/xmeter/emqtt/samplers
.. _JMeter: http://jmeter.apache.org
.. _fusesource-1.14: https://github.com/fusesource/mqtt-client
.. _emqttd-ubuntu16.04-v2.0.zip: http://emqtt.com/downloads/2006/ubuntu16_04

