# Shell.ai-EV-Network-Hackathon

### An optimaization problem:
In Shell.ai Hackathon 2022, the challenge was to optimally place EV charging stations so that the configuration remains robust to demographic changes. Our task was to
forecast EV charging demand in the coming years based on previous data and arrange charging stations to meet the demand and optimize geographical efficiency for users looking for chargers. The solution had to meet a few practical constraints, such as demand-supply balance and other mathematical objectives. The final submission was in csv format.<br>
The detailed problem statement, including constraints and dscription of the data can be viewed in Problem_statement.pdf.

### Data provided:
1. A time-series of EV charging demand data over a region
2. A set of parking locations with respective parking capacity/slots, i.e., potential EV
charging points within the region
3. Details of the existing EV infrastructure
4. The cost of charging point installations and operations
5. Other data related to power constraints, rate of charging of fast & slow chargers

2 datasets:
- demand_history.csv - Contains history of EV charging demand over a region from the year 2010 to 2018
- existing_ev_infrastructure_2018.csv - Contains details of existing EV infrastructure from the year 2018
- sample_submission.csv - was given to show format of the csv submission file

### Aproach:
- **Forecasting** - We tried moving average method, simple exponential smoothening, Holt's exponential smoothening, polynomial regression considering each supply point's data over the years as a separate time series. HOLT'S gave the most suitabe forecast.
Different hyperparameters were used in Holt's forcasting for different groups, divided based on the change in demand over the years.

- **Distance matrix** - spatial distance between every demand and supply point combination was found using Minkowski distance formula.

- **Clustering** - DBSCAN was used to make clusters of demand points with similar forecasted demand trends.

- **DS weights** - we made a mathematical formula using distance-based fractions of demands for finding how much does every demand point influence the demand at every supply point, with which we ultimately calculated the most optimal distribution of charging stations to meet the demand.


![image](https://user-images.githubusercontent.com/85495621/205630615-a9616f9c-268c-4625-a9ac-e10dd4612949.png)


