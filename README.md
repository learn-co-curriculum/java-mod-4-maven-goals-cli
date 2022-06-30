# Goals

## Learning Goals

- Explain goals in Maven.
- Examine goals of a specific plugin.

## What are Goals?

As discussed earlier, plugins are used to extend Maven’s core functionality.
Each plugin consists of **goals**. A goal is an action taken on the project as
defined by the POM file.

![Maven goals](https://curriculum-content.s3.amazonaws.com/java-mod-5/maven-goals.png)

## Examining Plugin Goals

We can find out the goals in a specific plugin using the following command:

```bash
mvn help:describe -Dplugin=org.apache.maven.plugins:maven-compiler-plugin
```

Here’s the output:

```plaintext
Name: Apache Maven Compiler Plugin
Description: The Compiler Plugin is used to compile the sources of your
  project.
Group Id: org.apache.maven.plugins
Artifact Id: maven-compiler-plugin
Version: 3.10.1
Goal Prefix: compiler

This plugin has 3 goals:

compiler:compile
  Description: Compiles application sources

compiler:help
  Description: Display help information on maven-compiler-plugin.
    Call mvn compiler:help -Ddetail=true -Dgoal=<goal-name> to display
    parameter details.

compiler:testCompile
  Description: Compiles application test sources.

For more information, run 'mvn help:describe [...] -Ddetail'
```

The command runs the `describe` goal of the `help` plugin specified as
`help:describe`. The `-Dplugin` argument specifies the plugin we want to
examine.

We can also use the `help` goal in most Maven plugins
([documentation](https://maven.apache.org/guides/mini/guide-configuring-plugins.html#help-goal)).

## Conclusion

We have learned that goals are specific tasks of a plugin and how to examine
what goals are available in a plugin.
