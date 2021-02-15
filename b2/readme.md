This is a reproducer for [#16152](https://github.com/gradle/gradle/issues/16152)

```
cd gradle-bug-reproducer-16152/b2
./gradlew :check_16152
```

This will run all publishToMavenLocal tasks (root build and included build) and 
compares the targets artifact id with the artifact id used in the dependency reference.

Fails if they are not equal.