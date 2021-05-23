These OSL scripts were written with Blender 2.9x. They do not use all features available in OSL, such as the `[[` `]]` syntax to provide explanatory comments for parameters in shader function signatures.

Older versions of Blender will support fewer features of OSL, such as the `select` method or the ability to define `struct`s. This means that stylistic conventions are uneven throughout this repository, depending on whether a script has been updated from, e.g, Blender 2.8x to Blender 2.9x.

There may be other discrepancies between this code and the documentation. For example, to define the `!=` operator for a `struct`, `__operator__neq__` is used, not `__operator__ne__` .

As of writing, OSL is compatible with Blender's Cycles renderer on a `CPU` device; not the Eevee renderer. Be sure to enable OSL prior to trying a script. Blender nodes do not distinguish between `vector`, `point` and `normal` data types (except when relevant), so their differences are ignored by this code except where necessary (e.g., matrix transformation).

Online, OSL language support is spotty. Github does not provide syntax highlighting. This code was written in Visual Studio Code with the assistance of [James-Ni's OSL Support](https://github.com/James-N/vscode-osl) extension. I have tried to occasionally switch to the language mode to C to format the code, but some code style may still be irregular.