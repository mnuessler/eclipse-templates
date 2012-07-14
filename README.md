# Eclipse Templates #

## Java Templates ##

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

Description: Same as `log` but with fixed ERROR level.

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

#### Test Assertion ####

Name: `assert`

Description: Creates a JUnit assertion body. Adds useful static imports.

Example:

This code

```java
public class FooTest {

	@Test
	public void testBar() throws Exception {
		assert<CTRL-SPC>
	}

}
```

expands

```java
import static org.junit.Assert.assertThat;
import static org.hamcrest.Matchers.*;

public class FooTest {

	@Test
	public void testBar() throws Exception {
		assertThat( , Matchers. );
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

#### Test Setup Before Class ####

Name: `beforeclass`

Description: Creates a test setup-before-class method body.

Example:

```java
public class FooTest {

beforeclass<CTRL-SPC>

}
```

expands to

```java
import org.junit.BeforeClass;

public class FooTest {

	@BeforeClass
	public void setUpBeforeClass() throws Exception {

	}

}
```

#### Test Teardown After Class ####

Name: `afterclass`

Description: Creates a test teardown-after-class method body.

Example:

```java
public class FooTest {

afterclass<CTRL-SPC>

}
```

expands to

```java
import org.junit.AfterClass;

public class FooTest {

	@AfterClass
	public void tearDownAfterClass() throws Exception {

	}

}
```

### Category: Misc ###

#### Iterate over Map ####

Name: `formap`

Description: Iterates over the entries of a `java.util.Map` with a
foreach loop.

Example:

This code

```java
Map<String, String> myMap = new HashMap<String, String>();

formap<CTRL-SPC>>
```

expands to

```java
Map<String, String> myMap = new HashMap<String, String>();

for (Map.Entry< , > entry : myMap.entrySet()) {

}
```

#### Check for null ####

Name: `ifnull`

Description: Creates a block to execute when a local variable is
null.

Example:

This code

```java
Integer i = null;

ifnull<CTRL-SPC>>
```

expands to

```java
Integer i = null;

if (i == null) {

}
```

#### Check for not-null ####

Name: `ifnotnull`

Description: Creates a block to execute when a local variable is
not null.

Example:

This code

```java
Integer i = null;

ifnotnull<CTRL-SPC>>
```

expands to

```java
Integer i = null;

if (i != null) {

}
```

## Installation ##



[slf4j]: http://www.slf4j.org/
