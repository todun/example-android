
[![Build Status](https://travis-ci.org/codecov/example-android.svg?branch=master)](https://travis-ci.org/codecov/example-android)
[![travis](https://travis-ci.org/todun/example-android.svg?branch=master)](https://github.com/todun/example-android)
# [Travis](https://travis-ci.org/todun/example-android) Android Example
## Guide
#### Travis Setup
If you use [Travis CI](https://travis-ci.org) as your continuous integration server you can
configure it to build the project, generate test coverage reports and upload them to
[Codecov](https://codecov.io). See an example [.travis.yml](.travis.yml) file on how to do this.
#### Produce Coverage Reports
Codecov parses uploaded test coverage reports but your project is required to generate them first.
You can use [jacoco-android-gradle-plugin](https://github.com/arturdm/jacoco-android-gradle-plugin)
to create appropriate gradle tasks and run this command to generate the reports:

```
./gradlew jacocoTestReport
```

#### Instrumentation tests coverage reports

Generating instrumentation tests code coverage reports requires a minor change to the build script.

```groovy
android {
  buildTypes {
    debug {
      testCoverageEnabled true
    }
  }
}
```

Running the command below generates the reports: 

```
./gradlew connectedCheck
```
## Support
### Contact
- TBA

