# Eclipse Templates #

## Templates Descriptions ##

### Category: Logging ###

#### Create SLF4J Logger ####

Name: `logger`

Description: Creates an [SLF4J][slf4j] logger instance with the name of the enclosing class.

Example:

This code

```java
public class Foo {
	logger<CTRL-SPC>
}
```

expands to

```java
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;

public class Foo {
	private static final Logger LOG = LoggerFactory.getLogger(Foo.class);
}
```

#### Log message ####

Name: `log`

Description: Creates a log statement. Lets you select the level from a
list of choices.

Example:

This code

```java
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;

public class Foo {
	private static final Logger LOG = LoggerFactory.getLogger(Foo.class);

	public void bar() {
		log<CTRL-SPC>
	}
}
```

expands to

```java
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;

public class Foo {
	private static final Logger LOG = LoggerFactory.getLogger(Foo.class);

	public void bar() {
		LOG.debug("");
	}
}
```

#### Log debug message ####

Name: `logd`

Description: Same as `log` but with fixed DEBUG level.

#### Log info message ####

Name: `logi`

Description: Same as `log` but with fixed INFO level.

#### Log warning message ####

Name: `logw`

Description: Same as `log` but with fixed WARN level.

#### Log error message ####

Name: `loge`

Description: Same as `log` but with fixed ERRORlevel.

### Category: JUnit Tests ###

#### Test method ####

Name: `test`

Description: Creates a JUnit test method body annotated with `@Test`
and prompts you for the test method name.

This templates is an enhancement of the standard template `Test`
shipped with Eclipse. Additional to the standard template, the
following static imports are added:

* `org.junit.Assert.*`
* `org.hamcrest.Matchers.*`
* `org.easymock.EasyMock.*`

Example:

This code

```java
public class FooTest {
}
```

expands to

```java
import static org.junit.Assert.*;
import static org.hamcrest.Matchers.*;
import static org.easymock.Easymock.*;

public class FooTest {

	@Test
	public void testX() throws Exception {
	}

}
```

#### Test Setup ####

Name: `before`

Description: Creates a test setup method body.

Example:

```java
public class FooTest {

before<CTRL-SPC>

}
```

expands to

```java
import org.junit.Before;

public class FooTest {

	@Before
	public void setUp() throws Exception {

	}

}
```

#### Test Teardown ####

Name: `after`

Description: Creates a test teardown method body.

Example:

```java
public class FooTest {

after<CTRL-SPC>

}
```

expands to

```java
import org.junit.After;

public class FooTest {

	@After
	public void tearDown() throws Exception {

	}

}
```


## Installation ##



[slf4j]: http://www.slf4j.org/
