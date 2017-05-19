# 领域驱动设计学习（1）

今天学习了领域驱动设计的导学，算是对DDD（Domain Driven
Design）有了一个初步的认识。下面是学习中归纳的一些信息，主要围绕六个问题展开。

> * 1.什么是DDD
> * 2.DDD解决了什么问题
> * 3.领域如何划分
> * 4.聚合和领域之间的关系
> * 5.战略建模与战术建模谁更重要
> * 6.ORM与领域建模

## 1.什么是DDD
Domain Driven
Design，领域驱动设计，那么什么是领域呢？领域就是业务，这里的领域是分层的。大致可以分为：实体、值对象、聚合、领域服务和领域事件等。

## 2.DDD解决了什么问题
解决软件的复杂性问题。

## 3.领域如何划分
按功能划分

## 4.聚合和领域之间的关系
聚合是领域的核心概念，在领域驱动设计中，大的对象实体是由小的对象实体聚合起来的。在想要访问某个小的对象实体时，需要以大的对象实体为入口进行访问。这规定了对象之间的边界，避免了一个对象被很多地方混乱的调用的情况，降低模型的复杂度。（很拗口，不知能不能被理解）

## 5.战略建模和战术建模谁更重要
当然，两个都很重要。但是，可以确定的一点就是，战术更难。讲到战术和战略，就不得不提领域驱动设计经典的两本书。
第一本是04年出版的DDD，它全书是以自下向上的方式写的，从细节的战术开始写，一直到第四部分，才讲到战略。当然，这是因为年代的不同，04年的时候流行自下向上的开发方式。
第二本是13年出版的IDDD，实现领域驱动设计，它采用的是自顶下下的方式，从战略开始写，后面才讲到战术。当然，这是有原因的。到了13年，微服务开始兴起，因此小公司也可以先考虑战略，将整个软件分为几个微服务模块进行开发。
上面两本书的区别也会影响到学习DDD时，如何阅读这两本书的顺序。这个之后再谈。

## 6.ORM与领域建模
ORM和领域建模不是一个东西。ORM其实就是DAO（data access
object），它最多跟领域模型最底部的Repository概念类似，且也不全然相同。可以这么说，Repository可以用ORM实现，但ORM并不是repository。

上述是根据本次技术交流做的总结，有问题请指出，祝进步。
[yaoel](http://yaoel.com)
2017年5月19日

参考：
1.[领域驱动设计](https://www.amazon.cn/dp/B01GZ6T12K/ref=cngwdyfloorv2_recs_0?pf_rd_p=7645736c-6759-4677-9dfb-2a3fd04770aa&pf_rd_s=desktop-2&pf_rd_t=36701&pf_rd_i=desktop&pf_rd_m=A1AJ19PSB66TGU&pf_rd_r=MAEG7SHMD36E23PTFMWH&pf_rd_r=MAEG7SHMD36E23PTFMWH&pf_rd_p=7645736c-6759-4677-9dfb-2a3fd04770aa)
2.[实现领域驱动设计](https://www.amazon.cn/dp/B00IYTVWA6/ref=cngwdyfloorv2_recs_0?pf_rd_p=7645736c-6759-4677-9dfb-2a3fd04770aa&pf_rd_s=desktop-2&pf_rd_t=36701&pf_rd_i=desktop&pf_rd_m=A1AJ19PSB66TGU&pf_rd_r=MAEG7SHMD36E23PTFMWH&pf_rd_r=MAEG7SHMD36E23PTFMWH&pf_rd_p=7645736c-6759-4677-9dfb-2a3fd04770aa)
3.[Domain-Driven-Design-Example](https://github.com/zkavtaskin/Domain-Driven-Design-Example) 
