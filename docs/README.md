# NeuroSyncNet

**Predictive Brain-Machine Interface for Real-Time Motor Imagery Forecasting**

NeuroSyncNet is a groundbreaking neural decoding system designed to predict a subject’s motor imagery **before it fully occurs**, using only the **first 300ms of EEG data**. Built on BCI Competition IV Dataset 2a, it pushes the boundaries of brain signal decoding, outperforming traditional pipelines in both speed and foresight.

---

## Project Goals
- Predict imagined movement (left hand, right hand, feet, tongue) **before neural intent stabilizes**
- Use transformer-based forecasting to decode intent in real-time
- Create interpretable attention maps that identify predictive brain activity
- Enable low-latency, high-efficiency BMI applications (prosthetics, drones, VR)

---

## Dataset
- BCI Competition IV Dataset 2a (GDF format)
- 9 subjects
- 4-class motor imagery EEG
- 22 EEG channels @ 250Hz
- Trials aligned to motor imagery cue

---

## Architecture Highlights
- Causal Transformer-based forecasting
- Contrastive learning + neural latent prediction
- Self-supervised pretraining on early signal windows
- Attention-based interpretability

---

## Project Structure
See [`docs/architecture.md`](docs/architecture.md) for full technical breakdown.
