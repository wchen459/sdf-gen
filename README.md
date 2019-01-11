# SDFGen

```bash
mkdir build
cd build
cmake ../
make
```

# Usage

```bash
bin/sdf_gen <.obj file path> <grid step (e.g. 0.01)> <padding (minimum 1)>
```
# Output

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
