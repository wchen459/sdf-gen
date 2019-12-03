# SDFGen

```bash
mkdir build
cd build
cmake ../
make
```

## Usage

```bash
bin/sdf_gen <filename> <dx> <padding>
```
Where:
  - `filename` specifies a Wavefront OBJ (text) file representing a *triangle* mesh (no quad or poly meshes allowed). File must use the suffix ".obj".
  - `dx` specifies the length of grid cell in the resulting distance field.
  - `padding` specifies the number of cells worth of padding between the object bound box and the boundary of the distance field grid. Minimum is 1.

## Output

The output file format is:
```
<n points x> <n points y> <n points z>
<origin x> <origin y> <origin z>
<grid step>
<value 1> 
<value 2> 
<value 3> 
[...]
```
`value n` are the signed distance data values, in ascending order of i, then j, then k.
The output filename will match that of the input, with the OBJ suffix replaced with SDF.
