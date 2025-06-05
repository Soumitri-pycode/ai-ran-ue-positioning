
# AI-Based UE Positioning for RAN Optimization

This repository supports the AI-RAN Alliance Hackathon 2025 proposal:
**AI-Based UE Positioning for RAN Optimization**.

## 🔍 Overview
A deep learning approach to achieve highly accurate User Equipment (UE) positioning using standardized OTDOA/NRPPa and Positioning Reference Signals (PRS). Designed to improve RAN performance in public safety and ultra-reliable low latency communication (uRLLC) use cases.

## 📌 Use Case
- Real-time UE positioning for emergency responders
- Indoor/outdoor tracking for public safety
- Location-aware RAN optimization and control

## 🧠 AI/ML Approach
- CNN-based supervised learning model
- Input: PRS signal metrics (e.g., RSTD, power delay profile)
- Output: (x, y, z) coordinates of UE
- RMSE target: < 1.5m

## ⚙️ System Architecture
1. **gNBs** transmit PRS
2. **UE** logs timing and signal metrics
3. **GNE** aggregates logs
4. **CNN Model** estimates location
5. **RIC xApp** integrates and visualizes

## 🧪 Dataset & Evaluation
- Simulated PRS/OTDOA logs or real OpenAirInterface traces
- Metrics: RMSE, 95% CEP
- Comparison with baseline geometric trilateration

## 📁 Repository Structure
```
ai-ran-ue-positioning/
├── data/               # Simulated OTDOA, PRS logs
├── models/             # CNN model and training scripts
├── notebooks/          # EDA and evaluation notebooks
├── src/                # Inference engine and integration code
├── configs/            # Model parameters, RIC integration
└── README.md
```

## 🧭 Tech Stack
- Python, PyTorch
- Kafka (stream simulation)
- TensorBoard (monitoring)
- OpenAirInterface (optional)
- O-RAN SC near-RT RIC (integration target)

## 📄 License
Apache 2.0

---

Maintained by [Soumitri-pycode](https://github.com/Soumitri-pycode).
