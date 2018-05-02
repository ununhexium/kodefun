---
title=Gradle HTML dependencies generation
date=2018-05-02
last_updated=2018-05-02
type=post
tags=gradle
status=published
categories=
author=Just Me
---

# Gradle HTML dependencies generation

To show gradle dependencies as HTML output and open the default web browser automatically (linux).

```kotlin
tasks {
  task<Exec>("htmlDeps") {
    dependsOn("htmlDependencyReport")
    val browser = "/usr/bin/sensible-browser"
    commandLine(browser, "build/reports/project/dependencies/index.html")
  }
}
```
