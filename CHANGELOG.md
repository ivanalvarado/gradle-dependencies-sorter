# gradle-dependencies-sorter

## Version 0.14
* [chore]: bump dependencies. Specifically antlr-related ones.
* [chore]: use newer version of Shadow, eliminate Gradle deprecations.

## Version 0.13
* [Fix]: update kotlin-editor to 0.10 and fix API breaking change.

## Version 0.12
* [Fix]: update to latest kotlin-editor and don't delete complex statements in dependencies blocks.

## Version 0.11
* [Fix]: emit errors even when not in verbose mode.
* [Fix]: update kotlin-editor for better parsing of dependency declarations.

## Version 0.10
* [Feat]: support enforcedPlatform
* [Fix]: bad version-checking logic was hiding check results.

## Version 0.9
* [Fix]: sort testFixtures closer to test deps.
* [Fix]: update KotlinEditor and handle GRADLE_DISTRIBUTION type.
* [Fix]: suggest fix action based on invocation context.
* [Chore]: build with Gradle 8.10.2.

## Version 0.8
* [New] improve support for parsing Kotlin DSL, using KotlinEditor.
* [Chore] built with Gradle 8.9.

## Version 0.7
* [Fix] Fix verbose flag in SortDependenciesTask.
* [Chore] Switch to Clikt CLI.
* [Build] Switched to `com.vanniktech:gradle-maven-publish-plugin` for publishing.

## Version 0.6
* [New] make `check` task dependency optional (but on by default).
  ```sortDependencies { check(<true|false>) }```

## Version 0.5
* [New] Warn (not fail) when encountering projects without a build script.

## Version 0.4
* New: Adds extension to permit setting custom program version.
* Fix: Change resource name to avoid clobbering with other plugins.
* Exclude icu4j from antlr dependency, reducing binary size.

## Version 0.3
* Replace `--quiet` with `--verbose` flag. The CLI and gradle plugin now run in quiet mode by default, and can be made verbose with `--verbose`.
* Split Gradle tasks into `sortDependencies` (which sorts) and `checkSortDependencies` (which checks that dependencies are sorted). The latter is automatically added as a dependency of the `check` lifecycle task too.
* New: Support `add(configuration, dependency)` notation. Thanks to [@kozaxinan](https://github.com/kozaxinan) for the contribution.
* New: Support function call dependency declarations like `gradleApi()`.
* New: Support for Map-syntax version of `project(...)`, such as `project(path: ':kool', configuration: 'config')`. Thanks to [@jamesonwilliams](https://github.com/jamesonwilliams) for the contribution.
* Fix: Fix path traversal ISE in `FileTreeIterator.hasNext()`.
* Fix: Close logger after invocation and print location if verbose or errors reported.
* Fix: Add thread safety for log file creation. Thanks to [@catherine-chi](https://github.com/catherine-chi) for the contribution.
* Fix: Tolerate `project()` declarations in non-`dependencies` text blocks. Thanks to [@jamesonwilliams](https://github.com/jamesonwilliams) for the contribution.
* Docs: Add badge link to central in README. Thanks to [@JakeWharton](https://github.com/JakeWharton) for the contribution.
* Docs: Document location of the fat jar to download in README.
* Docs: Add version badge to README. Thanks to [@SimonMarquis](https://github.com/SimonMarquis) for the contribution.

## Version 0.2
* Fixes and improvements.

## Version 0.1
* Initial release.
