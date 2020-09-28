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
- every atom type requires a defination of a force constant, k, and an equilibrium length, $r_{eq}$, between it and, in principle, every atom type difined so far
- NUmber of bond stretch parameters goes up as N^2 where N is the number of atom types...
- assignment of parameters from experimental data or from hign level QM calculations













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















