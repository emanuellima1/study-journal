# Julia Plotting

The Plots package provides an unified API to several supported [backends](http://docs.juliaplots.org/latest/backends/). Install the packages "Plots" and at least one backend, like `PlotlyJS` or `PyPlot.jl`. Example:

```julia
using Plots
plotlyjs()
plot(sin, -2pi, pi, label="sine function")
```
