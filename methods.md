# Methods

As a first effort, we reproduce the techniques developed in (Hance et al., 2021), which used a pair of models to describe the activity of fishers (_Pekania pennant_). First, for each given individual, a Hidden Markov Model (HMM) is fit to discern between resting ($$s=1$$) and non-resting activities ($$s=0$$), creating a time series of state ($${s_t : 0 \leq t \leq T}$$ for some observation period $$T$$). Then, a (linear, gaussian) state space model is used to infer the animals' locations and movement from their GPS time series, in this case a first-difference correlated random walk (DCRW). This is used to account for GPS location data errors, resulting in a bayesian model that can be post-processed to provide credible ellipses for the locations of the resting activity.

