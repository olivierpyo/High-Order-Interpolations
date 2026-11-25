
# Test de tesselation

## Hex 20

### ❌ `high_bent_block_hex20_with_scalar.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `TRI-QUADRATIC HEXAHEDRON`
- paraview filtre "tesselation" : `error CELL TYPE 29 not supported`

### ✅ `low_bent_block_hex20_with_scalar.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `QUADRATIC HEXAHEDRON`
- paraview filtre "tesselation" :
	- Slider à 0, c'est bon
	- Slider à 1, c'est bon
	- Slider à 2, c'est bon
	- Slider à 3 et +, pas de changement c'est le même que slider à 2
- fonctionne

## Hex 27

### ❌ `high_bent_block_hex27_with_scalar.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `TRI-QUADRATIC HEXAHEDRON`
- paraview filtre "tesselation" : `error CELL TYPE 29 not supported`

### ❌ `low_bent_block_hex27_with_scalar.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `TRI-QUADRATIC HEXAHEDRON`
- paraview filtre "tesselation" : `error CELL TYPE 29 not supported`

## Hex 64

### ❌ `high_bent_block_hex64_with_scalar.msh`

- meshio conversion `.msh > .vtu` : `KeyError: 'hexahedron64'`

### ❌ `low_bent_block_hex64_with_scalar.msh`

- meshio conversion `.msh > .vtu` : `KeyError: 'hexahedron64'`

## Tet 10

### ✅ `high_bent_block_tet10_with_scalar.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `QUADRATIC TETRAHEDRON`
- paraview filtre "tesselation" :
	- Slider à 0, c'est bon
	- Slider à 1 et +, pas de changement c'est le même que slider à 0
- fonctionne

### ✅ `low_bent_block_tet10_with_scalar.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `QUADRATIC TETRAHEDRON`
- paraview filtre "tesselation" :
	- Slider à 0, c'est bon
	- Slider à 1, c'est bon
	- Slider à 2, c'est bon
	- Slider à 3, c'est bon
	- Slider à 4 et +, pas de changement c'est le même que slider à 3
- fonctionne

## Tet 20

### ❌ `high_bent_block_tet20_with_scalar.msh`

- meshio conversion `.msh > .vtu` : `KeyError: 'tetra20'`

### ❌ `low_bent_block_tet20_with_scalar.msh`

- meshio conversion `.msh > .vtu` : `KeyError: 'tetra20'`

## ✅ PML `PML_v41.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `HEXAHEDRON`
- paraview filtre "tesselation" :
	- Slider à 0, c'est bon
	- Slider à 1 et +, pas de changement c'est le même que slider à 0
- fonctionne

## ✅ Chukrut `010_wrong_data1.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `QUADRATIC HEXAHEDRON`
- paraview filtre "tesselation" :
	- Slider à 0, c'est bon
	- Slider à 1 et +, pas de changement c'est le même que slider à 0
- fonctionne

## ✅ Kyoto `w0_ascii.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `QUADRATIC HEXAHEDRON`
- paraview filtre "tesselation" :
	- Slider à 0, c'est bon
	- Slider à 1 et +, pas de changement c'est le même que slider à 0
- fonctionne

