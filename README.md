# sr-artifactory
This is a dummy repository dedicated to store Organization packages.

In order to be readt the artifacts from this repo, make sure you have bellow configuration in your maven `$HOME/.m2/settings.xml` file.

```
</settings>
 .........
  <servers>
  .....
  <server>
      <id>github</id>
      <username>REPLACE_WITH_GHITHUB_USERNAME</username>
      <password>REPLACE_WITH_GHITHUB_TOKEN</password>
  </server>
  .....
  </servers>

  <profiles>
	<profile>
      <id>sr-github</id>
      <repositories>
        <repository>
          <id>central</id>
          <url>https://repo1.maven.org/maven2</url>
          <releases><enabled>true</enabled></releases>
          <snapshots><enabled>false</enabled></snapshots>
        </repository>
        <repository>
          <id>github</id>
          <name>GitHub SmartRent Maven Packages</name>
          <url>https://maven.pkg.github.com/mg-smartrent/sr-artifactory</url>
        </repository>
      </repositories>
    </profile>
  </profiles>
  
   <activeProfiles>
    <activeProfile>sr-github</activeProfile>
  </activeProfiles>
 
 .......
 </settings> 
```
