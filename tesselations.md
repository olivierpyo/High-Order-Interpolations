
# Test de tesselation

## Hex 20

### `high_bent_block_hex20_with_scalar.msh`

- ✅ meshio conversion `.msh > .vtu`
- ✅ paraview ouvre le `vtu` avec des cellules de type `TRI-QUADRATIC HEXAHEDRON`
- ❌ paraview tesselation : `error CELL TYPE 29 not supported`

### `low_bent_block_hex20_with_scalar.msh`

- ✅ meshio conversion `.msh > .vtu`
- ✅ paraview ouvre le `vtu` avec des cellules de type `QUADRATIC HEXAHEDRON`
- ✅ paraview tesselation :
	- Subdivision 0, OK
	- Subdivision 1, OK
	- Subdivision 2, OK, maximum

## Hex 27

### `high_bent_block_hex27_with_scalar.msh`

- ✅ meshio conversion `.msh > .vtu`
- ✅ paraview ouvre le `vtu` avec des cellules de type `TRI-QUADRATIC HEXAHEDRON`
- ❌ paraview tesselation : `error CELL TYPE 29 not supported`

### `low_bent_block_hex27_with_scalar.msh`

- ✅ meshio conversion `.msh > .vtu`
- ✅ paraview ouvre le `vtu` avec des cellules de type `TRI-QUADRATIC HEXAHEDRON`
- ❌ paraview tesselation : `error CELL TYPE 29 not supported`

## Hex 64

### `high_bent_block_hex64_with_scalar.msh`

- ❌ meshio conversion `.msh > .vtu` : `KeyError: 'hexahedron64'`

### `low_bent_block_hex64_with_scalar.msh`

- ❌ meshio conversion `.msh > .vtu` : `KeyError: 'hexahedron64'`

## Tet 10

### `high_bent_block_tet10_with_scalar.msh`

- ✅ meshio conversion `.msh > .vtu`
- ✅ paraview ouvre le `vtu` avec des cellules de type `QUADRATIC TETRAHEDRON`
- ✅ paraview tesselation :
	- Subdivision 0, OK, maximum

### `low_bent_block_tet10_with_scalar.msh`

- ✅ meshio conversion `.msh > .vtu`
- ✅ paraview ouvre le `vtu` avec des cellules de type `QUADRATIC TETRAHEDRON`
- ✅ paraview tesselation :
	- Subdivision 0, OK
	- Subdivision 1, OK
	- Subdivision 2, OK
	- Subdivision 3, OK, maximum

## Tet 20

### `high_bent_block_tet20_with_scalar.msh`

- ❌ meshio conversion `.msh > .vtu` : `KeyError: 'tetra20'`

### `low_bent_block_tet20_with_scalar.msh`

- ❌ meshio conversion `.msh > .vtu` : `KeyError: 'tetra20'`

## PML (Hex 343 element)

- PML fonctionne car la géométrie est d'ordre 1, mais je ne suis pas sûr que cela soit utile.

## Chukrut

- ✅ meshio conversion `.msh > .vtu`
- ✅ paraview ouvre le `vtu` avec des cellules de type `QUADRATIC HEXAHEDRON`
- ✅ paraview tesselation :
	- Subdivision 0, OK, maximum

## Kyoto

- ✅ meshio conversion `.msh > .vtu`
- ✅ paraview ouvre le `vtu` avec des cellules de type `QUADRATIC HEXAHEDRON`
- ✅ paraview tesselation :
	- Subdivision 0, OK, maximum

