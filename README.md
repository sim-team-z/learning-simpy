# learning-simpy
learning simpy, its gaps and strengths, write a simple user guide, and illustrating using a sample demo model


### simulation problem (women's shelter)

- An abused women's shelter has to take in women and often their young children to protect them from the abuser. 
- Several times, there are more clients than the beds at a shelter place, and that is when this women's shelter has to book hotel rooms as overflow for the clients. 

1. Hotel rooms are always more expensive than the shelter
2. always have fluctuating prices sometimes not available, or have fluctating prices
3. The women's shelter does have access to government funds but only on a quarterly and annual basis.
4. Hotel costs  Therefore, they need to pre-emptively account for the cost of hotel rooms, and make a request in a government grant.
5. It is important to be not too ask too much in the grant ask else they can get penalized next time; they have to submit receipts/proof of the engagement to the government every quarter to continue receiving money.



#### How to model the outflow from the shelter. 

That only can happen if 
(a) the environment is better to go back to; there is reconciliation, or  
	- (one faster rate but certain proportion X)
(b) the woman is able to find, and prefers moving to, an alternate option (family etc) 
	- (another a bit slower rate and certain proportion Y)
(c) the woman is able to get on her feet and able to earn. The women's shelter provides vocational education and options associated with the community colleges to help such women. (this may always not be a viable option depending on the circumstances of the client)
	- (the slowest outbound rate, with certain proportion Z)

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