

### Init:
init [[hyperparameters]]

set environment
[[actions]] dim,[[ observations]] dim <- environment

set actor network 
	ANN()
		input: number of total observations
		output: number of total actions
set critic network 
	ANN()
		input: number of total observations
		output: 1

set actor optimizer
	ADAM
		actor ANN: parameters
		learning rate: from [[hyperparameters]]
set critic optimizer
		critic ANN: parameters
		learning rate: from [[hyperparameters]]

set covariance matrix 
	cov(action dim,) 
	$$ cov = \begin{array}{cc} 0.5&0&0  \\ 0&0.5&0 \\ 0&0&0.5 \end{array} $$

init [[logging]]
### learn:

t : timesteps <- 0
	timesteps simulated so far
i : iterations <- 0
	iterations ran so far

loop ( t, i ): 
	 running environment steps
	 vars <- rollout
		 batch length, obs\[], acts\[], log_prob\[], rtg\[]
	 t++ (batch length)
	 i++
	 V <- evaluate(obs\[], acts\[])

### evaluate:


### Compute_rtg:

### Get action


