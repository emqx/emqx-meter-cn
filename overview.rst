
.. _overview:

============
测试环境说明
============

--------
测试工具
--------

`XMeter`_ 在线性能测试服务，国内专业的性能测试服务提供商

`JMeter-MQTT`_ 测试插件实现

`JMeter4.0`_ JMeter版本


--------
测试环境
--------

EMQ版本: `emqx-ubuntu18.04-v3.0.0.zip`

测试机: 青云8核CPU，32GB内存，Ubuntu-18.04.1

压力机：青云8核CPU，8GB，CentOS 7.2

压力机与被测系统之间的网络连接：青云北京三区内网基础网络，节点间带宽约2Gbps

--------
测试场景
--------

本次测试主要包括并发连接测试和消息吞吐测试，共计24个测试场景。相关的具体测试报告请参见每个测试用例的详细描述。并发连接测试有TCP、SSL单向认证和SSL双向认证三种，共计9个测试场景。消息吞吐测试有多SUB、少PUB，少SUB、多PUB，峰值测试，共享主题，收发和延时测试6大类型。

由于测试组合众多，测试场景的设计考虑了覆盖度和易于测试结果比较等因素，设计了这些测试场景。

--------
测试报告
--------

EMQ服务器端的测试指标都已经随本报告提供。

.. _XMeter: http://xmeter.net
.. _JMeter-MQTT: https://github.com/XMeterSaaSService/mqtt-jmeter/tree/master/src/main/java/net/xmeter/emqtt/samplers
.. _JMeter4.0: http://jmeter.apache.org
.. _fusesource-1.14: https://github.com/fusesource/mqtt-client
.. _emqx-ubuntu18.04-v3.0.0.zip: https://emqx.io/
