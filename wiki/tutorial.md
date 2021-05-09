## Usage example

### Commands
Firstly, to create a command you must create a class and extend VoidCommand:

```java
public class Example extends VoidCommand {}
```

Then implement the command method and annotate it with @Command:

```java
public class Example extends VoidCommand {

    @Command(
            name = "example",
            executor = Executor.PLAYER,
            permission = "example.permission",
            aliases = { "alias" }
    )
    public void command(Context context) {
        context.player().sendMessage(ChatColor.GRAY + "Hello, world!");
    }
}
```

@Command possible arguments:
```java
name ('required') ["Your command name, any String is valid"]
executor ('optional', default: "Executor.BOTH") ["Who can use this command, values: PLAYER, CONSOLE, BOTH"]
permission ('optional', default: "") ["Permission required to execute this command, any String is valid"]
aliases ('optional', default: {""}) ["Which aliases your command should have"]
```

### Sub Commands

To create Sub Commands, you just have to create a method with Context as the unique parameter:
```java
@SubCommand(
        name = "hello",
        permission = "example.permission.hello",
        executor = Executor.PLAYER
)
public void help(Context context) {
    context.player().sendMessage(ChatColor.GRAY + "Hello!");
}
```

@SubCommand arguments:
```java
name ('required') ["Your subcommand name, any String is valid"]
executor ('optional', default: "Executor.BOTH") ["Who can use this command, values: PLAYER, CONSOLE, BOTH"]
permission ('optional', default: "") ["Permission required to execute this subcommand, any String is valid"]
```

Remember that you can use multiple subcommands with the same start:

```java
@SubCommand(name = "use")
public void use(Context context) {
      context.player().sendMessage(ChatColor.GREEN + "You used a valid sub command!");
}

@SubCommand(name = "use secret")
public void useSecret(Context context) {
     context.player().sendMessage(ChatColor.YELLOW + "You found a secret!");
}
```

### Registration

To register commands is pretty simple, just add this to your plugin enable process:
```java
VoidRegister register = new VoidRegister(this); // "this" is the instance of your Main class.

register.add(new TestCommand(), new HelpCommand()); // Here you can register how many commands you want.
```