# Primera-letra-en-mayusculas-Java

Use Apache's common library. Free your brain from these stuffs and avoid Null Pointer & Index Out Of Bound Exceptions
Step 1:

Import apache's common lang library by putting this in build.gradle dependencies

```
compile 'org.apache.commons:commons-lang3:3.6'
```

Step 2:

If you are sure that your string is all lower case, or all you need is to initialize the first letter, directly call

StringUtils.capitalize(yourString);
If you want to make sure that only the first letter is capitalized, like doing this for an enum, call toLowerCase() first and keep in mind that it will throw NullPointerException if the input string is null.

StringUtils.capitalize(YourEnum.STUFF.name().toLowerCase());
StringUtils.capitalize(yourString.toLowerCase());
Here are more samples provided by apache. it's exception free

```
StringUtils.capitalize(null)  = null
StringUtils.capitalize("")    = ""
StringUtils.capitalize("cat") = "Cat"
StringUtils.capitalize("cAt") = "CAt"
StringUtils.capitalize("'cat'") = "'cat'"
```

Note:

WordUtils is also included in this library, but is deprecated. Please do not use that.

Link: https://commons.apache.org/proper/commons-lang/
