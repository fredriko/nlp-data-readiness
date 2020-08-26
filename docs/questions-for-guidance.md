# Questions for guidance

The questions below are intended to serve as guidance in the process of attaining the appropriate Data Readiness Levels for solving
a research or business problem related to NLP.

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
way of talking to stakeholders, both data owners and business problem owners. Being "available" in this context, means
that the data is at Band B or above, as discussed [here](data-readiness-levels.md).

With data at Band B, you will most likely be able to form working hypotheses about the suitability of the data with
respect to the problem you are trying to solve. For example to gauge whether the data contains the information you need;
the amount of data is sufficient; or there are any legal constraints for using the data.


## Are you allowed to use the data available?

The legal aspects of using the data depend on many things. As such, the legalities should be considered a primary citizen
of the Data Readiness Level assessment with respect to your particular challenge. Make sure you involve the appropriate 
legal competence early on in your project. Matters regarding, e.g., personal identifiable information, and 
GDPR have to be handled correctly. Failing to do so may result in a project failure, even though all technical aspects 
of the project are perfectly sound.


## What data do you need to solve the problem?

Given the insight into what data is available, ask yourself the questions: 

* What data do you need to solve the problem?
* Is that a subset of the data that is already available to you?
* If not: is there a way of getting all the data you need?

If there is a discrepancy between the data available, and the data required to solve the problem, that discrepancy
has to be mitigated. If it is not possible to align the data available with what is needed, then this is a cue to
go back to the drawing board and either iterate on the problem specification, or collect suitable data. 
Perhaps there are other ways to solve the business or research need than what has been specified so far?


## How do you know if you have succeeded in solving the problem?

When you are in the process of defining and specifying the problem to solve, you should also consider how to evaluate
the potential solutions to the problem. 

The type of data required to evaluate a solution is often tightly connected to
the way the solution is implemented: if the solution is based on supervised machine learning, i.e., requiring labelled examples, 
then the evaluation of the solution will also require labelled data. For example,
if the problem you face is to help users to find topically relevant sections in a large number of yearly reports
submitted by public agencies, then you will most likely need to construct a collection of sections labelled with the 
appropriate topic descriptors. Such data can then be used to assess and compare the technical solutions you come up with. 

On the other hand, if it is possible to produce a
solution based on unsupervised machine learning, then *perhaps* it is possible to conduct the evaluation based on 
unlabelled data too (although it is far from certain).

In any case, if the solution depends on labelled training data, the process of annotation usually also results in the 
appropriate evaluation data.

Any annotation effort should take into account:

* **The quality of the annotations**. The agreement between the annotators working on the data, aka the inter-annotator
 agreement, provides a good starting point for assessing the quality of the annotations overall. The reasons 
 for low inter-annotator agreement can be related to, e.g., 
 unclear annotation guidelines, difference in expertise among the annotators, that the task is simply too hard, or a 
 combination of all of the above. The annotations produced should be carefully monitored with respect their quality. 
 Deviations in quality over time should be analyzed so as to facilitate mitigation of a potential decrease in the capabilities of the
  model that relies on the annotated data for training. 
* **Temporal aspects of the data characteristics**. How often do the distribution of the data to learn from change, i.e.,
how often do we need to produce new annotations? When do we know that we need newly annotated data?
* **Representativity of the data**. Is the data annotated really suitable for the task at hand? Does it reflect the way
users interact with the system?

Obtaining the training, evaluation, and validation data is at the core of producing a machine learning-based solution to
a problem. The quality of the data sets the upper bound to what can be achieved by the learned functionality. Also included
in the production process are issues such as model selection, setting up infrastructure for machine learning, continuously
monitoring the solution's performance for decrease in performance, etc. A good overview of the end-to-end process is presented in the 
book [Building Machine Learning Powered Applications: Going from Idea to Product](https://mlpowered.com/book/).



 



