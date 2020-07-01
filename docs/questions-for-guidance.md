# Questions for guidance

The questions below are intended to serve as guidance in the process of attaining the appropriate data for solving
a business problem.

## What problem are you trying to solve?

The characteristics of the problem you set out to solve dictates the requirements on the data needed to solve it.
Thus, the specification of the problem is crucial for understanding the requirements on the data in terms of, e.g., 
training data, and the need for manual labelling of evaluation or validation data.

When specifying the problem, make sure to focus on the actual business need that is to be fulfilled, as opposed to 
a technology to solve the problem. Try to make all assumptions about the business need explicit; write them down, and
make sure to vet the assumptions thoroughly with the stakeholders to have them sign-off on a common understanding of
the problem.

As with everything else, you should expect to iterate on the specification of the problem, and as the process proceeds,
the adjustments to the specification will become smaller.

Having a detailed and agreed-on specification of the business need and problem is crucial since seemingly subtle details
may have a large impact on the space of possible techniques to actually solve the problem. For instance, if the 
stakeholder is expecting an implemented solution to extract, rank, and present passages from long documents 
with sub-second latency to a user, from a data point-of-view you have to know whether the document set is expected to 
change continuously, what format the documents are in, and what information there are to guide the learning-to-rank
process. Only when you know the characteristics of the data, it will be possible to come up with a candidate 
technological approach to solve the problem.

## What data do you need to solve it?

## What data are actually available to you?

What does "available to you" mean? There is a difference between knowing that there is data to be had, and actually having
the appropriate access to the right data at the right time. The Data Readiness Levels framework provides a good 
way of talking to stakeholders, both data owners and business problem owners. For data to be useful in 
an NLP project setting, it has to be 

* available in the sense that it is exists on a digital medium somewhere, such as in a data lake or a database.
 (Band C, in Data Readiness Level parlor),
* accessible
* validated

## How do you know if you have succeeded in solving the problem?

Test data set and validation data set.
 
## Is the problem possible to solve using unsupervised methods?

## Do you need annotated data?
  - Availability of experts
  - Tooling
  - Quality control
 
 Proxy tasks and available data?
 
 The annotation of the data must be at the same level of abstraction as is operated on by the technology for 
 implementing a solution. Compare: annotations at the document level will not help when building an event detector.