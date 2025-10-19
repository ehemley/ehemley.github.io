---
layout: post
title: The magic of 12
date: 2025-10-17 12:00:00
description: A blog post with LaTeX equations
tags: math research
---

The number 12 emerges in several striking contexts in the theory of elliptic curves. In this post, I will explain how a couple of these instances are related to the weight of the modular discriminant.

## The modular discriminant

Let $\Delta$ be the function $\mathfrak{H} \to \mathbb{C}$ given by

$$
\Delta(\tau) = (2 \pi i)^{12} q \prod_{n=1}^{\infty}\left(1-q^n\right)^{24}
$$

where $q = e^{2 \pi i \tau}$. Equivalently, $\Delta(\tau) = (2 \pi i )^{12} \eta(\tau)^{24}$ where $\eta$ is the *Dedekind eta function*. The function $\Delta$ is a modular form of weight 12 called the *modular discriminant*.

To understand this geometrically, we can interpret modular forms via the moduli stack of elliptic curves. Define $$\mathcal{M}_{\text{ell}}$$ to be the moduli stack of elliptic curves, which can be realized as the orbifold quotient of $$\mathfrak{H}$$ by the group $$\text{SL}_2(\mathbb{Z})$$. Let $$\pi: \mathcal{E} \to \mathcal{M}_{\text{ell}}$$ be the universal curve and define $$\omega = \pi_* \Omega_{\mathcal{E}/{\mathcal{M}_{\text{ell}}}}$$. We have the following characterization:

**Lemma.** A global section of $\omega^{\otimes k}$ is a weight $k$ modular form.

The remarkable fact is that $\Delta$ has no zeroes on $\mathfrak{H}$, and thus gives a trivialization $$\omega^{\otimes 12} \cong \mathcal{O}_{\mathcal{M}_{\text{ell}}}$$. Therefore

$$
\deg (\omega^{\otimes 12}) = 1
$$

and hence $\deg \omega = 1/12$.

For an elliptic curve $E$, the tangent space to the moduli stack at $E$ is isomorphic to the first cohomology of $E$ with respect to the tangent sheaf,

$$
T_E \mathcal{M}_{\text{ell}} \cong H^1(E,T_E)
$$

In view of Kodaira-Serre duality,

$$
H^1(E,T_E)^\vee \cong H^0(E, \omega_E^{\otimes 2})
$$

we see that $$\Omega_{\mathcal{M}_{\text{ell}}} \cong \omega^{\otimes 2}$$.

**Proposition.** The Euler characteristic $\chi(\mathcal{M}_{\text{ell}})$ is equal to $-\frac{1}{12}$.

*Proof.* Applying the Riemann-Roch formula, 

$$
\chi(\mathcal{M}_{\text{ell}}) = - \frac{\deg(\Omega_{\mathcal{M}_{\text{ell}}})}{2}
$$

and using $\deg (\Omega_{\mathcal{M}_{\text{ell}}}) = 2 \deg \omega$. ∎


**Proposition.** Let $$f: X \to \mathbb{P}^1$$ be a rational elliptic surface. The number of singular fibers of $f$, counted with multiplicity, is 12.

*Proof.* Let $$\phi: \mathbb{P}^1 \to \overline{\mathcal{M}}_{\text{ell}}$$ be the classifying map of the family. On the compactified moduli stack $\overline{\mathcal{M}}_{\text{ell}}$, the discriminant $\Delta$ has cusp at the point $\infty$ corresponding to the nodal cubic $y^2 = x^3 - x^2$. Hence

$$
\omega^{\otimes 12} \cong \mathcal{O}_{\overline{\mathcal{M}}_{\text{ell}}}(\infty)
$$

and $\Delta$ is a global section of $$\mathcal{O}_{\overline{\mathcal{M}}_{\text{ell}}}(\infty)$$. Let $$\omega_f := f_* \Omega_{X/\mathbb{P}^1}$$, and note $$\omega_f \cong \phi^* \omega$$. Then $$\Delta_f := \phi^* \Delta$$ is a section of $$\omega_f^{\otimes 12}$$, and

$$
\deg \operatorname{div} (\Delta_f) = \deg \omega_f^{\otimes 12} = 12 \deg \omega_f
$$

is precisely the number of singular fibers of $f$. To compute $$\deg \omega_f$$, we use the following result.

**Lemma** (Miranda, *The Basic Theory of Elliptic Surfaces*, III.4.3). Let $f: X \to C$ be a Weierstrass fibration. Then, 

$$
\chi(\mathcal{O}_X) = \deg \omega_f
$$

(*So that there is no confusion, here there is no stacky structure and the Euler characteristic is the traditional alternating sum of Betti numbers.*) Weierstrass fibrations $f: X \to C$ are equivalent to smooth, minimal, elliptic surfaces over $C$ with a section. Since $X$ is a rational surface, $\chi(\mathcal{O}_X) = 1$. ∎

<hr style="margin-top: 2rem;">

