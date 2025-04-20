---
title: "All about Integration"
categories:
  - Learning
tags:
  - calculus
header:
  teaser: /assets/images/integral-notation.png
  overlay_image: /assets/images/integral-notation.png
  overlay_filter: 0.4
author_profile: false
---

Integration somehow finds its way everywhere, even after calculus classes. Deep learning, physics, you name it, we integrate it.

# All About Integration

While I assume most of you know what integration is, here's a brief explanation/review. If you want a full explanation of integration, I would recommend 3Blue1Brown's excellent playlist, the [Essence of calculus](https://youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr&si=YGEAEDvr00VFtibe). 
For those who want a quick understanding, integration (at least for what we're doing) is the "area under the curve". So, integrating some function would give us the area under that function's curve. 

Before continuing, it is recommended that you have seen at least basic integrals and derivatives before and some of their "rules". Btw, when I introduce ideas in my blog, I'm not going to give the exact assumptions we make and all the definitions unless necessary (like if we're doing real analysis). By the (second part, aka the Newton–Leibniz theorem,) Fundamental Theorem of Calculus, let us recall that

$$ \int_{a}^{b} f(x) dx = \text{F}(b) - \text{F}(a)$$

where $$\text{F}(x)$$ is the antidervative of $$f(x)$$. All it's telling us is that the integral over some interval is just the difference of the antiderivative evaluated at the bounds. An indefinite integral is simply the definite integral (like the one we showed above) but with no bounds. Ex:

$$ \int f(x) dx = \text{F}(x) + \text{C}$$

The only real difference is that when we have no bounds, we have to add a " $$+ \text{C}$$ " after evaluating the integral, called the constant of integration. Why, you may ask? Because the derivative of any constant is always zero and so we account for the fact that when we undo the derivative of some function, there may have been some constant in that function.

## Taking Antiderivatives

For most calculus students, the transition from taking derivatives to undoing them can be hard. The best way I like to imagine it is undoing the rules we learned for differentiating. For example, the power rule, which states:

$$ \frac{d}{dx}x^n = n x ^{n - 1}$$ 

Undoing the power rule is a simple as going back to the original function, or in this case $$x^n$$. Essentially, how do we go from $$n x^{n-1}$$ to $$x^n$$? We multiply by $$\frac{1}{n}$$ to get rid of the $$n$$ and add $1$ to the exponent. So in general:

$$ \int x^n dx = \frac{1}{n} x^{n+1} + C$$

Each derivative rule has a subsequent undoing rule. U-substitution can be used to undo chain rules. Integration by parts can be used to undo the quotient rule and many other integrals. There are many ways we can take integrals, and each "technique" we learn is another tool in our toolbox for taking each one apart.

** Side Note ** Many people often forget what $$dx$$ means in both the integral and the derivative. You can think of it as infinitesimally small changes in x, which means $$\frac{dy}{dx}$$ is almost $$\frac{\text{infinitesimally small changes in y}}{\text{infinitesimally small changes in x}}$$.

## Improper Integrals

An improper integral is when we attempt to evaluate an integral where the integrand is undefined at one or more points in the interval, or when one or both of the limits of integration are infinite. There are two main types of improper integrals: ones with discontinuities and infinities. With infinities, we take the limit and we "approach" infinity (whether that be positive or negative) when evaluating. Ex:

$$ \int_{a}^{\infty} f(x) dx = \lim_{b \to \infty} \int_{a}^{b} f(x) dx$$

We do something similar when one of the bounds is $$-\infty$$. And if both bounds:

$$ \int_{-\infty}^{\infty} f(x) dx = \lim_{a \to -\infty} \int_{a}^{c} f(x) dx + \lim_{b \to \infty} \int_{c}^{b} f(x) dx$$

where $$c$$ is any chosen number. For discontinuities at the bounds, it's pretty similar. If there is a discontinuity within the interval of integration (at $$e$$, for example, where ($$a < e < b$$), we simply take the improper integral from $$a$$ to $$e$$ and then from $$e$$ to $$b$$. It's almost like the above integral, but we choose $$c$$.

## Cool Tricks

The more time you spend integrating, the more shortcuts you will find. Yet beware, too many shortcuts can lead to more mistakes. For example, one cool integration trick I learned from Griffith's famous Quantum Mechanics textbook is shortcuts when integrating over symmetric intervals. For example, we have an integral over the interval $$[-a, a]$$. If the function we are integrating is odd (that is $$f(-x) = -f(x)$$ ) we have:

$$ \int_{-a}^{a} f(x) dx = 0$$

Yes, I typed that right, the answer is $$0$$. Now before you go and Google why, think about what an odd function is (specifically, its end behavior) and why a symmetric interval. For an even function (that is $$f(-x) = f(x)$$) we have:

$$ \int_{-a}^{a} f(x) dx = 2\int_{0}^{a} f(x) dx$$

With those two thought problems, I leave you with. And as they say at integration bees, "Integrate!".

*Extra Credit: explain Tangent half-angle substitution in the comments*

## References
- Overlay image from 3blue1Brown [[video](https://youtu.be/rfG8ce4nNh0?si=aRLJ6cdK4dISm0V0)]
- Single Variable Calculus Early Transcendentals James Stewart, Daniel Clegg and Saleem Watson
