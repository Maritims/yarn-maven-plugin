# yarn-maven-plugin
Maven plugin for running yarn commands.

## Configuration
```xml
<build>
    <plugins>
        <plugin>
            <groupId>com.github.maritims</groupId>
            <artifactId>yarn-maven-plugin</artifactId>
            <version>0.0.1-SNAPSHOT</version>
            <configuration>
                <path>node</path>
                <install>true</install>
            </configuration>
            <executions>
                <execution>
                    <goals>
                        <goal>run</goal>
                    </goals>
                </execution>
            </executions>
        </plugin>
    </plugins>
</build>
```

## Options
| Option | Type     | Value                    | Explanation                                                                                                                 |
|--------|----------|--------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| install | boolean | true, false              | Indicates whether or not yarn packages should be installed.                                                                 |
| path | string | svelte, node, vue, react | Name of directory within the src directory containing package.json. The directory should live alongside the java directory. | 

## Install yarn packages
`mvn com.github.maritims:yarn-maven-plugin:<version>:run -Dinstall=true`

## Run yarn command
`mvn com.github.maritims:yarn-maven-plugin:<version>:run -Dpath=<path>`

## Install yarn packages and run yarn command
`mvn com.github.maritims:yarn-maven-plugin:<version>:run -Dpath=<path> -Dinstall=true`