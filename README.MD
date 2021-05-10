# Void Command

> Void Command is a basic API that can be used for easily creating commands and sub commands.

Void Command is an API designed for Spigot developers that facilitates the creation and registration of new commands and sub commands. You can easily add it to your project, and follow the [wiki](https://github.com/ianlibanio/VoidCommand/wiki) to create new commands.

## Installation

You can download the .jar into the [releases page](https://github.com/ianlibanio/VoidCommand/releases/), or use JitPack.

### Gradle

Add it at your root `build.gradle` at the end of repositories:
```gradle
repositories {
	...
	maven { url 'https://jitpack.io' }
}
```
Add the `dependency`:
```gradle
dependencies {
	implementation 'com.github.ianlibanio:VoidCommand:0.1'
}
```

### Maven
Add the JitPack repository to your `build` file:
```xml
<repositories>
	<repository>
		 <id>jitpack.io</id>
		 <url>https://jitpack.io</url>
	</repository>
</repositories>
```
Add the `dependency`:
```xml
<dependency>
	<groupId>com.github.ianlibanio</groupId>
	<artifactId>VoidCommand</artifactId>
	<version>0.1</version>
</dependency>
```

Other options available at: <https://jitpack.io/#ianlibanio/VoidCommand/0.1>.

## Wiki

For detailed instructions on how to use Void Command, you can check the [Wiki](https://github.com/ianlibanio/VoidCommand/wiki).

## Meta

This project was developed by [Ian](https://github.com/ianlibanio).

Distributed under the MIT license. See ``LICENSE`` for more information.

[https://github.com/ianlibanio/VoidCommand](https://github.com/ianlibanio/)

## Contributing

1. Fork it <https://github.com/ianlibanio/VoidCommand/fork>
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request
