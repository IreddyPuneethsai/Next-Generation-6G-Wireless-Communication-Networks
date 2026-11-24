# Next-Generation 6G Wireless Communication Networks

## About the Project

This repository presents a MATLAB-based performance evaluation of advanced multiple access techniques for next-generation 6G wireless communication networks. The project compares **OFDMA, NOMA, SCMA, PDMA**, and the proposed **CA-HMRA (Channel-Aware Hybrid Multiple Access and Resource Allocation)** across bit error rate, throughput, spectral efficiency, energy efficiency, and outage probability.

The goal is to provide a reproducible, easy-to-understand simulation framework for academic study and experimentation. The proposed CA-HMRA model combines assumed channel awareness, access efficiency, reduced interference, and resource allocation behavior to demonstrate how hybrid and channel-aware strategies may improve network performance.

> **Research scope:** This project is a simplified system-level comparative model. It uses explicit assumptions rather than measured data and is not a standards-compliant 6G physical-layer or radio-channel simulator.

## Algorithms Compared

### Existing Algorithms

| Algorithm | Full Name | Description |
|---|---|---|
| **OFDMA** | Orthogonal Frequency Division Multiple Access | Assigns orthogonal frequency resources to users and reduces inter-user interference. |
| **NOMA** | Non-Orthogonal Multiple Access | Uses power-domain multiplexing to serve multiple users by sharing time-frequency resources. |
| **SCMA** | Sparse Code Multiple Access | Uses sparse multidimensional codebooks for efficient, overloaded multiple-access communication. |
| **PDMA** | Pattern Division Multiple Access | Differentiates users through deliberately designed diversity patterns. |

### Proposed Algorithm

| Algorithm | Full Name | Description |
|---|---|---|
| **CA-HMRA** | Channel-Aware Hybrid Multiple Access and Resource Allocation | A proposed hybrid approach that combines channel awareness, adaptive resource allocation, improved access efficiency, and lower residual interference. |

## Key Evaluation Metrics

- **Bit Error Rate (BER):** Evaluated using a simplified BPSK/AWGN model across 0–30 dB SNR.
- **Throughput:** Total network throughput for 5–40 active users at 10 dB operating SNR.
- **Spectral Efficiency:** Achievable bit/s/Hz at the reference operating point.
- **Energy Efficiency:** Throughput divided by modeled base and per-user power consumption.
- **Outage Probability:** Estimated using a Rayleigh-fading formula at average channel SNR values of 0, 5, 10, and 15 dB.

## Simulation Configuration

- Base MATLAB; no additional toolbox is required
- System bandwidth: 20 MHz
- BER SNR range: 0–30 dB, in 5 dB steps
- Operating SNR: 10 dB
- Active-user range: 5–40 users
- Reference load: 20 users
- Reproducible random seed: `rng(10)`
- Outage threshold: 0 dB

## Representative Results

The following results are obtained from the reference model with 20 users at 10 dB SNR. They are simulation estimates, not measured network results.

| Algorithm | BER | Throughput (Mbps) | Spectral Efficiency (bit/s/Hz) | Energy Efficiency (Mbit/J) | Outage Probability |
|---|---:|---:|---:|---:|---:|
| OFDMA | 0.00118627 | 33.93 | 1.848 | 2.262 | 0.194696 |
| NOMA | 0.00025143 | 39.25 | 2.138 | 2.364 | 0.152293 |
| SCMA | 0.00029445 | 38.57 | 2.101 | 2.457 | 0.155776 |
| PDMA | 0.00044350 | 37.25 | 2.029 | 2.403 | 0.165565 |
| CA-HMRA | 1.57853×10⁻⁷ | 61.85 | 3.369 | 4.355 | 0.073627 |

Under the stated assumptions, CA-HMRA provides the best value for all five evaluated metrics.

## Repository Structure

| Path | Description |
|---|---|
| `code/` | MATLAB implementation of the complete simulation. |
| `6G_Multiple_Access_Dataset/` | MATLAB scripts, generated CSV datasets, algorithm folders, and benchmark charts. |
| `6G_Multiple_Access_Dataset/6G_Multiple_Access_Simulation.m` | Main simulation script. |
| `outputs/` | Exported result figures and reference images. |
| `*_Results.csv` | Numerical outputs for each performance metric. |
| `Combined_comparison.csv` | Metric-by-metric comparison of all algorithms. |
| `Best_Algorithm_Summary.csv` | Summary of the best-performing algorithm for each metric. |
| `benchmark charts/` | Combined charts for visual comparison. |
| `PROJECT_OVERVIEW.md` | Extended project description and methodology. |
| `LICENSE.md` | MIT license. |

## How to Run

1. Install MATLAB.
2. Clone the repository:
   ```bash
   git clone https://github.com/IreddyPuneethsai/Next-Generation-6G-Wireless-Communication-Networks.git
   cd Next-Generation-6G-Wireless-Communication-Networks
   ```
3. Open `6G_Multiple_Access_Dataset/6G_Multiple_Access_Simulation.m` in MATLAB.
4. Run the script from MATLAB. The script will:
   - Print comparison tables in the Command Window.
   - Generate CSV result files.
   - Save performance PNG figures.

No MATLAB toolbox or third-party package is required.

## Research and Usage Notes

The simulation uses simplified, explicit parameters for access efficiency, link gain, residual interference, bandwidth, and power consumption. The numbers in this repository should be used for comparative analysis and academic demonstrations—not as 6G standards measurements or guarantees of real-world performance.

## License

This project is licensed under the **MIT License**.

Copyright (c) 2026 Ireddy Puneeth Sai

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
