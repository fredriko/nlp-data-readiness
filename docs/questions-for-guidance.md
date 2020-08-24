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

## What data are available to you?

What does "available to you" mean? There is a difference between knowing that there is data to be had, and actually having
the appropriate access to the right data at the right time. The Data Readiness Levels framework provides a good 
way of talking to stakeholders, both data owners and business problem owners. For data to be useful in 
an NLP project setting, it has to be... 

* available in the sense that it is exists on a digital medium somewhere, such as in a data lake or a database.
 (Band C, in Data Readiness Level parlor),
* accessible
* validated

## Are you allowed to use the data available?

Make sure you involve the appropriate legal competence early on in your project. Matters regarding, e.g., 
personal identifiable information, and GDRP have to be handled correctly. Failing to do so may result in a project
failure, even though all technical aspects of the project is perfectly sound.

## What data do you need to solve the problem?

Given the insight into what data is available, ask yourself the questions: 

* What data do you need to solve the problem?
* Is that a subset of the data is available to you?
* If not: is there a way of getting all the data you need?

If there is a discrepancy between the data available, and the data required to solve the problem, that discrepancy
has to be mitigated. If it is not possible to align the data available with what is needed, then this is a cue to
go back to the drawing board and iterate on the problem specification. Perhaps there are other ways to solve the business
need than what has been specified so far?


## How do you know if you have succeeded in solving the problem?

Test data set and validation data set. Possibly evolving over time, in accordance with the overall system, including
annotation, training, monitoring for domain drift and decrease in system performance.  

## Do you need annotated data?

If the solution to the problem involves supervised learning, or assessment of performance based on human labelled data,
then you need to obtain annotated data. 


  - Availability of experts
  - Tooling
  - Quality control
 
 Proxy tasks and available data?
 
 The annotation of the data must be at the same level of abstraction as is operated on by the technology for 
 implementing a solution. Compare: annotations at the document level will not help when building an event detector.
 
 ## Resources

### General
  
 * [Data Readiness Levels](https://arxiv.org/abs/1705.02245)
 * [Building Machine Learning Powered Applications: Going from Idea to Product](https://mlpowered.com/book/)
 
 
 ### Text annotating tools


