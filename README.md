# kivio-theme (An Apache Roller theme)
This is a simple theme for the [Apache Roller](http://roller.apache.org) blogging software based on a HTML 5 template based on *Unique Template* by [WebThemez.com](http://webthemez.com).

## Usage
Put this folder into Roller's template directory _themes_ or if you have changed the directory via *roller-custom.properties* put it there:
```
...
themes.dir=/opt/roller
```

## Maven usage
Maven is added to this project to ease up development process.

```
mvn clean compile
```

Copies the content of the project directory to a Vagrant machine directory containing the Apache Roller templates.

```
mvn clean package
```

Copies the content to the directory of Vagrant machine (see target above) and creates a package containing the whole theme.

```
mvn clean install
```

Creates the package and installs it by SSH to an external server. Additional _config.properties_ is needed to define the values for _ssh.user_, _ssh.pwd_ and _ssh.host_. The Glassfish server gets automatically restarted.

Additional properties in pom.xml:
* _theme.destination_: destination directory for themes on remote machine for automated deploying.
* _machine.destination_: destination directory for themes on Vagrant machine.

## Missing features
Currently the template is not complete to compete with the templates delivered with Apache Roller or from roller-extras. This list tells what is missing:

*	archives.vm: Calendar browser and links to latest entries	
*	search.vm: Search results page
*	tags_index.vm: Tag index page
*	Missing screenshot as preview on template selection

Check out [CHANGELOG](CHANGELOG.md) for the latest changes and fixes.