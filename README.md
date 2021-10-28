# CS 573: Data Visualization - Final Project Proposal

## Data and Attributes

I am planning on using my [Honey Production in the United States Dataset](https://gist.github.com/apietrick24/bed0d1a799e856566704afc3f421abdf) for this project. Originally posted on Kaggle by [Jessica Li](https://www.kaggle.com/jessicali9530) under the title [Honey Production in the USA (1998-2012)](https://www.kaggle.com/jessicali9530/honey-production), this dataset has information on honey bee colonies and the production honey for almost all of the state from 1998 to 2012. I plan on using this data to explore how the honey industry has changed over time and what its future could be. 

Here is a simple breakdown of the attributes included:
- State: The aberration for the state for which this row's information is for. Not all states are included in this dataset to avoid disclosing data for individual operations
- Number of Colonies: The number of honey-producing colonies. Specifically, colonies from which honey was able to be taken in that year. 
- Yield Per Colony: The average honey yield per colony in pounds.
- Total Production: Estimated total production of the state's honey colonies in pounds (simply Number of Colonies times Yield Per Colony)
- Stocks: Stockpiles of honey held by producers in pounds.
- Price Per Pound: Average dollar price per pound of honey in the given state.
- Production Value: Estimated total value of the state production in dollars (Simply, Total Production times Price Per Pound)

## Questions and Tasks
- How has the rate of honey production yield changed? 
- Are there any notable trends that have appeared in the number of colonies or production value?
- Which states produce the most honey? Do these states have more colonies or do their colonies just net a larger yield? 
- Is there a "honey belt" in the United States or is production evenly spread through the country?
- How does a producer's stock change per year? Is there general a positive trend or are they having to sell more of their stock due to smaller yields?

## Prototype Visualizations

Due to pivoting my project so close to the deadline for this proposal, I only had time to construct a prototype for one of my visuals:

[![iamge](https://user-images.githubusercontent.com/61635768/137572596-4a633f93-148e-4ad0-a3c9-c5b6186666f8.png)](https://vizhub.com/apietrick24/b4fc3ff45ef245079748eecce6999268)

This visual is a prototype for element 2 in the project, which is a line graph with selectable variables over time. You can see that the total production of honey in the United States has heavily reduced over the interval in this dataset, almost decreasing by 50%. This insight leads to assumptions about other frightening trends with the rest of the variables in the dataset.

## Sketches
Here is a very rough sketch of what I think the final visualization could look like:

[![image](https://user-images.githubusercontent.com/61635768/137572274-6fc14642-889b-4900-aa8d-d0ca96d001b2.png)](https://user-images.githubusercontent.com/61635768/137572274-6fc14642-889b-4900-aa8d-d0ca96d001b2.png)

**Element 1 - Interactive Map of the United States**

Element 1 will be an interactive map of the United States. It will be heavily connected to other elements in the visual such as having each state's saturation depend on the value for selected variables in element 3 and have the value depend on the interval selected in element 6. If a viewer were to click on a state, element 2 will be updated to only focus on the state's value for the selected variable over time. 

**Element 2 - Line Graph of Selected Variable**

Element 2 will be a line graph with two specific phases. The first phase is when a state isn't selected in element 1. The line graph will show the total value of the selected variable in element 2 over the interval selected in element 6. This phase is what is shown in the prototype above. Phase two will be when the viewer clicks on a state in element 1. The line graph will then display the value of the selected variable for the state and then the average for all the states in the dataset. 

**Element 3 - Variable Menu**

Element 3 is simply a drop-down menu for the viewer to select which variable to base the two visuals on. 

**Element 4 - Supporting Text**

I think it's important to give context to the viewer some optional context to the information you are displaying. I would like to have a few paragraphs below my two visuals that talk about the honey industry in the United States and the importance of honey production.

**Element 5 - Statistics about Dataset**

Similarly to element 4, I would like to give some insight into the dataset I am using. I would like to have a paragraph or maybe bullets just describing the information included and how that information is important. Perhaps I could use some one-variable statistics to help.

**Element 6 - Year Brush**

Element 6 will be a brush for the viewer to select the interval of years they want the visual to display. By default, element 6 will include all the possible years in the dataset. 

**Stretch Goals**
- If the viewer hasn't selected a state yet, have the map cycle between displaying the selected variable's value for each year
- Animations for element 2 when changing selected variables or phases
- Have a bee represent the cursor?

## Schedule of Deliverables

**October 20th:**
- Rough Draft of Elements 1 and 6 (Interactivity doesn't have to be fully working yet)
- Modify Element 2 to Include Support for Element 3

**October 27th:**
- Modify Element 1 to Include Support for Element 3
- Figure Out How to Filter Data for Element 2 (so that the element doesn't have to rely on a separate CSV file)
- Prepare Element 2 to Support Phase 2

**November 3rd:**
- Prepare Element 1's interactivity functions
- Research How to Get Elements 1 and 2 to Communicate
- Set Ground Work for Communication

**November 10th:**
- Get Elements 1, 2, 3, and 6 to fully communicate with each
- Rough Draft of Final Project

**November 17th:**
- Clean Up Visuals and Write Element 4 and 5
- Work on Stretch Goals if no major issues with elements

**November 24th:**
- Start to Finalize Presentation of Visuals
- If haven't already, Export to GitHub
- Work on Stretch Goals if no major issues with elements

**December 1st:**
- Work on Stretch Goals if no major issues with elements
- Soft Due Date for Final Project

## Open Questions

### Why Pivot the Project?

After learning that the course was 5 weeks longer than I originally thought, I looked at my current project proposal and was unhappy at how dull it was. While I was happy with what I had coded so far, I felt that I could make a better end project if I wasn't restricted to the dataset I had chosen. I wanted to make something a little more expressive and that required the use of D3 and JavaScript. Hence, I decided to pivot my project and look for a new dataset. I don't regret switching so late, I learned a lot from my previous project and it has definitely changed the way I look at making these visuals. 

If you are curious about my previous project proposal, here is a link to the [old ReadMe File](https://github.com/apietrick24/DataViz-Project-Proposal/blob/3be806eee76ea5269429ba0352bbd86f56fd20ae/README.md). 

### Possible Project Pitfalls:
- I'm a little nervous about getting the interaction between elements 1 and 2 to work correctly. I'm still fairly due to D3 and JavaScript, so I'm a little dubious about my ability to code it correctly. 
- I'm also worried a bit about how clean the final visualization is going to look. I want all of the elements to cleanly fit together and work as a whole; I feel that it could be very easy for this vision to go astray. I don't want the final visual to look more like all of the elements were just half-heartedly stitched together.

## Update Log

### October 27th
This week I focus my time on preparing to tackle the project as one whole item, rather than as separate visual projects. I started to take the code for the visuals I have created so far and make them into separate files that are unreliant on their current HTML environments. I figured that this would be helpful to do now before I start adding more elements and features that need to communicate with each other. I also changed how I'm parsing my CSV file, specifically now I'm using d3.group functions to generate arrays of objects with values I need for each visual. Support for a drop-down menu has been added on the backend for my line graph. As for the feedback given to me on my project so far, I changed my line graph's curve function to fix issues of smoothing the line too much and misrepresenting the information. To help with this, I also added circles for each data point on the line. 

As for the work for next week, I'm going to finish my drop-down menus and properly construct the second part of my line graph. Ideally, I would like to have a rough draft of my map of the United States also done. 

#### Element 2

[![iamge](https://user-images.githubusercontent.com/61635768/139172131-5b00d34c-8e61-4389-8aea-76a31254fe3d.png)](https://vizhub.com/apietrick24/aa86472650884a7d8b63eefa06ba71e4)

- Added circles on the line to represent the values for the passed data
- Addressed feedback and changed the curve of the path from d3.curveBasis to d3.curveMonotoneX to fix issues with over smoothing and misrepresentation
- Changed CSV parsing function to make use of d3.group and avoid having to use a separate CSV file
- Started to convert/move the visual's code to a separate JS file in order to properly work with future elements (WIP, not shown in image) 
- Started to add the functionality of drop-down menus (WIP, not shown in image)
