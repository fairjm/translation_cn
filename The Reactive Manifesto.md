翻译自：[http://www.reactivemanifesto.org/][1]  

个人能力有限 翻译中如有错误请麻烦指正^_^  

fairjm 


----------
发布于2014年9月（v2.0）  

许多不同领域的机构独立地发现了一种相似的软件开发模式。用这个模式开发的系统更加健壮，更有韧性，更为灵活并且能更好地应对现代软件开发的要求。  
  
这些改变正在发生，因为对于应用程序的需求在近几年发生了相当大的变化。仅仅在几年之前，一个大型应用只有数十台服务器，拥有秒级的响应时间，需要数小时的离线维护时间。如今的许多应用在移动设备至运行着成千上万个多核处理器的云端被部署。用户预期的是毫秒级的响应时间和永不中断的服务。数据用PB来计量单位。如今的许多需求已不能靠过去的软件架构来实现。    

我们相信我们需要一个协调一致的系统架构，并且我们相信所有必要的方面已被单独地认可了。我们需要一个集具有响应性（`Responsive`），具有韧性（`Resillient`），具有可伸缩性（`Elastic`）和消息驱动（`Message Driven`）的系统。我们称之为反应式系统`Reactive Systems`。    

被构建为反应式系统的系统更为灵活，松耦合和[可扩展][2]。这使得它们更容易去开发、修改。它们对失败有更大的容忍，并且当[失败][3]发生时它们会优雅地应对而不是让系统崩溃。反应式系统有着高度的响应性，并会给[用户][4]有效的交互反馈。  
  
**反应式系统是：**   

**可响应的：**  [系统][5]在所有可能的情况下都会及时响应。响应性不止是可用性和实用性的基石，更意味着问题可以被快速地发现和有效地处理。反应式系统专注于提供迅速和一致的响应时间和确定可靠的时间上限以此来交付稳定质量的服务。这种一致的行为相应地简化了错误处理，逐渐增强了终端用户的信心，并且推动了进一步的交互。  

**有韧性的：** 系统在[失败][6]面前依旧能保持响应性。这不仅仅应用于高可用性、任务关键型的系统，任何没有韧性的系统在失败之后会变得响应迟缓甚至无法响应。韧性是通过[复制][7]，容忍，[隔离][8]和[委托][9]实现的。失败在任何[组件][10]中都会发生，将各个组件彼此隔离从而保证系统的一部分可以失败并恢复而不会影响整个系统。恢复是通过失败的组件委托到其他（额外的）组件实现的，高可用性是通过复制必须的部分保证的。组件的客户端没有处理组件失败的负担。  

**可伸缩的：** 系统在各种工作负载之下依旧能保持响应性。反应式系统可以通过增加或减少对输入服务的[资源][11]分配来对输入速度的改变反应。这暗示了系统的设计是不存在竞争点和中心瓶颈的，系统有能力分片或者复制组件并将请求分发到这些组件当中。反应式系统通过提供相关的实时性能测量支持预测性和反应性的伸缩算法。这些以对商用硬件和软件平台成本有效的方式实现了[伸缩性][12]。  

**消息驱动：** 反应式系统依赖[异步][13][消息传递][14]去建立不同组件间的边界，并以此确保松耦合，隔离，[位置透明][15]和提供一种方式将[错误][16]用消息委托。通过塑造和监视系统中的消息队列并在必要时使用[背压][17]，显式消息传递的使用可以实现负载管理、可扩展性和流程控制。在通信中使用位置透明的消息传递使得管理集群和单个主机拥有相同的结构和语义。[非阻塞][18]的通信允许接收者只在活动时消耗[资源][19]，可以减少系统的开销。    

![http://www.reactivemanifesto.org/][20]  

大型系统由较小规模的部分组成，因此依赖于这些组成部分的反应式性质。这意味着反应式系统的设计原则，让这些性质适用于各种规模，使得它们可组合。世界上最大的系统依赖于基于这些性质的架构并且每日服务数以亿计的人的需要。是时候从开始就有意识地应用这些设计原则而不是每次重新发现它们。  

---    
前段时间在manning买了[Reactive Design Patterns][21] 和 [Functional and Reactive Domain Modeling][22]。读了部分，就去看了下反应式宣言，有些地方感觉翻译得比较牵强，如有错误请麻烦指正下^_^。


  [1]: http://www.reactivemanifesto.org/
  [2]: http://www.reactivemanifesto.org/glossary#Scalability
  [3]: http://www.reactivemanifesto.org/glossary#Failure
  [4]: http://www.reactivemanifesto.org/glossary#User
  [5]: http://www.reactivemanifesto.org/glossary#System
  [6]: http://www.reactivemanifesto.org/glossary#Failure
  [7]: http://www.reactivemanifesto.org/glossary#Replication
  [8]: http://www.reactivemanifesto.org/glossary#Isolation
  [9]: http://www.reactivemanifesto.org/glossary#Delegation
  [10]: http://www.reactivemanifesto.org/glossary#Component
  [11]: http://www.reactivemanifesto.org/glossary#Resource
  [12]: http://www.reactivemanifesto.org/glossary#Elasticity
  [13]: http://www.reactivemanifesto.org/glossary#Asynchronous
  [14]: http://www.reactivemanifesto.org/glossary#Message-Driven
  [15]: http://www.reactivemanifesto.org/glossary#Location-Transparency
  [16]: http://www.reactivemanifesto.org/glossary#Failure
  [17]: http://www.reactivemanifesto.org/glossary#Back-Pressure
  [18]: http://www.reactivemanifesto.org/glossary#Non-Blocking
  [19]: http://www.reactivemanifesto.org/glossary#Resource
  [20]: http://www.reactivemanifesto.org/images/reactive-traits.svg
  [21]: http://www.manning.com/kuhn/
  [22]: http://www.manning.com/ghosh2/
