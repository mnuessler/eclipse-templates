# Eclipse Templates #

## Installation ##

## Templates ##

### Logging ###

#### Create SLF4J Logger ####

Name: `logger`
Abstract: Creates an SLF4J logger instance with the name of the enclosing class.

Example:
```java
	public class Foo {
		logger<CTRL-SPC>
	}
```
expands to:
```java
	import org.slf4j.Logger;
	import org.slf4j.LoggerFactory;
	
	public class Foo {
		private static final Logger LOG = LoggerFactory.getLogger(Foo.class);
	}
```
