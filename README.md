Provides an example of State Space Model with observed exogenous variables. The data generating process is as follows:
```math
\begin{cases}
y_t &= x_t + \beta_y u_t\\
x_t &= \alpha x_{t-1} + \beta_x v_t + \varepsilon_t
\end{cases}
```
where initial condition for the state variable is assumed to be deterministic, $`x_{0} = 0`$, the structural error 
$`\varepsilon_{t}`$ is a Gaussian white noise with mean 0 and variance $`\sigma_{\varepsilon}^2`$, $`\alpha`$ is real parameter
with abolute value less than one, $`\beta_y`$ and $`\beta_x`$ are non zero real parameters, finally $`\{u_t\}`$ and $`\{v_t\}`$
are exogenous stochastic processes.

Datasets are generated by `dgp/simulexogenousvariables.mod` and `dgp/simulsample.m`. Data can be obtained using the Makefile in the `dgp` folder:
```shell
~$ make all
```
the data are saved in file `data/sample.mat` which can be used to instantiate a `dseries` object. The mod files under subfolder `estim/` provide
estimates of the State Space Model.
