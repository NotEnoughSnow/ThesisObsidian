#summary 

A summary of [[Biologically Plausible Variational Policy Gradient with Spiking Recurrent Winner-Take-All Networks - summary]]
arxiv: https://arxiv.org/abs/2210.13225

### Methods Used

- **Spiking recurrent winner-take-all network (RWTA)**: A network structure used for the proposed method.
- **Spiking Variational Policy Gradient (SVPG)**: A new R-STDP method derived from the global policy gradient, eliminating heuristic designs.
- **Energy-based policy formulation**: Applied in conjunction with RWTA networks to establish theoretical relationships.

### Mentioned

- **Biologically plausible models**: Simulating biological intelligence for reinforcement learning.
- **Neuromorphic hardware**: Hardware that mimics neuro-biological architectures present in the nervous system.
- **Reward-modulated spike-timing-dependent plasticity (R-STDP)**: A method with potential in energy efficiency.
- **Artificial Neural Networks (ANNs)**: Previously applied to various scenarios with limitations in adaptability and robustness.
- **Spiking Neural Networks (SNNs)**: Divided into ANN-to-SNN conversion, heuristically approximated backpropagation, and modulated STDP.
- **Variational inference**: Used to derive local learning rules from a global target, providing a biologically plausible approach.

### Explained

- **Local learning rules**: Derived from the global policy gradient for SVPG, as opposed to heuristic designs.
- **Variational inference in R-STDP**: Investigated for the first time in this paper to bridge the gap between local learning rules and the overall RL optimization target.
- //algorithms and code

### Results

- **Training performance**: SVPG achieves comparable accuracy to BP in MNIST and near-optimal performance in Gym InvertedPendulum.
- **Robustness against noise**: SVPG shows superior robustness to input and network parameter noise, outperforming other methods in the presence of noise.
- **Adaptability to environment variations**: SVPG demonstrates natural adaptability to a range of pendulum shapes in the Gym InvertedPendulum task, indicating inherent robustness.
- **Network sparsity**: SVPG tends to learn a more sparse network, indicated by the distribution of synapse weights.
- **Hidden layer response**: The recurrent design of the network contributes to the robustness of SVPG against input noise.
- **Computational costs**: The rate coding version of SVPG is efficient in optimization and competitive in inference time.

### Conclusions

- SVPG bridges the gap between local R-STDP rules and the global RL target, offering a more robust and efficient approach.
- The method’s success in solving tasks and its robustness to noise suggest its potential for broader applications in RL.
- Future work will focus on further theoretical analysis and real-world control problem experiments to improve the method and advance research in biologically plausible RL methods.

