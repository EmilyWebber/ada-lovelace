# Defining optimal compute environment

### Optimal is a question of user preferences. This can range from:
1. Lowest dollar amount
2. Fast performance 
3. Reliable, predictable results
4. High modeling performance

In machine learning, this is a challenging question for both model development and model deployment. 

### In model training
- we want the absolute fastest response for the lowest dollar value. We’d also like assurance that the model result doesn’t change based on type of compute environment.

### In model deployment 
- We need to pick the bandwidth size of the instance to respond to our latency SLA
- We also need to pick the amount of memory on the instance to accommodate both the size of the model, and the amount of data that will be hitting the model within a single request

### We need to re-run our analysis every time:
- A new type of EC2 instance is launched, such as the elastic inference or the arm-based R machines
- A new version of EC2 instance is released, such as every year at re:Invent 
- A new model is deployed to the endpoint 

### Compute Needs Differ
When we're deploying a feature engineering strategy, vs a model running inference, compute needs can be vastly different. We want our system to be optimal under both patterns.

# Minimal Demonstration 
We propose building a system that, for a single set of data, can identify the most optimal EC2 instance for both training and inference. We anticipate using reinforcement learning for this.  