**Chapter 02: Introduction to Machine Learning System Design**
-
* If the system is built for a business, it must be driven by business objectives, that gonna be guiding the development of ML models.
* 4 requirements: reliability, scalability, maintainabilty, and adaptability.
* The difficulty of your job can change significantly depending on how you frame your problem.

**Business and ML Objectives**
-
* Consider the objectives of the proposed ML projects.
* EX. The matrics they can measure about the performance of their ML models such as accuracy, F1 score, inference latency, etc.
* The company cares only moves some business metrics: "Maximize profits for shareholders either directly or indirectly" (increasing sales revenue, cutting costs, higher client satisfactory, lower times spent on the production.)
* Business Performance
* A percent increase in the recommender system's predictive accuracy led to a certain increase in purchase-through rate.
* Many companies create their own metrics to map business metrics to ML metrics.
* Double-Sword: The effect of an ML projecto on business objectives can be hard to reason about (It can make your client spend more money on it or spend less money on it)
* Experiments like A/B testing and choose the model that leads to better business metrics regardless of whether this model has better ML metrics. but it's not accurate 100%.
* When evaluating ML solutions through the business lens, it's important to be realistic about the expected returns.
* Google has been investing in ML for decades to be this successful.
* Google: Search better, sell more ads, improve translation quality, and build better android applications.
* The longer I have adopted ML, the more efficient my pipeline will run, the faster the development cycle will be, the less time I will need it, and the lower bills will be.

**Requirements for ML Systems**
-
* The specified requirements for an ML system vary from use case to use case.

**1. Reliability**
* The system must continune to perform the correct function at the desired level of performance even in the face of adversity (hardware or software faults, and even human error.)
* ML systems can FAIL silently. End users don't even know that the system has failed and might have kept on using it.

**2. Scalability**
* It can grow in complexity: 1GB of ram today -> 16GB of ram in the future.
* It can grow in traffic volume: user base grows. the number of prediction requests of ML system grows too.
* It can grow in ML model count:  one model for one use case.
* How to solve it basically?: Expanding the resouces to handle growth or reducting the resources when not needed.
* 100 GPUs could cost a lot -> reduce it to 30 GPUs for this case.
* Many cloud services is autoscaling but could be a little tricky to implement.
* Artifact Management is also important: one model is fine but one hundread models? Automated it.

**3. Maintainability**
* There are many people who will gonna work on an ML system. Different backgrounds. Different tools and skills.
* It's important: I need to structure my workloads and set up my infrastructure in such a way that different contributors can work using tools that they are comfortable with, intead of one group of contributors forcing their tools onto other groips.
* Everything must be documented, versioned, and reproducible (Code, Data, Artifacts)

**4. Adaptability**
* The system should have some capacity for both discovering aspects for permance improvement and allowing updates without service interuption.
* Data change quickly -> ML systems must be able to evolve quickly as well.

**Iterative Process**
-
* It's an never ending process. Continually monitored and updated.
* The process looks more cycle than a traditional ML. Beyond just collect data, train a model, deploy a model, and done.
* (1.) Project Scoping = Laying goals, objectives, identified and involved stakeholders, resources allocation.
* (2.) Data Engineering = Handling data from different sources and formats.
* (3.) ML model development = Extracting features and develop initial models leveraging these features.
* (4.) Deployment = Made it accessible to everyone
* (5.) Monitoring and Continual Learning = Monitored and maintained to be adaptive to changing environments
* (6.) Business Analysis = Business goals and analyzed to generate business insights.

**Framing ML Problems**
- 
* defined by inputs, outputs, and the objective function that guides the learnging process
* The objective function is to minimize the difference between the predcited department and the actual department.

**Types of ML Tasks**
-
* The output of your model dictates the task type of my ML problem

**1. Classification Versus Regression**
* Classification models classify inputs into different categories.
* Regression models can easily be framed as a classification model and vice versa.

**2. Binary Versus Multiclass Classification**
* The fewer classes there are to classify, the simpler the problem is
* Dealing with binary classification problems is much easier than dealing with multi-class problems.
* When the number if classes is large, hierachical classification might be useful.

**3. Multiclass versus Multilabel Classification**
* Treat it as i would a multiclass classification.
* The second approach is to turn it into a set of binary classification problems.
* Multilabel means that the number of classes an example can have vaties from example to example.

**4. Multiple Ways to Frame a Problem**
* Changing the way I frame my problem might make my problem significantly harder to easier.
* I might have to retrain my model from scratch, or at least retrain all the components of your model whose number of parameters depends on it.
* Maybe build a new framing for a every new inputs for new features could help this.

**Objective Functions**
-
*