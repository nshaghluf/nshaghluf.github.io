---
layout: page
title: Projects
permalink: /projects/
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">

<section class="projects-overview">

  <p class="projects-intro">
    My projects combine research, software engineering,
    and intelligent decision-making to solve problems
    across different application domains.
  </p>

  <div class="projects-nav-grid">

    <!-- MADRL -->
    <a href="#madrl-project" class="projects-nav-card">
      <span class="project-type">Research</span>

     

      <h3>Multi-Agent Deep RL</h3>
      <p>
        Intelligent wireless resource allocation
        and decentralized decision-making.
      </p>
      <span class="project-nav-action">Explore Project →</span>
    </a>

    <!-- BIXI Prediction -->
    <a href="#bixi-prediction" class="projects-nav-card">
      <span class="project-type">Machine Learning</span>

    
      <div class="project-image-frame">
  <img
    src="{{ '/assets/bixi_availability_now_versus_next.png' | relative_url }}"
    alt="BIXI availability prediction concept"
    class="project-image">
</div>

      <h3>BIXI Availability Prediction</h3>
      <p>
        Short-term forecasting of bicycle
        and dock availability.
      </p>
      <span class="project-nav-action">Explore Project →</span>
    </a>

    <!-- BIXI DRL -->
    <a href="#bixi-drl" class="projects-nav-card">
      <span class="project-type">Deep Reinforcement Learning</span>

      <div class="project-image-frame">
  <img
    src="{{ '/assets/bixi-cyclist.png' | relative_url }}"
    alt="BIXI DRL agent"
    class="project-image">
</div>


      <h3>BIXI Intelligent Bike-Return Station Selection</h3>
      <p>
        Prediction-informed sequential
        station-selection decisions.
      </p>
      <span class="project-nav-action">Explore Project →</span>
    </a>

    <!-- ReturnEra -->
    <a href="#returnera-project" class="projects-nav-card">
      <span class="project-type">Software & Applied AI</span>

   
<div class="project-image-frame">
  <img
    src="{{ '/assets/returnera-bird.png' | relative_url }}"
    alt="ReturnEra parcel return platform illustration"
    class="project-image">
</div>
      <h3>ReturnEra</h3>
      <p>
        Full-stack parcel return management
        and intelligent logistics optimization.
      </p>
      <span class="project-nav-action">Explore Project →</span>
    </a>

  </div>

</section>


# Selected Projects

My projects reflect my interest in translating research,
technical ideas, and real-world problems into practical
solutions through experimentation and engineering.

---


<a id="madrl-project"></a>

## Multi-Agent Deep Reinforcement Learning for Intelligent Wireless Networks

**Multi-Agent Reinforcement Learning · PPO ·
Decentralized Decision-Making · Wireless Communications**

### Project Overview

My doctoral research investigated intelligent
resource allocation in wireless communication
networks using multi-agent deep reinforcement
learning (MADRL).

The research focused on cognitive device-to-device
(D2D) communications operating underlaying cellular
networks, where multiple communication pairs reuse
cellular spectrum.

The central challenge is to improve communication
performance while controlling interference and
protecting cellular users.


### Problem

Develop intelligent resource allocation strategies for
device-to-device (D2D) communications sharing cellular
spectrum while managing interference, fairness, and
quality-of-service constraints.

### Technical Approach

- Developed wireless network simulation environments
  with multiple D2D agents.
- Applied multi-agent Proximal Policy Optimization (PPO)
  for spectrum and transmit power allocation.
- Investigated centralized training with decentralized
  execution (CTDE) and decentralized training and
  execution (DTDE).
- Compared local, partial, and full observation models
  to investigate information requirements.
- Extended resource allocation to NOMA-enabled D2D
  communications with SIC and fairness constraints.

### Key Contributions

- Learning-based decentralized resource allocation.
- Information-aware observation design.
- Interference-aware and fairness-constrained
  multi-agent decision-making.
- Comparative evaluation of multi-agent learning
  architectures.

**Technologies:** `Python` · `PyTorch` · `Ray RLlib` · `PPO` ·
`Multi-Agent Reinforcement Learning` ·
`Wireless Network Simulation` ·
`MATLAB` · `Optimization`

[View Publications]({{ '/publications/' | relative_url }}) |
[PhD Dissertation](https://hdl.handle.net/1828/24053)

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

<a id="bixi-prediction"></a>


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
over **15, 30, and 45 minute forecasting horizons**.

The objective is to investigate whether historical
mobility patterns and station activity can improve
the estimation of future station conditions.

#### Research Questions

1. How accurately can bicycle and dock availability
   be predicted using historical station activity?
2. How does forecasting performance vary across
   15, 30, and 45 minute horizons?
3. Can predicted availability improve decisions
   compared with relying only on current information?

#### Technologies

`Python` · `Pandas` · `CatBoost` · `Scikit-learn` ·
`Time-Series Forecasting` · `Data Analysis`

---

<a id="bixi-drl"></a>

### Project 2 — Prediction-Informed DRL for Bike-Return Station Selection
![(DRL) cyclist agent that learns to select suitable return stations under dynamically changing dock availability illustration]({{ '/assets/bixi-cyclist.png' | relative_url }})

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

### Technical Approach

Developing a DRL environment where a cyclist agent
selects a return station from candidates near its
intended destination.

**Observation configurations:**

- **Reactive:** Current dock availability.
- **Prediction-informed:** Forecast dock availability
  at the expected arrival time.

**RL formulation:**

- **Agent:** Cyclist returning a bicycle.
- **Action:** Select a candidate BIXI station.
- **Reward:** Positive for a successful return.
- **Penalty:** Negative for selecting a full station.
- **Transition:** After failure, update the observation
  and select another station.
- **Termination:** Successful return or episode limit.

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

<a id="returnera-project"></a>

## ReturnEra — Intelligent Parcel Return Management

![ReturnEra parcel pickup and delivery illustration]({{ '/assets/returnera-bird.png' | relative_url }})

*ReturnEra — Multiple returns. One pickup. Less hassle.*

**Full-Stack Engineering · Cloud Infrastructure ·
Applied AI · Optimization · Computer Vision**

### Project Overview

ReturnEra is a technology-driven parcel pickup service
designed to simplify online shopping returns.

The platform allows customers to schedule doorstep pickups
for packages being returned through carriers such as
Canada Post, Purolator, UPS, and FedEx.

The objective is to consolidate multiple returns into
a single pickup, reduce unnecessary customer trips,
and improve return-logistics efficiency.

### The Problem

Online shopping has made purchasing products convenient,
but returning items can still require customers to
travel to different carrier drop-off locations.

Customers managing multiple returns may need to:

- Visit several carrier locations.
- Coordinate different return labels or QR codes.
- Spend time traveling and waiting.
- Track multiple packages independently.

ReturnEra addresses this problem through a centralized
booking and pickup-management platform.

### Solution

Developed ReturnEra, an online platform that allows
customers to schedule doorstep pickups for multiple
returns through a single booking process.

### Technical Implementation

- **Frontend:** Next.js, React, TypeScript, Tailwind CSS.
- **Backend:** Booking APIs, order management,
  reference codes, pricing, and validation.
- **Database:** PostgreSQL and Prisma for customers,
  pickup orders, packages, and tracking information.
- **Payments:** Stripe Checkout and webhook integration.
- **Deployment:** AWS Lightsail, Docker, Git,
  and database migrations.

### Applied AI and Optimization

- **Driver Assignment:** Intelligent selection of
  drivers based on location, availability, and workload.
- **Route Optimization:** Efficient scheduling of
  pickups and carrier drop-offs to reduce travel.
- **Computer Vision:** Image-based package matching
  between pickup and drop-off photographs to support
  package identification and handoff verification.

**Technologies:** Next.js · TypeScript · PostgreSQL ·
Prisma · Stripe · AWS · Docker · Python · Computer Vision

[Visit ReturnEra](https://returnera.ca)

---

## Ongoing Research Experiments

**Reinforcement Learning · Learning from Failure**

Exploring how negative feedback, advantage-based
learning, and temporal information may influence
policy learning and sample efficiency.

These are ongoing experimental investigations,
not established research conclusions.

