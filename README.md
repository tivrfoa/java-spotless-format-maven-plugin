

`mvn verify`

```java
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  18.537 s
[INFO] Finished at: 2020-12-31T08:01:06-03:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal com.diffplug.spotless:spotless-maven-plugin:2.6.1:check (default) on project spotless-test: The following files had format violations:
[ERROR]     src\main\java\org\App.java
[ERROR]         @@ -1,13 +1,9 @@
[ERROR]         +/*·(C)2020·*/
[ERROR]          package·org;
[ERROR]
[ERROR]         -/**
[ERROR]         -·*·Hello·world!
[ERROR]         -·*
[ERROR]         -·*/
[ERROR]         +/**·Hello·world!·*/
[ERROR]          public·class·App·{
[ERROR]         -····public·static·void·main(String[]·args·)
[ERROR]         -····{
[ERROR]         -········System.out.println(·"Hello·World!"·);
[ERROR]         +····public·static·void·main(String[]·args)·{
[ERROR]         +········System.out.println("Hello·World!");
[ERROR]          ····}
[ERROR]          }
[ERROR]         -
[ERROR] Run 'mvn spotless:apply' to fix these violations.
```

`mvn spotless:apply`

```java
[INFO]
[INFO] -------------------------< org:spotless-test >--------------------------
[INFO] Building spotless-test 1.0-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO]
[INFO] --- spotless-maven-plugin:2.6.1:apply (default-cli) @ spotless-test ---
Can't parse copyright year '', defaulting to 2020
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  7.369 s
[INFO] Finished at: 2020-12-31T08:03:01-03:00
[INFO] ------------------------------------------------------------------------
```

