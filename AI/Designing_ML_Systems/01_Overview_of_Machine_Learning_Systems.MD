**Chapter 01: Overview of Machine Learning Systems**
-
* The algorithm is only a small part of an ML system in production.
* Ops in MLOps comes from DevOps short for development and operations.
* including deploying, monitoring, and maintaining it.
* MLOps is a set of tools and best practice for bringing ML into production.
* ML systems design takes a system approach to MLOps, which means that it consider an ML system holistically to ensure that all the components. 
* their stakeholders can work together to satisfy the specified objectives and requirements.
* Algorithms might become outdated quickly as new algorithms are constantly being developed, but the framework proposed still work with new algorithm.

**When to Use Machine Learning**
-
* ML is not a magic tool that can solve all problems!
* Before starting an ML project, you might want to ask whether ML is neccessary or cost-effectiv.
* Machine Learning is an appraoch to: "learn complex patterns from existing data and use these patterns to make predictions on unseen data"

**1. Learn: The system has the capacity to learn**
* A relational database isn't an ML system because it doesn't have the capacity to learn.
* For an ML system to learn, there must be something for it to learn from. In most case, ML sysyem learn from data.
* In supervised learning, based on example input and output pairs, ML systems learn how to generate outputs for arbitrary.

**2. Complex Patterns: There are patterns to learn, and they are complex**
* ML Solutions are only useful when there are patterns to learn.
* However, there are patterns in how stocks are priced, and there fore companies have invested billions of dollars in building ML systems to learn those patterns.
* Whether a pattern exists might not be obvious, or if patterns exits, my dataset or ML algorithms might not be sufficiet to capture them.
* For example, A pattern in how Elon Musk's tweets affect cryptocurrentcy prices.
* ML has been very successful with tasks with complex patterns such as object detection and speech recognition.
* Many tasks that hard to for humans to do are easy for machines, such as raising a number of the power of 10.
* Many tasks that are easy for humans can be hard for machine, such as deciding whether there's a cat in a picture.
* (Inputs + Patterns) + Traditional software = Outputs
* (Inputs + Outputs) + Machine Learning = Patterns

**3. Existing data: data is available, or it's possible to collect data**
* Building a model to predict how much tax a person should pay a year, I must have access to tax and income data of a large population.
* Zero-shot learning or zero-data learning: it's possible for ax ML system to make good predictions for a task without having been trained on data for that task.
* This ML system was previously trained on data for other tasks, often related to the task in consideration.
* but somehow the system doesn't need data for the task at hand to learn from, it still requires data to learn.
* In the context of continual learning, ML models can be deployed without having been trained on any data, but they will learn from incoming data in production.
* (Serving insufficiently trained models to uses comes with certain risks, such as poor customer experience)

**4. Predictions: it's a predictive problem**
* ML models make predictions, so they can only solve problems that require predictive answers.
* ML can be appealing when you can benefit from a large quantity of cheap but approximate predictions.
* prediction = estimate a value in the future.
* As predictive machines or ML models are becoming more effective, more and more problems are being refraned as predictive problems. regardless of whether the question is about something in the future, the present, or even the past.
* Frame it as "What would the outcome of this process look like?"

**5. Unseen data: unseen data shares patterns with the training data**
* The patterns your model learns from existing data are only useful if unseen data also share these pattern.
* The unseen data and training data should come from similar distributions.
* "If the data is unseen, how the hell do we know what distribution it comes from? = We can make assumptions and hope that our assumptions hold.
* ML solutions will shine if the problem has these additional characteristics:

    **5.1: It's repetitive**
    * Mosy ML algorithms require many examples to learn a pattern. 
    * When a task is repetitive, each pattern is repeated multiple times, which makes it easier for machines to learn it.

    **5.2: The cost of wrong prediction is cheap**
    * Your model is going to make mistakes.
    * ML is suitable when the cost of a wrong prediction is low. for example, the recommender systems
    * The benefit of correct predictions outweigh the cost of wrong predictions.
    * Algorithmic of self-driving car making a mistakes could cause to death.

    **5.3: It's at scale**
    * "At scale" means different things for different tasks, but in general, it means making a lot of predictions.
    * A problem might appear to be a singular prediction, but it's actually a series of predictions.
    * For example, A model that predicts who will win a US presidential election seems likel it only makes one prediction every four years, but it might actually be making a prediction every hour ir even more frequently because that prediction has to be continually updated to incorporate new information.
    * Having a problem at scale also means that there's a lot of data for you to collect, which is useful for training ML models.

    **5.4: The patterns are constantly changing**
    * Culture change. Tastes change. Technologies change. What's trendy today might be old news tomorrow.
    * Figuring how your problem has changed so that you can update rules.
    * ML model learn from data, you can update it with a new data.
    * It's important to set up your system to adapt to the changing data distributions.

**6. Most of today's ML shouldn't be used under any of the following conditions**
* It's unthical.
* Simpler solutions do the trick.
* It's not cost-effective.

Break the problem into smaller components is key.
If you wait for the technology to prove its worth to the rest of the indusry befire jumping in, you might end up years or decades behind your competitors.

**Machine Learning Use Cases**
-
* ML is important in the era of informations and services.
* Search engine / Recommender system
* Amazon and Netflix search results in mostly ML. recommended items that are predicted to best match people taste and style.
* Your smart phone is assisting you in many of your daily activities predictive typing: predict what you mgiht say next.
* ML translations: automatically translating from one language to another.
* Smart security cameras can let you know when your pets leave home or watch your old parents.
* Enterprise ML application is the main and requires stricter accuracy but flexible on latency.

ML Applications in enterprises are diverse:
1. Internal use cases: reducting costs, generating customer insights and intelligence, internal processing automation.
2. External use cases: improving customer experience, retaining customers, interacting with customers.

"Fraud Detection" is the oldest applications of ML in the enterprise world.
Building a system that learn from historical fraud transactions and predict whether a future transaction is fraudulent.

"Price Optimization" is the process of estimating a price at a certain time perioud to macimize a defined objective function, such as the company's margin, revenue, or growth rate.s
To run a business, it's important to be able to forecast customer demand so that you can prepare a budget, stock inventory, allocate resources, and update pricing strategy.

"Churn Prediction" is predicting when a specific customer is about to stop using your products or services so that you can take appropriate actions to win them back.
Churn prediction can be used not only for customers but also for employees.

"Brand Monitoring" It's important to monitor how the public and your customers perceive your brand. 
If there's a negative sentiment in your brand, you might want to address it as soon as possible.
Sentiment analysis is a typical ML task.

"ML in Healthcare" detecting skin cancer and diagnose diabetes.

**Understanding Machine Learning Systems**
-
**1. Machine Learning in Research Versus in Production**
* Yes, they're different.
* Different stakeholder and requirements
* The most common objective is model performance, develop a model that achieves the state-of-the-art results on benchmark datasets.
* Different requirements leads to conflicting, conflicting leads to make it hard to design, develop, and select an ML model that satisfies all the requirements.
* Tips: develop one model for each objective and combine their predictions.
* It's important to understand all requirements from all stakeholders involved and how these requirements are.

Production having different requirements from research is one of the reason why successful reseach projects might not always be used in production.
Ensembling combines "multiple learning algorithms to obtain better predictive performance than could be obtained from any of the constituent learning algothms alone.

The ensembling tends to make a system too complex to be useful in production: slower to make predictions or harder to interpret the results.
For many tasks, a small improvement in performance can result in a hugh boost in revenue or cost saving.

Complex models must perform significantly better to justify the complexity

**2. Critism of ML Leaderboards**
Benchmarks have helped drive advances in Natural Language Processing or NLP by incentivizing the creation of more accurate models at the expense of other qualities valued by practitioners such as compactness, fairness, and energy efficiency.

* Rookies mistakes = Focusing too much on the model development part and not enough on the model deployment and maintenance part.
* The validation data is mostly smaller than the training data.
* During development phase, training is the bottlenect. The model has been deployed phase, inference is the bottleneck.
* Latency = the time it takes from receiving a quary to returning the result. Referring to the duration that a request is waiting to be handled. response time.
* If the average latency is 10 ms, it takes 10 ms to process a quary, the throughput is 100 queries/second.
* if the average latency is 100 ms, the throughput is 10 quesries/second.
* FPS = The higher the better, The latency = the lower the better.

Once the model is deployed, the latency matters a lot.
More that 60% of mobiles users will leave a page if it takes more than 3 seconds to load.

To reduce latency in production, you might have to reduce the number of queries you can process on the same hardware at a time.
The latency is not an individual number but a distribution. but this number can be misleading.

We can check by looking at the percentiles.
* The most common are 50th percentile or the median.
* Higher percentiles also help you discover outliers, by looking at 90th or 95th or p90 or p95
* Higher percentiles are important to look at because even though they account for a small percentage of your users, sometimes they can be the most important users!
* on the Amazon website, the customers with the slowest requests are often those who have the most data on their accounts because they have made many purchases. that's the most valuable customers.
* It's a common practice to use high percentiles to specify the performance requirements for your system.

**3. Data**
