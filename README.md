# Final Project: Obesity and ACT Scores 
## Code Snipets 

### 1. Obesity Prevalence and Overall ACT Score per State 
This histogram shows shows the spread of ACT scores by state. The color of the bar shows the obesity. The lighter blue the bar, the more prevelant obesity is in that state. The darker blue the bar, the less prevalent obesity is in that state.

```
ggplot(ACT_obs, aes(x = State, y = Composite_score , fill = Obesity_Prev)) + 
  geom_col()+
  labs(title = "ACT and Obesity", x = "State", y = "ACT", fill = 'Prevelance of Obesity')+
  theme(axis.text = element_text(angle = 90, vjust = .5, hjust = 1))

```
### 2. State and Overall ACT
This histogram shows the ACT scores for each state.

```
ggplot(df, aes(x = State, y = Composite_score)) +
  geom_bar(stat = "identity", fill="skyblue") +
  labs(title = "State and ACT Score ", x = "State", y = "ACT Composite Score") +
  theme_minimal()+ 
  theme(axis.text.x = element_text(angle = 90, hjust = 1))

```
### 3. Obesity and State 
This histogram shows the obesity in each state.

```
ggplot(df, aes(x = State, y = Obesity_Prev)) +
  geom_bar(stat = "identity", fill= "indianred") +
  labs(title = "State and Obesity ", x = "State", y = "Obesity") +
  theme_minimal()+
  theme(axis.text.x = element_text(angle = 90, hjust = 1))

```
### 4. States with the highest obesity rates 
After creating the previous charts we were able to see the states with the highest obesity rates. To better see them we created this chart that shows the 6 states with the highest obesity rates. 

```
ggplot(filtered_data, aes(x = State, y = Obesity_Prev)) +
  geom_bar(stat = "identity", fill= "indianred") +
  labs(title = "States with highest Obesity Rates", x = "State", y = "Obesity") +
  theme_minimal()+
  theme(axis.text.x = element_text(angle = 90, hjust = 1))

```
### 5. States with highest Act score 
After creating the previous charts we were able to see the states with the highest ACT scores. To better see them we created this chart that shows the 6 states with the highest ACT scores. 

```
ggplot(filtered_data, aes(x = State, y = Composite_score)) +
  geom_bar(stat = "identity", fill="skyblue") +
  labs(title = "States with highest ACT Scores",
       x = "State",
       y = "ACT Composite Score") +
  theme_minimal()+ 
  theme(axis.text.x = element_text(angle = 90, hjust = 1))

```
### 6. States with lowest Act score 
Similar to the above, but instead of pulling out the highest ACT scores we selected the 6 states with the lowest ACT score. 

```
ggplot(filtered_data, aes(x = State, y = Composite_score)) +
  geom_bar(stat = "identity", fill="skyblue") +
  labs(title = "States with lowest ACT Score ", x = "State", y = "ACT Composite Score") +
  theme_minimal()+ 
  theme(axis.text.x = element_text(angle = 90, hjust = 1))

```
### 7. States with lowest obesity rates 
Similar to the above, but instead of pulling out the highest obesity rates we selected the 6 states with the lowest obesity rates. 

```
ggplot(filtered_data, aes(x = State, y = Obesity_Prev)) +
  geom_bar(stat = "identity", fill= "indianred") +
  labs(title = "States with Lowest Obesity ",
       x = "State",
       y = "Obesity") +
  theme_minimal()+
  theme(axis.text.x = element_text(angle = 90, hjust = 1))

```
### -> Conclusion: One state fit our expectation of having high obesity and low ACT scores and that is Tennessee. One state also fit our expectation of low obesity and high ACT score and that is Massachusetts. We came to this conclusion from the 4 charts above (4, 5, 6, 7). 

### 8. Obesity Prevalence and Overall English ACT Score per State 
This histogram looks at the English score of the ACT. Connecticut has the highest English ACT score.

```
ggplot(english_obs, aes(x = State, y = English, fill = Obesity_Prev)) + 
  geom_col()+
  labs(title = "English ACT and Obesity", x = "State", y = "English ACT Score", fill = 'Prevelance of Obesity')+
  theme(axis.text = element_text(angle = 90, vjust = .5, hjust = 1))

```
### 9. Obesity Prevalence and Overall Math ACT Score per State 
This histogram looks at the Math score of the ACT. Massachusetts has the highest Math ACT score. 

```
ggplot(Math_obs, aes(x = State, y = Math, fill = Obesity_Prev)) + 
  geom_col()+
  labs(title = "Math ACT Score and Obesity Prevlance Per State", x = "State", y = "Math ACT Score", fill = 'Prevelance of Obesity')+
  theme(axis.text = element_text(angle = 90, vjust = .5, hjust = 1))

```
### 10. Obesity Prevalence and Overall Reading ACT Score per State 
This histogram looks at the Reading score of the ACT. Massachusetts has the highest Reading ACT score. 
```
ggplot(Reading_obs, aes(x = State, y = Reading, fill = Obesity_Prev)) + 
  geom_col()+
  labs(title = "Reading ACT Score and Obesity Prevlance Per State", x = "State", y = "Reading ACT Score", fill = 'Prevelance of Obesity')+
  theme(axis.text = element_text(angle = 90, vjust = .5, hjust = 1))

```
### 11. Obesity Prevalence and Overall Science ACT Score per State 
This histogram looks at the Science score of the ACT. Connecticut, Massachusetts, and New Hampshire have the highest Science ACT scores. 

```
ggplot(sci_obs, aes(x = State, y = Science, fill = Obesity_Prev)) + 
  geom_col()+
  labs(title = "Science ACT Score and Obesity Prevlance Per State", x = "State", y = "Reading ACT Score", fill = 'Prevelance of Obesity')+
  theme(axis.text = element_text(angle = 90, vjust = .5, hjust = 1))

```
### 12. Obesity Prevalence and State Percentage of Test Taking 
This histogram shows a wide color variety for states with 100% rate of taking ACT. These shows that regardless of obesity rates in states the ACT will still be taken. 

```
ggplot(test_obs, aes(x = State, y = percent_taking_ACT, fill = Obesity_Prev)) + 
  geom_col()+
  labs(title = " Percent Taking ACT and Obesity Prevlance Per State", x = "State", y = "Percent Taking ACT", fill = 'Prevelance of Obesity')+
  theme(axis.text = element_text(angle = 90, vjust = .5, hjust = 1))

```
