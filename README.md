# Jshell playground

I often want to use jshell with some libraries. Here's the low-fi way of doing this:

    CLASSPATH="/path/to/joda-time.jar" jshell
    jshell> import org.joda.time.DateTime;

But I'm stuck with locating the right jar every time. Why not let a fancy build system do the heavy lifting?

    // add something to the build.gradle in this repo
    ./jshell.sh
    [...snip...]
    |  Welcome to JShell -- Version 9
    
    jshell> import org.apache.commons.math3.analysis.function.Abs;
    
    jshell> new Abs().value(-1.0);
    $2 ==> 1.0
    
## Requirements

Java 9. Make sure your JAVA_HOME points to it.