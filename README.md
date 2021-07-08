# Capstone Project - AI Trading Platform

### What is the project?

To build a platform for creating, backtesting and paper trading new automated strategies on real-time, minute scale data with the help of AI models.

# Components in the project

## Data Feeder

- Used to source real-time minute scale data from over 5000 stocks in the stock market.

- Perform very fast, basic calculations on the raw data.

## Database

- We use a database to store the data from the data feeder.

- We also use it to perform more complex calculations (such as indicators) very quickly at a large scale for all stocks whose data has been sent from the data feeder.

## Strategies

###### This is the heart of the project

- Strategies read data from the database and can use multiple indicators, machine learning models, or a combination to generate orders according to the rules mentioned in the strategy.

- There may be multiple strategies created and deployed in this service.

## Backtester

- This service helps in building Strategies. It allows us test how a strategy would have performed over past data over previous weeks, months and years.

- It takes a parameterised strategy and data over the period of the back test as input. It generates orders over the previous data according to the strategy's rules and outputs a detailed report on the performance of the strategy.

## Paper Trader

- This is used to test strategies in real-time market scenarios after a strategy has performed well in back testing.

- It tracks and evaluates orders generated by multiple strategies in real-time market conditions and provides various performance metrics for both strategies and orders.

## UI

- This service is a website which provides a GUI for the user to interact with all the other services.

- It allows the user flexibility to create, back test, paper trade and deploy new strategies on real-time data from the stock market.

# To build this project

### Development environment

1. run these commands to initialize the project:

```

git clone "git@github.com:Varun487/CapstoneProject_AITradingPlatform.git"

cd CapstoneProject_AITradingPlatform

docker-compose -f devops/docker-compose.dev.yml up

```

2. To start the backend and frontend development servers + run all containers:

```

docker-compose -f devops/docker-compose.dev.yml up

```

3. To stop and destroy all containers:

```

docker-compose -f devops/docker-compose.dev.yml down

```

4. Run with fresh build:

```

docker-compose -f devops/docker-compose.dev.yml down

docker-compose -f devops/docker-compose.dev.yml up --build

```

5. To create a super user for the database

```

docker-compose -f devops/docker-compose.dev.yml run restapi python3 manage.py createsuperuser

```

6. To run all restapi tests
```

docker-compose -f devops/docker-compose.dev.yml run restapi python3 manage.py test

```

7. Command to Initialize the database
```

docker-compose -f devops/docker-compose.dev.yml run restapi python3 services/Initialization/initialize_database.py

```
8. Command to run all paper trade services
```

docker-compose -f devops/docker-compose.dev.yml run restapi python3 manage.py papertrade

```

###### NOTE: To run in production, the commands are the same, but the file is `docker-compose.prod.yml`

# Project members

###### All members are from Semester 6 Pes University EC Campus

1. Varun Seshu - PES2201800074
2. Hritik Shanbhag - PES2201800082
3. Disha Venkatesh - PES2201800109
4. Samrudhi R Rao - PES2201800126

# Future prospects

We intend to build a trading system with a broker to place orders generated by the strategies in the live market and generate consistent profits.

# TODO

**PROJECT PHASE 1** _-> COMPLETE BY APRIL END_

![phasecomplete]

1. Final presentation ![doccomplete]
2. FILL WEEKLY PROGRESS PAGE ![doccomplete]
3. 2 Research papers per person ![doccomplete]

**PROJECT PHASE 2** _-> COMPLETE BY JUNE END_

![phaseincomplete]

1. DEV OPS WORK ![componentincomplete]
- [Link to DEVOPS README](https://github.com/Varun487/CapstoneProject_AITradingPlatform/tree/main/devops/)

2. REST API WORK ![componentincomplete]
- [Link to RESTAPI README](https://github.com/Varun487/CapstoneProject_AITradingPlatform/tree/main/restapi/)

3. UI WORK ![componentincomplete]
- [Link to UI README](https://github.com/Varun487/CapstoneProject_AITradingPlatform/tree/main/ui/)

4. REVIEW 1 ![componentcomplete]
- Demo of partial product ![done]
- Presentation ![done]

### VERSION 0.1.0 LAUNCH !

5. FINAL REVIEW ![componentincomplete]
- Demo of full product
- Presentation
- Research paper

### Future features
- Add passive vs active returns feature in backtesting service
- Add analytics on backtests
- Interactive backtest report
- Different Stop Loss /  Take Profit methods
- Risk %, Initial and Final account size
- Grid search on backtests
- Screening Stocks
- Live Trading
- Add Crypto / Forex trading

[done]: https://img.shields.io/badge/DONE-brightgreen
[incomplete]: https://img.shields.io/badge/INCOMPLETE-red
[varunincomplete]: https://img.shields.io/badge/VARUN-INCOMPLETE-red
[varuncomplete]: https://img.shields.io/badge/VARUN-COMPLETE-brightgreen
[dishaincomplete]: https://img.shields.io/badge/DISHA-INCOMPLETE-red
[dishacomplete]: https://img.shields.io/badge/DISHA-COMPLETE-brightgreen
[samrudhiincomplete]: https://img.shields.io/badge/SAMRUDHI-INCOMPLETE-red
[samrudhicomplete]: https://img.shields.io/badge/SAMRUDHI-COMPLETE-brightgreen
[hritikincomplete]: https://img.shields.io/badge/HRITIK-INCOMPLETE-red
[hritikcomplete]: https://img.shields.io/badge/HRITIK-COMPLETE-brightgreen
[bug]: https://img.shields.io/badge/BUG-red
[bugfixed]: https://img.shields.io/badge/BUG-FIXED-brightgreen
[featureincomplete]: https://img.shields.io/badge/FEATURE-INCOMPLETE-red
[featurecomplete]: https://img.shields.io/badge/FEATURE-COMPLETE-brightgreen
[componentincomplete]: https://img.shields.io/badge/COMPONENT-INCOMPLETE-red
[componentcomplete]: https://img.shields.io/badge/COMPONENT-COMPLETE-brightgreen
[phasecomplete]: https://img.shields.io/badge/PHASE-COMPLETE-brightgreen
[phaseincomplete]: https://img.shields.io/badge/PHASE-INCOMPLETE-red
[meetingincomplete]: https://img.shields.io/badge/MEETING-INCOMPLETE-red
[docincomplete]: https://img.shields.io/badge/DOC-INCOMPLETE-red
[doccomplete]: https://img.shields.io/badge/DOC-COMPLETE-brightgreen
