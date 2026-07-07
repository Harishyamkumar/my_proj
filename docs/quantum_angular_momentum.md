# Quantum Angular Momentum

## Introduction

Angular momentum is one of the most important observables in quantum mechanics. Unlike its classical counterpart, quantum angular momentum is **quantized** — it can only take specific discrete values. It plays a central role in atomic structure, nuclear physics, particle physics, and quantum chemistry.

There are two broad categories of angular momentum in quantum mechanics:

- **Orbital angular momentum** ($\mathbf{L}$) — arises from the spatial motion of a particle, analogous to the classical $\mathbf{r} \times \mathbf{p}$.
- **Spin angular momentum** ($\mathbf{S}$) — an intrinsic property of particles with no classical analogue.

---

## 1. Orbital Angular Momentum

### 1.1 Definition

Classically, angular momentum is defined as:

$$
\mathbf{L} = \mathbf{r} \times \mathbf{p}
$$

In quantum mechanics, $\mathbf{r}$ and $\mathbf{p}$ become operators, so:

$$
\hat{L}_x = \hat{y}\hat{p}_z - \hat{z}\hat{p}_y, \quad
\hat{L}_y = \hat{z}\hat{p}_x - \hat{x}\hat{p}_z, \quad
\hat{L}_z = \hat{x}\hat{p}_y - \hat{y}\hat{p}_x
$$

### 1.2 Commutation Relations

The components of angular momentum do **not** commute with each other:

$$
[\hat{L}_x, \hat{L}_y] = i\hbar \hat{L}_z, \quad
[\hat{L}_y, \hat{L}_z] = i\hbar \hat{L}_x, \quad
[\hat{L}_z, \hat{L}_x] = i\hbar \hat{L}_y
$$

This means you **cannot** simultaneously know all three components of angular momentum with perfect precision — a direct consequence of the uncertainty principle.

However, the **total angular momentum squared** operator commutes with each component:

$$
[\hat{L}^2, \hat{L}_z] = 0
$$

This is why we choose $\hat{L}^2$ and $\hat{L}_z$ as the pair of commuting observables to label quantum states.

### 1.3 Eigenvalues

The eigenvalue equations are:

$$
\hat{L}^2 |l, m\rangle = \hbar^2 l(l+1) |l, m\rangle
$$

$$
\hat{L}_z |l, m\rangle = \hbar m |l, m\rangle
$$

where:

- $l = 0, 1, 2, 3, \dots$ is the **orbital angular momentum quantum number**
- $m = -l, -l+1, \dots, l-1, l$ is the **magnetic quantum number** (2l + 1 possible values)

### 1.4 Spherical Harmonics

The eigenfunctions of $\hat{L}^2$ and $\hat{L}_z$ in position space are the **spherical harmonics** $Y_l^m(\theta, \phi)$:

$$
\hat{L}^2 Y_l^m(\theta,\phi) = \hbar^2 l(l+1) Y_l^m(\theta,\phi)
$$

$$
\hat{L}_z Y_l^m(\theta,\phi) = \hbar m \, Y_l^m(\theta,\phi)
$$

These functions describe the angular part of the wavefunction for any central potential problem (e.g., the hydrogen atom).

| $l$ | Spectroscopic Label | Degeneracy ($2l+1$) |
|-----|---------------------|----------------------|
| 0   | s                   | 1                    |
| 1   | p                   | 3                    |
| 2   | d                   | 5                    |
| 3   | f                   | 7                    |

---

## 2. Spin Angular Momentum

### 2.1 Intrinsic Property

Spin is **not** derived from spatial motion — it is an intrinsic form of angular momentum carried by particles, even when they are point-like. It obeys the same algebra as orbital angular momentum:

$$
[\hat{S}_x, \hat{S}_y] = i\hbar \hat{S}_z \quad \text{(cyclic permutations)}
$$

$$
\hat{S}^2 |s, m_s\rangle = \hbar^2 s(s+1) |s, m_s\rangle, \quad
\hat{S}_z |s, m_s\rangle = \hbar m_s |s, m_s\rangle
$$

### 2.2 Key Difference from Orbital Angular Momentum

Unlike $l$, the spin quantum number $s$ can take **half-integer** values:

$$
s = 0, \tfrac{1}{2}, 1, \tfrac{3}{2}, 2, \dots
$$

- **Fermions** (electrons, protons, neutrons, quarks) have half-integer spin ($s = 1/2, 3/2, \dots$)
- **Bosons** (photons, gluons, W/Z bosons) have integer spin ($s = 0, 1, 2, \dots$)

### 2.3 Spin-1/2 and Pauli Matrices

For spin-1/2 particles (like the electron), the spin operators are represented using the **Pauli matrices**:

$$
\hat{S}_i = \frac{\hbar}{2}\sigma_i
$$

$$
\sigma_x = \begin{pmatrix}0 & 1\\ 1 & 0\end{pmatrix}, \quad
\sigma_y = \begin{pmatrix}0 & -i\\ i & 0\end{pmatrix}, \quad
\sigma_z = \begin{pmatrix}1 & 0\\ 0 & -1\end{pmatrix}
$$

The two eigenstates of $\hat{S}_z$ are "spin up" ($m_s = +1/2$) and "spin down" ($m_s = -1/2$).

---

## 3. Addition of Angular Momenta

When a system has multiple sources of angular momentum (e.g., orbital + spin, or two coupled particles), the **total angular momentum** is:

$$
\mathbf{J} = \mathbf{L} + \mathbf{S}
$$

For two angular momenta $j_1$ and $j_2$, the total $j$ ranges over:

$$
j = |j_1 - j_2|, \, |j_1 - j_2|+1, \, \dots, \, j_1 + j_2
$$

The combined states are expressed using **Clebsch–Gordan coefficients**:

$$
|j, m_j\rangle = \sum_{m_1, m_2} C^{j\,m_j}_{j_1 m_1\, j_2 m_2} \, |j_1, m_1\rangle |j_2, m_2\rangle
$$

### 3.1 Spin-Orbit Coupling

In atoms and nuclei, $\mathbf{L}$ and $\mathbf{S}$ couple to form total angular momentum $\mathbf{J} = \mathbf{L} + \mathbf{S}$. This coupling is responsible for **fine structure splitting** in atomic spectra and plays a major role in nuclear shell structure (e.g., spin-orbit splitting in the nuclear shell model).

---

## 4. Ladder (Raising/Lowering) Operators

It is often useful to define raising and lowering operators:

$$
\hat{L}_\pm = \hat{L}_x \pm i\hat{L}_y
$$

These act on states as:

$$
\hat{L}_\pm |l,m\rangle = \hbar\sqrt{l(l+1) - m(m\pm1)}\, |l, m\pm1\rangle
$$

They shift $m$ up or down by one unit while keeping $l$ fixed — a powerful tool for constructing the full multiplet of states from a single eigenstate.

---

## 5. Physical Significance

- **Atomic physics**: Angular momentum quantization explains atomic orbitals (s, p, d, f), selection rules in spectroscopy, and fine/hyperfine structure.
- **Nuclear physics**: Angular momentum coupling (jj-coupling) underlies the nuclear shell model, determines allowed nuclear transitions, and governs selection rules in beta decay and gamma emission (e.g., Gamow-Teller transitions).
- **Particle physics**: Spin determines whether particles are fermions or bosons, dictating statistics (Fermi-Dirac vs. Bose-Einstein) and the structure of the Standard Model.
- **Quantum computing**: Spin-1/2 systems are natural physical qubits.

---

## Summary Table

| Quantity | Operator | Eigenvalue | Quantum Number Range |
|----------|----------|------------|------------------------|
| Orbital angular momentum² | $\hat{L}^2$ | $\hbar^2 l(l+1)$ | $l = 0, 1, 2, \dots$ |
| Orbital z-component | $\hat{L}_z$ | $\hbar m$ | $m = -l, \dots, l$ |
| Spin angular momentum² | $\hat{S}^2$ | $\hbar^2 s(s+1)$ | $s = 0, \tfrac{1}{2}, 1, \dots$ |
| Spin z-component | $\hat{S}_z$ | $\hbar m_s$ | $m_s = -s, \dots, s$ |
| Total angular momentum² | $\hat{J}^2$ | $\hbar^2 j(j+1)$ | $j = |l-s|, \dots, l+s$ |

---

## References

- Griffiths, D. J., *Introduction to Quantum Mechanics*
- Sakurai, J. J., *Modern Quantum Mechanics*
- Cohen-Tannoudji, C., *Quantum Mechanics, Vol. 1*
