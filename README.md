# 🐦 Vicsek Model: Flocking and Phase Transitions

<img src="Viscek_Swarm_Animation.gif" alt="Swarm Animation" width="40%">

## 📖 About

This repository implements the **Vicsek model**, a minimal model for describing collective behaviour such as flocks of birds.

Starting from random initial velocities, agents iteratively align their direction with neighbouring particles, leading to the emergence of **global polarisation**. This collective behaviour is quantified using a normalised velocity-based **order parameter**.

The system exhibits a **phase transition** from disordered motion to coherent flocking, governed by key parameters such as **noise** and **particle density**.

The included Jupyter notebooks provide both the **implementation** and an explanation of the underlying mathematical model.


## 🚀 Features

* Simulation of self-propelled agents in 2D
* Flocking dynamics using local alignment rules
* Phase transition analysis with respect to
  * Noise
  * Density
* Visualization of:
  * Swarm animations
  * Order parameter evolution


## 📂 Repository Structure

```bash
.
├── Viscek_model-animation.ipynb              # Swarm animation
├── Viscek_model-Phase_transition-noise.ipynb # Phase transition vs noise
├── Viscek_model-Phase_transition-density.ipynb # Phase transition vs density
├── Viscek_Swarm_Animation.gif               # Example animation
├── Viscek_Swarm_Animation.mp4               # Animation video
├── README.md
```

---

## 🧠 Model Description

Each agent:
* Moves with constant speed
* Aligns direction with neighbors within a radius of influence
* Is subject to noise

### Dynamics

At each time step:
1. Identify neighbors within radius (r)
2. Compute average direction of neighbors
3. Add random noise
4. Update velocity and position
5. Apply periodic boundary conditions

---

## 📊 Order Parameter

The **global order parameter** quantifies alignment:

$$
\Phi = \frac{1}{N v} \left| \sum_{i=1}^{N} \vec{v}_i \right|
$$

* $$(\Phi \approx 1)$$: ordered (flocking)
* $$(\Phi \approx 0)$$: disordered


## 📦 Requirements

```bash
python -m pip install numpy matplotlib tqdm ipython jupyter
```


## 🔗 References

* Vicsek Model — Vicsek et al., *Phys. Rev. Lett.*, 1995




