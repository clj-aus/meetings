# clj-aus #1 — Three native Clojures, one C game library

**Wednesday 16 September 2026, 6:30–7:30pm AEST · Online**
[Meetup event](https://www.meetup.com/clojure-australia/events/316277511/)

## Talk

raylib is a C game library. Clojure isn't just one language any more, so this
talk runs the same raylib examples under three different Clojures and looks at
where each one puts the boundary to C:

- **Jolt** — Clojure on Chez Scheme, calling `libraylib` directly over its C
  ABI through `jolt.ffi`. No wrapper library, no codegen, no C shim.
- **jank** — Clojure compiled to a native binary through C++/LLVM, where
  `(:include "raylib.h")` turns raylib into ordinary interop.
- **JVM Clojure** — over coffi and JDK 22+'s Panama Foreign Function & Memory
  API, where the runtime does the marshalling for you.

The interesting part is the ABI. raylib passes structs *by value* everywhere,
and each host earns a different answer to that problem.

## Source

| Suite | Repo | Gallery |
|---|---|---|
| Jolt | [b12n-raylib-jlt](https://github.com/burinc/b12n-raylib-jlt) | [raylib-jlt.b12n.app](https://raylib-jlt.b12n.app/) |
| jank | [b12n-raylib-jnk](https://github.com/burinc/b12n-raylib-jnk) | [raylib-jnk.b12n.app](https://raylib-jnk.b12n.app/) |
| JVM Clojure | [b12n-raylib-clj](https://github.com/burinc/b12n-raylib-clj) | [raylib-clj.b12n.app](https://raylib-clj.b12n.app/) |

## Slides

_Added after the session._

## Recording

_Added after the session._
