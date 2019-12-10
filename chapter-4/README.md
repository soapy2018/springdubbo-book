Chapter 4 Examples
==================
一、注册中心

本例使用Zookeeper作为注册中心，需事先安装好Zookeeper。

二、接口工程

dubbo-api工程里有一个接口IHello

三、服务端

dubbo-server工程添加Dubbo和接口工程的依赖，实现IHello接口，并用注解@Service暴露服务，在application.properties文件中配置Dubbo。

四、消费方

dubbo-client工程添加Dubbo和接口工程的依赖，编写远程调用Dubbo服务，@Reference注解可以用于生成远程服务代理，在application.properties文件中配置跟服务端一样的服务注册中心。

五、网关

模块之间互相调用时，为了降低由网络波动带来的不确定性
