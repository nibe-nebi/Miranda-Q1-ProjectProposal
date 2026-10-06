# Miranda-Q1-ProjectProposal
A Household Electricity Usage Estimator and Saving Advisor

Problem Statement: There is no doubt that many families get monthly statements showing their electricity consumption without knowing which appliances use the most electricity. These facts are not mentioned on the statement, which shows only the total sum without any more information. People who earn very little money are the ones most affected by this, since the statement may prevent them from buying other necessities. There is no easy way to know which appliances cost the most electricity.

Project Objectives

1. By the end of the first quarter, the program should be able to calculate the estimated kWh and the cost of at least 10 commonly used appliances in a household, with 100 percent accuracy compared to manual computation.
2. By the end of the first quarter, the program should be able to rank the appliances from the most to least expensive appliance and determine the top three appliances consuming energy per every test done.
3. By the end of the first quarter, the program should give at least one energy-saving suggestion for each of the top three appliances, tested with five sample households.

Planned Features

Appliances List (Name, Wattage, Hours per day, Number of days per month used)
Will compute the total energy consumption per month in kWh together with cost based on the electricity rates
Cost analysis of the appliances
Percentage that each appliance contributes to the total costs incurred
Saving advice for the two major consumers of power
Difference between estimate and user bill
File Output

Planned inputs and outputs

INPUTS:
  Cost of electricity per kWh
  Name of appliance
  Energy usage per appliance
  Number of hours used per day
  Number of days of use per month
  Actual bill
OUTPUTS:
  Monthly energy consumption and cost per appliance
  List ranked from highest cost to lowest
  Calculated total bill for the month
  Share of bill per appliance (%)
  Top three energy-consuming appliances
  Difference between actual and estimated bill

Logic Plan (Pseudocode) 

START
  ASK user for electricity rate per kWh
  CREATE empty list called appliances

  REPEAT
    ASK for appliance name, wattage, hours per day, days per month
    IF any value is negative or not a number
      SHOW error message and ask again
    ELSE
      kWh = (wattage × hours × days) / 1000
      cost = kWh × rate
      ADD (name, kWh, cost) to appliances
    ASK "Add another appliance? (yes/no)"
  UNTIL user answers no

  total_cost = sum of all appliance costs
  FOR each appliance
    share = (cost / total_cost) × 100
  SORT appliances from highest to lowest cost

  DISPLAY ranked list with kWh, cost, and share
  DISPLAY total_cost

  FOR each of the top 3 appliances
    DISPLAY the saving tip for that appliance type

  ASK if user wants to enter actual bill
  IF yes
    difference = actual_bill − total_cost
    DISPLAY difference

  SAVE results to a file
END

