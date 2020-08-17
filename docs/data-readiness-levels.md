# Data Readiness Levels

The notion of [Data Readiness Levels](http://data-readiness.org/) (DRL), introduced by Lawrence 
([2017](https://arxiv.org/abs/1705.02245)), provides a way of 
talking about data much in the same way [Technology Readiness Levels](https://en.wikipedia.org/wiki/Technology_readiness_level) facilitate 
communication regarding the maturity of technology. As such, it is a framework suitable for
exchanging information with stakeholders regarding data **accessibility**, **validity**, and **utility**.

The table below illustrates the three different major Bands of the DRL:s. Each band can be thought of as consisting of multiple
levels. At the lowest level, Band C, level 4, someone has heard that there is data to be had. This "hearsay" level is
often where a new project starts — someone knows that there should be data available to work with. Since the access
to data often dictates the bounds of possible analysis, and thus the level of results attainable, walking a new project
or stakeholder through the DRL:s is not only a nice-to-have, it is a must-do. If there is no data to work with, it does
not matter what kind of algorithms are available.

![Data Readiness Levels table](img/drl-table.png)

* **Band C** concerns the **accessibility** of data. All work at this level all serves to grant the team 
intended to work with the data access to it. One of the major challenges faced within NLP is the conversion of
documents from a source format, e.g., PDF, Word or Excel, to a format suitable for addressing the task at hand. 
In order to move beyond Band C, data conversion and encoding have to be in place, and the resulting data should be
possible to work with in the analysis software of choice, such as Python, R or Matlab. 

* **Band B** concerns the **validity** of data. In order to pass Band B, the data has to be valid. ...

* **Band A** concerns the **utility** of data. The utility of the data concerns the way in which the data is intended to be
used. ...

Note that the Data Readiness Levels should be interpreted with respect to a given task: data that is at Band A 
for the task of, e.g., training a large Transformer network, might be considered Band B if the task instead concerns the
 evaluation of an existing event resolution system, simply because the requirements on the data are different in the 
 two tasks. In the first task, it is enough if the data is clean and representative of the domain, while in the second
 task it has to be annotated with the appropriate event information. 




## Resources

* [Data Readiness](http://data-readiness.org/)
* [FAIR](https://www.go-fair.org/fair-principles/)