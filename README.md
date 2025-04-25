# Example project showing warings and errors with Maven 4 a parent pom located at `../..`

See the comments in the POM files in the child `examples` projects:

- [group-artifact](/examples/group-artifact/pom.xml) - POM points to GAV of parent, expected only GA needed
- [relative-path](/examples/relative-path/pom.xml) - POM points to the relative path of parent, unexpected warning in build log
- [relative-path-and-group-artifact](/examples/relative-path-and-group-artifact/pom.xml) - POM points to the GA and relative path of parent, shows expected warning in build log (use either GA or relativePath)

Build the project:

```sh
./mvnw verify -e
```