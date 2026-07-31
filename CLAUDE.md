This is the jsonmodel library's own source repository, distributed as a haxelib library (see `haxelib.json`).

`jsonmodel` provides JSON (un)serialization for typed models via build macros: classes opt in through the `JsonSerializable`/`JsonUnserializable` marker interfaces, which `SerializationMacros`/`UnserializationMacros` process at build time (with `IJsonSerializableMacro`/`IJsonUnserializableMacro` as the macro-facing contracts). `UnserializerInput` wraps the parsed JSON AST for unserializers, `StdParsers` supplies parsers for common standalone types, and `UnserializableArray`/`UnserializableBool` handle collection/primitive edge cases; unserialization failures surface as typed exceptions (`exceptions.UnserializationException`). All source lives under `src/jsonmodel` (`jsonmodel` package and its subpackages).

ANY AMBIGUITY OR MANUAL GAP SURFACING DURING IMPLEMENTATION SHOULD NOT BE RESOLVED SILENTLY. Instead, explicitly ask the question.

If told to take a dubious or possibly suboptimal approach (whether from the UI/UX or technical standpoint), also ask a question, providing details on why you're uncertain about this and what are the better practices or better ways to solve the problem.

# Code style conventions

See `code_style.md`.

# Dependencies

- `morestd` - small, universal utilities (e.g. `DateTime`).
- `hxjsonast` - JSON parsing into an AST that unserialization macros operate on.
- `json2object` - underlying JSON (un)serialization support.

See `haxelib.json`'s `dependencies` for the authoritative list.
