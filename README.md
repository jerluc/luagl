LuaGL
=====

Straight-forward LuaJIT FFI bindings for OpenGL

Usage
=====

For usage in a purely LuaJIT environment:

```lua
local gl = require("libs/gl") ("libGL.so")

...

gl.Begin(gl.GL_TRIANGLES)
gl.Color3f(1., 0., 0.)
gl.Vertex3f(-0.6, -0.4, 0.)
gl.Color3f(0., 1., 0.)
gl.Vertex3f(0.6, -0.4, 0.)
gl.Color3f(0., 0., 1.)
gl.Vertex3f(0., 0.6, 0.)
gl.End()

...
```

However, if you intend to run your script from an embedded LuaJIT environment which has OpenGL
already linked, you can omit the library name argument from the import:

```lua
local gl = require("libs/gl") ()
```

