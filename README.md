# JNanoId
[![Build Status](https://travis-ci.org/aventrix/jnanoid.svg?branch=develop)](https://travis-ci.org/aventrix/jnanoid)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.aventrix.jnanoid/jnanoid/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.aventrix.jnanoid/jnanoid)

A unique string ID generator for Java. 

### Secure
JNanoID uses Java’s SecureRandom to generate cryptographically strong random IDs with a proper distribution of characters.

### Compact
JNanoID generates compact IDs with just 21 characters. By using a larger alphabet than UUID, JNanoID can generate a greater number of unique IDs, when compared to UUID, with fewer characters (21 versus 36).

### URL-Friendly
JNanoID uses URL-friendly characters (`A-Za-z0-9_~`). Perfect for unique identifiers in web applications.

### Customizable
JNanoID is fully customizable. All default options may be overriden. Supply your own Random Number Generator, alphabet, or size.

### Tested
JNanoID is thoroughly tested with Junit.

## Latest Release

The most recent release is JNanoId 1.0.1.

### Maven

```xml
<dependency>
  <groupId>com.aventrix.jnanoid</groupId>
  <artifactId>jnanoid</artifactId>
  <version>1.0.1</version>
</dependency>
```

## Usage

JNanoId provides one easy-to-use utility class (`NanoIdUtils`) with two methods to generate IDs.

#### Standard IDs - `randomNanoId()`

The default method creates secure, url-friendly, unique ids. It uses a url-friendly alphabet (`A-Za-z0-9_~`), a secure random number generator, and generates a unique ID with 21 characters.

```java
String id = NanoIdUtils.randomNanoId(); // "ku~qLNv1wDmIS5_EcT3j7"
```

#### Custom IDs - `NanoIdUtils.randomNanoId(random, alphabet, size);`

An additional method allows you to generate custom IDs by specifying your own random number generator, alphabet, or size.

```java
Random random = new SecureRandom();
char[] alphabet = {'a','b','c'};
int size = 10;

String id = NanoIdUtils.randomNanoId(random, alphabet, 10); // "babbcaabcb"
```

## Copyright and license

Code copyright 2017 [The JNanoID Authors](https://github.com/aventrix/jnanoid/graphs/contributors), [Aventrix LLC](https://www.aventrix.com), and [Andrey Sitnik](https://github.com/ai). Code released under the [MIT License](https://github.com/aventrix/jnanoid/blob/master/LICENSE).

Based on the original [NanoId](https://github.com/ai/nanoid) for JavaScript by [Andrey Sitnik](https://github.com/ai/).

## Other Programming Languages

* [JavaScript](https://github.com/ai/nanoid)
* [Go](https://github.com/matoous/go-nanoid)
* [PHP](https://github.com/hidehalo/nanoid-php)
* [Python](https://github.com/puyuan/py-nanoid)
* [Ruby](https://github.com/radeno/nanoid.rb)
