# Summary
The crash of the Titanic was one of the most famous shipwrecks in history, leaving only a few to survive. Why did some passengers, like the charming Rose DeWitt Bukater (Kate Winslet), survive the Titanic compared to the orphan young adult, Jack Dawson (Leonardo DiCapro)? In this Tableau story, we will explore what factors influenced a passenger's probability of survival. It turns out those who were either woman, bought a first class ticket or were under the age of 19, where more than likely to survive.

# Design

## Initial Design
[Visualization Link](https://public.tableau.com/profile/john.wu#!/vizhome/titanic-draft/TitanicStory?publish=yes)

Through this project, I wanted to easily convey the key factors that lead to the survival of many passengers. For discrete variables, like `sex`, I wanted to simultaneously show both the probability of survival and the number of passengers within a given category (i.e. male/female). Both count and probability clearly indicate how likely a passenger within a certain category will survive. To do this, I created a univariate barplot where each bin is a category for a discrete variable and the height of a factor is the number of passengers that belong to that bin. Each bar shows how many passengers survived or died in that bin. This is done by showing how many passengers survived in that bin as a green color and then showing how many passengers died as a red color on top of it. Also, there is a tooltip that shows information of each bar, such as the percentage of survived or died and the number of passengers that survived or died. Furthermore, I created a tabular form of this graph so that readers have an easier time grasping an information about a variable. Additionally, I showed the distribution of category (disregarding `survival`) as a stacked barplot to gain a better understanding of the variable. It looks like being female or having a first class ticket is a strong indication of survival.

Furthermore, I wanted to learn more about how `class` and `age` simultaneously influence `survive` by plotting these variables on a facet grid. The facet grid conveys almost the same information as the univariate bar plot mentioned previously except that class and gender are displayed as a hierarchy. It looks like first class women are most likely to survive whereas third class males are least likely to survive. I didn't include text to these bar plots as they some texts were not displayed.

Also, I wanted to see the relationship between `age` and `survive` since human instincts will lead most people to save children as their first priority in a dangerous situation. Since `age` is a continuous variable, I thought it would be intuitive to represent `age` as 5 discrete bins divided evenly by percentile. I used percentile because the distribution of `age` is not uniform and there is a high number of passengers that are between the age of 20 to 35. Since `age` is now treated as a discrete variable, I visualized the relationship between `age` with `survived` similarly to the dashboards of my univariate analysis. However, I did not display information about the distribution of the bins, because they are trivially almost evenly distributed. I chose five bins because those are intuitive age groups. Namely, these groups are children, young adults, adults who are starting to have children, adults who raised a family for years, and retiree. I also added an interactive filter based on `class` and `sex` so that the user can see how age affects survival with respect to the most influencing variables.

## After Feedback
[Visualization Link](https://public.tableau.com/profile/john.wu#!/vizhome/titanic-after-feedback/Titanic?publish=yes)

Overall, I added the suggestions that Brian made (See section Feedback). I removed tables displaying statistics that were conveyed within the stack bar plots of the stories. I also changed the labels of `class` from (1, 2 and 3) to (First, Second and Third). For the dashboard that displays `sex` and `class`, I added text that shows the number of passengers and percentage of passengers that are within each barplot. I removed the dashboard `Embarked` as Brian had a difficult time seeing the relationship between `Embarked` and `Survival`. I finally changed the alias of each percentile groupings to ranges within those groups.  

On top of what he said, I made the title of plots consistent with each other across different dashboard. I also removed grid lines from plots. This is because these gridlines were a bit distracting for the reader.



# Feedback 
Reviewer: Brian Tom [LinkedIn Profile](https://www.linkedin.com/in/brian-tom-510866a1/)

Overall, Brian could see that I was trying to determine the main attributes of surviving the Titanic. He could easily see that gender played a huge role in the survival of passenger and the stacked barplot can clearly convey that. He liked the color scheme I chose for showing how many passengers survived and died in the crash. He did not like the table summary statistics as the statistics were already conveyed through the graph and it was hard to read. He mentioned that he did not even read the table. He thought that the stacked barplot displaying the distribution of `sex` was useful.

For the dashboard with `class`, he could tell those first-class passengers were the most likely to survive. He had the same issues with the dashboard that displayed information about `sex` and survival. He was initially confused what the x-axis labels meant, but then later associated with socioeconomic class and the price of the ticket.

After seeing how both `sex` and `class` were significant factors of survival, he wanted to see how both `sex` and `class` simultaneously account for the survival of passengers. The next dashboard conveyed that and he was quite surprised that first class women had a 91% survival rate. He was initially deceived that third class males had a higher chance of survival compared to second class males. However, he hovered on the graph saw those second class males had a higher chance of survival. He thought that was useful. He did not refer to the table that displays the actual survival rate of each value.

When Brian saw the dashboard for that compares the relationship between `Embarked` and `Survival`, he wanted to know why Cherbourg had the most amount of survivors and why Southampton had the most amount of passengers. He had a difficult time interpreting the results shown from the graph.

For the `age` dashboard, Brian said that he could see that the youngest passengers were the most likely to survive. He liked playing around with the filters to see how `sex` and `class` influenced the chart. He was curious what were the boundaries of each percentile range.

Overall, Brian like the Tableau story I made and thought that I was clearly answering the question, "What factors lead to the survival of passengers in the titanic"?








# References
- Guide to generate univariate plots whose bins are percentile ranges https://www.dynatrace.com/news/blog/why-averages-suck-and-percentiles-are-great/