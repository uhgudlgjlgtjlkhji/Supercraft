# Port notes

## Current status: blocked — no usable Minecraft 26.3 JAR

- Source tested: `tapeQz/Shine` public `main` branch, which contains the older Shine 1.0.0 / Minecraft 1.21.11 source line.
- Target tested: Minecraft 26.3, Fabric Loader 0.19.5, Java 25.
- Build workflow setup succeeds, but `:compileJava` fails with 100 compiler errors.
- The errors are not just Gradle configuration: the source references removed or unavailable Minecraft rendering APIs, Fabric world-rendering/keybinding APIs, GLFW classes, and Sodium internals.
- The public source repository currently exposes only the `main` branch; it does not provide the newer Shine 3.1.1+26.2 source needed for a faithful forward port.
- The separate Shine `3.1.1+26.2` binary is not the source used by this build.
- No valid mod JAR was produced. The uploaded workflow artifact contains diagnostics only, not a usable mod.
- Do not install or test this output as a mod.

## Next required input

A source release corresponding to Shine 3.1.1+26.2 (or permission/access to a source tree for that exact version) is needed before a reliable 26.3 port can continue. With only the older 1.21.11 source, a correct port would require substantial rendering, Fabric API, and Sodium rewrites rather than simple version-number changes.
