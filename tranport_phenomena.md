# transport phenomena

## lecture zero on 200915

#### contents of Text Book

- Flow of pure fluids at constant temperature
    + with emphasis on viscous and convective momentum transport (C1-8)
- Flow of pure fluids at varying temperature
    + with emphasis on conductive, convective, and radiative energy transport (C9-16)
- Flow of fluids with varying composition
     + with emphasis on diffusive and convective mass transports (C17-24)

#### Syllabus

four unit tests, two in Autumn

#### Grading

Unit Exams = 10% * 4; Assignments = 20%; Final Exam = 40%;

Assignments：
- Each assignment has been listed on the course syllabus.
- Assignments are due within a week after each lecture (before each Tuesday).
- Should be written in English.

Unless you have an acceptable excuse, there will be a penalty on late assignments.
- if late, the grade will be reduced.

Write assignments by hand.

#### what are transport phenomena

- fluid Mechanics / momentum transport
    + conservation of momentum, fluid statics and dynamics
- heat transport 
    + conservation of energy / energy transport
- mass transport 
    + mass balance of various chemical species / mass transport

#### why do we need to study these topics

- biotechnology
- microelectronics
- nanotechnology
- polymer science

#### why study them together

- often occur together (in above processes)
- mechanisms of transport are similar, based on molecular movements and interactions
- basic equations are similar, solving three transport problems "by analogy"
    + eg. the basic equations describing molecular transport:
        $$ \tau_{yx}= -u \frac{dv_{x}}{dy}$$
        $$ q_{y} = -k \frac{dT}{dy}$$
        $$ j_{A,y}=-cD_{AB}\frac{dx_A}{dy}$$
- similar mathematic tools for solving three transport problems

#### three levels of transport

- macroscope level (equipment level)
    + a set of equations called "macroscopic balances" are used to describe the total change of momentum, energy and mass in the system
- microscope level (molecule < scale equipment)
    + a set of equations called the "equations of change" are used to describe how change of momentum, energy and mass within a small region
- molecular level
    + seek a fundamental understand of the mechanisms of transport

#### contents of the course

- Part 1. preparative knowledge
- Part 2. fundamental concepts & simple illustrations
- part 3. foundation of transport phenomena
- Part 4. typical solutions in transport phenomena
- Part 5. selected topics in transport phenomena


## lecture one on 200915

**Part 1. preparative knowledge: vectors and tensors in cartesian coordinates (I)**

### concept of vectors

the concept of vectors came from the physical quantities which posses two characteristics: **magnitude** & **direction**.

#### Addition & Subtraction

Addition & Subtraction by Parallelogram/Triangle
$$\underline{v} + \underline{w}$$ 
$$\underline{v} - \underline{w}$$ 

Multiplication by a scalar
$$\underline{w}= k \underline{v} $$ 
The magnitude is altered by a factor |k|. The direction keeps the same or reversed, depending on the sign of k.

#### Dot product of two vectors

$$\underline{v} · \underline{w} = vwcos\phi_{\underline{v}\underline{w}}$$ 

the dot prduct of two vectors is a scalar.

commutative: 
$$\underline{v} · \underline{w} = \underline{w} · \underline{v}$$ 

**Not associate**: 
$$(\underline{u} · \underline{v})\underline{w} \ne \underline{u}(\underline{v}·\underline{w})$$ 

distributive: 
$$\underline{w}·(\underline{u} + \underline{v} = (\underline{w}·\underline{u}) + (\underline{w}·\underline{v})$$


#### cross product of two vectors

$$\underline{v} \times \underline{w} = (vwsin\phi_{\underline{v}\underline{w}})\underline{n}_{\underline{v}\underline{w}}$$ 

the cross product of two vectors is a new vector perpendicular to both the vectors by right hand rule.

**Not Commutative** : 
$$\underline{v}\times\underline{w} = - \underline{w} \times \underline{v}$$ 

**Not associative**:
$$(\underline{u}\times\underline{v})\underline{w} \ne \underline{u}(\underline{v}\times\underline{w})$$ 

#### Analytical description of vectors

- a vectors can be expressed in Cartesian coordinates as the following sum. $\underline{\delta}_i$ are unit vectors in the directions of coordinate axes $x_i$, named as _base vectors_. $v_{i}$ are known as the components of vector _v_.

$$
\begin{aligned}
\underline{v} =& \underline{v}_{1} + \underline{v}_{2} + \underline{v}_{3} \\
              =& v_1 \underline{\delta}_1 + v_2 \underline{\delta}_2 + v_3 \underline{\delta}_3 \\
              =& \sum^{3}_{i=1}v_i \underline{\delta}_i
\end{aligned}
$$


- addition & subtraction
$$
\begin{aligned}
\underline{v} + \underline{w} =& (v_1 + w_1) \underline{\delta}_1 + (v_2+w_2)\underline{\delta}_2 + (v_3 + w_3)\underline{\delta}_3 \\ =& \sum_i (v_i +w_i)\underline{\delta}_i
\end{aligned}
$$ 

- multiplication by a scalar
$$
\begin{aligned}
a\underline{v} =& av_1 \underline{\delta}_1 + av_2 \underline{\delta}_2 + av_3 \underline{\delta}_3 \\
               =& \sum_i av_i \underline{\delta}_i
\end{aligned}
$$ 






#### summary of algebraic operations

<++>


## Lecture 2. Vectors and Tensors in Cartesian Coordinates

#### review

$$(\delta_i · \delta_j) = 0 if cos(i, j) = 90$$

$$(\delta_i \times \delta_j) = \sum_{k=1} ...$$

$$hhhhh_$$ 

#### cnocept of Tensors

Teh concept of tensors came from the physical quantities with characteristics connected to more than **one direction**.

#### Dyadic Product & Dyads

- the dyadic product of two vectors **a** and **b**, donoted as **ab**, forms a 2nd-order tensor.

$$ab = ab^t$$

#### unit dyads

with the help of unit dyads, the dyadic product of two vectors can be defined analytically as:
$$_vw_ = \sum_{i} v_{i}\sigma_{i}$$ 

<++>

#### second-order tensors


#### matrix notation of second-order tensors


#### special second-order tensors 

the **unit tensor** is defined as 
$$\delta = \sum_{i}\sum_{j}\delta_{ij}...$$ 

<++>

<++>

<++>

#### decomposition theorem

<++>

#### algebraic operations of tensors

<++>

: first . inside two unit tensor, then outside two unit tensors


#### summation by dummy indices

<++>

the two indices alike are called <++>

#### transformation rules ot <++>









