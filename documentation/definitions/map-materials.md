# Map Materials

When creating custom textures, you can define materials used within the map to give specific textures a sound style for when a player interacts (runs, attacks, etc.) with a brush/entity using that texture.

This can be done in multiple ways, such as prefixing texture names (Sven Co-Op only) or defining a `mapname_materials.txt` file.

## File Definition

The file contains a list of tags and their coressponding texture name.

```
V DUCT_FLR01
D GENERIC48
G CRETE2_FLR03
M AIR_C1
...
```

The letter describes the sound style to be used with the texture.

- `M` metal
- `V` ventilation
- `D` dirt
- `S` slosh liquid
- `T` tile
- `G` grate
- `W` wood
- `P` computer
- `Y` glass
- `F` flesh
- `O` snow

Whereas concrete is the default sound style.

Example:

```
// mapname_materials.txt

M MTL_FLOOR
T TILE_FLOOR
O MTN_SNOW01
```

### Using Texture Names (Sven Co-Op Only)

In Sven Co-Op, rather than creating a materials file, you can also name your textures with prefixes that will be used to determine their sound style.

```
V VENTTEXTURE_
D DIRTTEXTURE_
G GRATETEXTURE
M METALTEXTURE
S SLOSHTEXTURE
T TILETEXTURE_
W WOODTEXTURE_
P COMPTEXTURE_
Y GLASSTEXTURE
F FLESHTEXTURE
O SNOWTEXTURE_
```

So for example, if you have a texture `MTL_FLOOR` you can rename it to `METALTEXTUREMTL_FLOOR`, or `SNOWTEXTURE_MTN_SNOW01`.
