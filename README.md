## Comands

### Table of contents

- [Run the project](#run-the-project)
- [Run tests](#run-tests)

> ![NOTE]
> This project uses [Gradle](https://gradle.org/) as a build tool.
>
> All commands are executed using the `gradlew` script.
>
> Commands are gradle tasks and can be seen in the [build.gradle.kts](build.gradle.kts) file.

### Run the project

> [!IMPORTANT]
> With [Docker Compose](https://docs.docker.com/compose/) installed, run the following command:
>
> ```bash
> ./gradlew composeUp
> ```
>
> To stop the project, run the following command:
>
> ```bash
> ./gradlew composeDown
> ```

### Run tests

> [!IMPORTANT]
> To run all tests, run the following command:
>
> ```bash
> ./gradlew check
> ```
