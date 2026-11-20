---
layout: page
title: Projects
permalink: /projects/
---

# Selected Projects

My projects reflect my interest in translating research,
technical ideas, and real-world problems into practical
solutions through experimentation and engineering.

---

## Multi-Agent Deep Reinforcement Learning

**Research · Deep RL · Wireless Communications**

Doctoral research investigating intelligent decision-making
and resource allocation in wireless communication networks.

Explored multi-agent reinforcement learning, cooperation,
partial observability, fairness, and system constraints.

**Technologies:** Python, PyTorch, Ray RLlib, PPO, MATLAB.

[Explore my research]({{ '/research/' | relative_url }})

---

## BIXI — Intelligent Urban Mobility

BIXI is Montréal's public bicycle-sharing system.
My research explores how machine learning and deep
reinforcement learning can improve bicycle-sharing
decisions through availability forecasting and
intelligent station selection.

The work consists of two connected projects:

1. Short-Term Bike and Dock Availability Prediction
2. DRL-Based Bike-Return Station Selection

---

### Project 1 — Short-Term Bike and Dock Availability Prediction
![BIXI availability prediction concept — current versus future bike and dock availability]({{ '/assets/bixi_availability_now_versus_next.png' | relative_url }})


*Concept visualization illustrating how predictive availability could improve BIXI trip planning.*

**Machine Learning · Time-Series Forecasting · Urban Mobility**

<!-- Keep your existing working BIXI image here. -->

#### The Problem

Bicycle-sharing systems are highly dynamic. The number
of available bicycles and empty docks changes continuously
as users pick up and return bicycles.

Although BIXI provides real-time station availability,
current information does not guarantee that a bicycle
or dock will remain available when a user arrives.

This creates two challenges:

- A user may reach a station with no available bicycles.
- A cyclist returning a bicycle may find that the station
  has become full.

#### Research Objective

Develop machine learning models to predict bicycle
and dock availability at individual BIXI stations
over **15-, 30-, and 45-minute forecasting horizons**.

The objective is to investigate whether historical
mobility patterns and station activity can improve
the estimation of future station conditions.

#### Technical Implementation

**Data Collection and Preprocessing**

- Analyzed historical BIXI trip records and station data.
- Investigated station-level bicycle arrivals and departures.
- Processed trip records to construct time-based activity features.
- Examined variations across stations, hours, and weekdays.
- Investigated station-specific demand and mobility patterns.

**Predictive Modeling**

- Applied CatBoost regression for station-level predictions.
- Modeled bicycle arrival and departure patterns.
- Investigated forecasting approaches for future bicycle
  and dock availability.
- Considered temporal and station-specific characteristics.

**Model Evaluation**

The evaluation focuses on:

- Prediction accuracy across different forecasting horizons.
- Variations in forecasting performance across stations.
- Performance during periods of high station activity.
- The usefulness of predicted availability for downstream
  station-selection decisions.

#### Research Questions

1. How accurately can bicycle and dock availability
   be predicted using historical station activity?
2. How does forecasting performance vary across
   15-, 30-, and 45-minute horizons?
3. Can predicted availability improve decisions
   compared with relying only on current information?

#### Technologies

`Python` · `Pandas` · `CatBoost` · `Scikit-learn` ·
`Time-Series Forecasting` · `Data Analysis`

---

### Connection to Deep Reinforcement Learning

Availability prediction provides estimates of future
station conditions, but it does not directly determine
which station a cyclist should choose.

This motivates a second project that investigates
**prediction-informed deep reinforcement learning**
for bicycle-return station selection.

The DRL agent learns to select a return station from
nearby candidates. If the selected station has no
available dock upon arrival, the agent receives a
penalty and must choose another station.

Two observation configurations are investigated:

- **Reactive Agent:** Uses current dock availability.
- **Prediction-Informed Agent:** Uses predicted dock
  availability at the expected arrival time.

Both agents use the same action space and reward
mechanism, allowing the effect of predictive
information on decision-making to be evaluated.

---

### Project 2 — Prediction-Informed DRL for Bike-Return Station Selection

**Deep Reinforcement Learning · Sequential Decision-Making ·
Predictive Modeling · Urban Mobility**

#### The Problem

When returning a BIXI bicycle, a cyclist may have several
stations near their intended destination.

Selecting the nearest station does not guarantee a
successful return because dock availability can change
while the cyclist travels.

An unsuccessful attempt forces the cyclist to search
for another station, increasing travel time and
inconvenience.

#### Research Objective

Develop a Deep Reinforcement Learning (DRL) cyclist
agent that learns to select suitable return stations
under dynamically changing dock availability.

The agent learns through repeated interactions with
a simulated bicycle-sharing environment, receiving
positive rewards for successful returns and penalties
for unsuccessful attempts.

The research investigates whether predictions of
future dock availability can improve station-selection
decisions compared with current availability alone.

#### Reinforcement Learning Environment

The environment represents a cyclist approaching an
intended destination with several candidate BIXI
stations nearby.

At each decision step:

1. The agent observes availability information for
   candidate stations.
2. It selects a station to return the bicycle.
3. The simulated cyclist travels to that station.
4. The environment checks actual dock availability
   at the time of arrival.
5. The agent receives a reward or penalty.

If the selected station has an available dock,
the bicycle is returned and the episode ends
successfully.

If the station is full, the agent receives a penalty,
observes the updated environment, and selects
another station.

This process continues until a successful return
or an episode termination condition is reached.

#### Observation Design

Two observation configurations are investigated.

**1. Reactive DRL Agent**

The agent observes currently available dock
information for nearby candidate stations.

This configuration represents decision-making
based on the latest observed station conditions.

**2. Prediction-Informed DRL Agent**

The agent observes predicted dock availability
for candidate stations at their expected arrival times.

These predictions are derived from the machine
learning forecasting component developed in
Project 1.

Both configurations use the same station-selection
action space and reward mechanism.

#### Action Space

The action is selecting one station from a set
of candidate stations near the intended destination.

For K candidate stations:

`Action = {Station 1, Station 2, ..., Station K}`

After an unsuccessful return, the agent can
select another candidate station using the
updated observation.

#### Reward Design

The reward function encourages successful
returns while discouraging unsuccessful
station selections and unnecessary travel.

**Successful return:**

- Positive reward when a free dock is available
  at the selected station upon arrival.

**Unsuccessful return:**

- Negative reward when the selected station
  is full upon arrival.

**Travel efficiency:**

- An additional travel-time penalty can be used
  to discourage unnecessarily long journeys.

The episode ends when the bicycle is
successfully returned or a predefined
termination condition is reached.

#### Learning Algorithms

The framework considers deep reinforcement
learning algorithms suitable for discrete
station-selection actions, including:

- Proximal Policy Optimization (PPO)
- Deep Q-Networks (DQN)

The experiments will investigate how
observation design influences policy learning,
station-selection behavior, and decision quality.

#### Experimental Comparison

The two DRL configurations will be evaluated
under comparable simulation conditions.

**Reactive DRL vs. Prediction-Informed DRL**

Potential evaluation metrics include:

- Successful bicycle-return rate
- Number of unsuccessful station attempts
- Additional travel time before successful return
- Cumulative episode reward
- Robustness to prediction errors

Simple station-selection strategies, such as
choosing the nearest station or the station
with the highest available-dock count,
can serve as baselines.

#### Research Questions

1. Can a DRL agent learn effective station-selection
   strategies through successful and unsuccessful
   bicycle-return experiences?

2. Does predicted dock availability improve
   decision-making compared with relying on
   current availability?

3. How do prediction errors affect the
   performance of the learned policy?

4. Can sequential decision-making reduce
   unsuccessful docking attempts and
   unnecessary travel?

#### Technologies

`Python` · `Deep Reinforcement Learning` ·
`PPO` · `DQN` · `Gymnasium` ·
`Predictive Modeling` · `Simulation`

**Project Status:** Research and experimental development.
Comparative performance results will be added
after training and evaluation.
---
## ReturnERA

**Product Engineering · Full-Stack Development · Cloud**

A parcel-return pickup service designed to make online
shopping returns more convenient.

Developed an online booking platform with backend APIs,
relational database models, payment integration, and
cloud deployment workflows.

**Technologies:** Next.js, React, TypeScript,
PostgreSQL, Prisma, Stripe, AWS Lightsail, Docker.

[Visit ReturnERA](https://returnera.ca)

---

## Ongoing Research Experiments

**Reinforcement Learning · Learning from Failure**

Exploring how negative feedback, advantage-based
learning, and temporal information may influence
policy learning and sample efficiency.

These are ongoing experimental investigations,
not established research conclusions.

