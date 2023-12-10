# Semester Stays Analysis 📊

## Author
**Shashank Raj**  
GitHub: [shashoriginal](https://github.com/shashoriginal)

## Project Overview 🌐
This project focuses on analyzing data from a student survey conducted to understand various aspects of semester stays. The insights derived from this analysis aim to provide a comprehensive understanding of student preferences, challenges, and experiences related to their accommodation and lifestyle during their semester stays.

## Dataset 📁
The dataset used in this analysis was collected via a comprehensive student survey. This survey includes a variety of questions that cover different dimensions of a student's stay during the semester, encompassing aspects like accommodation preferences, lifestyle choices, academic commitments, and personal experiences.

> **Note:** Due to privacy concerns, the raw data from the survey does not contains names. The analysis is performed ensuring the confidentiality of the respondents' information.

## Analysis Pipeline 🧬

### Data Loading and Preprocessing 🔄

The analysis begins with loading the data collected from a comprehensive student survey. This survey captures various aspects of student life and preferences during their semester stays.

### Data Loading 📂

The `readxl` library is used for reading the Excel file containing the survey responses. It's a straightforward and efficient way to import data into R for analysis.

### Data Visualization 🎨

For the visualization part:

- `ggplot2` is utilized for creating sophisticated and highly customizable plots. In this case, a bar plot is generated to show the distribution of education levels among the students surveyed.
- `dplyr` is leveraged for data manipulation tasks that are essential before plotting, such as filtering, sorting, and summarizing the data.
- `plotly` is applied to the `ggplot2` object to make the plot interactive, which allows for a more detailed examination of the data points.

The resulting interactive bar chart provides insights into the educational background of the survey participants, distinguishing between graduate and undergraduate students.

![Distribution of Education Level Chart](https://i.imgur.com/XbdYx0F.png "Distribution of Education Level")

### Stacked Bar Plot for Housing Preferences by Age Range 🏠📊

The `ggplot2` library is employed again to craft a stacked bar plot that illustrates the housing preferences segmented by age range. This visual helps in identifying how housing choices vary between different age groups within the student population.

The `geom_bar` function is used with the `position = "fill"` argument, which stacks the bars and scales them so that each bar has the same height, allowing us to compare proportions across categories.

To enhance the interactivity of the plot, `plotly` is again wrapped around the `ggplot` object. This interactivity allows users to hover over different segments of the bars for more detailed information, such as the exact proportion of students within each age range that prefer a certain living situation.

Below is the stacked bar chart representing the proportion of housing preferences by age range:

![Housing Preferences by Age Range Chart](https://i.imgur.com/Vgv0U8d.png "Housing Preferences by Age Range")

### Analysis of Rent Budget by Education Level 💵🎓

To better understand the financial aspects of student housing preferences, we analyze the rent budget in relation to the education level of the students. A categorical conversion of the rent budget variable facilitates a more meaningful visual representation.

A boxplot is generated to depict the distribution of rent budgets for graduate versus undergraduate students. This boxplot provides a clear visual summary of the median, quartiles, and outliers for each group.

The boxplot visualization is then made interactive using `plotly`, which allows viewers to interact with the plot to see exact values and gain a deeper understanding of the rent budget ranges among different education levels.

Below is the boxplot showing the rent budget by education level:

![Rent Budget by Education Level Chart](https://i.imgur.com/fx7Nr4Z.png "Rent Budget by Education Level")

### Awareness of Semester-Based Leasing Pie Chart Analysis 🍰🏠

An essential part of the analysis is to assess the awareness levels of semester-based leasing among students. To do this, we first count the frequency of each awareness level within the dataset using the `group_by` and `summarise` functions from the `dplyr` package.

With these counts, we create a pie chart to visually represent the proportion of respondents who are 'Neutral', 'Somewhat aware', and 'Very aware' of semester-based leasing options. The `plot_ly` function from the `plotly` package creates an interactive pie chart, enhancing the data presentation with the capability for users to see percentage values and labels on hover.

The chart clearly indicates the spread of awareness and can be a critical factor in understanding how well-informed students are about their leasing options and what educational initiatives might be necessary.

Below is the pie chart showing the awareness levels:

![Awareness of Semester-Based Leasing Chart](https://i.imgur.com/QEGmycw.png "Awareness of Semester-Based Leasing")

## Data Simulation Process for Semester Stays Analysis 📊

### Libraries Utilized 📚

- **dplyr**: A comprehensive package for data manipulation, providing a suite of tools for performing common data manipulation operations.

### Setting Up for Reproducibility 🎯

- **set.seed()**: A function used to ensure reproducibility in processes that involve random number generation.

### Simulating the Dataset 🧪

- **sample()**: A versatile function used for random sampling from a given set of data, crucial for simulating categorical variables.

- **tibble()**: A modern data structure from the `tibble` package, which extends the functionality of traditional data frames.

- **lapply() and function()**: Used in conjunction to apply a function over a list or vector, perfect for simulating complex or multi-attribute variables.

### Variables Simulated 📈

- **Age Range**: Captures the distribution of age groups.
- **Education Level**: Differentiates respondents by educational status.
- **Living Situation**: Reflects the diversity of living arrangements.
- **Rent Budget**: Indicates various financial constraints and preferences.
- **Important Housing Factors**: Details what students value in housing.
- **Awareness of Semester-Based Leasing**: Gauges knowledge of leasing options.
- **Likelihood of Semester Housing**: Measures propensity for semester housing.
- **Openness to Subleasing**: Assesses attitudes towards subleasing.
- **Needs Met by Current Housing**: Evaluates satisfaction with current living situations.
- **Challenges with Current Housing**: Identifies common issues faced by students.
- **Preferred Features in Semester Leasing**: Highlights desirable leasing features.
- **Importance of Community Events**: Assesses the significance of community engagement.

### Previewing the Dataset 👀

- **head()**: A quick peek function to review the initial entries of the dataset, providing immediate insight into the data's structure.

The simulated data serves as a foundation for further analysis on semester-based student housing preferences, encapsulating a rich spectrum of student experiences and perspectives. 🏘️📚

![Simulated Data Process](https://i.imgur.com/YdmAOQA.png "Simulated Data Process")

## Visualization Libraries and Plot Creation 📊🛠️

### Libraries Utilized 📚

- **ggplot2**: A powerful package for creating graphics in R, based on The Grammar of Graphics.
- **plotly**: An interactive graphing library that can transform your ggplot2 plots into interactive web plots.
- **dplyr**: Provides a set of tools for efficiently manipulating datasets in R.

### Generating the Faceted Bar Plot 📉

- **ggplot()**: Initiates the creation of a plot that can be layered with additional elements to make a complete plot.
- **geom_bar()**: Adds the bar geometry to create bar charts, counting the number of cases for each group.
- **facet_wrap()**: Allows for the visualization of data as a collection of smaller plots split by a factor, in this case 'Age Range'.
- **theme_minimal()**: Offers a clean and minimalist theme, ideal for professional presentations of data.
- **labs()**: Defines the plot title and axis labels, which are crucial for making the chart understandable.

### Interactive Plot Output 🖱️

- The resulting plot is interactive, enabling users to hover over elements to see additional details, which enhances the data exploration experience.
- This approach to visualization provides a clear and interactive means of understanding the distribution of education levels across different age ranges within the dataset.

![Educational Level Distribution by Age Range](https://i.imgur.com/kGHFjgt.png "Educational Level Distribution by Age Range")

## Interactive Data Visualization Setup 🌐✨

### Libraries and Data Preparation 📚🔧

- **ggplot2 & plotly**: Leveraged for creating interactive visualizations. 📉🖱️
- **shiny**: Utilized for building interactive web applications straight from R. 🌐✨
- **dplyr**: Employed for data manipulation tasks. 🛠️
  
The script begins by loading the necessary libraries that provide tools for data manipulation, plotting, and interactive web app creation. The data is then read from a CSV file and the categorical variables are converted to factors to ensure they are treated appropriately in the analysis.

### Building the Shiny App Interface 📲

The Shiny user interface (UI) is crafted with various input options allowing users to customize the X-axis, Y-axis, color, size, and facets of the plot. This dynamic selection capability offers a highly interactive and user-driven visualization experience.

### Server Logic and Reactive Plotting 🔁📊

The server part of the Shiny app is where the reactive plotting magic happens. It listens for user inputs and dynamically updates the plot. The `renderPlotly()` function is key here, as it takes a `ggplot` object and turns it into an interactive plotly object. The plot is further customized with color and size aesthetics based on user selection, and faceting is added if chosen.

### Running the Shiny App 🚀

Finally, the `shinyApp()` function is called to run the app, combining the UI and server components into a live interactive application.

The documentation outlines the process of setting up an interactive visualization tool using R and Shiny, emphasizing the ability for end-users to explore data through various graphical dimensions and controls. This approach not only enhances data exploration but also encourages user engagement and data-driven decision-making. 📈🎨👥


### Shiny App Interface 🎛️

The Shiny app interface provides a range of interactive controls to manipulate the visualization. Users can choose variables for the X-axis, Y-axis, color, size, and facets of the plot. Adjustments can be made to the point opacity and size for better visualization clarity.

![Interactive Shiny App Interface](https://i.imgur.com/plZZQ88.png "Interactive Shiny App Interface")

### Disclaimer ⚠️

Please note that when interacting with the app, it is important to select only continuous variables for the 'Size Variable' to ensure the plot renders without errors. Choosing a categorical variable for size may lead to unexpected results or error messages.

### Visualization 📈

The interface enables users to create a custom plot by selecting different variables to compare against each other. The color and size of the points can be varied to represent additional dimensions of the data, such as Rent Budget and Education Level, providing a rich, multi-faceted view of the information.

## Machine Learning 🤖📊

Leveraging the power of R's machine learning libraries, this section covers the setup and execution of a predictive modeling workflow, including data preprocessing and model training, followed by the deployment of a predictive model within a Shiny application.

### Libraries and Parallel Processing Setup 🛠️🖥️

- **caret & doParallel**: Utilized for building predictive models and setting up parallel processing to optimize computational efficiency.
- **shiny**: Employed to create an interactive web application that allows users to input parameters and receive model predictions.

### Data Preprocessing 🔄

- All relevant categorical variables in the dataset are converted into factors, a necessary step for many modeling functions within the caret package to treat the data correctly.

### Model Selection and Training 📐🎓

- A control object is created using `trainControl` to specify the method of cross-validation and number of repeats.
- The `train` function from the caret package is then used to build a decision tree model, predicting the likelihood of students choosing semester-based housing given various predictors.

### Interactive Shiny Application Interface 🌐🔧

- The Shiny application's user interface provides a user-friendly form for inputting predictor variables, such as age range, education level, and housing preferences.
- An action button is provided to trigger the prediction process.

### Server Logic and Prediction Output 🔀🔮

- The server logic listens for the predict button event, gathers input values, and formats them into a data frame that matches the training data's structure.
- The prediction is made using the trained model and the results are displayed to the user in a main panel.

### Running the Shiny App 🚀

- The Shiny app is executed, bringing to life a web application where users can get real-time predictions on the likelihood of choosing semester-based housing.

This setup demonstrates the integration of machine learning with interactive web technologies to provide actionable insights and predictive analytics directly to the end-user. 📈💡👩‍💻

![Model Overview](https://i.imgur.com/mGzJfIh.png "Model Overview")

## Likelihood of Choosing Semester-Based Housing Prediction 🏠🎓

The Shiny app presents a user-friendly interface for predicting the likelihood of students choosing semester-based housing. By selecting from various dropdown menus, users can input their personal circumstances and preferences, which are then processed by the underlying predictive model to generate a likelihood estimate.

### Output Analysis 📈🔍

Upon inputting their details and clicking the 'Predict' button, the user is presented with a prediction statement. For example, a user who indicates a strong openness to subleasing, a need for amenities, and a budget of $1001 - $1500 for rent might receive a prediction such as "Very likely" to choose semester-based housing. This output suggests that the model has identified a pattern in the data that associates these particular inputs with a higher likelihood of choosing semester-based housing.

### Visual Representation 🌟

The application not only provides textual predictions but also allows for the visual representation of the input data against the predicted outcome. This can offer intuitive insights into how different factors may weigh upon the decision-making process related to housing.

![Predictive Model Output](https://i.imgur.com/AcQ1HDS.png "Predictive Model Output")

The use of a machine learning model within a Shiny app exemplifies how data science can directly inform individuals' decisions in real-time, providing a bridge between complex algorithms and everyday choices. 🌉💡

