# API-interaction-and-Data-Visualization-
*COMPANY*: CODTECH IT SOLUTIONS
*NAME*: NEHA NITIN BANKAR 
*INTERN ID*: CT04DH786
*MENTOR*: NEELA SANTOSH 
*DOMAIN*: PYTHON 
*DURATION*: 4 WEEKS 

#DESCRIPTION

This Python script demonstrates how to simulate road accident data using a mock API approach and visualize the data using Matplotlib. It is designed to represent how real-time data from an actual API (such as government accident databases or open data platforms) can be fetched, processed, and visualized to analyze trends in road accidents over a period of time. The code follows three main steps: data simulation (mock API), data extraction, and data visualization.

Step 1: Simulating API Data

Since actual API integration is not performed here, the code uses a function called get_mock_accident_data() to simulate API responses. This function mimics a real-world API that would typically return accident data over the past few days. It generates accident data for the last 15 days dynamically.

Using Python’s datetime module, the script calculates dates starting from 14 days before the current date up to today. For each date, a random number of accidents (between 100 and 300) is generated using Python's random.randint() function. This simulates variability in daily accident counts. The data is structured into a list of dictionaries, where each dictionary holds a date and its corresponding accident count. The function then returns a dictionary mimicking a typical API response with a status key and a data key containing the list of accident records.

Step 2: Fetching Data (Simulated API Response)

In a real API scenario, a requests.get() call would fetch JSON data from an online endpoint. Here, however, the mock function is called directly, simulating the process of fetching an API response. The returned JSON-like dictionary is stored in the response variable.

The script then parses the response by iterating through the data key. It extracts two lists:

dates: A list of date strings for the past 15 days.

accidents: A list of corresponding accident counts for each date.

These lists are prepared for visualization.

Step 3: Data Visualization using Matplotlib

The visualization phase uses Matplotlib, a popular Python plotting library, to create a line graph representing the trend of road accidents over the last 15 days. A figure is initialized with a size of 12x6 inches for better clarity.

A line plot is generated where:

The X-axis represents dates.

The Y-axis represents the number of accidents per day.

The plot uses orange-colored lines with circular markers (marker='o', color='orange') to highlight individual data points for each date.

To enhance readability:

The title of the plot is set as "Simulated Daily Road Accidents (Last 15 Days)".

X-axis labels (dates) are rotated 45 degrees using plt.xticks(rotation=45) to avoid label overlap.

Grid lines are added for better visual guidance.

The plt.tight_layout() method ensures that labels and titles are adjusted within the plot area, preventing clipping of text.


Finally, plt.show() displays the graph.


