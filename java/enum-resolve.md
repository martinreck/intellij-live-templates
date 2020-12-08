# Enum `resolve` Method
> This Live Template adds a static `resolve` method to a Java `enum`, to resolve the corresponding Enum constant using the given `String`.

```java
public static $ENUM$ resolve(final String $VALUE$) throws IllegalArgumentException {
	for ($ENUM$ $ENUM_ELEMENT$ : $ENUM$.values()) {
		if ($ENUM_ELEMENT$.$VALUE$.$EQUALS_METHOD$($VALUE$)) {
			return $ENUM_ELEMENT$;
		}
	}
	throw new IllegalArgumentException("No $ENUM$: '" + $VALUE$ + "'");
}
```

Variables
---
  - ### `ENUM`

    > The name of the enclosing enum.

    Expression: `className()`
  
  - ### `ENUM_ELEMENT`

    > The name of the variable which contains the iterated enum members.

    Expression: `suggestVariableName()`
    
    > This will suggest a variable name according to the context.

  - ### `VALUE`

    > The name of the local variable and the name of the instance variable used to compare the enum.

    Expression: `enum("value", "code", "id")`

    Default: `"value"`

    > This will suggest a variable name from this list.

  - ### `EQUALS_METHOD`

    > The option to choose the method name that is used for comparison: either `equals` or `equalsIgnoreCase`.

     Expression: `enum("equalsIgnoreCase", "equals")`

     Default: `"equalsIgnoreCase"`

Applicable in
---

`Java: declaration`

Options
---
  - Reformat according to style
  - Shorten FQ names
