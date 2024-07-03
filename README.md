# Olympic-game
Analyze a data set containing 120 years of Olympic history, and use data visualization to explore how the number of athletes from each country has trended over time.



# Olympic game::




Data Visualization Of Olympic game over 120 years

Problem Statement::

The Olympic Games are a global sporting event that brings together athletes from around the world to compete in various sports. Understanding the participation trends of different countries in the Olympics can provide valuable insights into the growth and development of the Olympic movement over time.
The provided dataset includes information on athletes who have participated in the Olympic Games from 1896 to 2016. The data includes fields such as athlete ID, name, sex, age, height, weight, team, National Olympic Committee (NOC) code, year, season, city, sport, event, and medal won..


Steps followed.

Load the Data: Load the athlete_events.csv file into Power BI.
Group by Country: In the Power Query Editor, group the data by the NOC (National Olympic Committee) column to get the total count of athletes per country.

// Step 1: Group by NOC
grouped_data = Table.Group(data, {"NOC"}, {{"TotalAthletes", each Table.RowCount(_), type number}});

Create the Card Visual: In the report view, add a new card visual to the canvas.

Bind the Data: In the "Fields" well of the card visual, select the "TotalAthletes" field from the grouped data.
Format the Card: Customize the card visual by adjusting the font, size, color, and other formatting options to make it visually appealing.

Add Filters: If desired, you can add filters to the card visual to allow users to view the total athletes for specific countries or time periods.


![POWER BI](https://github.com/KIsmail23/Olympic-game/assets/156454800/904e2d3c-9adc-41f5-ba20-fb2867d03323)



Detailed Steps;

Load the Data:
In Power BI Desktop, go to the "Home" tab and click "Get Data".
Select "Text/CSV" and navigate to the athlete_events.csv file.
Click "Open" to load the data into Power BI.
Group by Country:
In the Power Query Editor, select the "NOC" column.
Go to the "Transform" tab and click "Group By".
In the "New column name" field, enter "TotalAthletes".
In the "Operation" dropdown, select "Count rows".
Click "OK" to apply the grouping.
Create the Card Visual:
In the report view, click the "+" icon in the "Visualizations" pane to add a new visual.
Select the "Card" visual type.
Bind the Data:
In the "Fields" well of the card visual, drag the "TotalAthletes" field from the grouped data.
Format the Card:
In the "Format" pane, you can customize the card's appearance, such as the font, size, color, and other formatting options.

