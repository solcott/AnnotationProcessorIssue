To reproduce the issue run ./gradlew :module1:compileDebugJavaWithJavac --info

You will notice that quite a bit the compileDebugJavaWithJavac isn't up to date due to options.compilerArgs changing.

If you run ./gradlew :module1:compileDebugJavaWithJavac --debug you can see the compiler args and compare them with a different run.  It seems the only change is the order of entries in -classpath and -processorpath