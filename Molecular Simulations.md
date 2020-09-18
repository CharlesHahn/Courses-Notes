# Molecular Simulations

Yi He

#### Course Objectives

- Awareness of the opportunities and limitations of MD simulation for scientific and engineering research
- Understanding of the compromise between model complexity/realism and computational expense
- Background that enables interpretation of MD studies reported in the literature
- Physical understanding of the theoretic basis of MD modeling

#### TextBooks

- Molecular Modelling : Principles and Applications (2nd Edition), by Andrew Leach
- Understanding Molecular Simulation: From Algorithms to Applications (2nd edition), by Daan Frenkel and Berend Smit
- Computer Simulation of Liquids by M.P.Allen (Author), D.J.Tildesley (Author)

#### Grading

- 30% from ur attendance and quiz in class
- 70% from ur final presentation, term paper/final project
    + Presentation about Simulation/Experimental paper
        - Pros
        - Cons
- Bonus: people volunteer to answer questions

#### what MD can do

- understanding
- prediction

#### historical perspective on MD

- A few key papers appeared in the 50s and in the 60s that can be regarded as milestones in molecular dynamics:
    + The first paper reporting a molecular dynamics simulation was written by Alder and Wainwright in 1957.
- First MD simulation using continuous potentials ( 1964)
    + RDF : ridial distribution function
    + MSD : mean square displa <++>
    + VACF : 速度自相关函数 <++>
- Loup Verlet calculated in 1967 **the phase diagram of argon** using the Lennard-Jones potential, and computed correlation functions to test theories of the liquid state. The bookkeeping devide which became konwn as **Berlet neighbor list** was introduced in these papers. Moreover the "**Verlet time integration algorithm**" was used. Phase transitions in the same system were investigated by Hansen and Verlet.

#### Computational methods in molecular modelling

- most primitive attempting to compute of some property (often the energy ) as a function of atomic positions
- approaches to the computation
    + fundamental physics
    + paramerisations
    + density functional theory (some parameters)

#### Potential Energy Surface

- PES only depends on the relative position of atoms
- the degree of PES is 3N-6 (N means number of atoms, minus 6 means to get rid of XYZ coordinates and XYZ speeds)
- **在计算键断裂生成的过程中，可能需要多次relax，以使得体系弛豫** 

#### 生物材料界面的模拟实例

**Nonfouling/Super-low fouling** - resistant to the attachments of biomolecules，抗吸附材料，可用于医药设备、海洋涂料等

**Whitesides' nonfouling mechanism** 
- not be hydrophobic
- present hydrogen-bond acceptors
- not contain hydrogen-bond donors
- be electrically neutral

but this mechanism is not adequate, eg. OEG, SAMs, maniitol SAMs.

both of them contain hydrogen-bond donors, but they are nonfouling.

**Simulation methods** - Monte Carlo, Molecular Dynamics

**Monte Carlo** 
- step 1 





