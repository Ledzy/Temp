## Ineffective Reusage of Intermediate Derivatives

![derivative_reusage](derivative_reusage.png)

**Figure 1.** In BCD's backward, the derivative of intermediate activations $z_\ell, \cdots z_L$ are only used for computing the gradient of the active block $W_{\ell}$. The proposed BREAD framework reuses these derivatives for efficiently computing the gradient of correction matrices.

## Suboptimal Optimization Landscape

![bcd limitation](suboptimality.png)

**Figure 2.** Suboptimality issue of BCD. **left figure** shows that BCD fails to minimize the loss to zero when the final layer is frozen, as the groudtruth $y$ lies out of the positive column space of the last layer's weight. **Right figure** verifies the Proposition 4.1, where rotating the column space of the last layer effectively covers the label $y$.