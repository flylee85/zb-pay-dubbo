
---

:confused: 或许你在网上看过一些资料，了解一些分布式事务的解决办法，然而，一切还只是停留在理论阶段。

:confused: 或许你知道可以通过可靠消息、TCC、最大努力通知等方案来解决分布式事务问题，然而，一切还只是停留在理论阶段。

:confused: 或许你能说出来可以通过一些开源的技术来实现分布式事务，然而，一切还只是停留在理论阶段。

---


#### > 好吧，先简单看一下分布式事务相关的业务场景
以商城下单支付作为案例

    1. 支付成功后，可能会出现垮多个服务修改数据，就会遇到分布式事务问题，如何保证垮服务下的业务数据一致性？

    2. 支付成功后，积分、账户等数据需要实时变更，在分布式服务下，如何保证数据实时一致性？

    3. 支付成功后，银行异步通知支付结果，如果网络或者自身服务器出现故障，如何保证业务数据一致性？

    4. ......


#### > 当前项目的功能业务说明
    以商城下单支付作为当前分布式项目的业务功能，最终的目的是通过该项目完整的实现和解决分布式事务的问题。

#### > 分布式事务的解决方案：
    1. 可靠消息最终一致性（异步确保型）

    2. 最大努力通知（定期校对）

    3. TCC（两阶段型、补偿型）

以上3种分布式事务的解决方案，将会在项目中通过代码完整的展现。

#### > 技术选型
    该分布式项目主要以dubbo作为服务治理框架，采用SpringBoot作为微服务开发框架。服务之间可独立部署、业务解耦、扩展性好。

#### > 最新动态
    目前处于开发阶段，还未完成，敬请期待。

#### > 通过此项目，你能学到什么？
    对于分布式事务相关的技术，现网络上都是一些理论性的文字介绍，没有任何项目代码上的实现。这让初学者很是头疼茫然。
    故因此，通过此项目完整的通过代码，实现分布式事务的功能。
    重要的是，此项目完全免费开源，这才是我个人一直尊崇的技术共享的思想。
