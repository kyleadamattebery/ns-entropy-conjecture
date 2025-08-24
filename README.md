# Entropy Regularity

Exploring entropy-based criteria for smoothness in 3D Navier–Stokes equations.

---

## 1. Navier–Stokes equations

```
∂_t u + (u · ∇)u = -∇p + νΔu + f
∇ · u = 0
```

---

## 2. Spectral shell entropy

```
E_q(t) = || Δ_q u ||_2^2
p_q(t) = E_q / Σ_r E_r
H_shell(t) = - Σ_q p_q(t) log(p_q(t))
```

- High H_shell → energy spread across scales  
- Low H_shell → energy concentrated in few shells (risk of UV pile-up)

---

## 3. Alignment entropy

At each point x:

```
p_i = ( (ω · e_i)^2 ) / Σ_j ( (ω · e_j)^2 )
H_align(x,t) = - Σ_i p_i log(p_i)
```

- ω = vorticity = ∇ × u  
- {e_i} = eigenvectors of the strain tensor S = ½(∇u + (∇u)^T)

- High H_align → vorticity spread across directions  
- Low H_align → vorticity aligned with max-stretch direction (dangerous)

---

## 4. Conjecture (Entropy Regularity)

If there exist constants η_shell, η_align > 0 such that:

```
H_shell(t) ≥ η_shell
H_align^min(t) ≥ η_align
```

for all time t ≥ 0, then the solution to 3D Navier–Stokes remains smooth.  
Finite-time blow-up requires **dual entropy collapse**.

---

## 5. Motivation

- Classical criteria (Beale–Kato–Majda, Ladyzhenskaya–Prodi–Serrin) use norm bounds.  
- Entropy conditions measure *spread vs collapse* instead of absolute size.  
- Reframing in terms of entropy may give new structure conditions or diagnostics.

---

## 6. Goals

- [x] Formalize entropy criteria in PDE framework  
- [ ] Lemma A: Entropy floor ⇒ control of high-frequency tail  
- [ ] Lemma B: Entropy floor ⇒ bounded vortex stretching  
- [ ] Combine A+B ⇒ BKM integrability ⇒ smoothness  
- [ ] Test on simulations and DNS datasets  
- [ ] Draft and publish research note

---

## License

MIT
