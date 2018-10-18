# Pseudo Textbook
### an annotated list of useful reading materials for data science, math, and machine learning

#### Neural networks
1. [The Deep Learning Book](http://www.deeplearningbook.org), things of note:
    * The introduction gives a good overview of the history and motivation behind neural networks
    * Part 1 helps guide you through necessary mathematical foundations (that are generally useful beyond just neural networks)
    * Part 3, Monte Carlo methods may be useful to look through as well
    * Remaining parts (esp. those concerning the various architectures) may be best skimmed through for ideas, as a hands-on practical approach (e.g. deeplearning.ai) may be more fruitful at first. 
  
2. [deeplearning.ai](https://www.deeplearning.ai/): Andrew Ng's Coursera course on neural networks
    * Course 3, "Machine Learning Projects", is possibly the most useful for general, practical considerations when trying to solve any data science problem
    * Course 2, "Improving Deep Neural Networks, Hyperparameter tuning, Regularization and Optimization", is the next useful (again, with respect to practical use of neural networks)
    * The remaining courses give solid foundations for understanding the most popular network architectures
    * Generally, the quizzes are useful to save for future reference when you need to quickly review concepts of neural networks or general practical considerations for solving data problems
  
#### Data science  
1. [Data Science Interview Questions & Detailed Answers](https://rpubs.com/JDAHAN/172473): a cheat sheet of sorts to review common knowledge for data science practitioners
2. [ModeAnalytics](https://modeanalytics.com): a useful resource for learning and honing SQL skills, also has useful case studies
   * see also [Visual JOIN](http://joins.spathon.com/) to wrap your head around table joining
3. Andrew Ng's [Machine Learning](https://www.coursera.org/learn/machine-learning) course on Coursera: basic principles of common / classic machine learning (and incidentally, data analysis) methods, as well as motivation and practical use tips
4. Honing programming skills with [LeetCode](https://leetcode.com/problemset/algorithms/): the problems you solve are completely irrelevant to data science, but this is a good resource to help you program more efficiently and make robust algorithms.
5. I probably need to add something related to data engineering / data cleaning here, although I feel like these are sometimes secondary to actually solving the data problem / answering the data question. 

#### Useful math / stats / probability concepts
1. [Bayesian inference](https://brohrer.github.io/how_bayesian_inference_works.html): a simple primer
2. [Markov chain Monte Carlo (MCMC)](https://github.com/CamDavidsonPilon/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers) methods, in the context of Bayesian methods: accessible (but deeper) primer on Bayesian methods, with added benefit of learning MCMC
3. [Linear algebra tutorial quickie](https://www.analyticsvidhya.com/blog/2017/05/comprehensive-guide-to-linear-algebra/): if you're short on time and patience, start here. Simple matrix operations (what is a matrix, basic arithmetic) you probably know. But things unique to linear algebra (trace, SVD, inverse, eigenvalues) need to be learned.
   * note that SVD is NOT covered in this post
   * one sticking point for me with this (and other more formal texts, e.g. [MIT OpenCourseWare](https://ocw.mit.edu/courses/mathematics/18-06sc-linear-algebra-fall-2011/least-squares-determinants-and-eigenvalues/eigenvalues-and-eigenvectors/), or [Wolfram Mathworld](http://mathworld.wolfram.com/Eigenvector.html)) was with computing eigenvectors. Namely, if `(A−Iλ)x = 0`, where `A` is our square matrix, `I` is the identity matrix, `λ` is our eigenvalue, and `x` is our eigenvector; then it's not immediately clear why the matrix `A−Iλ` must be singular. It's clear that we want / are only interested in a nonzero eigenvector, `x`, so `x` can't be 0. It's also clear that if `A-Iλ` was singular, its determinant would be zero, allowing us to solve for `λ` (and subsequently `x`). After searching, the intuition that made most sense was conveyed in this [StackExchange comment](https://math.stackexchange.com/questions/2619022/why-can-the-determinant-be-assumed-to-be-0#comment5957261_2885009): let's assume `A-Iλ` is some other matrix `M`; our equation becomes `Mx = 0`. If `M` *were* invertible, then we can divide each side by `M` to solve for `x`: `M^-1*M*x = M^-1*0` (because only invertible matrices have inverses). But since `M^-1*M` is just `I` (an identity matrix), then we get `x=0`, which is not what we want. So the only other alternative must be that `M` is noninvertible, i.e. is singular. Thus `A-Iλ` must be singular.
4. [Applied math and machine learning basics, starting with linear algebra](https://www.deeplearningbook.org/contents/linear_algebra.html): ...else if you have time, can bring yourself up to speed with linear algebra and other useful topics here
5. Entropy (information theory): [accessible primer for intuition of Shannon entropy formula](https://medium.com/udacity/shannon-entropy-information-gain-and-picking-balls-from-buckets-5810d35d54b4). 
   * And here's [a more detailed primer](http://www.win-vector.com/blog/2011/09/the-equivalence-of-logistic-regression-and-maximum-entropy-models/) about how maximum entropy models (that is, those that build a model given the data, and assume all else to be equal probability (i.e. have maximum uncertainty / information / entropy) end up taking the same form of (i.e. are exactly) multi-class logistic regression models.
5. Generally, [Math on StackExchange](https://math.stackexchange.com) and [Wolfram Mathworld](http://mathworld.wolfram.com) are useful supplemental resources to clarify esoteric sticking points in understanding ([e.g.](https://math.stackexchange.com/questions/52717/column-vectors-orthogonal-implies-row-vectors-also-orthogonal) why must / when is a matrix with columns of orthogonal eigenvectors necessarily have orthogonal rows and thus be an orthogonal matrix?) and clear mathematical ground truth, respectively. I've found Wikipedia to actually be less clear and harder to follow -- even sometimes if you just want a quick definition.

#### Case studies
i.e. things to help you think about and solve data problems
1. Course 3 from [deeplearning.ai](https://www.deeplearning.ai/)
2. Some of the questions on the [data science cheat sheet](https://rpubs.com/JDAHAN/172473)
3. [ModeAnalytics' SQL analytics training](https://community.modeanalytics.com/sql/tutorial/sql-business-analytics-training/)
