# bgfx bazel

Clone and get submodules
```
git clone --recursive git@github.com:VertexStudio/bgfx.bazel.git
```

### bx
```
bazel build //bx:bx
```

### bimg
```
bazel build //bimg:bimg
```

### bgfx
```
bazel build //bgfx:bgfx
```

## Examples

### 29-debugdraw
```
bazel build //bgfx:29-debugdraw
```

## Tools

### geometryc
```
bazel build //bgfx/tools/geometryc:geometryc
```

### geometryv
```
bazel build //bgfx/tools/geometryv:geometryv
```

### texturec
```
bazel-bin/bimg/tools/texturec/texturec
```

### texturev
```
bazel build //bgfx/tools/texturev:texturev
```

### shaderc
```
TODO
```
