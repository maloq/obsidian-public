
### Problem statement

"Understanding homogeneous crystal nucleation under deep undercooling conditions remains a formidable issue, as crystallization is essentially heterogeneous in nature and initiated from impurities, surfaces, or near grain boundaries that often hinder its occurrence. Unreachable until very recently, experimental observations of early stages of nuclei was achieved by a _tour de force_ using time tracking of three-dimensional (3D) Atomic Electron Tomography of metallic nanoparticles. Those complex phenomena remain to date out-of-reach experimentally for bulk systems, thus hindering our theoretical understanding. This line of research still belongs mostly to the domain of atomic-level simulations and more particularly to molecular dynamics (MD) with generic interaction model. To reach statistically meaningful events, large scale simulations are required. This still remains challenging as only few studies are providing now million-to billion-atom simulations for monatomic metals."
[🧷Unsupervised topological learning approach of crystal nucleation](🧷Unsupervised%20topological%20learning%20approach%20of%20crystal%20nucleation.md)

In short: We want to assign atoms or groups of atoms to $S$ groups which have physically distinct properterties(liquid, crystal forms, etc). 
Data represented by $N$ $(~10^6)$ atoms of known element, with known momentum $\vec{p_i}$ and coordinates $\vec{q_i}$ for every timestep $t_i$ , with total $T$ steps and known $\Delta t$ time resolution.
### Goals

- Develop a machine learning framework that characterizes and differentiates local atomic structures and crystalline order in atomic simulation data.
- Build informative representations for phase trajectories of local atomic structures.
- Study the resulting data for physical insights.

 *Phase trajectories here is a set of system states over time*

### Approaches

Local:
1. [Implement informative local representations](Implement%20informative%20local%20representations.md)
1. Perform clustering or classification of local structures
2. Study life of local structures, maybe [Equivariant Graph Neural Operator](Equivariant%20Graph%20Neural%20Operator.md)
3. ???

Global:
Try [[Topological clustering of multilayer networks]]


Вопросы к предыдущему проекту 
Добавить статьи 
Графы
Постановка задачи

Какая область стала кристаллом 
Классифицировать траектории структур во времени 

### Ideas: 
* Use prior crystal structure to move from clustering to classification(or something else)
* Use knowledge that almost all atoms at the end of simulation is are in a solid state
* From future steps we know wich structures will become part of crystal 
* Melting(crystal disintegration) as diffusion process, reverse diffusion as crystallization(genetative model)  
* ...






