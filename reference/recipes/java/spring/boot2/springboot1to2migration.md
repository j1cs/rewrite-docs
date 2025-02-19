# Spring Boot 2.x migration from Spring Boot 1.x

 **org.openrewrite.java.spring.boot2.SpringBoot1To2Migration** _Migrates Spring Boot 1.x to 2.x including best practices._

### Tags

* spring
* junit
* testing
* spring-boot
* mockito

## Source

[Github](https://github.com/openrewrite/rewrite-spring), [Issue Tracker](https://github.com/openrewrite/rewrite-spring/issues), [Maven Central](https://search.maven.org/artifact/org.openrewrite.recipe/rewrite-spring/4.9.0/jar)

* groupId: org.openrewrite.recipe
* artifactId: rewrite-spring
* version: 4.9.0

## Usage

This recipe has no required configuration options and can be activated directly after taking a dependency on org.openrewrite.recipe:rewrite-spring:4.9.0 in your build file:

{% tabs %}
{% tab title="Gradle" %}
{% code title="build.gradle" %}
```groovy
plugins {
    id("org.openrewrite.rewrite") version("5.7.0")
}

rewrite {
    activeRecipe("org.openrewrite.java.spring.boot2.SpringBoot1To2Migration")
}

repositories {
    mavenCentral()
}

dependencies {
    rewrite("org.openrewrite.recipe:rewrite-spring:4.9.0")
}
```
{% endcode %}
{% endtab %}

{% tab title="Maven" %}
{% code title="pom.xml" %}
```markup
<project>
  <build>
    <plugins>
      <plugin>
        <groupId>org.openrewrite.maven</groupId>
        <artifactId>rewrite-maven-plugin</artifactId>
        <version>4.9.0</version>
        <configuration>
          <activeRecipes>
            <recipe>org.openrewrite.java.spring.boot2.SpringBoot1To2Migration</recipe>
          </activeRecipes>
        </configuration>
        <dependencies>
          <dependency>
            <groupId>org.openrewrite.recipe</groupId>
            <artifactId>rewrite-spring</artifactId>
            <version>4.9.0</version>
          </dependency>
        </dependencies>
      </plugin>
    </plugins>
  </build>
</project>
```
{% endcode %}
{% endtab %}
{% endtabs %}

Recipes can also be activated directly from the command line by adding the argument `-DactiveRecipe=org.openrewrite.java.spring.boot2.SpringBoot1To2Migration`

## Definition

{% tabs %}
{% tab title="Recipe List" %}
* [Upgrade to Spring Boot 2.0 from 1.x](upgradespringboot_2_0.md)
* [Upgrade to Spring Boot 2.5](upgradespringboot_2_5.md)
* [Remove the `@Autowired` annotation on inferred constructor](../noautowiredonconstructor.md)
* [Migrate multi-condition `@ConditionalOnBean` annotations](conditionalonbeananynestedcondition.md)
* [Migrate `RestTemplateBuilder`](resttemplatebuilderrequestfactory.md)
* [Replace `EnvironmentTestUtils` with `TestPropertyValues`](replacedeprecatedenvironmenttestutils.md)
* [Spring Boot 2.x best practices](springboot2bestpractices.md)
{% endtab %}

{% tab title="Yaml Recipe List" %}
```yaml
---
type: specs.openrewrite.org/v1beta/recipe
name: org.openrewrite.java.spring.boot2.SpringBoot1To2Migration
displayName: Spring Boot 2.x migration from Spring Boot 1.x
description: Migrates Spring Boot 1.x to 2.x including best practices.
tags:
  - spring
  - junit
  - testing
  - spring-boot
  - mockito
recipeList:
  - org.openrewrite.java.spring.boot2.UpgradeSpringBoot_2_0
  - org.openrewrite.java.spring.boot2.UpgradeSpringBoot_2_5
  - org.openrewrite.java.spring.NoAutowiredOnConstructor
  - org.openrewrite.java.spring.boot2.ConditionalOnBeanAnyNestedCondition
  - org.openrewrite.java.spring.boot2.RestTemplateBuilderRequestFactory
  - org.openrewrite.java.spring.boot2.ReplaceDeprecatedEnvironmentTestUtils
  - org.openrewrite.java.spring.boot2.SpringBoot2BestPractices
```
{% endtab %}
{% endtabs %}

