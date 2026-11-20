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

      <img
        class="project-card-thumb"
        src="{{ '/assets/bixi_availability_now_versus_next.png' | relative_url }}"
        alt="BIXI bicycle and dock availability prediction"
        loading="lazy"
      >

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

      <img
        class="project-card-thumb"
        src="{{ '/assets/bixi-cyclist.png' | relative_url }}"
        alt="DRL cyclist selecting an available BIXI station"
        loading="lazy"
      >

      <h3>BIXI Intelligent Cyclist</h3>
      <p>
        Prediction-informed sequential
        station-selection decisions.
      </p>
      <span class="project-nav-action">Explore Project →</span>
    </a>

    <!-- ReturnEra -->
    <a href="#returnera-project" class="projects-nav-card">
      <span class="project-type">Software & Applied AI</span>

      <img
        class="project-card-thumb"
        src="{{ '/assets/returnera-bird.png' | relative_url }}"
        alt="ReturnEra parcel pickup service"
        loading="lazy"
      >

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

### The Research Problem

Traditional resource allocation methods can become
computationally expensive or difficult to adapt
to dynamic wireless conditions.

D2D communication introduces additional challenges:

- Multiple users compete for limited spectrum.
- D2D transmissions create interference for
  cellular users and other D2D pairs.
- Wireless channels and network conditions change
  dynamically.
- Agents may have access to limited local information.
- Decisions must respect communication constraints
  while improving network performance.

These challenges motivate learning-based
resource allocation strategies.

### Research Objectives

Develop and evaluate multi-agent reinforcement
learning methods that enable D2D users to make
resource allocation decisions under changing
network conditions.

The research investigated:

1. Decentralized decision-making among D2D agents.
2. Spectrum reuse and transmit power allocation.
3. Interference management and cellular QoS protection.
4. Fairness and efficient resource utilization.
5. The effect of observation design on policy learning.
6. NOMA-enabled D2D communication strategies.

### Technical Implementation

#### 1. Multi-Agent Wireless Environment

Developed simulation environments representing
cellular uplink communications with multiple
D2D pairs sharing spectrum resources.

Each D2D communication pair acts as an agent
that makes decisions affecting both its own
communication performance and network-wide
interference.

The environment models:

- Cellular users and D2D communication pairs.
- Wireless channel conditions and path loss.
- Co-channel interference.
- Signal-to-interference-plus-noise ratio (SINR).
- Communication rate and spectral efficiency.
- Cellular QoS and interference constraints.

#### 2. Multi-Agent Reinforcement Learning

Investigated learning-based resource allocation
using multi-agent deep reinforcement learning.

The agents learn resource allocation strategies
through repeated interactions with a simulated
wireless environment.

Applied Proximal Policy Optimization (PPO)
to investigate policy learning under
different multi-agent training architectures.

#### 3. Centralized and Decentralized Learning

Investigated two multi-agent learning approaches:

**Centralized Training with Decentralized Execution
(CTDE)**

Uses centralized information during training
to support policy learning while enabling
agents to execute their decisions using
locally available information.

**Decentralized Training and Decentralized Execution
(DTDE)**

Agents learn and execute their policies using
decentralized information.

The comparison investigates the tradeoffs
between training information, coordination,
and decentralized decision-making.

#### 4. Information-Aware Observation Design

Investigated how different levels of network
information affect multi-agent policy learning.

Considered observation configurations including:

- **Local observations:** Information available
  to individual D2D agents.
- **Partial observations:** Local information
  augmented with selected network indicators.
- **Full channel information:** More comprehensive
  channel-state information.

The objective was to assess the relationship
between information availability, learning
performance, and practical decentralized
operation.

#### 5. NOMA-Enabled D2D Communications

Extended the resource allocation investigation
to non-orthogonal multiple access (NOMA)
enabled D2D communications.

Studied power allocation and spectrum-sharing
decisions under constraints associated with:

- Cellular-user communication quality.
- Interference management.
- Successive interference cancellation (SIC).
- Resource utilization and fairness.

### Reinforcement Learning Formulation

**Agents**

Individual D2D communication pairs.

**Observations**

Wireless environment information available
to each agent, depending on the selected
observation configuration.

**Actions**

Resource allocation decisions, including
spectrum selection and transmit power
allocation as applicable to the network model.

**Reward**

Learning signals reflecting communication
performance while accounting for QoS,
interference, and feasibility constraints.

**Objective**

Learn policies that improve network
performance while respecting wireless
communication constraints.

### Research Contributions

The doctoral research explored:

- Predictive and cooperative spectrum
  management in cognitive radio networks.
- Learning-based resource allocation for
  cognitive D2D communications.
- Centralized and decentralized multi-agent
  learning architectures.
- Information-aware observation design.
- NOMA-enabled resource allocation with
  communication constraints.
- The role of fairness and interference
  management in intelligent spectrum sharing.
  
### Experimental Evaluation and Research Findings

The proposed learning-based resource allocation
frameworks were evaluated through wireless network
simulations under dynamic communication conditions.

The evaluation investigated network performance,
resource allocation efficiency, and the impact of
information availability on decentralized learning.

#### 1. Spectrum and Energy Efficiency

The predictive cooperative spectrum sensing
framework combined spectrum prediction with
cooperative decision-making.

The results demonstrated improvements in spectrum
utilization while reducing sensing overhead and
energy consumption.

#### 2. MADRL-Based Resource Allocation

A multi-agent reinforcement learning framework
was developed for cognitive D2D communications
underlaying cellular networks.

PPO-based agents learned joint channel-selection
and transmission-power decisions under dynamic
wireless channel conditions.

The experimental evaluation investigated:

- System throughput and spectrum utilization.
- Resource allocation under interference constraints.
- Learning performance in dynamic environments.
- Distributed decision-making with imperfect
  network information.

#### 3. Information-Aware Learning

The NOMA-D2D framework investigated how different
observation configurations affect decentralized
multi-agent policy learning.

Three information configurations were considered:

- **Local Observation:** Locally available
  wireless environment information.
- **Partial Observation:** Local observations
  augmented with selected network indicators.
- **Full Observation:** More comprehensive
  channel-state information.

The experiments explored the relationship between
information availability, network performance,
and decentralized learning requirements.

#### Observation Configuration Comparison

| Configuration | Information Available | Research Purpose |
|---|---|---|
| Local | Agent-specific network observations | Minimize information requirements |
| Partial | Local observations plus selected network indicators | Balance information and performance |
| Full | More comprehensive channel-state information | Evaluate benefits of additional information |

The comparison investigates whether selected
network indicators can provide useful information
for decentralized decision-making without
requiring complete channel-state information.


#### 4. NOMA-Enabled Resource Allocation

The research extended cognitive D2D resource
allocation to NOMA-enabled communications.

The learning framework investigated joint
spectrum reuse and power allocation while
accounting for:

- Cellular quality-of-service requirements.
- Interference constraints.
- Successive interference cancellation (SIC).
- Throughput and fairness objectives.

The simulation results demonstrated improvements
in network performance and fairness relative
to the evaluated comparison methods.

#### Key Research Finding

The research demonstrates the potential of
multi-agent reinforcement learning to address
complex wireless resource allocation problems
through adaptive, distributed decision-making.

It also highlights the importance of observation
design when balancing network information
requirements against learning performance.

**Research Reference:**

[PhD Dissertation — Adaptive and Efficient Resource
Allocation for Cognitive Radio Networks](https://hdl.handle.net/1828/24053)


### Technologies

`Python` · `PyTorch` · `Ray RLlib` · `PPO` ·
`Multi-Agent Reinforcement Learning` ·
`Wireless Network Simulation` ·
`MATLAB` · `Optimization`

### Related Publications

This work contributed to my peer-reviewed
journal research in intelligent wireless
communications and multi-agent reinforcement
learning.

[View Publications]({{ '/publications/' | relative_url }})

[Read My PhD Dissertation](https://hdl.handle.net/1828/24053)


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

<a id="bixi-drl"></a>

### Project 2 — Prediction-Informed DRL for Bike-Return Station Selection
![(DRL) cyclist agent that learns to select suitable return stations under dynamically changing dock availability illustration]({{ '/assets/bixi_cyclist.png' | relative_url }})

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

### Technical Implementation

#### 1. Full-Stack Web Application

Developed a customer-facing booking platform using:

- **Next.js and React** for the web application.
- **TypeScript** for application development.
- **Tailwind CSS** for responsive interface design.
- **Node.js** for server-side application logic.

Implemented customer booking workflows, package
information collection, reference-code generation,
and booking confirmation.

#### 2. Backend and Database Architecture

Designed the backend to support customer information,
pickup orders, and multiple return packages.

Technical components include:

- PostgreSQL relational database.
- Prisma ORM and database migrations.
- REST-style API endpoints for booking operations.
- Unique reference identifiers for pickup orders.
- Package-level data management.
- Booking status tracking.

The database structure supports the relationship
between customers, pickup orders, and individual
return packages.

#### 3. Payment Integration

Integrated Stripe Checkout for online payment
processing.

The implementation includes:

- Checkout session creation.
- Server-side payment processing workflows.
- Stripe webhook handling.
- Payment-status verification.
- Configuration for test and live environments.

#### 4. Cloud Deployment and DevOps

Worked with AWS Lightsail and Docker for application
deployment and infrastructure configuration.

The development workflow includes:

- Git-based source control.
- Environment and configuration management.
- Database schema migrations.
- Application debugging and deployment testing.
- AI-assisted development using coding agents.

### Applied AI and Optimization

The following components are areas of ongoing
development and planned technical research.

#### 5. Intelligent Driver Assignment

Developing methods to assign pickup requests to
available drivers based on operational constraints.

Potential decision factors include:

- Driver availability.
- Driver location.
- Pickup proximity.
- Existing assigned pickups.
- Route efficiency and workload.

The objective is to improve assignment efficiency
and support scalable pickup operations.

#### 6. Pickup and Drop-Off Route Optimization

Exploring optimization methods for consolidating
multiple pickup requests and carrier drop-offs
into efficient routes.

Research considerations include:

- Multiple customer pickup locations.
- Different carrier destinations.
- Travel distance and estimated travel time.
- Pickup scheduling and operational constraints.
- Reducing unnecessary driving.

The objective is to reduce travel costs, improve
service efficiency, and support more sustainable
return logistics.

#### 7. Computer Vision for Package Verification

Exploring computer vision techniques to compare
package images captured at pickup and drop-off.

The proposed system uses image-based matching to
help determine whether the package recorded at
pickup corresponds to the package presented at
the carrier drop-off location.

Potential techniques include:

- Image feature extraction.
- Visual similarity measurement.
- Package identification and matching.
- Detection of package appearance changes.
- Image-based evidence for package traceability.

The objective is to improve package tracking,
support handoff verification, and reduce the
risk of package mix-ups.

Image matching provides supporting evidence
but does not independently prove carrier acceptance.

### Engineering and Research Objectives

ReturnEra combines practical software engineering
with opportunities for applied machine learning.

The project explores how data-driven methods can
improve logistics decisions while integrating
those methods into a functioning customer platform.

Future work includes evaluating driver assignment
strategies, route optimization algorithms, and
computer vision-based package matching.

### Technologies

`Next.js` · `React` · `TypeScript` · `Node.js` ·
`Tailwind CSS` · `PostgreSQL` · `Prisma` ·
`Stripe` · `AWS Lightsail` · `Docker` ·
`Python` · `Computer Vision` · `Optimization`

### Project Website

[Visit ReturnEra](https://returnera.ca)


---

## Ongoing Research Experiments

**Reinforcement Learning · Learning from Failure**

Exploring how negative feedback, advantage-based
learning, and temporal information may influence
policy learning and sample efficiency.

These are ongoing experimental investigations,
not established research conclusions.

