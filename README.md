# soup2ply

## Soup of triangles

List of vertices, three subsequent values represent a 3D vertex, nine subsequent values represent a planar triangle in 3D. Vertices are not unique, can appear multiple times in the file.

```
-9.659780e-02 -1.969390e-02 1.874010e-02
-9.673700e-02 -2.205980e-02 1.878610e-02
-9.683260e-02 -2.207070e-02 2.881010e-02
-9.683260e-02 -2.207070e-02 2.881010e-02
-9.670800e-02 -1.968200e-02 2.873670e-02
-9.659780e-02 -1.969390e-02 1.874010e-02
-9.682140e-02 -2.478340e-02 1.883970e-02
-9.692880e-02 -2.477640e-02 2.884680e-02
-9.683260e-02 -2.207070e-02 2.881010e-02
...
```

## PLY format

PLY separates the definition of unique vertices and an element field with indeces to the vertex field, see https://en.wikipedia.org/wiki/PLY_(file_format).

```
ply
format ascii 1.0
element vertex XXX
property float x 
property float y
property float z
element face YYY
property list uchar int vertex_indices
end_header
-9.659780e-02 -1.969390e-02 1.874010e-02
-9.673700e-02 -2.205980e-02 1.878610e-02
-9.683260e-02 -2.207070e-02 2.881010e-02
...
0 1 2
2 1 3
...
```
`XXX` ... number of vertices

`YYY` ... number of faces
