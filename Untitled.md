Language Modeling (LM)

Language models (LMs) serve to estimate the likelihood of different words or phrases relative to others, enhancing various NLP applications. Most LM-based models utilize probabilistic inferences to gauge the probability of upcoming words the user might input, or to assess the likelihood of specific words or phrases within existing data.

![[Pasted image 20240319020725.png]]

where \( n \) represents the total occurrences in the given data and \( i \) signifies the instance for which we seek occurrence.

1. Grammar-Based Language Modeling

This model, as the name implies, relies on grammatical inferences provided to predict sentences based on probabilistic inferences derived from past occurrences. The language to interpret a particular event is deduced from historical data. Let's illustrate this model with an example:

![[Pasted image 20240319020744.png]]

2. Statistical-Based Language Modeling

This model, as its name suggests, relies on statistical inferences drawn from input data. It heavily depends on correctly formatted and appropriate input data. Probability distributions are established over required word sequences, which are then applied to textual data for inferences based on assigned values.