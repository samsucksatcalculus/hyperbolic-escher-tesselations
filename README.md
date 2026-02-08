# hyperbolic-escher-tesselations

This repository contains the Cayley graphs and group presentations of the Fuchsian groups underlying M.C. Eschers Circle Limit artworks. It does not contain any code. If you follow this very brief tutorial, you should be able to read a group presentation off a (Euclidean, hyperbolic or spherical) tesselation.

<div style="display: flex; justify-content: center;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/readme/Circle-Limit-I.jpeg?raw=true" 
       alt="Circle Limit 1" 
       style="width: 24%; margin: 1%;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/readme/Circle-Limit-II.jpeg?raw=true" 
       alt="Circle Limit 2" 
       style="width: 24%; margin: 1%;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/readme/Circle-Limit-III.jpeg?raw=true" 
       alt="Circle Limit 3" 
       style="width: 24%; margin: 1%;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/readme/Circle-Limit-IV.jpeg?raw=true" 
       alt="Circle Limit 4" 
       style="width: 24%; margin: 1%;">
</div>

Fuchsian groups are discrete subgroups of the group of orientation preserving isometries of the upper half plane. They act properly discontinuously on the upper half plane and thus give rise to a tesselation. Along the Cayley map $C$ we can pass back and forth between the upper half plane model and the unit disk model of the hyperbolic plane without losing notions of hyperbolic distance.

$$
\begin{aligned}
  C: \mathbb{D} &\to \mathbb{D} \\
              z &\mapsto \frac{z-i}{z+i}
\end{aligned}
$$
$$
\begin{aligned}
  C^{-1}: \mathbb{D} &\to \mathbb{D} \\
              z &\mapsto -i \, \frac{z+1}{z-1}
\end{aligned}
$$

<div style="display: flex; justify-content: center;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/readme/Circle-Limit-III.jpeg?raw=true" 
       alt="Circle Limit 3" 
       style="width: 48%; margin: 1%;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/readme/CKL3-tiling-halfplane.png?raw=true" 
       alt="Circle Limit 3 mapped into upper half plane" 
       style="width: 48%; margin: 1%;">
</div>

In general Fuchsian groups have Dirichlet regions, i.e. in particular they have polygonal, convex fundamental domains. In the case of M.C. Eschers Circle Limit, we can find Dirichlet regions which are compact and finite-sided.

<div style="display: flex; justify-content: center;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/Circle-Limit-1-Dirichlet.png?raw=true" 
       alt="Circle Limit 1" 
       style="width: 24%; margin: 1%;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/Circle-Limit-2-Dirichlet.png?raw=true" 
       alt="Circle Limit 2" 
       style="width: 24%; margin: 1%;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/Circle-Limit-3-Dirichlet.png?raw=true" 
       alt="Circle Limit 3" 
       style="width: 24%; margin: 1%;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/Circle-Limit-4-Dirichlet.png?raw=true" 
       alt="Circle Limit 4" 
       style="width: 24%; margin: 1%;">
</div>

By Sabidussis Theorem the Cayley graph of the Fuchsian groups underlying these Circle Limits is isomorphic to the dual tiling graph of the tesselations by these compact, finite-sided fundamental polygons. From this Cayley graph we can deduce a set of generators (the transformations which moves an arbitrary but fixed "start-tile" to a tile with which it shares a side). These generators pair the sides of the start-tile in a unique way and thus are called side-pairing transformations. 

For finite sided fundamental polygons its vertex set must be finite as well. The side-pairing transformations partition the vertex set of the fundamental polygon into vertex cycles. These subsets are called vertex cycles because a subset of the side pairing transformations cyclically permutes the elements in each vertex cycle.

Taking the elements $T_{i_1}, T_{i_2},..., T_{i_k}$ (in order) which cyclically permute the $i$th vertex cycle, we can derive a relation between them by looking at the sum of the angles at the vertices in the interior of the fundamental polygons. The angle sum for each vertex cycle will always be $\frac{2\pi}{k}$, for some $k \in \mathbb{Z}$. The relation $T_{i_k}...T_{i_2}T_{i_1}^k$ holds (recall that the rightmost element is applied first).

<div style="display: flex; justify-content: center;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/Circle-Limit-3-Side-Pairing.png?raw=true" 
       alt="Side-pairing transformations in Circle Limit III" 
       style="width: 48%; margin: 1%;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/readme/anglesums.png?raw=true" 
       alt="Interior angles of fundamental polygon in Circle Limit III" 
       style="width: 48%; margin: 1%;">
</div>

The figure above shows the side pairing of our fundamental polygon in Circle Limit III. The sides of $F$ which meet in the four-fin vertex are paired by the hyperbolic rotations $T_1, T_1^{-1}$ about the four-fin vertex through $2\pi/4$ and $-2\pi/4$, respectively. Similarly, the remaining two sides of $F$, which meet in the three-fin vertex, are paired by the hyperbolic rotations $T_2,T_2^{-1}$ about the three-fin vertex through $2\pi/3$ and $-2\pi/3$, respectively.

<p>The side-pairing transformations identify three vertex cycles.</p>

<ul>
  <li>
    The first vertex cycle contains only the vertex at which four fins meet. It is fixed by $T_1$ and the interior angle of $F$ 
    at this vertex is $2\pi/4$.
  </li>
  <li>
    The second vertex cycle contains only the vertex at which three fins meet. It is fixed by $T_2$ and the interior angle of $F$ 
    at this vertex is $2\pi/3$.
  </li>
  <li>
    The third vertex cycle contains the mouth and tail-fin vertex. The mouth vertex is mapped onto the tail-fin vertex by $T_1$
    and the tail-fin vertex is mapped back to the mouth vertex by $T_2$. The sum of interior angles of this vertex cycle is 
    $2\pi/6 + 2\pi/6 = 2\pi /3$.
  </li>
</ul>

In this fashion we can identify all vertex cycles of a fundamental polygon and a relationship for each cycle. Through this approach, we can derive a group presentation for the underlying Fuchsian groups of all four Circle Limits (or any other symmetry group of any other tesselation). 

<div style="display: flex; justify-content: center;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/Circle-Limit-1-Side-Pairing.png?raw=true" 
       alt="Circle Limit 1" 
       style="width: 48%; margin: 1%;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/Circle-Limit-1-Cayley-Graph.png?raw=true" 
       alt="Circle Limit 2" 
       style="width: 48%; margin: 1%;">
</div>

$$
  \Gamma_{\mathrm{I}} = \langle T_1, T_2, T_3 \; | \; T_1^3 = T_2^2 = (T_3T_1)^2 = (T_3T_2)^2 = id \rangle
$$

<div style="display: flex; justify-content: center;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/Circle-Limit-2-Side-Pairing.png?raw=true" 
       alt="Circle Limit 1" 
       style="width: 48%; margin: 1%;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/Circle-Limit-2-Cayley-Graph.png?raw=true" 
       alt="Circle Limit 2" 
       style="width: 48%; margin: 1%;">
</div>

$$
  \Gamma_{\mathrm{II}} = \langle T_1, T_2, T_3 \; | \; T_1^4 = T_2^3 = T_3^3 = T_2T_3T_1 = id \rangle
$$

<div style="display: flex; justify-content: center;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/Circle-Limit-3-Side-Pairing.png?raw=true" 
       alt="Circle Limit 1" 
       style="width: 48%; margin: 1%;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/Circle-Limit-3-Cayley-Graph.png?raw=true" 
       alt="Circle Limit 2" 
       style="width: 48%; margin: 1%;">
</div>

$$
  \Gamma_{\mathrm{III}} = \langle T_1, T_2 \; | \; T_1^4 = T_2^3 = (T_2T_1)^3 = id \rangle
$$

<div style="display: flex; justify-content: center;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/Circle-Limit-4-Side-Pairing.png?raw=true" 
       alt="Circle Limit 1" 
       style="width: 48%; margin: 1%;">
  <img src="https://github.com/samsucksatcalculus/fuchsian-groups-escher/blob/main/Circle-Limit-4-Cayley-Graph.png?raw=true" 
       alt="Circle Limit 2" 
       style="width: 48%; margin: 1%;">
</div>

$$
  \Gamma_{\mathrm{IV}} = \langle T_1, T_2 \; | \; T_1^3 = T_2^4 = (T_2T_1)^4 = id \rangle
$$
