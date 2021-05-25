You are developing a sewer-side enterprise appliceation.It must support a variety of different clients including desktop browsers.mobile brewsers and native mobile applications.The application might also expose an API for 3rd?parties to custume.It might also（请作答此空）with other applications via either web services or a message broker.The application handles requests (HTTP reuests and messages) by executing business logic;accessing a databse;exchanging messages with other systems;and returning a HTML/JSON/XML( ).There are logical components corresponding to different funitional areas of the application.What’s the application’s deployment architecture?Define an architecture that structures the application as a set of( ), collaborating services.This approach corresponds to the Y-axis of the Scale Cube.Each service is:Flighly maintainable and testable-enables rapid and frequent development and deploymentLoosely coupled with other seruices-enables a team to work independently (the majority of time on their seruicers) without being impouted by changes to other services and without affecting other services.( )deployable -enable a team to deploy their services without having to cortdinate with other teamsCapable of being developed by a small team-essential for high productivity by avoiding the high communication head of large teamsServices( )using either syn chronous protocals such as HTTP/REST or a syn chronous protocols such as AMQP.Services can be developed and deployed independently of one another.Each service has its own database in order to be decoupled from other services.Data consistency between services is maintained using some particular pattern.


你正在开发一个下水道企业应用程序。它必须支持各种不同的客户端，包括桌面浏览器、移动啤酒和本地移动应用程序。该应用程序也可能暴露一个API供第三方使用。 应用程序通过执行业务逻辑处理请求（HTTP请求和消息）；访问数据库；与其他系统交换消息；并返回HTML/JSON/XML( ).有一些逻辑组件对应于应用程序的不同功能区域。 每个服务都是：高度可维护和可测试的--可快速和频繁地开发和部署与其他服务松散地耦合--可使一个团队独立工作（大部分时间在他们的服务器上）而不被其他服务的变化所影响，也不影响其他服务。 ()可部署性--使一个团队能够部署他们的服务，而不必与其他团队相联系能够由一个小团队开发--通过避免大团队的高通信量而对高生产率至关重要服务()使用同步协议，如HTTP/REST或同步协议，如AMQP.服务可以独立开发和部署。


integrate 
Coordinate 
cooperate 
Communicate 
request 
response 
text 
File 
loosely coupled 
loosely cohesion 
High coupled 
Highly cohesion 
Dependently 
Independently 
Coordinately 
Integratedly 
interoprate 
coordinate 
communicate 
depend 