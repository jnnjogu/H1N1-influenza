# H1N1-influenza
<img width="1792" height="1024" alt="image" src="https://github.com/user-attachments/assets/08065d50-6da2-4556-adbd-94f728c45d00" />


## Background
_____
H1N1 flu also known as the swine flu is a type of influenza A respiratory virus that normally causes illness outbreaks in pigs. The disease is characterised by a high morbidity rate and low mortality in animals. In 2009, the influenza virus mutated and was now able to infect humans and other animal species such as birds. 
Initially, human cases were limited to individuals with direct exposure to pigs. However in 2009, the virus demonstrated human-to-human transmission, and infections began appearing in people with no known contact with animals. The virus spread rapidly, and by June 2010, more than 214 countries had reported laboratory-confirmed cases, with over 18,239 deaths worldwide. In response to its global impact, the World Health Organization (WHO) officially declared H1N1 a pandemic in August 2010.
To curb the spread of the disease, public health authorities launched massive vaccination campaigns to protect millions of people from the virus. The goal of these programs was to ensure that everyone who desired to get vaccinated actually got the vaccine. Concerted efforts across various stakeholders groups made the campaigns successful.
However, vaccination decisions are influenced by many factors a wide range of behavioral, socio-economic, and informational factors. Understanding these determinants can help public health agencies improve vaccination campaigns and target interventions effectively. 
This study utilizes data from the 2009 National H1N1 Flu Survey to predict vaccine uptake for both the H1N1 and seasonal influenza viruses.
______
### Problem statement
This study aims at developing a predictive model that estimates the probability that individuals received the H1N1 and seasonal flu vaccines based on their demographic attributes, health behavior, medical history, and personal opinions regarding flu and vaccination. With the goal being to identify patterns that can inform targeted interventions and enhance public health decision-making.
____
### Stakeholders
Some of the stakeholders that would be interested in this work include but not limited to:
|Stakeholder|Area of interest and use case|
|------|--------|
|Public health agencies (e.g., CDC, WHO)| aiming to improve vaccination strategies|
|Policy makers |seeking data-driven guidance for pandemic preparedness|
|Healthcare providers |planning outreach and education programs|
|Epidemiologists and researchers |studying vaccine hesitancy and uptake|
|Non-profit organizations |involved in community health campaigns|

## Data source
The data was sourced from 
DrivenData. (2020). Flu Shot Learning: Predict H1N1 and Seasonal Flu Vaccines. Retrieved [July 18 2025] from https://www.drivendata.org/competitions/66/flu-shot-learning.
The data was collected through a phone survey in the United States asking respondents whether they had received the H1N1 and seasonal flu vaccines, in conjunction with questions about themselves. The other additional questions covered their _social_, _economic_, and _demographic background_, _opinions on risks of illness_ and _vaccine effectiveness, and behaviors towards mitigating transmission_. 
#### Assumption:
Our assumption is that a better understanding of how these characteristics are associated with personal vaccination patterns can provide guidance for future public health efforts.
### Model building process
![alt text](crispdm.png)

# Recommendations
---------------------------------------

Based on model evaluation metrics and feature importance analysis, we recommend using the hyperparameter-tuned Logistic Regression model (Model 2) for predicting H1N1 vaccination uptake. Although it does not have the highest ROC-AUC score overall, it achieves the highest recall (72%) among all models—making it especially valuable in public health contexts where identifying as many vaccinated individuals as possible is critical.

This model also offers a balanced trade-off between precision (47%) and recall, as reflected in its highest F1 score (0.573), indicating better generalization than other classifiers.

Feature analysis shows that the most influential predictors of H1N1 vaccination include:

We recommend that vaccination drives / campaigns look into the following attributes because they are highly correlated with vaccine uptake

- Doctor_recc (doctor recommendation) -  Patients often trust their healthcare providers and are more likely to get vaccinated if explicitly advised to do so.

- opinion_h1n1 (perception of vaccine effectiveness) - Personal belief in the effectiveness or safety of the H1N1 vaccine directly influences willingness to get vaccinated. Positive attitudes usually correlate with higher uptake.

- race_Hispanic and race_Other or Multiple - Differences in cultural beliefs, access to healthcare, and targeted public health campaigns may cause variations in vaccine uptake across racial/ethnic groups.

- education level, employment factors, and marital status - Missing education data may correlate with lower socioeconomic status or limited health literacy—both linked to vaccine hesitancy or access issues.

Industry - Different industries/ companies have varying exposure risks and workplace vaccination policies that may enhance or impede vaccination targets.

More data on education and environmental factors may give a clearer light on access and underlying patterns

