# learning-simpy
learning simpy, its gaps and strengths, write a simple user guide, and illustrating using a sample demo model


## Simulation Problem (non-profit women's shelter)

The non-profit women's foundation we volunteer with provides services for abused women in North Texas. One of the services is to provide a safe shelter for the women and their families.
The foundation is now at capacity with their shelter. It is actively seeking to apply for a loan create another shelter. The cost of the new shelter is directly proportional to the number of beds. Therefore, it has to determine, and explain in the business case, the optimum number of beds to cater for the growing needs.

This model attempts to simulate the current scenario and simulate the distribution of families this organization has to turn away because of current capacity constraints.

### Workflow Diagram

![The workflow for clients coming into the shelter](images/shelter-workflow.png "Shelter Workflow")


### Workflow details

- An abused women's shelter has to take in women and often their young children to protect them from the abuser. 
- Several times, there are more clients than the beds at a shelter place, and that is when this women's shelter has to either talk to the victim's other family members to take them, or if the issue is life threatening, take them into a private undisclosed hotel.
- In the pandemic the foundation had to refer 30-40 clients/months clients because of capacity problems
- Over the last 6 months, the number has dropped to 15-20 clients.


#### How to model the outflow from the shelter. 

The clients successfully leave the shelter in 4 scenarios:

1. Capable and quickly back on their feet: 

2. Language and cultural barrier: 

3. Mental barrier: 

4. Skills barrier: The women's shelter provides funds for vocational education and options associated with the community colleges to help such women. (this may always not be a viable option depending on the circumstances of the client)

The shelter does not force any of its client out ever, so the outflow is completely variable and needs to be modeled as well.

other notes:

- these events are happening over days of year (so thats a decent granularity/time horizone)
- there are other costs, like travel (Uber), food etc which also are related to whether the woman lives at a shelter or at a hotel room
- they are also exploring rented apartments as an option for another location, and this is another cost that could use help modeling, but its up to us if this would complicate the modeling further



### running jupyter notebooks locally

1. git clone this repo, and cd into the `learning-simpy`directory

2. create a virtual environment 

```
knail1s-MBP.home [learning-simpy]$
knail1s-MBP.home [learning-simpy]$ python3.7 -m venv venv
```

3. activate the venv

```
knail1s-MBP.home [learning-simpy]$ . venv/bin/activate
(venv) knail1s-MBP.home [learning-simpy]$
```

4. install the requirements for the venv
```
(venv) knail1s-MBP.home[learning-simpy]$ pip install -r requirements.txt
```

4. start jupyter notebook, go into the notebooks/ directory and open any of the notebooks there.

```
[learning-simpy]$ jupyter notebook
```