The code is run according to the rules described in the task.

The approach: the built-in predictor fit_tx_prediction from helpers is used twice. First, p0 = fit(rx) - as in the baseline, an estimate of the TX-induced interference. Then, the residual r_mid = rx - p0 is fitted again, after that  rx_hat = rx - p0 - p1 is returned. The idea is to fix the residual self-interference after the first step and fit the same model again using TX-induced features.

I would also like to subtract external coherent interference from all channels, identified by calculating the correlation between channels in the frequency range under consideration, but I will do this outside of the competition after the deadline.
