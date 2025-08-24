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
H_shell(t) = - Σ_q p_q(t) log p_q(t)

where

p_q(t) = E_q / Σ_r E_r
```

- High H_shell → energy spread across scales  
- Low H_shell → energy concentrated in few shells (risk of UV pile-up)

---

## 3. Alignment entropy

At each point x:

```
H_align(x,t) = - Σ_i p_i log p_i

where

p_i = ( (ω · e_i)^2 ) / Σ_j ( (ω · e_j)^2 )
```

- ω = vorticity = ∇ × u  
- {e_i} = eigenvectors of strain tensor S = ½(∇u + (∇u)^T)

- High H_align → vorticity spread across directions  
- Low H_align → vorticity aligned to max-stretch direction (dangerous)

---

## 4. Conjecture (Entropy Regularity)

If there exist constants η_shell, η_align > 0 such that:

```
H_shell(t) ≥ η_shell
H_align^min(t) ≥ η_align
```

for all time t ≥ 0, then the solution to 3D Navier–Stokes remains smooth.  
Conversely, finite-time blow-up requires dual entropy collapse.

---

## 5. Motivation

- Known criteria (Beale–Kato–Majda, Ladyzhenskaya–Prodi–Serrin) bound blow-up using norms.  
- Entropy conditions measure *spread vs collapse* instead of absolute size.  
- This reframing may give new structure conditions or numerical diagnostics.

---

## 6. Goals

- [ ] Formalize entropy criteria in PDE framework  
- [ ] Test entropy diagnostics on simulations / DNS data  
- [ ] Compare to existing smoothness criteria  
- [ ] Draft and publish research note

---

## License

MIT
