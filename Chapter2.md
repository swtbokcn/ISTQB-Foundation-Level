# **2. 贯穿软件开发生命周期的测试 **
**关键字**

验收测试(acceptance testing)， alpha测试 (alpha testing)， beta 测试(beta testing)， 商业现货软件(commercial off-the-shelf (COTS))， 组件集成测试(component integration testing)， 组件测试(component testing)， 确认测试(confirmation testing)， 合同验收测试(contractual acceptance testing)， 功能测试(functional testing)， 影响分析(impact analysis)， 集成测试(integration testing)， 维护测试(maintenance testing)， 非功能测试(non-functional testing)， 运行验收测试(operational acceptance testing)， 回归测试(regression testing)， 法规验收测试(regulatory acceptance testing)， 顺序开发模型(sequential development model)， 系统集成测试(system integration testing)， 系统测试(system testing)， 测试依据(test basis)， 测试用例(test case)， 测试环境(test environment)， 测试级别(test level)， 测试对象(test object)， 测试目标(test objective)， 测试类型(test type)， 用户验收测试(user acceptance testing)， 白盒测试(white-box testing) 

**贯穿软件开发生命周期的测试的学习目标**

**2.1 软件开发生命周期模型**

FL-2.1.1  (K2)解释软件开发活动与软件开发生命周期中测试活动之间的关系

FL-2.1.2  (K1)识别软件开发生命周期模型必须适应项目和产品特点的原因

**2.2 测试级别**

FL-2.2.1  (K2) 从目标、测试依据、测试对象、典型缺陷和失效、方法和职责的角度比较不同的测试级别

**2.3 测试类型**

FL-2.3.1 (K2)比较功能测试、非功能测试和白盒测试

FL-2.3.2 (K1)认识到功能测试、非功能测试和白盒测试可以在任何测试级别进行

FL-2.3.3 (K2)比较确认测试和回归测试的目的 

**2.4 维护测试**

FL-2.4.1  (K2)总结维护测试的触发因素

FL-2.4.2  (K2)描述维护测试中影响分析的角色


## **2.1 软件开发生命周期模型**
### **2.1.1 软件开发和软件测试**

为了能够进行适当的测试活动，熟悉常见的软件开发生命周期模型是测试人员职责的重要组成部分。

在任何软件开发生命周期模型中，好的测试都有以下特点：
  * 每个开发活动都有对应的测试活动
  * 每个测试级别都有与该级别对应的特有测试目标
  * 在相应的开发活动中开始对给定的测试级别进行测试分析和设计
  * 测试人员参加讨论，以确定和完善需求和设计，并在初稿完成后立即参与评审工作产品(如需求、设计、用户故事等)

无论选择哪种软件开发生命周期模型，测试活动都应该在生命周期的早期阶段开始，以遵循测试尽早介入的原则。

这里将常见的软件开发生命周期模型分类如下：
  * 顺序开发模型
  * 迭代增量开发模型

顺序开发模型将软件开发过程描述为线性且按照顺序的活动次序。这意味着开发过程的任何阶段都应在前一阶段完成时开始。理论上阶段没有重叠，但在实践中，从下一阶段得到早期反馈是有益的。
#### **2.1.1.1 顺序开发模型**
**1.瀑布模型**

瀑布模型最早由Winston W. Royce在1970年提出，在软件工程中占有重要的地位，它提供了软件开发的基本框架。从测试的角度而言，瀑布模型最大的缺点是，测试是软件开发过程中的一个阶段，测试被看做是对软件产品的最终检查，类似于制造业中将产品交付给客户之前的检查。

图2.1.1-1显示了一个传统的瀑布模型，它将软件开发生命周期划分为系统需求(System Requirment)、软件需求(Software Requirement)、分析(Analysis)、程序设计(Program Design)、编码(Coding)、测试(Testing)和运行(Operations)七个基本阶段，并且规定了它们自上而下、相互衔接的固定次序，如同瀑布流水，逐级下落。从本质来说，它是一个软件开发架构，开发过程是通过一系列阶段顺序展开的，只有当一个开发阶段完成后，下一个开发阶段才会开始。
![图片](https://uploader.shimo.im/f/Z5feU6fAhokQwaas.png!thumbnail)

图2.1.1-1 瀑布模型

尽管瀑布模型由于存在一些缺点而招致很多的批评，但是它对很多类型的项目而言依然是有效的。如果瀑布模型能够正确使用，可以节省大量的时间和金钱。是否采用瀑布模型，主要取决于是否能够充分理解客户的需求，以及在项目开发过程中这些需求是否经常发生变更。对于需求经常发生变更的项目，采用瀑布模型是不合适的，这时候就需要考虑其他类型的软件开发生命周期模型。       
>Royce， W.， Managing the Development of Large Software Systems: Concepts and Techniques， Proc. IEEE WESCON， 1970

**2.V模型  **

与瀑布模型不同，V模型在整个开发过程中集成了测试过程，践行了尽早测试的原则。此外，V模型还包括与每个相应开发阶段对应的测试级别，这进一步支持了尽早测试（关于测试级别的讨论见第2.2节）。在此模型中，与每个测试级别相关联的测试的执行按照顺序方式进行，但在某些情况下会发生重叠。

V模型是瀑布模型的变种，它体现的主要思想是：开发任务和测试任务是相互对等的活动且同等重要。V模型的左右两侧组成字母V的两个边，形象地体现了这一点。V模型的左侧代表软件开发过程，在软件开发过程中，系统是逐步设计完善的，编码是最后一步。V模型的右侧描述了集成和测试的过程，通过不断组合程序组件，形成更大的子系统（集成），并对它们的功能和非功能进行测试。根据这个模型，开发得到的整个系统将以验收测试作为系统集成和测试活动的结束点。

图2.1.1-2显示了由开发活动和测试活动共同组成的一个V模型，V模型主要的开发活动有需求规格说明、系统功能设计、系统技术设计、组件规格说明和编码，相应的测试级别有组件测试、集成测试、系统测试和验收测试。在不同资料中，V模型的左边各个活动可能略有不同，但是其思想都是一致的。其中，构成V模型左侧的活动就是人们熟知的瀑布模型中的活动：
  * 需求规格说明：从客户或将来的系统用户中收集，并对它们进行详细描述，最终得到批准的要求和需求。需求规格说明定义了开发系统的目的和需要实现的特性和功能。
  * 系统功能设计：将需求映射到系统的功能和框图上。
  * 系统技术设计：设计系统的具体实现方式。这个阶段包括定义系统环境的接口，同时将整个系统分解成更小且容易理解的子系统（系统架构），从而可以对每个子系统进行独立的开发。
  * 组件规格说明：定义每个子系统的任务、行为、内部结构以及与其他子系统的接口。
  * 编码：通过编程语言实现所有已经定义的组件（例如：模块、单元、类）。


![图片](https://uploader.shimo.im/f/YVHzszWNKrUATukb.png!thumbnail)

图2.1.1-2 V模型

在V模型中，随着整个构建阶段的进行，软件系统的描述越来越详细。通常来说，在某个构建中引入的错误最容易在本构建阶段中发现。因而，对于每个构建阶段，V模型的右边定义了相应的测试级别。在每个测试级别，都要检查开发的输出是否满足具体的要求，或者是否满足这些特定阶段相关的要求。
  * 组件测试：验证软件组件是否按照组件规格说明（详细设计说明）正确执行，即保证每个最小的单元能够正常运行。组件测试一般由开发人员来执行，首先设定最小的测试单元，然后通过设计相应的测试用例来验证各个组件功能的正确性。
  * 集成测试：检查多个组件是否按照系统技术设计描述的方式协同工作。集成测试的主要关注点是系统能够成功编译，实现了主要的业务功能，系统各个模块之间数据能够正常通信等。
  * 系统测试：验证整个系统是否满足需求规格说明。
  * 验收测试：从用户的角度检查系统是否满足合同中定义的需求或者用户需求。
> ANDREAS SPILLNER，TILO LINZ，HANS SCHAEFER，SOFTWARE TESTING FOUNDATIONS，人民邮电出版社，2008-4-1


#### **2.1.1.2 增量开发模型** 
顺序开发模型交付的软件包含了全套的功能，但通常需要几个月或几年的时间才能交付给利益相关者和用户。增量开发涉及到建立需求、设计、构建和测试部分系统，这意味着软件的特性逐渐增加。这些特性逐步增加的大小各不相同，有些方法增加的大一些，有些方法小一些。增加的特性可以小到对一个用户接口界面的修改或者一个新的查询选项。

这里面首先要说一下“增量”和“迭代”的区别。迭代，就是在实现软件的每一功能时反复求精的过程，是提升软件质量的过程，是从模糊到清晰的过程；而增量，则是强调软件在发布不同的版本时，每次都多发布一点点，是软件功能数量渐增地发布的过程。二者的对比如图2.1.1-3所示。

![图片](http://www.uml.org.cn/SoftWareProcess/images/clip-image020-thumbsww.jpg)

图2.1.1-3 增量和迭代的区别
>https://blog.csdn.net/l12345678/article/details/5642851

现在大部分软件开发其实都是既有增量又有迭代。在日常工作中，这两个概念混用的比较多。
迭代开发发生在多个特性在一系列周期中一起被指定、设计、构建和测试的时候，通常是固定的时间周期。迭代可能涉及到对早期迭代中开发的特性的更改，以及项目范围的更改。每次迭代都交付工作软件，这是整个特性集中不断增长的一个子集，直到最终软件交付或开发停止。

迭代开发的例子包括：
  * Rational统一过程RUP：每次迭代相对较长（例如：两到三个月），特性增加相应较大，例如两组或三组相关特性
  * SCRUM：每次迭代都较短（例如：几个小时、几天或几个星期），相应的特性增加较小，例如一些增强和（或）两三个新特性
  * 看板：实现时使用或不使用固定长度的迭代，这种迭代可以在完成时交付单个增强或特性，也可以将特性组合在一起立即发布
  * 螺旋式（或原型）：包括创造实验性增量，其中一些可能被大量返工，甚至在后续的开发工作中被放弃

下面介绍一下螺旋模型。螺旋模型由Barry W.Boehm于1988年提出。螺旋模型是增量迭代开发模型的一种，如图2.1.1-4所示，它兼顾了快速原型迭代的特征以及瀑布模型的系统化与严格监控。螺旋模型最大的特点在于引入了其他模型不具备的风险分析，使软件在无法排除重大风险时有机会停止，以减小损失。在每个迭代阶段构建原型是螺旋模型用以减小风险的途径。螺旋模型更适合大型的系统级的软件应用。

![图片](https://uploader.shimo.im/f/AL71wd0Fw30uvBtO.png!thumbnail)

图2.1.1-4 螺旋模型

螺旋模型中一个典型的迭代包括以下步骤：
1.   明确本次迭代的目标、备选方案以及应用备选方案的限制；
2.   对备选方案进行评估，明确并解决存在的风险，建立原型；
3.   当风险得到很好的评估与解决后，应用瀑布模型进行本次迭代的开发与测试；
4.   对下一迭代进行计划与部署；
5.   项目利益相关者对本次迭代的交付物进行评审，同时检查下一阶段的计划。

螺旋模型的优点是它在引入了风险驱动方法的同时，兼顾了原型开发和瀑布模型等开发模型的优点。在一定条件下，螺旋模型能够演变成其他的开发模型，例如：如果项目获得错误用户接口或无法满足性能需求等方面的风险很低，而同时它在控制成本和进度方面的风险很高的情况，螺旋模型将会演化成瀑布模型。除了这个优点以外，螺旋模型还具有以下优点：
  * 可以在项目前期考虑对已经存在的软件进行重用；
  * 在软件产品开发过程中考虑了软件质量目标；
  * 关注于缺陷预防，并能够尽早的发现缺陷；
  * 更好的控制项目活动的资源和相关成本；

螺旋模型在很多领域得到了广泛的引用，但是螺旋模型也存在一定的不足，包括：
  * 过分依赖风险评估，一旦在风险管理过程中出现偏差将造成重大损失；
  * 过于灵活的开发过程不适合开发者和客户之间有明确合同约定的情况；

该模型本身的文档化和推广需要大量的工作量。       
>Barry W.Boehm， A spiral model of software development and enhancement ， ACM SIGSOFT SOFTWARE ENGINEERING NOTES vol 11 no 4 ，Aug 1988 
>[http://zh.wikipedia.org/wiki/](http://zh.wikipedia.org/wiki/)螺旋模型

在整个开发过程中，使用这些方法开发的组件或系统往往涉及到测试级别的重叠和迭代。理想的情况是，每个特性在交付之前，在多个测试级别上进行测试。在某些情况下，团队使用持续交付或持续部署，这两者都涉及到作为其交付过程一部分的多个测试级别的大量自动化。许多使用这些方法的开发工作量还包括自组织团队的概念，它可以改变测试工作的组织方式以及测试人员和开发人员之间的关系。

这些方法形成了一个不断发展的系统，它可以按照特性、迭代，或者以更传统的主版本发布方式交付给最终用户。无论软件增量是否发布给最终用户，随着系统的增强回归测试变得越来越重要。
与顺序模型不同，增量开发模型可以在几周甚至几天内交付可用的软件，但只能在几个月甚至几年内交付全套需求产品。

有关敏捷开发背景下的软件测试的更多信息，请参见ISTQB-AT基础级敏捷测试扩展大纲。

### **2.1.2 基于上下文的软件开发生命周期模型**
前面的1.3节就提到一个测试原则“测试依赖上下文”。在软件工程的发展历史中，出现了很多的软件开发模型，从刚开始的瀑布模型和V模型等线性模型，到后来的螺旋模型和Scrum等增量迭代模型等。目前有些观点认为越是最新的开发模型越好，这种想法是错误的。不同的模型适合不同的上下文场景。软件开发生命周期模型必须根据项目和产品的特点选择和调整。应根据项目目标、正在开发的产品类型、业务重点(如市场要求时间)以及已识别的产品和项目风险，选择和调整合适的软件开发生命周期模型。例如：小型内部管理系统的开发和测试，应与汽车制动控制系统等安全关键系统的开发和测试有所不同。另一个例子是，在某些情况下，组织和文化问题可能会阻碍团队成员之间的交流，从而阻碍迭代开发。

根据项目的背景，可能需要合并或重组测试级别和/或测试活动。例如：为了将现成的商用现货软件产品集成到更大的系统中，购买者可以在系统集成测试级别（例如：与基础设施和其他系统的集成)和验收测试级别(功能测试和非功能测试，以及用户验收测试和操作验收测试) 上进行互操作性测试。关于测试级别的讨论见第2.2节，关于测试类型的讨论见第2.3节。

此外，软件开发生命周期模型本身也可以合并。例如：V模型可用于开发和测试后端系统及其集成，而敏捷开发模型可用于开发和测试前端用户界面（UI）和功能。在项目早期可以使用原型，在试验阶段完成后采用增量开发模型。

物联网（IoT）系统由许多不同的对象组成，如设备、产品和服务，通常为每个对象应用单独的软件开发生命周期模型。这对物联网系统版本的开发提出了特殊的挑战。另外，这些对象的软件开发生命周期更强调在它们运行使用（例如：运行、更新和退役阶段）之后的软件开发生命周期的后期阶段。

## **2.2测试级别**
测试级别是一组共同组织和管理的测试活动。每个测试级别都是测试过程的实例，由1.4节所述的活动组成，在特定软件开发级别上开展，从单元或组件到完整的系统，或在特定情况下的综合系统。测试级别按ISTQB大纲规定有：组件测试、集成测试、系统测试、验收测试，这与V模型（如图2.1.1-2所示）正好一致。

对于每个测试级别，都需要明确：测试的总体目标、测试的依据、测试的对象（即测试什么）、发现的典型缺陷和失效、测试工具的支持（测试工具介绍见第六章）、专门的方法和职责等。

### **2.2.1 组件测试**
组件测试，也就是我们常说的单元测试。首要得搞清楚单元的含义，根据项目和编程语言的不同，单元可能代表的内容也不同，可能是组件、类、函数、代码块、数据结构等。更加清晰的说，单元可以理解成：实现独立的、可测试的特定功能，其粒度根据应用的上下文可大可小，边界也是随着测试设计的深入可以调节。

组件测试的典型测试对象包括：
  * 组件、单元或模块
  * 代码和数据结构
  * 类
  * 数据模块

组件测试，最好是将组件隔离出来独立测试，主要关注组件内部的行为，组件之间的接口在这一测试级别不受关注（集成测试考虑的范畴），在测试中，经常会使用到桩、驱动器和模拟器等，这些都不是软件产品的组成部分，而且也是需要一定的开发费用；

组件测试的目标包括：
  * 减少风险
  * 验证组件的功能和非功能行为是否符合设计和规定
  * 建立对组件质量的信心
  * 发现组件的缺陷
  * 防止缺陷遗漏到更高的测试级别

组件测试依据主要是详细设计，也可依据开发编写的代码、数据模型或者组件规格说明。组件测试的主要关注点也是经常出现错误的点：
  * 组件的接口参数：这是组件测试的基础，只有数据能正确流入、流出组件，其他的测试才有意义，而且这也是实际测试中最容易忽略漏测的地方；
  * 局部数据结构：例如，不正确或不一致的数据类型声明、未赋值或初始化的变量、变量名拼写错误或不符合编码规范等；
  * 独立路径：应对路径进行覆盖测试，例如，保证组件中每条语句至少执行一次，发现误解或者用错了算符优先级、混合类型运算等；
  * 控制流相关：例如，不同数据类型对象间的比较、死循环等；
  * 出错处理：例如，出错描述难以理解、异常处理不当或者没有处理、显示的异常与实际场景不符合等；

通常情况下，组件测试由开发人员执行，发现的缺陷也可以立即得到修复，不需要正式的缺陷管理。但测试至少需要深入到被测代码中。开发人员可以将组件开发与发现和修复缺陷交替进行。开发人员通常会在编写了组件代码之后编写和执行测试。然而，特别是在敏捷开发中，编写自动化组件测试用例可能先于编写应用程序代码。例如：考虑测试驱动开发（TDD）。测试驱动开发是高度迭代的，基于开发自动化测试用例，构建和集成小段代码，然后执行组件测试，再纠正任何问题并重构代码的循环。该过程一直持续到组件完全构建完成并且所有组件测试都通过为止。测试驱动开发是一个测试优先方法的例子。虽然测试驱动开发起源于极限编程（XP），但它已经推广到了其他形式的敏捷以及顺序生命周期（见ISTQB -AT基础级敏捷测试扩展教学大纲）。
### **2.2.2 集成测试**
集成测试是对组件之间的接口进行测试，以及测试一个系统内不同部分的相互作用，比如操作系统、文件系统、硬件系统之间的接口。

本文描述的集成测试有两个不同的层次，可以在不同规模的测试对象上进行，具体如下：
  * 组件集成测试：通常组件集成测试在组件测试之后进行，也就是说集成测试开展前，组件测试已经完成。如果组件测试未完成或者测试不充分，遗留的问题将会在集成测试阶段付出更大的代价，从而导致集成效果不佳。组件集成通常是自动化的。在迭代和增量开发中，组件集成测试通常是持续集成过程的一部分。
  * 系统集成测试：对不同系统之间的相互作用进行测试，一般在系统测试之后。在这种情况下，开发组织/团体通常只能控制自己开发的这部分接口，所以变更可能是不稳定的。按照工作流执行的业务操作可能包含一系列系统，因此跨平台的问题对于系统集成测试至关重要。特别是如今的系统架构设计的越来越复杂，为了业务隔离、容量、效率等考虑划分的子系统以及对外的第三方系统越来越多，这类跨平台的端到端测试能力对功能测试人员提出来了更高的要求。

集成测试的目标主要揭示被集成部分之间的接口、配合或者冲突问题，验证接口功能和非功能行为（接口的处理性能、容量等）是否符合设计和规定。

系统化集成的策略可以根据系统结构（例如自顶向下或自底向上）、功能任务集、事务处理顺序或系统和组件的其他方面等来制定。为了减少在生命周期后期才发现缺陷而产生的风险，集成程度应逐步增加，而不是一下子将系统集成为“Big-Bang”来进行测试。

### **2.2.3 系统测试**
系统测试关注的是在开发项目或程序中定义的一个完整的系统/产品的行为。系统测试的目的是验证最终软件系统是否满足用户规定的需求。

在系统测试中，测试环境应该尽量和最终的目标或生产环境相一致，从而减少不能发现和环境相关的失效的风险。

系统测试的测试目标：
  * 减少风险
  * 验证系统的功能和非功能行为是否符合设计和规定
  * 验证系统是否完整并按预期工作
  * 建立对整个系统质量的信心
  * 发现缺陷
  * 防止缺陷遗漏到更高的测试级别或生产环境

系统测试可能包含基于不同方面的测试：根据风险评估的、根据需求规格说明的、根据业务过程的、基于用例的、或根据其他对系统行为的更高级别描述的、根据与操作系统的相互作用的、根据系统资源的等。

系统测试一般由独立的测试团队进行。
### **2.2.4 验收测试**
验收测试通常是由使用系统的用户或客户来进行，同时系统的其他利益相关者也可能参与其中。	验收测试是向未来的用户表明系统能够像预定要求那样工作。

类似系统测试，验收测试通常侧重于整个系统或产品的行为和能力。验收测试的目标包括：
  * 建立对整个系统质量的信心
  * 确认系统是否完整并将按预期工作
  * 验证系统的功能和非功能行为符合规定

验收测试可以用来评估系统对于部署和使用的准备情况，但是验收测试不一定是最后级别的测试。比如，可能会在某个系统验收测试之后，进行大规模的系统集成测试。

验收测试可以在多个测试级别上进行，比如：
  * 商业现货软件产品可以在安装或集成时进行验收测试
  * 组件的可用性验收测试可以在组件测试中进行
  * 增加新功能的验收测试可以在系统测试之前进行

验收测试的内容取决于应用风险（彻底的验收测试、简单的验收测试、互操作验收等）。

验收测试类型包括：
  * 用户验收测试
  * 操作验收测试
  * 合同和法规验收测试
  * Alpha测试和Beta测试

上面提到的这些验收测试类型看起来有点混乱，其实是从不同的维度分别来看验收测试而引起的。这些验收测试在具体的执行中，各有特点，但是他们的主要区别可以从以下方面考虑：
  1. 谁来执行验收测试：如果是用户，那么就是用户验收测试；如果是系统管理员，那么就是操作验收测试。用户和系统管理员在验收测试的关注点显然是不同的。例如：我们作为微信的用户，我们更关注微信面向终端用户的功能是否能够正常使用，是否好用；但是如果你是微信的管理员，那么你可能就会更关注数据备份恢复、系统性能、安全性和用户管理等方面的测试。
  2. 验收测试的依据是什么：合同和法规验收测试这种就是从验收测试依据这个维度来看验收测试的。顾名思义，这种验收测试是根据合同和法规来验收的。
  3. 验收测试在什么地方执行：Alpha测试和Beta测试最显著的区别就是执行验收测试的地点不同。Alpha测试在开发组织所在地点进行的，而Beta测试是潜在的或现有的客户，和/或操作人员在他们自己所在地点进行。

上述三个维度可以帮助大家理解这几个验收测试内容的主要区别，更加具体的内容，可以参考大纲。
## **2.3测试类型**
### **2.3.1 功能测试**
系统的功能测试也称为行为测试，通常根据工作产品，如业务需求规格说明、用户故事、用例或功能规格说明中对产品特性、操作描述等应执行的功能进行评估的测试。功能测试是为了确保程序以期望的方式运行，通过对系统的所有特性和功能进行测试以确保符合需求和规范。而非功能测试是用来评估系统和软件的非功能性，是测试系统表现得“多好”。

功能测试既可以使用白盒技术，也可以使用黑盒技术。黑盒技术常用来获取组件或系统功能的测试条件和测试用例，常见的黑盒测试技术有等价类划分、边界值分析、决策表测试、状态转换测试、错误推测法和综合策略（详见4.2节）。与黑盒测试相对应的是白盒测试，与黑盒测试不同的是，白盒测试需要考虑软件产品的内部结构和处理过程，它是在已知产品的内部工作过程情况下，测试某种内部操作是否按照设计规格说明实现。常见的白盒测试技术有语句覆盖测试、判定覆盖测试。

功能测试应该在所有测试级别上执行，尽管每个测试级别的关注点不同。例如：基于组件测试规格说明的组件测试，其测试目标之一就是验证组件的功能和非功能行为是否符合设计和规定；集成测试的测试目标之一，即验证接口功能和非功能行为是否符合设计和规定。（详见2.2节）

功能测试的完整性可以通过功能覆盖来衡量。功能覆盖是指某种类型的功能元素在多大程度上已通过测试得到检查，并以所覆盖的元素类型的百分比表示。例如：利用测试和功能需求之间的可追溯性，可以计算通过测试覆盖需求的百分比，从而识别覆盖的差距。

功能测试设计和执行会涉及特殊技能或知识，例如对软件所解决的特定商业问题的了解（例如石油和天然气工业的地质建模软件）或软件所发挥的特定作用（例如提供互动娱乐的电脑游戏）。

在《GB/T 25000.10-2016 系统与软件工程 系统与软件质量要求和评价（SQuaRE）第10部分：系统与软件质量模型》（对应的国际标准是ISO/IEC 25010:2011， System and software enginerring-Systems and software Quality Reuirements and Evaluation(SQuaRE)-System and software quality models）中产品质量模型将系统/软件产品质量属性划分成的8个特性中，功能性属于功能质量特性。功能性是指在指定条件下使用时，产品或系统提供满足明确和隐含要求的功能的程度。功能性质量特性包括:功能完备性、功能正确性、功能适合性和功能性的依从性。
1.功能完备性：系统/软件产品对指定的任务和用户目标提供一组相应功能的能力以及覆盖程度。功能的完备性既包括软件产品提供明确的功能的能力，也包括提供隐含要求的能力。明确的功能能力，如需求规格说明中描述的功能要求，根据功能要求分解所获得的功能项的完成程度，若某些功能尚存在缺陷，则不能认为其功能已完成；隐含要求的能力，如需求规格说明中未明确说明的隐含需求功能项。
2.功能正确性：系统/软件产品提供具有所需精度的正确的结果的程度。功能的正确性包括所测试功能的准确性和稳定性，如功能的精度要求、或数值计算的正确性，持续运行某一功能不出现异常、正确完成功能要求的能力。
3.功能适合性：系统/软件产品为促使指定的任务和目标实现的程度。功能适合性包括测试环境的软硬件要求、人员要求的适合性，以及所测试功能对输入错误数据的处理能力。
4.功能性的依从性：系统/软件产品遵循与功能性相关的标准、约定或法规以及类似规定的程度。例如：所测试功能不属于软件使用地区的法律法规所禁止的功能。  

### **2.3.2 非功能测试**
系统的非功能测试用来评估系统和软件的非功能特性，是测试系统表现得“多好”，有一定的主观性。
按照测试原则，越早介入越好，非功能测试也应该尽早介入，尽早完成。

非功能测试可以且经常在所有测试级别上执行。例如：在单元测试阶段，单元接口的性能效率及可靠性要尽可能测试；代码的安全漏洞扫描、用户差错防御性检查要尽可能实施。做到性能从代码开始，安全从代码开始。

黑盒技术可用于获取非功能测试的测试条件和测试用例。例如边界值分析法，可以帮助定义压力条件。

非功能测试的完整性可以通过非功能覆盖来测量。非功能覆盖是指某种类型的非功能元素在多大程度上已通过测试得到检查，并以所涵盖的元素类型的百分比表示。例如某系统需要测试X（种操作系统）×Y（种浏览器）×Z（种分辨率），或者某APP需要测试N（种机型），可以计算通过测试的百分比从而确定潜在的覆盖差距。

非功能性测试的设计和执行会涉及到特殊技能或知识。例如信息安全性测试，可能会用到SQL注入、安全漏洞、内存溢出等技能或知识。

依据《GB/T 25000.10-2016》（ISO/IEC 25010:2011），质量模型包括使用质量模型及产品质量模型。一般在测试过程中，多采用产品质量模型。CNAS（中国合格评定国家认可委员会，英文名称为：China National Accreditation Service for Conformity Assessment 英文缩写为：CNAS）软件检测实验室也遵循这个标准。

产品质量模型将系统/软件产品质量属性划分为8个特效：功能性、性能效率、兼容性、易用性、可靠性、信息安全性、维护性和可移植性。如图2.3.2-1：

![图片](https://images-cdn.shimo.im/2kv9vYmIaXAgCzoj/image.blob!thumbnail)

图2.3.2-1 质量模型

除了功能性外，其他质量特性都可划分到非功能质量特性。针对非功能质量特性的测试，可以称之为非功能测试。大家经常提及的性能测试就是属于非功能测试。接下来将结合实际工作探讨非功能测试所包含的内容。

**1.****性能效率**

主要测试某个业务/功能点的处理效率以及对应的消耗。性能效率指标的度量可反映系统和软件目前达到的效率水平，性能与在指定条件下所使用的资源量有关。
  * 时间特性：产品或系统执行其功能时，其响应时间、处理时间及吞吐率满足需求的程度。
  * 资源利用性：产品或系统执行其功能时，所使用资源（可包括其他软件产品、系统的软件和硬件配置、以及原材料）数量和类型满足需求的程度。
  * 容量：产品或系统参数（参数可包括存储数据项数量、并发用户数、通信带宽、交易吞吐量和数据库模式）的最大限量满足需求的程度。容量特性主要反映系统能够承受的最大并发用户数、最大的请求极限以及系统可能存在的最大事务吞吐量、最大数据容量和数据处理容量。在何种极端的情况下，测试系统出现缓冲区溢出、访问超时等问题。

**2.****兼容性**

验证在共享相同的硬件或软件环境的条件下，产品、系统或组件能够与其他产品、系统或组件交换信息，和/或执行其所需的功能的程度。
  * 共存性：在与其他产品共享通用的环境和资源的条件下，产品能够有效执行其所需的功能并且不会对其他产品造成负面影响的程度。共存性主要考察软件产品安装和运行时与正在运行的软件之间的共存性约束。
  * 互操作性：两个或多个系统、产品或组件能够交换信息并使用已交换的信息的程度。例如数据格式的可交换性：软件互操作性表现为软件之间共享并交换信息，以便能够互相协作共同完成一项功能的能力，常见的测试点为导入导出；数据传输的交换接口：在与其他软件进行通信时，对于规定的数据传输，交换接口的功能是否能正确实现，常见的测试点为打印。

**3.****易用性**

随着软件的广泛应用，越来越多的人在日常工作中大量的依赖于软件。易用性也越来越受到重视。例如：人体工程学、建模、浸入式体验等。
  * 可辨识性：用户能够辨识产品或系统是否适合他们的要求的程度。可辨识性将取决于通过对产品或系统的初步印象和/或任何相关文档来辨识产品或系统功能的能力。产品或系统提供的信息可包括演示、教程、文档或网站的主页信息。常见的测试点如Logo，布局色系等。
  * 易学性：在指定的使用周境中，产品或系统在有效性、效率、抗风险和满意度特性方面为了学习使用该产品或系统这一指定的目标可为指定用户使用的程度。易学性既可以被当作在指定使用周境中产品或系统在有效性、效率、抗风险和满意度特性方面为了学习使用该产品或系统这一指定的目标被指定用户使用的程度，也可以通过相当于ISO 9241-110中定义的学习的适宜性的产品属性来进行指定或测量。常见的测试点如在线帮助等。
  * 易操作性：产品或系统具有易于操作和控制的属性的程度。评估用户能否操作和控制系统或软件。产品或系统的提示信息易于理解，便于用户纠正使用中的错误。
  * 用户差错防御性：系统预防用户犯错的程度。常见的测试点如删除操作是否有提示。
  * 用户界面舒适性：用户界面提供令人愉悦和满意的交互的程度。体验经济的支撑。
  * 易访问性：在指定的使用周境中，为了达到指定的目标，产品或系统被具有最广泛的特征和能力的个体所使用的程度。能力的范围包括与年龄有关的能力障碍。例如，有些人对特定的颜色无法正确识别，软件也需要考虑这样的用户。

**4.****可靠性**

系统、产品或组件在指定条件下、指定时间内执行指定功能的程度。军方产品的可靠性要求非常严格。
  * 成熟性：系统、产品或组件在正常运行时满足可靠性要求的程度。成熟性这个概念可以被用于其他质量特性中，以表明它们在正常运行时满足需求的程度。
  * 可用性：系统、产品或组件在需要使用时能够进行操作和访问的程度。可用性可以通过系统、产品或组件在总时间中处于可用状态的百分比进行外部评估。
  * 容错性：尽管存在硬件或软件故障，系统、产品或组件的运行符合预期的程度。在用户文档集陈述的限制范围之内对产品或系统进行操作，不应丢失数据。输入违反句法条件的信息，产品或系统给出提示信息，并且不能作为许可的输入加以处理。
  * 易恢复性：在发生中断或失效时，产品或系统能够恢复直接受影响的数据并重建期望的系统状态的程度。

**5.****信息安全性**

随着网络安全的重要性越来越大，信息安全性被单独列为一个质量特性，在ISO 25010之前的ISO 9126中，“安全保密性”作为功能性的一个子特性。验证产品或系统保护信息和数据的程度，以使用户、系统产品或系统具有与其授权类型和授权基本一致的数据访问度。
  * 保密性：产品或系统确保数据只有在被授权时才能被访问的程度。
  * 完整性：系统、产品或组件防止未授权访问、篡改计算机程序或数据的程度。
  * 抗抵赖性：活动或事件发生后可以被证实且不可被否认的程度。
  * 可核查性：实体的活动可以被唯一地追溯到该实体的程度。
  * 真实性：对象或资源的身份标识能够被证实符合其声明的程度。

**6.****维护性：**

产品或系统能够被预期的维护人员修改的有效性和效率的程度。
  * 模块化：由多个独立组件组成的系统或计算机程序，其中一个组件的变更对其他组件的影响最小的程度。
  * 可重用性：资产能够被用于多个系统，或其他资产建设的程度。
  * 易分析性：可以评估预期变更（变更产品或系统的一个或多个部分）对产品或系统的影响、诊断产品的缺陷或失效原因、识别待修改部分的有效性和效率的程度。
  * 易修改性：产品或系统可以被有效地、有效率地修改，且不会引入缺陷或降低现有产品质量的程度。
  * 易测试性：能够为系统、产品或组件建立测试准则，并通过测试执行来确定测试准则是否被满足的有效性和效率的程度。

**7.****可移植性**

系统、产品或组件能够从一种硬件、软件、或者其他运行（或使用）环境迁移到另一种环境的有效性和效率的程度。
  * 适应性：产品或系统能够有效地、有效率地适应不同的或演变的硬件、软件、或者其他运行（或使用）环境的程度。适用性包括内部能力（例如屏幕域、表、实物量和报告格式等）的可伸缩性。
  * 易安装性：在指定环境中，产品或系统能够成功地安装和/或卸载的有效性和效率的程度。如果系统或产品能被最终用户所安装，那么易安装性会影响到所产生的功能合适性和易操作性。
  * 易替换性：在相同的环境中，产品能够替换另一个相同用途的指定软件产品的程度。软件产品的新版本的易替换性在升级时对于用户来说是重要的。易替换性可包括易安装性和适应性的属性。
### **2.3.3 白盒测试**
白盒测试也称结构测试，除此之外有时也被称为透明盒测试、逻辑驱动测试或基于代码的测试。当然称为基于代码的测试其实不够准确，因为内部结构包括系统内的代码、架构、工作流和/或数据流(见4.3节)。白盒测试不仅基于代码，也可以基于架构或者工作流等。白盒测试按照程序内部的结构测试程序，通过测试来检测产品内部动作是否按照设计规格说明书的规定正常进行，检验程序中的每条通路是否都能按预定要求正确工作。

软件的白盒测试是基于过程细节的封闭检查。通过提供检查特定条件集合（或）循环的测试用例，测试贯穿软件的逻辑路径和构建间的协作。

白盒测试用例设计方法，利用作为构件层设计的一部分而描述的控制结构来生成测试用例。利用白盒测试方法，软件工程师设计的测试用例可以：
  * 保证一个模块中的所有独立路径至少被执行一次
  * 对所有的逻辑值均需测试真（true）和假（false）
  * 在上下边界及可操作的范围内执行所有的循环
  * 检验内部数据结构以确保有效性
>（from：软件工程实践者的研究方法 原书第6版）

### **2.3.4 与变更相关的测试**
软件在整个生命周期中不是一气呵成的，期间会不断的有各种变更。这里的变更可能是为了修复缺陷，也可能是功能的新增或加强。这些变更都会触发相应的测试。和变更相关的测试主要有下面两种：
  * 确认测试：又称为再测试，缺陷修复后，所有因该缺陷而失败的测试用例都需要在软件中进行测试，并在新的软件版本上重新执行。确认测试通常是在软件修复了发现的缺陷后，执行之前没有通过的测试用例，以确认原来的缺陷已经被成功修复。但是有些缺陷的修复涉及到增加新的功能，这时候也可能会需要增加相应的测试用例。
  * 回归测试：代码中某个部分的变更，无论是修复还是其他类型的变更，都有可能影响到代码其他部分的行为，不管是在同一个组件中，在同一系统的其他组件中，还是在其他系统中。变更包括环境的变化，例如操作系统或数据库管理系统的新版本。这种意外的影响叫做回归。回归测试包括运行测试以检测这种意外的影响。

确认测试和回归测试都属于和变更相关的测试。确认测试和回归测试可以在所有测试级别开展。但是两者的目的是不同的。确实测试的主要目的是验证之前发现的缺陷被成功修复；而回归测试是验证软件变更对已有软件中其他部分是否有影响。

随着增量迭代开发生命周期的广泛应用，与变更相关的测试越来越受到重视。新功能、已有特性的更改以及代码重构都会导致代码频繁变更，这也需要与变更相关的测试。和变更相关的测试的工作量越来越大。尤其是回归测试工作量随着迭代的不断进行，对测试团队的挑战越来越大。随着迭代的不断进行，每个迭代新增加的功能g规模可能是类似的，但是由于之前迭代积累的已有功能越来越多，回归测试的工作量随着迭代的进行也会越来越大。

回归测试套件通常需要运行多次，同时还会缓慢增加，因此回归测试非常适合进行自动化。这些测试的自动化应在项目早期就开始（见第6章）。谈到回归测试，就不可避免的面临回归测试用例的选择。如何选择合适的回归测试用例体现了测试团队对变更影响的理解。完美状态是，所有上一个迭代中的测试用例都能再重新运行一遍。在个别软件中，自动化程度很高，利用多个测试环境并行回归测试，可以实现所有测试用例都运行一遍。但是很多软件都做不到实际上，一个完整的回归测试通常非常耗时间，而且成本很高。因而需要寻找一些方法以帮助选择合适的测试用例，并能最大程度的减少系统存在缺陷的风险。在测试过程中，这通常意味着风险和成本的平衡。决定这种平衡的最好的办法就是对变更进行详细的风险分析，尽量确定负面影响可能在哪发生以及造成的影响。回归测试的范围可以根据软件修改引起的风险程度来决定。常用的方法有：
  * 只重复执行测试计划中的高优先级的测试用例。
  * 只针对系统的特定配置开展测试，比如针对英文版产品的测试或者针对一个操作系统版本的测试。
  * 只针对特定子系统或测试级别的测试。

这些列出的策略通常主要针对系统测试。在更低的测试级别，回归测试策略可以同样基于设计或架构文档（例如，类继承）的测试级别。
### **2.3.5 测试类型和测试级别**
这里将上面讲到的测试级别和测试类型总结如表2.3.5-1所示。

表2.3.5-1 测试级别和测试类型

![图片](https://uploader.shimo.im/f/a8hYFzkotIQU1ZEz.png!thumbnail)

这里罗列的所有测试类型都可以在任何测试级别开展。对于这个论述，很多人可能会有疑问。其中疑问比较多的地方有：
  * 非功能测试不是在高级别的测试中进行吗？在实际的测试过程中，很多测试团队只有在像系统测试和验收测试中才会进行非功能测试，在前面的组件测试中只会进行功能测试。这并不是一个好的实践。我们都知道应该尽可能早的去发现缺陷，我们有什么理由让非功能相关的缺陷留到系统测试才发现呢？为什么不尽早在组件测试就开始进行非功能测试呢？成熟测试团队通常在需求阶段就关注非功能测试，而不是等到系统测试才开始非功能测试。否则就会出现在系统测试发现一些非功能的缺陷，例如：性能无法满足需求，但是受到系统设计和代码实现的限制，后期再修改的成本太高而不得不放弃。
  * 白盒测试不是只用于组件测试吗？在系统测试中也可以用吗？如果我们看白盒测试的另外一个叫法，可能更容易理解。白盒测试也称为基于结构的测试。那么什么算是结构呢？代码当然算是一种结构，函数调用关系也算结构，系统测试中界面中菜单的导航也是一种结构。这里的白盒测试不仅仅针对代码，所有的结构都可以使用白盒测试，所以说白盒测试可以用于所有测试级别。

通过对上面两个经常出现的疑问的分析，我们应该可以更容易的理解测试级别和测试类型。他们是从两个不同的维度来划分测试活动，所以才会出现说这些测试类型都可以在任何测试级别上开展这样的说法。

下面以银行应用程序为例，描述功能测试、非功能测试、白盒测试和与变更相关测试在所有测试级别中的应用。首先从功能测试开始：
  * 对于组件测试，测试的设计是基于组件是如何计算利息的。
  * 对于组件集成测试，测试的设计是基于用户界面捕获的帐户信息如何传递到业务逻辑中。
  * 对于系统测试，测试的设计是基于账户持有人如何在其支票账户上申请信贷额度。
  * 对于系统集成测试，测试的设计是基于系统如何使用外部微服务来检查账户持有人的信用评分。
  * 对于验收测试，测试的设计是基于银行如何处理批准或拒绝信贷申请。

以下是非功能测试的例子：
  * 对于组件测试，性能测试的设计旨在评估执行复杂的总利息计算所需的CPU周期的数量。
  * 对于组件集成测试，安全测试的设计是针对从用户界面传递到业务逻辑的数据所产生的缓冲区溢出漏洞。
  * 对于系统测试，移植性测试的设计旨在检查表示层是否适用于所有支持的浏览器和移动设备。
  * 对于系统集成测试，可靠性测试的设计用来评估在信用评分微服务没有响应时系统的健壮性。
  * 对于验收测试，易用性测试的设计旨在评估银行信贷处理界面对残疾人的无障碍性。

以下是白盒测试的例子：
  * 对于组件测试，测试的设计是为所有进行财务计算的组件实现完整的语句和判定覆盖（见第4.3节）。
  * 对于组件集成测试，测试的设计是为了检查浏览器接口中的每个屏幕如何将数据传递到下一个屏幕和业务逻辑。
  * 对于系统测试，测试的设计是为了覆盖信用额度应用中出现的网页序列。
  * 对于系统集成测试，测试的设计是为了检查所有可能的查询类型发送到信用评分微服务。
  * 对于验收测试，测试的设计是为了覆盖银行对银行转账所支持的所有财务数据文件结构和价值范围。

最后，以下是与变更相关的测试的例子：
  * 对于组件测试，为每个组件构建自动回归测试，并将其纳入持续集成框架。
  * 对于组件集成测试，测试的设计是为了确认与接口相关的缺陷已得到修复，当修复已集成到代码库时。
  * 对于系统测试，假如工作流上的任何屏幕发生变更，则相关工作流的所有测试都将重新执行。
  * 对于系统集成测试，每天重新进行应用程序与信用评分微服务之间交互的测试，并作为该微服务持续部署的一部分。
  * 对于验收测试，在验收测试中发现的缺陷得到修复后，所有先前失败的测试都将重新执行。

虽然本节提供了各个级别的不同测试类型的示例，但对于所有软件来说，没有必要让每个级别包括所有测试类型。但是，必须在每个级别上运行适用的测试类型，特别是特定测试类型发生的最早级别。

# **2.4维护测试**

要想弄明白维护测试首先需要搞清楚它的定义：针对运行系统的更改，或者新的环境对运行系统的影响而进行的测试。这个定义里面涉及到一个“运行系统”（operational system)。所谓“运行系统“指的是这个系统已经在用户或者客户环境中使用了。那么相对应的，如果这个系统还只是在开发阶段，没有部署到客户环境中，那么就不是”运行系统“。一旦运行系统需要进行变更，或者运行系统的环境发生了变化，那么就需要进行维护测试。

所以纯粹从理论上来判断一个测试是否属于维护测试的关键是看被测试对象是否已经是运行系统。这里大家可以看到维护测试是一个新的测试活动维度，是从被测试对象是否是运行系统来区分的。这个维度和我们上面提到的测试类型和测试级别又是不同的。搞清楚他们的观察点不同后，我们可以很容易的知道：维护测试中可以用到上面提到的所有测试类型和测试级别。

根据维护版本的范围，维护测试可能需要在多个测试级别上进行各种测试类型的测试。维护测试的范围取决于：

  * 变更的风险程度，例如：软件的变更区域与其他组件或系统通信的程度
  * 已有系统的规模
  * 变更的规模

### **2.4.1 维护的触发**
针对一个运行的系统，什么时候会触发维护呢？常见的原因分类如下：
  * 修改：计划中的增强改进(例如：基于版本的)、纠正和紧急变更、运行环境的改变(例如：计划中的操作系统或数据库升级)、COTS软件升级以及缺陷和漏洞的补丁；
  * 移植：例如从一个平台迁移到另一个平台，这可能需要对新环境和已变更的软件进行操作测试，或者将来自另一个应用程序的数据迁移到正在维护的系统时进行数据转换测试；
  * 退役，如应用程序到其生命周期结束时，当应用程序或系统退役时，如果需要较长的数据保存时间，则可能需要测试数据迁移或存档。可能还需要在长时间保存后进行恢复规程的测试。此外，可能需要进行回归测试，以确保任何仍在使用的功能依然有效。

对于物联网系统，维护测试可能是由于在整个系统中引入了全新的或经过修改的东西，如硬件设备和软件服务。这类系统的维护测试特别强调不同层面的集成测试(例如网络层面、应用层面和安全方面)，特别是与个人数据有关的方面。
### **2.4.2 维护的影响分析**
影响分析针对维护版本的变更进行评估，以确定变更的预期后果以及变更的可能的副作用，并确定系统中将受变更影响的领域。

影响分析会很困难，常见的一些挑战包括：
  * 规格说明（如业务需求、用户故事、架构）过时或缺失
  * 测试用例没有文档化或过时
  * 没有维护测试与测试依据之间的双向可追溯性
  * 工具支持薄弱或不存在
  * 参与的人员不具备领域和/或系统知识
  * 开发过程中对软件的可维护性关注不够

为了更好的进行维护的影响分析，可以分别从下面两个方面来考虑：
  * 从对已有的业务方面：这个方面的分析主要是从技术方向，针对变更，一方面对新修改、增加的地方进行全面测试；另一方面是分析这些变更对已有的系统的影响，从而确定需要回归测试的范围和深度；
  * 从对已经在使用的用户方面：维护版本发布时，已经有用户在使用该系统了，那么就需要测试系统的变更对已经使用该系统的用户是否造成了不必要的影响。例如，需要对用户数据进行向前兼容等。