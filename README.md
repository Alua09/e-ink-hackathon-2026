# E-Ink Display Micro-Mechanism Simulator 🔬⚡

> **Global Virtual Hackathon 2026 Submission**  
> **Team:** ALDA  
> **Live Demo:** https://alua09.github.io/e-ink-hackathon-2026/

---

## 📌 What is this project?
Most people use e-readers (like Kindle) and electronic shelf labels every day without wondering how a screen can hold an image indefinitely with 0 Watts of power. 

This project is an interactive, browser-based physical simulation of **Electrophoretic E-Ink microcapsules**. It lets users manipulate voltage, temperature, and pulse timing to discover the hidden physics of particle movement, bistability, and thermal ghosting.

---

## ✨ Key Features & Interactivity
1. **Interactive 8x8 E-Reader Screen:** Draw or select preset patterns (Letters, Gradients, Shapes) to see how pixels update.
2. **Micro-Microscope View:** Inspect 8 adjacent microcapsules in real-time. Watch positively charged white titanium dioxide particles ($\text{TiO}_2^+$) and negatively charged black carbon particles ($\text{Carbon}^-$) collide and migrate through dyed oil.
3. **Bistability Demonstration ("Power Off" test):** Cut the battery power ($0\text{V}$) and watch the image remain completely stable, explaining why e-ink consumes zero standby power.
4. **Thermal Ghosting Simulation:** Adjust the temperature slider down to $-20^\circ\text{C}$ to increase fluid viscosity ($\eta$). Observe how particles fail to reach the surface during standard pulses, creating the classic "ghosting" artifact seen on outdoor e-ink displays in winter.
5. **Anti-Ghosting Waveform Engine:** Toggle between a direct pulse and a professional 3-phase clearing waveform (Reset $\rightarrow$ White $\rightarrow$ Target) to see how modern e-readers clean the screen.

---

## ⚙️ Under the Hood & Technical Stack
* **Built with:** Pure HTML5 Canvas, Vanilla JavaScript (ES6+), and CSS3. No heavy frameworks or external libraries required for core physics.
* **Physics Engine:** Implements the electrophoretic drift velocity formula:
  $$v = \frac{q \cdot E}{6\pi \cdot \eta(T) \cdot r}$$
  where viscosity $\eta$ follows the Arrhenius temperature dependency model, combined with an elastic particle collision resolver inside each microcapsule boundary.

---

## 📝 Simplifications & Scope (Honest Disclosure)
To keep the simulation real-time and responsive within a browser environment while meeting the 2-minute clarity rule:
* We simulate a 2D cross-section of spherical 3D microcapsules.
* Fluid hydrodynamics are approximated via particle drag and inter-particle repulsion forces rather than full Navier-Stokes fluid solvers.
* Only two primary pigment types (white and black) are simulated, with grayscale achieved via pulse-width modulation (partial particle translation).

---

## 👥 Team ALDA & Code Explanation Readiness
Every member of Team ALDA fully understands all 100% of the source code in this repository and is fully prepared for the Round 2 live recorded interview.
