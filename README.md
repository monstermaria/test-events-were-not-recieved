# test-events-were-not-recieved

Project created with Gradle 6.7. I'm using SDK 15.0.1 for both the project and Gradle, and IntelliJ IDEA 2020.2.4 (Community Edition)

Worked fine until I added JavaFX and made main a module to be able to use JavaFX. Then the tests would not run, and I got the message
"Test events were not recieved" in the test window. This is the output from the run window:

    Testing started at 10:16 ...

    > Configure project :app
    Project :app => 'se.monstermaria.media.library' Java module
    > Task :app:compileJava UP-TO-DATE
    > Task :app:processResources NO-SOURCE
    > Task :app:classes UP-TO-DATE
    > Task :app:compileTestJava UP-TO-DATE
    > Task :app:processTestResources NO-SOURCE
    > Task :app:testClasses UP-TO-DATE
    > Task :app:test
    > Task :app:test FAILED
    FAILURE: Build failed with an exception.
    * What went wrong:
    Execution failed for task ':app:test'.
    > There were failing tests. See the report at: file:///C:/Users/monst/Documents/Javautvecklare/TestdrivenUtveckling/GradleJavaFX/app/build/reports/tests/test/index.html
    * Try:
    Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output. Run with --scan to get full insights.
    * Get more help at https://help.gradle.org
    BUILD FAILED in 10s
    3 actionable tasks: 1 executed, 2 up-to-date

If I change Gradle setting "Run tests using:" from Gradle to IntelliJ IDEA, it works. Solution found here: https://youtrack.jetbrains.com/issue/IDEA-221159
