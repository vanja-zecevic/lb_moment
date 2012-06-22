Copyright (C) 2012 Vanja Zecevic
Contact vanja.zecevic@sydney.uni.edu.au

This file is part of lb_moment

lb_moment is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

lb_moment is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

================================================================================
Introduction:
                              --------------------------------------------------
The generalised lattice Boltzmann method [1] requires a set of orthogonal basis
vectors related to moments of the particle distribution. This software takes a
set of linearly independent vectors, defined in terms of the lattice velocities
(c_x, c_y and c_z) and performs a Gram-Schmidt orthogonalization procedure in
order to form an orthogonal set. The set is defined in terms of the original
vectors and also printed out explicitly.

================================================================================
Author:
                              --------------------------------------------------
This software was written by, 

Vanja Zecevic
School of Aerospace, Mechanical and Mechatronic Engineering
The University of Sydney
Sydney, NSW, 2006
Australia

Please send any correspondence to,

vanja.zecevic@aeromech.usyd.edu.au

================================================================================
Use:
                              --------------------------------------------------
You will need to have 'maxima' installed since 'lb_moment' is a series of maxima
scripts. Run 'lb_moment' and when prompted, enter the lattice you want to use.
By default, dx, dy and dz are set to 1 however if you want to have them as
variables, simply comment out the lines,

dx: 1;
dy: 1;
dz: 1;

The first output of 'lb_moment' is a list of components of each orthogonal basis
vector in terms of input vectors. For example, if the third orthogonal vector is
made up of (2*second input vector) plus 1*(third input vector), then the output
will be,

1, 0, 0, 0
x, 1, 0, 0
0, 2, 1, 0
x, x, x, 1

The second output is the orthogonal matrix written out explicitly.
 
================================================================================
Reference material:
                              --------------------------------------------------
Details regarding the generalised lattice Boltzmann method as well as the
orthogonal basis sets used can be found in the following papers,

[1] Lallemand, P. and Luo, L. S.
Theory of the lattice Boltzmann method: Dispersion, dissipation, isotropy,
  Galilean invariance, and stability
Phys. Rev. E 61 (2000)

[2] Bouzidi, M. and d'Humieres, D. and Lallemand, P. and Luo, L. S.
Lattice Boltzmann equation on a two-dimensional rectangular grid
J. Comp. Phys. 172 (2001)

[3] d'Humieres, D. and Bouzidi, M. and Lallemand, P.
Thirteen-velocity three-dimensional lattice Boltzmann model
Phys. Rev. E 63 (2001)

[4] d'Humieres, D. and Ginzburg, I. and Krafczyk, M. and Lallemand, P.
  and Luo, L.S.
Multiple-relaxation-time lattice Boltzmann models in three dimensions
Philos. Trans. R. Soc. Lond. Ser. A-Math. Phys. Eng. Sci. 360 (2002)


