#summary

A summary of [[An Implementation of Actor-Critic Algorithm on Spiking.pdf]].
mpdi: https://www.mdpi.com/2076-3417/12/20/10430

### methods used
Improved Leaky integrate-and-fire neurons.
Temporal coding.
actor-critic architecture with TD agent.

### Mentioned
Unmanned aerial vehicles (UAV) decision making.
Reinforcement learning learning and related methods.
Advantages of SNN:
- spatiotemporal dynamics
- diverse coding mechanisms
- event-driven
- reduced network size
- less resource consumption
 spike-timing-dependent (STPD)
 Spiking neuron model
 Actor-critic structure

### Explained
Spiking neuron model
Actor-critic structure with TD
	 ![[Pasted image 20240316013217.png]]

- Actor-critic network structure with TD:
**Input:** the initial parameters of actor-critic network θ(0) and ω(0); the parameters of the network after the ith update θ(i) and ω(i); input signal; the maximum running time time_end; the learning rate of actor-critic network αθ > 0, αω > 0;

**1: Initialize the running time time = 0; the state St. 
2: Repeat 
3:     time ← time + 1 
4:     Input signal[time] to the actor-critic network 
5:     if actor network generates action signals then 
6:         Calculate ∇θlogπ(A|S, θ) based on the selected action A 
7:         Update the state S′ and the reward signal Rt+1 
8:     end if 
9:     if critic network generates value function then 
10:        Calculate ∇ωυ(S, ω) 
11:    end if 
12:    if value function gradient and policy gradient have been solved then 
13:        δ ← R(S′) + γυ(S′, ω) − υ(S, ω) 
14:        ω ← ω + βδ∇ωυ(S, ω) 
15:        θ ← θ + αδ∇θlogπ(A|S, θ) 
16:        S ← S′ 
17:    end if 
18: Until time > time_end**
### results
Gridworld
UAV Flying through Window Task
UAV Avoiding Flying Basketball Task

### Conclusions
- explores the application of temporal encoding in **reinforcement learning**
- The network, consisting of 2–3 layers, is capable of complex tasks like UAV navigation and obstacle avoidance.
- temporal coded spiking neural network RL method offers faster decision-making and better biological interpretability compared to traditional networks.


#### related references
[A decision-making model based on a spiking neural circuit and synaptic plasticity](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5637713/)
[A model of hippocampally dependent navigation, using the temporal difference learning rule](https://onlinelibrary.wiley.com/doi/10.1002/(SICI)1098-1063(2000)10:1%3C1::AID-HIPO1%3E3.0.CO;2-1)
[Temporal difference model reproduces anticipatory neural activity](https://pubmed.ncbi.nlm.nih.gov/11255572/)
[Reinforcement Learning Through Modulation of Spike-Timing-Dependent Synaptic Plasticity](https://direct.mit.edu/neco/article-abstract/19/6/1468/7190/Reinforcement-Learning-Through-Modulation-of-Spike?redirectedFrom=fulltext)
[Learning in neural networks by reinforcement of irregular spiking](https://journals.aps.org/pre/abstract/10.1103/PhysRevE.69.041909)
