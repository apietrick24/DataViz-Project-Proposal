# CS 573 - Data Visualization Project Proposal

## Data and Attributes

I plan on using my [Book Publishing Dataset](https://gist.github.com/apietrick24/bfffc6c0d47abf00029790381e89626d) for this project. This dataset contains publishing data on more than a thousand books published between 1600 and 2016 and from seven different publishers. There are various attributes about revenue, units sold, ratings, and book metadata. This dataset originated from [Josh Murrey](https://data.world/josh-nbu) on data.world under the name [Books].

Here is a simple breakdown of the attributes included:
- Publishing Year: The year the book was originally published in
- Book Name: The title of the book
- Author: The author(s) who contributed to the book
- Language Code: The language code for the language the book is written in (ara, en-CA, en-GB, en-US, eng, fre, nl, spa)
- Author Rating: The rating of the author's writing complexity and/or notability (Excellent, Famous, Intermediate, Novice)
- Book Average Rating: The average rating of a book out of five
- Book Rating Count: The number of ratings a book has received
- Genre: The book's associated genre (children, fiction, genre fiction, nonfiction) 
- Gross Sales: The total amount of money the book made 
- Publisher Revenue: The amount of money the publisher made off of the book
- Sale Price: The amount of money the book was sold for
- Sales Rank: Rank of the book's unit sold compared to the other books in this database
- Publisher: The publishing company which was the book was sold under
- Unit Sold: The total amount of copies sold for the book

## Questions and Tasks
- Is there any correlation between an author's rating and the number of units sold? 
- How are a book's average rating and number of ratings correlated? Is there a pattern that can be observed?
- Are books more likely to be bought if they are published by certain publishers? 
- Given a book in a certain genre, what is the publisher to publish the book to maximize gross sales?
- Within each author rating, what author has seen the most literary success?

(Within some extra data) 

- Do prestigious literary awards result in larger sales? 
- Which countries have produced the most influential authors? 
- How have our cultural taste in literature changed over time?


## Prototype Visualizations

Here are a few of my proof of concepts for some visualizations aimed to answer the questions and tasks above:

This first visualization looks at the relationship between a book's average rating and its' number of ratings. The size of each point is based on a book's unit sold; the bigger the point, the more units the book sold. Size is not linear, rather it is exponential. 

[![image](https://user-images.githubusercontent.com/61635768/134409740-c83e1e83-4337-41a7-90cc-f6e929704703.png)](https://vizhub.com/apietrick24/a9c2039c7d0644d1a4a3e320f4ea62d2)

With this visualization, you can see that the more ratings a book has, the higher its average rating is. There also seems to be a correlation between the number of ratings a book has and the unit sold. All of the smaller points (the book with less unit sold compared to the rest) are on the left side of the visual. Interestingly, it seems that units sold don't really affect the average rating, as these smaller points seem evenly distributed on the y-axis. 

The second visualization looks at the expected gross sales of a book for each of the publishers in the dataset. Any publisher whose expected average gross sales for a book is less than 1.5k has their bar colored in red. If their value is greater than 1.5k, their bar is colored green. Users are able to highlight a specific publisher by moving their mouse over a bar; making the bar yellow.

[![image](https://user-images.githubusercontent.com/61635768/134410356-47dfedd2-9341-47c5-99a7-21c1102590de.png)](https://vizhub.com/apietrick24/b4b49a43a43c4b67a4e30aa01525b1d6)

The contrast between the bars colored red and the bars colored green tells an interesting story. 1.5k seems like a good split between the publishers as the ones that are colored green have average gross sales well beyond it. As expected, Amazon Digitial Services has the lowest average gross sales per book. This is because, well some of the books they publish do very well, they as publish more books than any other publisher. 

## Sketches

Here is a very rough sketch of what I think the final visualization could look like:

[![image](https://user-images.githubusercontent.com/61635768/134430490-215344f2-5a6a-47e3-ad27-73f87f8d095d.png)](https://user-images.githubusercontent.com/61635768/134430490-215344f2-5a6a-47e3-ad27-73f87f8d095d.png)

**Element 1 - Scatter Plot of Books Based on Gross Sales and Average Rating**

Element 1 will be a scatter plot depicting books with the x-axis being gross sales and the y-axis being average rating. This visual aims to look at the question of whether a book's average rating actually affects its' gross sales. The data this visual draws from will be selected from element 2. This visual will hopefully look similar to the first prototype visual. 

**Element 2 - Publisher, Author Rating, and Genre Selection/Filter Tools**

Element 2 will be comprised of three drop-down menus and a button. The three menus will allow the user to select specific categorical data from the attributes to base the rest of the elements on. The button will select all of the data in the dataset.

**Element 3 - List of Top Books**

Element 3 will display the top three to five books that fit the currently selected data from element 2. It will also display the book's author, publisher, gross sales, and genre. 

**Element 4 - Stacked Horizontal Bar Chart of Publishers and Average Sales per Book**

Element 4 will look similar to prototype visual two, except for the fact that it is a stacked bar chart. Each of the publisher's bar will be made of the publish revenue and the gross sales. Like all of the other elements, element 4 will change based on the information feed to it from element 2. 

**Element 5 - Vertical Bar Chart of Publishers and Units Sold**

Element 5 will be a vertical bar chart and have each bars' height relate to the sum of each publisher's unit sold. This height will change as the user selects different data with element 2.

## Open Questions

Possible Project Pitfalls:
- I'm a little nervous about getting all the selections from element 2 to work with the rest of the visualization. I feel somewhat confident for the element individually; however, I think the complexity and scale of getting the elements to work with element 2 will be the project's biggest road bump.
- I'm also worried a bit about how clean the final visualization is going to look. I want all of the elements to cleanly fit together and work as a whole; I feel that it could be very easy for this vision to go astray. I don't want the final visual to look more like all of the elements were just half-heartedly stitched together.
