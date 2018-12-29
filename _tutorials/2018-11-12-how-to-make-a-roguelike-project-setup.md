---
excerpt: This article explains how to set up the tutorial project on your computer and get started with it.
title: "How To Make a Roguelike: Project Setup"
tags: [zircon, caves-of-zircon, roguelikes, kotlin]
author: addamsson
short_title: "How To Make a Roguelike: Project Setup"
series: coz
---

> Now that you are decided to write your own roguelike, the first thing to do is to
  set up the project on your computer!
  
## What you'll need

To get started with the project you'll need to install:

- [Git](https://git-scm.com/)
- [A JDK](https://openjdk.java.net/) and
- [Intellij IDEA Community Edition](https://www.jetbrains.com/idea/download/)

The latter is not mandatory, but it is highly recommended.

## What we're gonna write

In this tutorial we'll write [Caves of Zircon](https://github.com/Hexworks/caves-of-zircon-tutorial).
The game is about an adventurer, who descends into the **Caves of Zircon** to gather zircon crystals
and fight zombies, kobolds and other mythical creatures along the way.

This game is a classic roguelike. This means that you only have one life, the creatures are
ruthless, and if you'll even have to look out for food, since you can starve to death!

## Checking out the project

To get started, let's check out the code from Git. Navigate to an empty folder and perform
this command:

```bash
git clone https://github.com/Hexworks/caves-of-zircon-tutorial.git
```

then navigate to the newly created project:

```bash
cd caves-of-zircon-tutorial
```

This project contains the code from start to finish and for each article there is a Git *tag*.
So let's reset our project to see the initial project setup by running this command:

```bash
git reset --hard PROJECT_SETUP
```

### Using Gradle

We're not going to go into details about how to use Gradle, so the only thing you have to know
is the command for building the project:

```bash
./gradlew clean build
```

> If the CLI complains about execution permissions run this command: `chmod +x gradlew`

You can run this command any time you want to build a `.jar` file from your project.
To run it you just have to call Java with your `.jar` file as a parameter:

```bash
java -jar build/libs/caves-of-zircon.jar
```

With little luck you'll see this screen:

![Hello, from Caves of Zircon](/assets/img/hello_coz.png)

## Importing the project to IDEA

Now let's import the project we just downloaded into IDEA, so we can start coding.
For this we're gonna use the *New > Project from Existing Sources* menu:

![New project from existing sources](/assets/img/project_import_00.png)

Then we select Gradle:

![Gradle select](/assets/img/project_import_01.png)

and finally we'll need to select "Use auto import" and a JVM:

![import + jvm](/assets/img/project_import_02.png)

If you have trouble setting up a JDK, then navigate to the *File > Project Structure* menu:

![project structure](/assets/img/sdk_00.png)

and add a new JDK. Use the one which you installed previously.

## Conclusion

We're all set now! We cloned the skeleton project from GitHub which contains all the setup
which is necessary to get started with our project and also imported it into our IDE.

In the next article we'll take a look at how our tools work and how we can start writing
our *actual* game.


 