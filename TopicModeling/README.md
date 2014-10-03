## Topic Modeling:


- [Topics over Time: A Non-Markov Continuous-Time Model of Topical Trends](tot-kdd06.pdf) [![Example](totkdd06.jpg)](https://raw.github.com/yning/papers/TopicModeling/master/totkdd05.jpg)
  - Summary: A variant of LDA model trying to capture the topical trends. The mixture distribution over topics is influenced by both word co-occurrences and the document’s timestamp. Timestamp for each word is the same with that document. 
  
  - Draw T multinomials &phi;<sub>z</sub> from a Dirichlet prior &beta;, one for each topic z;
  - For each document d, draw a multinomial &theta;<sub>d</sub> from a Dirichlet prior &alpha;, then for each word w<sub>di</sub> in document d:
    - Draw a topic z<sub>di</sub> from multinomial &theta;<sub>d</sub>;
    - Draw a word w<sub>di</sub> from multinomial &phi;<sub>z<sub>di</sub></sub>;
    - Draw a timestamp t<sub>di</sub> from Beta &psi;<sub>z<sub>di</sub></sub>;
  - They use Gibbs Sampling to perform approximate inference and evaluate their model on 3 dataset: NIPS papers(17 years: 1987-2003), A Researcher's Emails(9 months), State-of-the-Union Addresses(21 decades) and compare TOT to LDA. Also, they use topic distributions of documents to predict timestamps. Number of topics T is fixed to be 50. &alpha;=50/T, &beta; = 0.1.

- [Modeling Flu on Twitter using Temporal Topic Models]()
  - Summary: This paper proposes temporal topic models to capture hidden states of a user from his tweets and aggregate states in a geographical region for better estimation of flu trends. They define states of flue and combines the states as a hidden random variable into the temporal topic graphical models. 