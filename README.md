This project implements a Hybrid Neural ODE model to predict irregularly sampled patient vital signs (e.g., heart rate, blood pressure, oxygen saturation).
The HybridODE is a Mixture-of-Experts applied to continuous dynamics:
Each expert learns a regime-specific derivative function.
A gating network dynamically weights the experts to produce the overall trajectory.
The goal is to capture multiple physiological regimes, handle irregular time intervals, and improve prediction accuracy over standard sequence models.

Motivation
Patient vital signs are often recorded at irregular time intervals due to sensor availability, measurement schedules, or clinical interventions. Traditional RNNs, LSTMs, or Transformers assume regular time steps, which can limit their ability to model true physiological dynamics.
HybridODEs provide a continuous-time approach, enabling:
Accurate prediction at arbitrary time points
Regime detection (e.g., stable vs. critical patient states)
Better extrapolation and interpolation

