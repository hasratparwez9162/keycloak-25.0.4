# Keycloak
## Configure database 
- Create a database:  
  CREATE DATABASE keycloak;
- Update the database configuration in conf -> keyclock.conf:
```sh
db=mysql
db-username[Enter your username]
db-password=[Enter your password]
db-url=jdbc:mysql://localhost:3306/[Enter your database name]
```
To get help configuring Keycloak via the CLI, run:

on Linux/Unix:

    $ bin/kc.sh

on Windows:

    $ bin\kc.bat

To try Keycloak out in development mode, run:

on Linux/Unix:

    $ bin/kc.sh start-dev

on Windows:

    $ bin\kc.bat start-dev

After the server boots, open http://localhost:9090 in your web browser. The welcome page will indicate that the server is running.

To get started, check out the [configuration guides](https://www.keycloak.org/guides#server).

if Get error like below:
JAVA_HOME is not set. Unexpected results may occur.
Set JAVA_HOME to the directory of your local JDK to avoid this message.
Unrecognized option: --add-opens=java.base/java.util=ALL-UNNAMED
Error: Could not create the Java Virtual Machine.
Error: A fatal exception has occurred. Program will exit

Solution :
$env:JAVA_HOME="C:\Users\hasratp\.jdks\corretto-17.0.10" {Enter your jdk path}
$env:PATH="$env:JAVA_HOME\bin;$env:PATH"
