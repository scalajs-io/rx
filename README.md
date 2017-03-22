Rx.js API for Scala.js
================================
[rx](http://reactivex.io/rxjs/) - Library for composing asynchronous and event-based operations in JavaScript

### Description

Applications, especially on the web have changed over the years from being a simple static page, 
to DHTML with animations, to the Ajax revolution. Each time, we're adding more complexity, more data, 
and asynchronous behavior to our applications. How do we manage it all? How do we scale it? By moving 
towards "Reactive Architectures" which are event-driven, resilient and responsive. With the Reactive Extensions, 
you have all the tools you need to help build these systems.

### Build Requirements


* [SBT v0.13.13](http://www.scala-sbt.org/download.html)

### Build/publish the SDK locally

```bash
 $ sbt clean publish-local
```

### Examples

```scala
import io.scalajs.npm.rx._ 

Rx.Observable.range(0, 5).filterWith(_ % 2 == 0).drainFuture map { values =>
    println(s"output: $values") //=> 0, 2, 4
}
```

### Artifacts and Resolvers

To add the `Rx` binding to your project, add the following to your build.sbt:  

```sbt
libraryDependencies += "io.scalajs.npm" %%% "rx" % "4.1.0-4"
```

Optionally, you may add the Sonatype Repository resolver:

```   
resolvers += Resolver.sonatypeRepo("releases") 
```
