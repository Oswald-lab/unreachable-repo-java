# 04-java-unreachable-repository
Declares two unreachable repositories (DNS failure + non-routable IP/timeout) and a dependency that
only exists there. Short timeouts configured in `.mvn/maven.config` and `gradle.properties`.
Expected: "Could not transfer artifact ... / Could not resolve ..." mentioning the repo ids/URLs,
and the tool surfaces it as a network/repository error rather than a generic crash.
Alternative: import 01-java-dual-valid-app with network disabled during `mvn install` / `gradle build`.
