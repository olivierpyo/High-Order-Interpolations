
# `high_bent_block_hex20_with_scalar.msh`

✅ meshio conversion `.msh > .vtu`
✅ paraview ouvre le `vtu` avec des cellules de type "tri-quadratic hexahedron"
❌ paraview tesselation : `error CELL TYPE 29 not supported`



# `low_bent_block_hex20_with_scalar.msh`
hex20 LOW , meshio OK, (quadratic hexahedron) tesselation OK avec "0-1-2"


high_bent_block_hex27_with_scalar.msh
hex27 HIGH, meshio OK, CELL TYPE 29 not supported (tri-quadratic hexahedron)
low_bent_block_hex27_with_scalar.msh
hex27 LOW , meshio OK, CELL TYPE 29 not supported (tri-quadratic hexahedron)

hex64 HIGH, KeyError: 'hexahedron64'
hex64 LOW , KeyError: 'hexahedron64'

tet10 HIGH, meshio OK, (quadratic tetrahedron) paraview tesselation OK avec "0"
tet10 LOW , meshio OK, (quadratic tetrahedron) paraview tesselation OK avec "0-1-2-3"

tet20 HIGH, KeyError: 'tetra20'
tet20 LOW , KeyError: 'tetra20'

PML OK mais inutile car ordre 1

chukrut OK (quadratic hexahedron) paraview tesselation OK avec "0"

kyoto OK (quadratic hexahedron) paraview tesselation OK avec "0"