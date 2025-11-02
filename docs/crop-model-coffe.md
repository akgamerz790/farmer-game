# Crop Model Diagram
![Crop Model Diagram](crop-model-diagram.png)

# Coffee Lifescyle
![Coffee Lifescyle](coffee-lifecycle.png)

ID-C : Initial Development Cycles = 50
D-C : Development Cycles = 100
F-C: Flowery Cycles = 10
P-C: Production Cycles = 40

### Development Stage
Will determine the amount of flowers and leaves.
Flower production has higher priority, but if the `leaf_rate` is set too low at the beginning of this stage, the plant will be forced to produce more leaves and fewer fruits.

### Flowery Stage
The max number of fruits is already determined on the last stage.
In this stage, the flowers will grow and fall.
It will determine the amount of healthy fruits that will mature in the Production stage.

### Production Stage
The number of fruits determined by the end of the Flowery stage will develop.
This stage will determine fruit quality and average size (although size is mainly defined by the variety).

# Coffee Growth Tests
I'm trying to analyze the effects of the environment on the crop growth.

## Effects of sun with no hydric stress
![Coffee Lifescyle](leaf-growth-by-sun-model.png)


# Coffee Crop model

### TODO: complete

- **Nutrition**:
  - **Components:**
    - Water
    - Minerals
    - Organic Matter
  - **Mechanics:** In each cycle, a quantity determined by the *absorption flow* is extracted until the *saturation quantity* is reached. The plant's health in each cycle is determined, among other things, by the quantity present in the plant.
    - Absorption flow
    - Desired quantity
    - Saturation quantity
- The entity Substract is a container of nutrients.

- **Health:**
   - **Mechanical**: In each cycle, health is calculated/altered based on plant factors.
  - **It directly affects:** The immune system, the plant's vital state (alive/dead).
  - **Nutrition:** (Water, minerals, organic matter)
    -Affected by: low concentration in the soil
  - *Defoliation index*: percentage of leaves lost
    - Affected by: diseases
    - It affects: *Energy capacity* (photosynthesis)
      - It affects: Development capacity

- **Development:**
  - Affected by:
    - Nutrition
    - Energy capacity
  - Phases:
    - Branch development (growth)
    - Reduction of defoliation (recovery)
    - Fruit development (production)
  - *Mechanics*: In each cycle, the plant dedicates a certain percentage to each phase, totaling 100%. What influences this distribution? **TODO: Research**

- **Problems**
  - Rust / Cercospora leaf spot
    - It affects: defoliation
    - Action stage: **TODO: research**
    - Life cycle: **TODO: research**
  - Bicho Mineiro
    - It affects: defoliation
    - Action stage: **TODO: research**
    - Life cycle: **TODO: research**
  - Nematode
    - Affects: **TODO: search**
    - Action stage: **TODO: research**
    - Life cycle: **TODO: research**
  - Fruit borer
    - Affects: productivity
    - Stage of action: while there are fruits
    - Life cycle: remains alive, but inactive in *old remaining fruits* **(TODO: new model parameter? This parameter can be used to determine the probability of infection by the fruit borer)** after harvest. They migrate to new fruits during the productive stage.

- **Immune system**
  - Mechanical: with each cycle, it reduces the health of present agents.
  - Natural
  - Defensives

- **Climate:**
  - Temperature
  - Humidity / Rainfall

- **Geographical**
  - Relief?
  - Altitude
