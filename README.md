# About

Bazel rules for building and compiling bgfx: Cross-platform, graphics API agnostic, "Bring Your Own Engine/Framework" style rendering library.

## Set Up

You can clone recursively:

```
git clone --recursive --depth 1 git@github.com:VertexStudio/bgfx.bazel.git
```
Or just clone, and follow:
```
git submodule init
git submodule update
```



## Building

```
bazel build //:bgfx
```

### Build the testing

```
bazel build //:debugdraw
```
### Running the test example
Just run:
```
{PATH_TO_BGFX}/bazel-bin/debugdraw
```
You should see a new window with basic shapes and some functionality
