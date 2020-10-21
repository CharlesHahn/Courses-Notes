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
    + MSD : mean square deviation
    + VACF : 速度自相关函数 velocity autocorrection function
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

## simulation components

#### Simulation methods

Monte Carlo, Molecular Dynamics : both techniques require force fields as inputs


**Monte Carlo** 

```
    step 1 : generate initial structure R. calculate V(R)
    step 2 : modify structure to R', calculate V' = V(R')
    step 3 :  If V' < V then 
                  R <- R', V <- V'
              else
                  generate random number RAND
                  if e^{-(V'-V)/kT} > RAND
                      R <- R', V <- V'
                  endif
              endif
    step 4 : repeat step 2-3 for N steps
```
- energy driven process
- orientation and adsorption


**molecular dynamics**
```
    step 1 : generate initial structure R, r_{i}(0)
    step 2 : generate initial velocity v_{i}(0)
    step 3 : calculate V_{i}(t,R) -> F_{i}(t) = -dV_{i}(t)/dr_{i}(t)
             solve Newton's Law F_{i} = m_{i} \times a_{i}
             Update
                r_{i}(t+ \delta t) = r_{i}(t) + v_{i}(t) \delta t + 0.5a_{i}(t)\delta t^2
                v_{i}(t+\delta t) = v_{i}(t) + 0.5[a_{i}(t) + a_{i}(t+\delta t)] \delta t
    step 4 : repeat step 3 for N steps
```

- force driven process
- conformational structure and time correlation properties

#### components of one simulation software 

**developers**
- Jie Zheng
- Jian Zhou
- Yi He

**inputs**
- molecule lists
- nonbond lists
    + brute search algorithm
- active lists
- constraint list
- initial velocity
    + maxwell algorithm

**engine**
- molecular dynamics
    + residue and all-atom models
- force fields
    + CHARMM, UFF, self-defined FF
- energy and force calculation
    + intra : bond, angle, UB, dihedral, improper
    + inter : VDW & Electrostatic
- neighbor lists
    + Atom, group, and cell lists
- constraint method
    + Harmonical and Fixed
- P.B.C.
    + Arbitrary P.B.C.
- temperature control
    + velocity scaling, Berendsen
- shear movements & controls

**analysis**
- structure
    + MSD, RDF, density, dipole distribution, RMSD, radius of gyration
- Friction anlysis
- solvent dynamics
- hydrogen bonds
- multipole components
- energy components

#### analysis

- rasidence time dynamics of water around surface
- reorientational dynamics of water around surface

#### 20200923

系综平均 ：我们用模拟求到的数据大部分都是系统一段时间里面的平均值

MD假设：MD在短时间内的模拟cover了实际实验发生的所有情况

#### deeper aspects of the PES

- PES (potential energy surface) : each structure has associated with its unique energy
- depends in a fundamental way on the Born-Oppenheimer approximation
- inherently a classical construct with respect to che nuclei (but quantum in the electronics)
- corresponds to a single molecule; thinking about a collection of molecules requires us to bring in thermdynamics
- minima and saddle points matters !

#### mature concepts in physical organic chemistry

- strain is a phenomenon associated with individual components of a molecular geometry being constrained by the overall geometry not to be able to adopt a common, "transferable", ideal
- strain comes in various flavors: bond, angle, and torsional, for example
- ideal values of bond lengths, angles, and torsions, depends on more than just the atomic number, e.g., there are different "types" of the same atom
- a "force field" is defined by its atom types, its functions for computing strain, and the ideal constants that appear in those functions

#### the constants

- more atom types, the more sensitive the force field is
- every atom type requires a defination of a force constant, k, and an equilibrium length, $r_{eq}_$, between it and, in principle, every atom type difined so far
- NUmber of bond stretch parameters goes up as N^2 where N is the number of atom types...
- assignment of parameters from experimental data or from hign level QM calculations

#### torsional strain is a periodic function of tihedral angle

<++>

#### simulation with MM force fields

Monte Carlo (MC) and Molecular Dynamics (MD)

1. how wo find she lowest point on the PES ?
- at absolute zero a system in thermal equilibrium state must in the global minimum.
- increase the efficiency of searching for the global minimum is an active area of research.

2. some commom search strategies
- systematically search all coordinates
- dynamics + "quench"
    + roam over the surface, occasionally sliding down to the nearest local minimum.
- simulated annealing
    + heat the system up, and cool very slowly.
- evolutionary/genetic algorithm
    + allow the good geometries to survive and share properties, but bad ones to die

3. phase space - 1d harmohic oscillator ( speed and location)

4. 计算的步长很重要，一般是0.5 - 1 fs，如果更高，就需要对原子的某些采取限制（如 LINCS）

5. Integrating over phase space
- expectation values are dictated by the relative probabilities of being in different regions of phase space

6. phase space is 6N-dimentional. 3N of position and 3N of momentum.

7. **ergodic dypothesis**
    - 分子动力学模拟的各态遍历特性
    - 如果MD的模拟时间足够长，那么体系一定经历了所有可能的状态

8. MC
- 计算不需要计算导数，只计算速度，会更快
- 不需要更新全局的数据和坐标
- MC不能得到时间相关的概念

### lammps software

1. usages: 
    - MD
    - EM
    - MC

2. can model systems from a few particles up to billions of particles

3. open source in C++

4. input files
    - structure.dat
        + size of box, atoms types, the position of atoms, etc
    - In.filename
        + instructions
        + ff
        + position of each atoms
    - pot.mod 
        + potential file, contains information about the potential to use
        + not necessary




## Tutorials on Linux cluster, Monte Carlo and Molecular Dynamics Methods

#### Numerous Websites

- http://www.ch.embnet.org/MD_tutorial/
- http://www.ece.uci.edu/~sjenks/Presentations/Linux%20Clustering.pdf
- http://www.sci.hkbu.edu.hk/hpccc/sciblade/course/linux/linuxNcluster.ppt
- http://www.centors.org/docs/5/pdf/Cluster_Administration.pdf
- http://www.ele.polyu.edu.hk/~enpklun/ENG224/Linux.ppt
- http://www.csun.edu/~vcact00f/311/termProjects/700class/Linux.ppt

#### Linux

- **shell** interprets the commands and request service from kernel
- Similar to DOS but DOS has onjy one set of interface while Linux can select different shell
    + Bourne Again shell(bash)
    + TC shell (Tcsh)
    + Z shell (Zsh)
- different shell has similar but different functionality
- bash is the default for Linux
- Graphical user interface of Linux is in fact an application program work on the shell
- UNIX is case sensitive
- UNIX filename contain only letters, numbers, underscore, dot, dash characters
- the extension can be any legal characters
- convert plain text files from DOS/MacOS to UNIX format: $ dos2unix
- only one file in the same directory with the same name
- always backup your source code and data

#### Linux system

/
    - bin : Important Linux commands available to the average user.
    - boot : the files necessary for the system to boot. Not all linux distribution use this one. Fedora does
    - dev : all device drivers. Device drivers are the files that system uses to talk for hardware.
    - etc : system configuration files.
    - home : every user except root gets its own folder in here.
        - larry
        - neo
    - lib : system libraries. Libraries are lust bunches of programming code that the programs on this system use to get things done.
    - proc
    - mnt : Mount point. 
    - root : the root user's home directory.
    - sbin : essential commands that are only for the system administrator.
    - tmp : temporary files and storage space. 
    - usr : programs and data that can be shared across many system and don't need to be changed.
    - var : data that changes constantly ( log files that contain information about system and something)

#### Linux Command

- compress - compress file1
- diff f1 f2
- du summarized disk usage of your home directory
- find (find ./ -name .cshrc -print) search and print
- grep (grep student \*) search all files with the word "student"
- history (history 50) find the last 50 commands stored in the shell
- kill (kill -9 2036) terminate the process with pid 2036
- ps (ps -ef) find out all process run in the systems
- lpr (lpr -h f1 f2) print f1, f2 without header page
- man (man tar) displaying the manual page on-line
- nohup (nohup matlab < a &) run matlab (a.m) without hang up after logout
- sort (sort -r -n studno) sort studno in reverse numerical order
- tar (tar czvf/xzvf abc.tar.gz abc/) create archive file, z means zip, c means compress, v means verbose
- uncompress (uncompress file1.Z) the oppsite of compress
- wc (wc -l f1) count the number of lines in f1
- who who is on line
- whoami identify yourself

#### material studio 0930

- quench 淬火 : 升到高温然后快速降温，得到复杂构型
- anneal 退火 ： 变化到结构比较合理的状态
- forcite -> 计算动力学
    + energy -> 算能量
    + dynamics -> 做EM
    + NPT ...

#### interaction

- contacts
    + bond 
    + angel
    + proper dihedral(torsion)
    + improper dihedral (torsion) ( three atoms linked to one atom)
- non contacts
    + coulomb
    + van der vaal

#### 奥本海默近似

原子和电子是一起的，相互之间不会有位移，被认为是一个整体

#### 计算扩散系数和径向分布函数

要考虑 周期性边界条件 导致的误差

要先去周期性，再计算





# task

## code a monte carlo MD program in Julia

## MC和MD的结合 - 算抑制剂与蛋白质之间的能量和性质

1. 小分子与蛋白质结合位置、体位随机 - MC
2. 选取MC最低能量的构型进行MD






# read reports

### 1 二维纳米层状材料间层储能机理

nvt 系综，1fs，cutoff of coulomb 1.6 nm, cutoff of VDW 1.0 nm.

探索电极片间离子的扩散等

### 2. 描述聚乙烯实验分子构象、熔体动力学和相变的MD

ff 
- PYS : PE熔体的物理性质和熔体动力学
- TraPPe-UA : 广泛应用于PE熔体的<++>

### 3. 利用能量空间中的盒分子动力学自适应加速反应分子动力学文献报告

加速方法：
- milestoning
- transition interface sampling
- nested sampling approaches
- boxed molecular dynamics

### 4. 基于分子模拟的NNS凝胶化过程机理研究

ff : COMPASII

监视所有si-o的原子距离，统计

### 5. MDS of a superhydrophobic cellulose <++> 化工材料, adulose 

开发性能优异的环境友好型疏水材料

通过评估**接触角**评价疏水性，接触角大于150°，超疏水

### 6. 基于金属参杂的MoS2纳米化的适温SO2气敏特性

这个人讲的量子化学计算

### 7. Simulation study on CO2-adsorption by MOFs modification

利用MC模拟气体在MOFs里面的吸附行为

可以预测MOFs对于气体的筛选能力

### 8. FEC作为电解液添加剂对电解液性能低影响

研究溶剂化结构和扩散系数

非极化力场模型；OPLS-AA力场

计算溶剂配位数

结合了MD和第一性原理计算

### 9. 聚合物熔体剪切变稀分子动力学模拟

体积自相关函数 - 解聚 - 物质待在某一体积内的随时间变化的比例 ???

LJ势能是为描述惰性分子性质而建立的

### 10. Peptides MOFs 手性药物拆分

MC 探究拆分机制

在MOFs的有机骨架中添加手性受体

### 11. 甲烷和二氧化碳在纳米孔中的吸收

...

### 12. 液相激光破碎法制备石墨烯量子点的机理研究

Mangiardi提出混合并行化短程分子动力学模拟算法，但仍运用Verlet list

相互作用计算
- verlet list
- 投影排序法

### 13. 重复不计

...

### 14. 陈润道 稀有气体 MOFs 高通量吸附分离捕捉 吸附稳定性

MOFs 结构参数化：最大孔穴直径（腔体）、最小孔穴直径（瓶颈）

**步进式高通量筛选**
- 1000步MC之后选前0.05
- 3000步MC之后选...

### 15. 氢键对分子旋转运动的影响

定量描述水分子的重定向

轨迹- 角位移-多项式拟合

### 16. 冰对甲烷水合物成核的影响：微观分子动力学的研究

...

### 17. 基于玻璃态的分子动力学建模过程

...

### 18. MOFs 吸附分离模拟研究

Grand Canonical Monte Carlo (GCMC)

### 19. 氧化石墨烯与水合硅酸钙界面键合性质的MD模拟

...

### 20. 铜镍薄膜的结构和力学特征

...














