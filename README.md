# Machine Learning Project Checklist

A collection of steps to help engineers structure machine learning projects.

## Contents

### Project Kick-Off Phase

- User Experience Considerations
  - Why is this a problem?
  - Have a look at existing workflows:
    - Which areas of the current workflow could be improved upon?
    - What impact will these changes have for users?  
  - What should the user experience be?
    - Automation vs. Augmentation
    - Precision vs. Recall
    - Impact of false predictions
    - Potential side-effects

- Engineering Considerations
  - Defining the engineering problem
    - Classification or regression task?
    - What related solutions can I use?
    - How will the solution be deployed?
    - Are domain experts available for this task?
    - Are there any research papers available for this problem?
      - Blogs
      - Academic papers
    - Supervised vs. Unsupervised Learning
  - Data Considerations
    - Data Bias
      - What steps can we take to ensure our model's predictions are fair?
      - Data Privacy and Security concerns
      - Metrics used for model evaluation
    - Do we have the data we need?
      - Document data requirements
    - Do we need more data?
    - Are we going to collect data ourselves?
      - Crowdsourcing
  - Team Considerations
    - Is machine learning a good fit for this solution?
    - Can I solve this using traditional software engineering techniques?
    - What is our minimal accepted model performance?
    - Document decisions and draw up a roadmap to coordinate efforts across teams

### Data Collection Phase

- Engineering Considerations

  - Existing Dataset
    - Is my dataset representational of the problem I am trying to solve?
    - What assumptions were made when creating this dataset?
    - Does the dataset have relevant documentation?
  - Data Collection
    - How will we collect data?
    - How and who will label our data?
    - Do we need to collect more data?
    - Can we use synthetic data?

- Data Exploration Phase

  - Engineering Considerations
    - Data privacy and security
      - What steps can we take to ensure the data we use is stored securely?
      - Which features need to be anonymised?
      - What are the legal implications of using this data?
    - Each feature in dataset should be thoroughly understood
      - What does this feature represent?
      - What data type does it have?
      - Does it have missing values?
      - Does it have outliers?
      - How are the values distributed?
      - Are certain values more frequently present than others?
    - Visualise each feature to explore the dataset
    - Analyse targer variable in supervised learning
      - Is the labelling consistent?
      - Are there missing labels?
    - Inspect the correlations between each feature
    - Document your learnings
    - Automate as much as you can

### Data Preparation Phase

- Engineering Considerations

  - Clean Data
    - Fill or remove missing values
    - Remove rows with outliers
  - Feature Selection
    - Which features are relevant?
    - Can a domain expert help me determine which features are relevant?
  - Feature Engineering
    - What features can I create using existing ones?
    - Can a domain expert help me determine which features to create?
  - Feature Scaling
    - Does my machine learning algorithms require my data to be within a certain range?
  - Data Fairness
    - Does my data reflect the distribution of the real-world?
    - Does my data reflect negative stereotypes?
    - Are there features that indirectly reflect these negative stereotypes?
    - How can we spot historical bias?
    - Are there certain categories that are relevant to my task, that are not in my dataset?
  - Assess whether or not the project can proceed
    - Do we need more data?
    - Do we need other data?
    - Is the data of high enough quality?
    - Are there certain categories that are over-represented?
    - Are there certain categories that are under-represented?
  - Document the data pipeline setup
  - Automate your data pipeline

### Modeling
  -  Baseline Models
    - Train models from different categories and compare performance
      - Which features affect the performance of the algorithm the most?
      - What errors are being made by which algorithm?
   - Feature Selection & Engineering
      - Using this feedback to select new or create new features
      - Repeat process and select top performing algorithms
  - Document learnings
  - Fine-Tuning
    - Use Cross-Validation to tune your models
      - Random Search
      - Grid Search 
      - Bayesian Optimization
    - Ensemble Methods
    - Measure performance against the test dataset
    - Document learnings 
- Minimal-Viable-Model
- Hyperparameter Tuning
- Testing

- Deployment
