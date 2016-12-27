## Compiler Brush Textures

##### `AAATRIGGER`
  Used on brush entities of the trigger type, and buyzones in Counter-Strike.

##### `BEVEL` (PRECISE)
  Acts like NULL but doesn't expand when generating clip hulls. It can be used
  to eliminate exterior corner clipping bugs, without using
  `cliptype` flag, however it's recommended to use `-cliptype precise` as this
  feature is experimental.

##### `BEVELBRUSH`


##### `BLACK_HIDDEN`
  Blocks light and can be used to create shadow patterns.

##### `BOUNDINGBOX`
  Used to determine the direction of rotation of an entity. Used with `ORIGIN`.

##### `CLIP`
  Solid to all objects but physically simulated projectiles, dropped
  weapons and items.

##### `CLIPHULL1` (STAND)
  Clips standing players and only allows crouching. Also allows players to
  crouch jump inside.

##### `CLIPHULL2` (BIG SIZE)
  Clips entities that has a big collision hull.

##### `CLIPHULL3` (CROUCH)
  Clips crouching players and only allows standing. Will stuck players who
  crouch inside the brush.

##### `CONTENTEMPTY` (EMPTY BRUSH)
  Behaves like `func_illusionary` without texture. Will block thirdperson
  camera as if the camera hit a wall behind the player.

##### `CONTENTWATER` (WATER BRUSH)
  Behaves like `func_water` without texture. Players inside the brush it will
  render a black screen for the player.

##### `HINT`
  This texture is used to instruct the compiler to cut visleaves and is used
  in combination with `SKIP` textures.

##### `NOCLIP`
  Behaves like `NULL`, except it is opaque and soft cover?

##### `ORIGIN`
  Used for setting the origin of origin based brushes like
  `func_door_rotating`, `func_tracktrain`, etc.

##### `SKIP`
  Has no effect on anything. Useful in combination with the `HINT` texture.
  Skip faces are removed during compilation, so a brush textured with skip won't prevent leaks. Also useful as a tool in Hammer for grouping, moving and
  place-holding objects.

##### `SKY`
  This texture is used to make 2D skyboxes. Casts light if there is a
  `light_environment` entity in the map.

##### `SOLIDHINT`
  Similar to `HINT` but can be applied to faces of solid brushes. Can reduce
  number of visleaf cuts and decrease the size of the compiled map.

  Makes it possibe to manually add extra faces for hlbsp to choose from, in order to help reduce face count and other counts.

##### `TRANSLUCENT`
  Similar to `CLIP` and behaves like `func_wall` and clips projectiles, dropped weapons and items. It can also prevent VIS, unlike a `func_wall`
  with a transparent texture.

### Unused/Unknown Brush Textures

##### `SPLITFACE`
  Behaves like  `HINT` when `HLCSG_NOSPLITBYHINT` is enabled in the compiler,
  whereas `HINT` will act as `CONTENTEMPTY`.

##### `CONTENTSKY` (SKY BRUSH)
  Behaves like SKY brush. Unused and untested.

##### `CONTENTSOLID` (SOLID BRUSH)
  Behaves like a solid brush. Unused and untested.
