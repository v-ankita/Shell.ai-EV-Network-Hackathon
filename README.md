# Shell.ai-EV-Network-Hackathon

### An optimaization problem:
In Shell.ai Hackathon 2022, the challenge was to optimally place EV charging stations so that the configuration remains robust to demographic changes. Our task was to
forecast EV charging demand in the coming years based on previous data and arrange charging stations to meet the demand and optimize geographical efficiency for users looking for chargers. The solution had to meet a few practical constraints, such as demand-supply balance and other mathematical objectives. The final submission was in csv format.<br>
The detailed problem statement, including constraints and dscription of the data can be viewed in Problem_statement.pdf.

### Data provided:
1. a time-series of EV charging demand data over a region
2. a set of parking locations with respective parking capacity/slots, i.e., potential EV
charging points within the region
3. details of the existing EV infrastructure
4. the cost of charging point installations and operations
5. other data related to power constraints, rate of charging of fast & slow chargers

2 datasets:
- demand_history.csv - Contains history of EV charging demand over a region from the year 2010 to 2018
- existing_ev_infrastructure_2018.csv - Contains details of existing EV infrastructure from the year 2018
- sample_submission.csv - was given to show format of the csv submission file

### Aproach:
forecast - methods tried
distance matrix - distances
calculating formula for assigning demand-supply weights

![image](https://user-images.githubusercontent.com/85495621/205630615-a9616f9c-268c-4625-a9ac-e10dd4612949.png)


