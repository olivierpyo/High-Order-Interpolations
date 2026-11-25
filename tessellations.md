
# Test de tessellation

## Hex 20

### ❌ `high_bent_block_hex20_with_scalar.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `TRI-QUADRATIC HEXAHEDRON`
- paraview filtre "tessellation" : `error CELL TYPE 29 not supported`

### ✅ `low_bent_block_hex20_with_scalar.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `QUADRATIC HEXAHEDRON`
- paraview filtre "tessellation" :
	- Slider à 0, c'est bon
	- Slider à 1, c'est bon
	- Slider à 2, c'est bon
	- Slider à 3 et +, pas de changement c'est le même que slider à 2
- fonctionne

NORMAL :
![low_hex20.png](./scr/tessellation/low_hex20.png)

TESSELLATION_0 :
![low_hex20_tessellation_0.png](./scr/tessellation/low_hex20_tessellation_0.png)

TESSELLATION_1 :
![low_hex20_tessellation_1.png](./scr/tessellation/low_hex20_tessellation_1.png)

TESSELLATION_2 :
![low_hex20_tessellation_2.png](./scr/tessellation/low_hex20_tessellation_2.png)

## Hex 27

### ❌ `high_bent_block_hex27_with_scalar.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `TRI-QUADRATIC HEXAHEDRON`
- paraview filtre "tessellation" : `error CELL TYPE 29 not supported`

### ❌ `low_bent_block_hex27_with_scalar.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `TRI-QUADRATIC HEXAHEDRON`
- paraview filtre "tessellation" : `error CELL TYPE 29 not supported`

## Hex 64

### ❌ `high_bent_block_hex64_with_scalar.msh`

- meshio conversion `.msh > .vtu` : `KeyError: 'hexahedron64'`

### ❌ `low_bent_block_hex64_with_scalar.msh`

- meshio conversion `.msh > .vtu` : `KeyError: 'hexahedron64'`

## Tet 10

### ✅ `high_bent_block_tet10_with_scalar.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `QUADRATIC TETRAHEDRON`
- paraview filtre "tessellation" :
	- Slider à 0, c'est bon
	- Slider à 1 et +, pas de changement c'est le même que slider à 0
- fonctionne

NORMAL :
![high_tet10.png](./scr/tessellation/high_tet10.png)

TESSELLATION_0 :
![high_tet10_tessellation_0.png](./scr/tessellation/high_tet10_tessellation_0.png)

### ✅ `low_bent_block_tet10_with_scalar.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `QUADRATIC TETRAHEDRON`
- paraview filtre "tessellation" :
	- Slider à 0, c'est bon
	- Slider à 1, c'est bon
	- Slider à 2, c'est bon
	- Slider à 3, c'est bon
	- Slider à 4 et +, pas de changement c'est le même que slider à 3
- fonctionne

NORMAL :
![low_tet10.png](./scr/tessellation/low_tet10.png)

TESSELLATION_0 :
![low_tet10_tessellation_0.png](./scr/tessellation/low_tet10_tessellation_0.png)

TESSELLATION_1 :
![low_tet10_tessellation_1.png](./scr/tessellation/low_tet10_tessellation_1.png)

TESSELLATION_2 :
![low_tet10_tessellation_2.png](./scr/tessellation/low_tet10_tessellation_2.png)

TESSELLATION_3 :
![low_tet10_tessellation_3.png](./scr/tessellation/low_tet10_tessellation_3.png)

## Tet 20

### ❌ `high_bent_block_tet20_with_scalar.msh`

- meshio conversion `.msh > .vtu` : `KeyError: 'tetra20'`

### ❌ `low_bent_block_tet20_with_scalar.msh`

- meshio conversion `.msh > .vtu` : `KeyError: 'tetra20'`

## ✅ PML `PML_v41.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `HEXAHEDRON`
- paraview filtre "tessellation" :
	- Slider à 0, c'est bon
	- Slider à 1 et +, pas de changement c'est le même que slider à 0
- fonctionne

NORMAL :
![PML.png](./scr/tessellation/PML.png)

TESSELLATION_0 :
![PML_tessellation_0.png](./scr/tessellation/PML_tessellation_0.png)

## ✅ Chukrut `010_wrong_data1.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `QUADRATIC HEXAHEDRON`
- paraview filtre "tessellation" :
	- Slider à 0, c'est bon
	- Slider à 1 et +, pas de changement c'est le même que slider à 0
- fonctionne

NORMAL :
![chukrut.png](./scr/tessellation/chukrut.png)

TESSELLATION_0 :
![chukrut_tessellation_0.png](./scr/tessellation/chukrut_tessellation_0.png)

## ✅ Kyoto `w0_ascii.msh`

- meshio conversion `.msh > .vtu`
- paraview ouvre le `vtu` avec des cellules de type `QUADRATIC HEXAHEDRON`
- paraview filtre "tessellation" :
	- Slider à 0, c'est bon
	- Slider à 1 et +, pas de changement c'est le même que slider à 0
- fonctionne

NORMAL :
![kyoto.png](./scr/tessellation/kyoto.png)

TESSELLATION_0 :
![kyoto_tessellation_0.png](./scr/tessellation/kyoto_tessellation_0.png)

> PS : sur Kyoto en .vtu avec paraview, il y a un petit souci au clic enfoncé de souris, il s'affiche ça (pour normal ou tessellé, les deux) :

![kyoto_bug.png](./scr/tessellation/kyoto_bug.png)
