# Jodd Change Log

All notable changes to Jodd project are documented here.

## [Unreleased](https://github.com/oblac/jodd/compare/v3.8.6...master)

n/a

## [3.8.6](https://github.com/oblac/jodd/compare/v3.8.5...3.8.6)

### Bug Fixes

+ **core** - fixes `downloadFile` to download bigger files as well.
+ **lagarto** - bug introduced in 3.8.5; bad parsing of pseudo-function arguments [#407](https://github.com/oblac/jodd/issues/407).

### Features

+ **http** - default user agent now can be set [#410](https://github.com/oblac/jodd/pull/410).
+ **log** - added Log4j2 support.
+ **jtx** - added `ReadWriteTransaction` annotation to codebase.

## Breaking changes

+ **log** - factories are now called "providers", now stored in each logger.
+ **email** - Content-Disposition and Content-ID flags are now separate [#404](https://github.com/oblac/jodd/issues/404).


## [3.8.5](https://github.com/oblac/jodd/compare/v3.8.1...v3.8.5)

### Bug Fixes

+ **db** - `SqlBuilder#generateQuery` may be called multiple times.
+ **http** - `response#cookies()` does not throw exception on invalid cookies.
+ **http** - fixed special case with `Cookie` parsing. 
+ **core** - natural comparison has been fixed to follow comparator contracts.

### Features

+ **core** - added `FileLRUCache`.
+ **proxetta** - added `AopProxy`, simple tool for aop using just java.
+ **core** - added `AppendableWriter`.
+ **email** - `SendMailSession` is now `AutoCloseable`.
+ **db** - added Db detector [#401](https://github.com/oblac/jodd/issues/401).
+ **db** - added basic callable support [#389](https://github.com/oblac/jodd/issues/389).
+ **lagarto** - allow strings in css selector pseudo functions without quotation marks [#301](https://github.com/oblac/jodd/issues/301).
+ **db** - added `resetAll` method for hard-resetting the queries.
+ **http** - address parsing and exception message is much better.
+ **http** - added optional encoding for `HttpRequest#readFrom`.
+ **email** - email parser is improved.
+ **core** - natural comparison improved and accents added.
+ **core** - added `ThreadFactoryBuilder.
+ **core** - added `Futures` utilities.
+ **core** - added stream-related `Collection` utilities.

### Breaking changes

+ **core** - `ClassUtil#invoke` methods are gone.
+ **core** - `ReflectUtil` is now `ClassUtil`: sorry, but the name was super ugly.
+ **core** - `PreattyStringBuilder` simplified the interface.
+ **core** - `DirWatcher` now accepts `Consumer`s instead of custom listener.
+ **core** - `FindFile` interface changed to match Java8.
+ **core** - renamed methods in `Cache` interface.
+ **email** - renamed `EmailAddress`, it is used now as a Email parser.
+ **dboom** - method `_` has been removed. Use `append` instead.

### System

+ **gradle** - updated to Gradle 3.4.1


## [3.8.1](https://github.com/oblac/jodd/compare/v3.8.0...v3.8.1)

### Bug Fixes

+ **core** - fixed issue with `StringBand` calculation.

## Performance

+ **core** - added performance check for `StringBand`.

### Features

+ **lagarto** - added `contents`, `.after`, `replaceWith`, `unwrap`, `prepend`, `prevAll()`, `nextAll` to Jerry.
+ **http** - added `trustAllCerts` to http client.
+ **core** - added `Chalk` class.

## Breaking changes

+ **core** - `CommandLine` removes custom shell execution code.
