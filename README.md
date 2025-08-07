# TestSys Maven Repository

This repository serves as the custom Maven repository for the TestSys organization, hosting internal dependencies and artifacts.

## Branches

- **releases**: Contains stable, production-ready artifacts.
- **snapshots**: Contains snapshot (development) versions for testing and ongoing development.

## Usage

To use this repository in your Maven project, add the following to your `pom.xml`:

```xml
<repositories>
    <repository>
        <id>testsys-releases</id>
        <name>TestSys Releases</name>
        <url>https://raw.githubusercontent.com/trik-testsys/maven-repo/releases/</url>
        <releases>
            <enabled>true</enabled>
            <updatePolicy>daily</updatePolicy>
            <checksumPolicy>warn</checksumPolicy>
        </releases>
        <snapshots>
            <enabled>false</enabled>
        </snapshots>
    </repository>
    <repository>
        <id>testsys-snapshots</id>
        <name>TestSys Snapshots</name>
        <url>https://raw.githubusercontent.com/trik-testsys/maven-repo/snapshots/</url>
        <releases>
            <enabled>false</enabled>
        </releases>
        <snapshots>
            <enabled>true</enabled>
            <updatePolicy>always</updatePolicy>
            <checksumPolicy>warn</checksumPolicy>
        </snapshots>
    </repository>
</repositories>
```

## Contributing

This repository is managed by the TestSys organization. If you need to publish new artifacts, please follow the internal guidelines or contact the repository maintainers.

## License

This repository is licensed under the [Apache License 2.0](LICENSE).
