---
layout: post
title: The magic of 12
date: 2025-10-17 12:00:00
description: A blog post with LaTeX equations
tags: math research
---

The number 12 emerges in several striking contexts in the theory of elliptic curves. In this post, I will explain how a couple of these instances are related to the weight of the modular discriminant.

## The modular discriminant

Let $$\Delta$$ be the function $$\mathfrak{H} \to \mathbb{C}$$ given by

$$
\Delta(\tau) = (2 \pi i)^{12} q \prod_{n=1}^{\infty}\left(1-q^n\right)^{24}
$$

where $$q = e^{2 \pi i \tau}$$, or equivalently $$\Delta(\tau) = (2 \pi i )^{12} \eta(\tau)^{24}$$ where $$\eta$$ is the *Dedekind eta function*. The function $$\Delta$$ is a modular form of weight 12 called the *modular discriminant*.

To understand this geometrically, we can interpret modular forms via the moduli stack of elliptic curves. Define $$\mathcal{M}_{\text{ell}}$$ to be the moduli stack of elliptic curves, which can be interpreted as the orbifold quotient of $$\mathfrak{H}$$ by the group $$\text{SL}_2(\mathbb{Z})$$. Let $$\pi: \mathcal{E} \to \mathcal{M}_{\text{ell}}$$ be the universal curve and define $$\lambda = \pi_* \Omega_{\mathcal{E}/\mathcal{M}_{\text{ell}}}$$. We have the following characterization:

**Lemma.** A global section of $$\lambda^{\otimes k}$$ is a weight $$k$$ modular form.

The remarkable fact is that $$\Delta$$ has no zeros on $$\mathfrak{H}$$, and thus gives a trivialization $$\lambda^{\otimes 12} \cong \mathcal{O}_{\mathcal{M}_{\text{ell}}}$$. On the compactified moduli stack $$\overline{\mathcal{M}}_{\text{ell}}$$, the discriminant $$\Delta$$ has a cusp at the point $$\infty$$ corresponding to the nodal cubic $$y^2 = x^3 - x^2$$. Hence

$$
\lambda^{\otimes 12} \cong \mathcal{O}_{\overline{\mathcal{M}}_{\text{ell}}}(\infty)
$$

and $$\Delta$$ is a global section of $$\mathcal{O}_{\overline{\mathcal{M}}_{\text{ell}}}(\infty)$$. Since the nodal cubic has an automorphism group of order 2,

$$
\deg (\lambda^{\otimes 12}) = \frac{1}{2}
$$

by the formula $$\deg \mathcal{L} = \sum \deg \mathcal{L}_x/\text{Aut}(x)$$ for a line bundle $$\mathcal{L}$$ on a Deligne-Mumford stack $$X$$. Hence $$\deg \lambda = 1/24$$.

For an elliptic curve $$E$$, the tangent space to the moduli stack at $$E$$ is isomorphic to the first cohomology of $$E$$ with respect to the tangent sheaf,

$$
T_E \mathcal{M}_{\text{ell}} \cong H^1(E,\mathcal{T}_E)
$$

In view of Kodaira-Serre duality,

$$
H^1(E,\mathcal{T}_E)^\vee \cong H^0(E, \Omega_E^{\otimes 2})
$$

we see that $$\Omega_{\mathcal{M}_{\text{ell}}} \cong \Omega_{\overline{\mathcal{M}}_{\text{ell}}}(\log \infty) = \lambda^{\otimes 2}$$.

This allows us to deduce a special case of the *Harer-Zagier formula*, which relates the orbifold Euler characteristic of the moduli stack of genus $g$ curves with a base point to the special values of the Riemann zeta function: $$ \chi(\mathcal{M}_{g,1}) = \zeta(1-2g)$$.

**Proposition.** The Euler characteristic $$\chi(\mathcal{M}_{\text{ell}})$$ is equal to $$-\frac{1}{12}$$.

*Proof.* For a smooth complex Deligne–Mumford curve $$U$$ with smooth compactification $$X$$ and boundary $$D$$, the orbifold Euler characteristic satisfies

$$
\chi(U) = -\deg \Omega_X(\log D)
$$

([Costantini-Möller-Zachhuber, Proposition 2.1](https://arxiv.org/abs/2006.12803)). Therefore

$$
\chi(\mathcal{M}_{\text{ell}}) = - 2 \deg \lambda
$$

which completes the proof. ∎

**Remark.** The isomorphism $$\lambda^{\otimes 12} \cong \Omega_{\overline{\mathcal{M}}_{\text{ell}}}(\infty)$$ is a special case of the relation

$$
12 \lambda = \delta + \kappa
$$

in the Chow ring of the moduli space of stable curves $$\overline{\mathcal{M}}_{g}$$.

The weight of $\Delta$ also shows up in the theory of elliptic surfaces.

**Proposition.** Let $$f: X \to \mathbb{P}^1$$ be a rational elliptic surface. The number of singular fibers of $$f$$, counted with multiplicity, is 12.

*Proof.* Let $$\phi: \mathbb{P}^1 \to \overline{\mathcal{M}}_{\text{ell}}$$ be the classifying map and define $$\lambda_f := f_* \Omega_{X/\mathbb{P}^1}$$, and note $$\lambda_f \cong \phi^* \lambda$$. Then $$\Delta_f := \phi^* \Delta$$ is a section of $$\lambda_f^{\otimes 12}$$ which vanishes at the points in $$\mathbb{P}^1$$ whose fibers are singular. Therefore

$$
\deg \text{div} (\Delta_f) = \deg \lambda_f^{\otimes 12} = 12 \deg \lambda_f
$$

is precisely the number of singular fibers of $$f$$. To compute $$\deg \lambda_f$$, we use the following result.

**Lemma** (Miranda, *The Basic Theory of Elliptic Surfaces*, III.4.3). Let $$f: X \to C$$ be a Weierstrass fibration. Then,

$$
\chi(\mathcal{O}_X) = \deg \lambda_f
$$

(*So that there is no confusion, here the Euler characteristic is the traditional alternating sum of Betti numbers.*) Weierstrass fibrations $$f: X \to C$$ are equivalent to smooth, minimal, elliptic surfaces over $$C$$ with a section. Since $$X$$ is a rational surface, $$\chi(\mathcal{O}_X) = 1$$. ∎

<hr style="margin-top: 2rem;">

