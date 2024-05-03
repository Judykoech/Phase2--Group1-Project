
 King-County-House-Sales-Analysis

Business and Data Understanding Explain your stakeholder audience here Modeling Regression Results Conclusion
OVERVIEW

King County is located in the U.S. state of Washington. It is the most populous county in Washington and the 13th-most populous in the United States. The county seat is Seattle, also the state's most populous city.
Business Understanding

A real estate agent of a company in Seattle(stakeholder) wants to know which factors significantly impact the prices of a house in King County. This will aid in strategizing the best criteria to take in order to maximize profit. I have been given the task by the company to come up with a model that will be used to predict property prices in King County and obtain significant recommendations on steps that they should take for the business to be successful.

Stakeholders:

The Real Estate Agents who are the stakeholders play an important role between homeowners who are willing to sell their houses and potential buyers. They are responsible for listing and marketing properties, negotiating deals, and advising homeowners on strategies to increase the value of their homes. Providing them with accurate and data-backed recommendations can enable them to better serve their clients and achieve successful sales.
Data Understanding

The dataset I will use is the King County House Sales dataset, which contains information about house sales in a northwestern county. The dataset is provided in the kc_house_data.csv file in the data folder of the project's GitHub repository. The data utilized in this project is kc_house_data.csv file as it provides relevant information for the analysis process. These columns below provide essential information about the houses in the dataset, which can be used for various analyses, such as predicting house prices, understanding the relationship between different features, or exploring the housing market trends.
Column Names and Descriptions for King County Data Set

    id - Unique identifier for a house
    date - Date house was sold
    price - Sale price (prediction target)
    bedrooms - Number of bedrooms
    bathrooms - Number of bathrooms
    sqft_living - Square footage of living space in the home
    sqft_lot - Square footage of the lot
    floors - Number of floors (levels) in house
    waterfront - Whether the house is on a waterfront
        Includes Duwamish, Elliott Bay, Puget Sound, Lake Union, Ship Canal, Lake Washington, Lake Sammamish, other lake, and river/slough waterfronts
    view - Quality of view from house
        Includes views of Mt. Rainier, Olympics, Cascades, Territorial, Seattle Skyline, Puget Sound, Lake Washington, Lake Sammamish, small lake / river / creek, and other
    condition - How good the overall condition of the house is. Related to maintenance of house.
        See the King County Assessor Website for further explanation of each condition code
    grade - Overall grade of the house. Related to the construction and design of the house.
        See the King County Assessor Website for further explanation of each building grade code
    sqft_above - Square footage of house apart from basement
    sqft_basement - Square footage of the basement
    yr_built - Year when house was built
    yr_renovated - Year when house was renovated
    zipcode - ZIP Code used by the United States Postal Service
    lat - Latitude coordinate
    long - Longitude coordinate
    sqft_living15 - The square footage of interior housing living space for the nearest 15 neighbors
    sqft_lot15 - The square footage of the land lots of the nearest 15 neighbors

Modeling

We used the following regression models:

    Simple Linear Regression model - Price vs Sqft_living
    Multiple Linear Regression model - Price vs sqft_living + sqft_living15 + sqft_above
    Multiple Linear Regression model - Price vs sqft_living + sqft_living15 + sqft_above + bedrooms
    
    

Conclusion

Summary of Findings and Recommendations

Q1 House attributes

We recommend targetting the campaign towards houses with a higher bedroom count. However for a given house depending on its square-footage, note that adding an additional bedroom does not necessarily result in a a sale price increase.
We can see that square foot living has the highest influence on the price of the house.
The variables that have a major influence on the price of the house are; square foot living, age of the house,good condition of the house,if the house is on a waterfront and has an excellent view.
The variables that has the least influence on the price of the house are; grade,number of bedrooms,sqft lot,sqft basement and sqft lot.

Q2 Time of the year

-The peak season for home sales typically occurs during the spring and summer months. Specifically, the busiest home selling months are March,April, May, June, July, and August. Buyers are actively searching for properties, and there’s typically increased demand.

The slowest months for home selling activity are November, December, January, and February. Demand tends to be lower during these months.

Factors Influencing Seasonality

Weather Warmer weather encourages more people to explore the housing market.

School Year: Families often want to move before the start of the school year, which aligns with the spring and summer months.

Q3 Model

A model was developed using linear regression and it provided details such how the square footage of living space affects pricing levels, thus influencing market trends.

Q4 Location

Waterfront living is key, with the median house price for a house with a waterfront view being almost double that of one that does not have this feature.The neighbourhoods with the highest average house prices are Medina, Clyde Hill, Yarrow Point, Bellevue and Mercer Island

Recommendation

Future Work

The following data would provide additional insights and improve our model's performance.

Commuting time Time it takes from the house location to downtown Seattle could be a good indicator, with better connected properties potentially being valued higher.

Median Income per zipcode Understanding income distribution amongst zipcodes would also be an indicator of which neighbourhoods are more affluent and should be the focus of the campaign.

Longer time span Having data beyond the one year of May 2014-May 2015 would let us examine whether there are any trends in location. For instance some neighbourhoods may be experiencing a price increase due to recent infrastructure development. Which areas are up and coming?

School rankings Proximity to a good school is often a key requirement for wealthy parents and likely to drive a house price up.

House Architectural Shape: Additionally investigate certain features, such as constructional/architectural values of the house, to see what trends we could discern from that. In addition, further work on our model would include the following:

investigating Principal Component Analysis to tackle multicollinearity
considering other algorithms beyong linear regression
consider regression methods to deal with under/over fitting

Finally with input from our stakeholders we could develop a more tailored model, focusing on houses of a certain value or in a certain neighbourhood.
