These OSL scripts were written with Blender 2.8x . For that reason they do not use all features available in OSL. For example, the [[ ]] syntax to provide explanatory comments for parameters in shader function signatures.

Nor do they consider all the methods listed in the most current OSL documentation PDF. For example, the `select` function is not supported, so ternary operators are used in stead.

There may be other discrepancies between this code and the documentation. For example, to define the `!=` operator for a `struct`, `__operator__neq__` is used, not `__operator__ne__` .

Older versions of Blender will support even fewer features of OSL, such as the ability to define `struct`s.

As of writing, OSL is compatible with Blender's Cycles renderer, not its Eevee renderer. Be sure to turn it on prior to trying a script. Blender nodes do not distinguish between `vector`, `point` and `normal` data types (except when relevant), so their differences are ignored by this code except where necessary (e.g., matrix transformation). `int`s are a supported data type in Blender nodes, but are infrequently used.

Online, OSL language support is spotty as well. Github does not provide syntax highlighting. This code was writtein in Visual Studio Code with the assistance of James-Ni's OSL Support extension. I have tried to occasionally switch to the language mode to C to format the code, but some code style may be irregular.