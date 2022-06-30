# Reading 14 
> Data Visualization
- what is data visualization
  - Data visualization is a field in data analysis that deals with visual representation of data. 
  - It graphically plots data and is an effective way to communicate inferences from data.
- Using data visualization
  - we can get a visual summary of our data
  - With pictures, maps and graphs, the human mind has an easier time processing and understanding any given data.
- Overview of seaborn plotting functions 
  - Most of your interactions with seaborn will happen through a set of plotting functions.
  - Later chapters in the tutorial will explore the specific features offered by each function.
  - This chapter will introduce, at a high-level, the different kinds of functions that you will encounter.

    
> Similar functions for similar tasks
- The seaborn namespace is flat; all of the functionality is accessible at the top level.
- But the code itself is hierarchically structured, with modules of functions that achieve similar visualization goals through different means
- Most of the docs are structured around these modules: youâ€™ll encounter names like â€œrelationalâ€‌, â€œdistributionalâ€‌, and â€œcategoricalâ€‌.
```
penguins = sns.load_dataset("penguins")
sns.histplot(data=penguins, x="flipper_length_mm", hue="species", multiple="stack")
```



- Figure-level vs. axes-level functions
- 



```
sns.jointplot(data=penguins, x="flipper_length_mm", y="bill_length_mm", hue="species")
```
- Combining multiple views on the data
- 


> Building structured multi-plot grids
- When exploring multi-dimensional data, a useful approach is to draw multiple instances of the same plot on different subsets of your dataset
- This technique is sometimes called either â€œlatticeâ€‌ or â€œtrellisâ€‌ plotting, and it is related to the idea of â€œsmall multiplesâ€‌. It allows a viewer to quickly extract a large amount of information about a complex datase
- Matplotlib offers good support for making figures with multiple axes;
- seaborn builds on top of this to directly link the structure of the plot to the structure of your dataset.
```
g = sns.FacetGrid(tips, col="time")
g.map(sns.histplot, "tip")
```

- 
```
g = sns.FacetGrid(tips, col="day", height=4, aspect=.5)
g.map(sns.barplot, "sex", "total_bill", order=["Male", "Female"])
```


> For th colorization of the data you can use this function: 
- color_palette()
  - This function provides an interface to most of the possible ways that one can generate color palettes in seaborn
  - And itâ€™s used internally by any function that has a palette argument.

## Things I want to know more about

None

[sources1](https://www.labri.fr/perso/nrougier/teaching/matplotlib/)

[sources2](https://seaborn.pydata.org/tutorial.html)

[sources3](https://mybinder.org/v2/gh/bokeh/bokeh-notebooks/master?filepath=tutorial%2F00%20-%20Introduction%20and%20Setup.ipynb)