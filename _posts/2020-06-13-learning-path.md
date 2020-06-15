---
title: 'Choosing a learning path'
date: 2020-06-12
permalink: /posts/2020/06/blog-post-2/
tags:

---
**It has been almost 2 years since I graduated from college.** I curiously dabbled in finance for a short while as though I had something to prove, before returning back to work in data science. Like how some linguistic experts claim that being bilingual from a young age helps to inculcate greater open-mindedness towards different cultures, I strongly believe in the benefits of pursuing multiple domains concurrently, because life would be too boring if we do only one thing at a time. **At the moment, I am a data scientist specialising in product analytics, which entails the use of experimentation and statistics to make critical product decisions - think A/B testing, statistical modelling, insights generation, etc.**

[Wikipedia](https://en.wikipedia.org/wiki/A/B_testing) provides a good infographic illustrating a common use case for A/B experimentation:

<p align="center"><img src="/images/abtesting_example.png" title="A/B Testing" width="500" height="300" /></p>

**More often than not, A/B testing involves far more than superficial UI changes.** It may be used to test variations in search/ranking algorithms, entire user experience flows, product pricing, and even for evaluating system performance and stability. Analytics work requires a technology stack accorded only to mature companies with more developed data infrastructure and sufficient engineering resources to build experimentation platforms. While commonplace in mature technology hubs like Silicon Valley and Shen Zhen, I would not say that product analytics is a critical research function for most technology start-ups, as there are valid logical and domain constraints inhibiting adoption:

1. **Scale**: The service must receive sufficient data beyond a threshold volume (in the range of millions of clickstream events per day) to make infrastructure investments worthwhile. Each analytics-driven decision should drive financial impact of at least millions of dollars.
2. **Industry**: As an indirect requirement of achieving scale, companies with product analytics functions tend to be consumer facing, with millions of daily active users. Enterprise-facing companies like Slack or Atlassian would have found qualitative user research and intuition sufficient to obtain actionable feedback to product.
3. **Cost**: A dedicated data engineering and internal tools product team would typically be required to develop and maintain data infrastructure for insights generation. This is a luxury that most early stage, inadequately-funded startups would not be able to afford.

Given the above, knowledge expertise on product analytics and experimentation in Southeast Asia would naturally be concentrated in only a handful of e-commerce, fintech and logistics companies. The same probably holds true for Silicon Valley, New York and London, but in those places the scale of industry is perhaps multiplied by a factor incorporating greater product diversity, heightened consumerism and the difference in market economics.

**It may take at least a decade before Southeast Asian technology companies start to approach the level of technological maturity seen in the developed western world, and for us to see an elevated uptake of experimentation principles in product management and development.** However, I am not a fan of waiting for things to happen - which brings me back to my first point of the inclination to embark on a parallel learning path. Any chosen learning path should bolster my existing capabilities in product analytics and experimentation, but also provide more leeway to apply statistical concepts to a broader field. **Machine learning** is a strong candidate, but it has been over-popularised by universities, governments and interest groups in recent years - leading to an influx of students and enthusiasts attempting to enter the field. **At Oxford, machine learning was taught as part of an information engineering specialisation, and classes were specifically focused on linear algebra and statistical theory from an academic perspective.** Compared to the wide array of online 'machine learning' courses found on Coursera and Datacamp, traditional machine learning theory had much less emphasis on what libraries (i.e. Tensorflow, SciPy, scikit-learn) we should use, but on how we understand and manage intrinsic complexities in linear algebraic computations that drive the underlying machine learning algorithms. For Masters/PhD graduates who spent years researching the art of statistical learning, they suddenly find themselves perceivably competing for jobs against business students with colourful machine learning certifications lining their LinkedIn profiles.

**In the spirit of social distancing, let's not enter a crowded space.** Drawing some inspiration from my 4th year engineering thesis in epidemiological Bayesian Modelling, I envision **time-series modelling** to be a fundamental academic field with a large myriad of scientific applications - ranging from product performance forecasting, econometrics, epidemiology, to quantitative research in finance. From my current experience, about 30% of product analytics workflows require some level of time series analysis, which may be applied to product metrics monitoring and forecasting, churn models and changepoint detection. Product impact sizing, when executed properly, may sometimes even call for a justifiable model of sales/revenue forecasting, which can then be used to inform product prioritization and engineering resource allocation.

**Looking up the field briefly, I collate a couple of common concepts and models below:**
1. Random Walk and White Noise, Augmented Dickey-Fuller Test
2. Autocorrelation
3. Auto-Regressive Moving Average Models
4. Linear Regression
5. Cointegration between two or more time series
6. Generalized Autoregressive Conditional Heteroskedasticity (GARCH) Process Models (quite a mouthful)
7. Nonlinear Models
8. Multivariate Time Series Models
9. State Spaces Models and Kalman Filtering

**Not surprisingly, some of these concepts actually coincided with my information engineering curriculum at Oxford.** Linear and multivariate models should easily be found in any data scientist's toolbox. Kalman filering was taught in 4th year as part of probabilistic control theory and control systems engineering - forming a critical component of vehicular guidance systems such as in F-1 racing. Considering my prior education in information engineering and signals processing, I shall rightfully aim to understand and master the above concepts in a period of 4-6 weeks. Given the current context of the pandemic, it may be insightful to perform some time-series analysis on epidemiological trends using published statistics. This should shed some light on some medical jargon (i.e. *R0*) being thrown around by the media, and inform my own perspective on the state of things.

