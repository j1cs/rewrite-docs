# Mockito 3.x migration from 1.x

**org.openrewrite.java.testing.mockito.Mockito1to3Migration**  
_Spring Boot 2.x requires upgrading from Mockito 1.x to 3.x._

### Tags

* testing
* mockito

## Recipe list

* [Change type](../../../java/changetype.md)
  * oldFullyQualifiedTypeName: org.mockito.MockitoAnnotations.Mock
  * newFullyQualifiedTypeName: org.mockito.Mock
* [Change method name](../../../java/changemethodname.md)
  * methodPattern: org.mockito.Matchers anyVararg()
  * newMethodName: any
* [Change type](../../../java/changetype.md)
  * oldFullyQualifiedTypeName: org.mockito.Matchers
  * newFullyQualifiedTypeName: org.mockito.ArgumentMatchers
* [Change method name](../../../java/changemethodname.md)
  * methodPattern: org.mockito.invocation.InvocationOnMock getArgumentAt(int, java.lang.Class)
  * newMethodName: getArgument
* [Change type](../../../java/changetype.md)
  * oldFullyQualifiedTypeName: org.mockito.runners.MockitoJUnitRunner
  * newFullyQualifiedTypeName: org.mockito.junit.MockitoJUnitRunner
* [Cleanup Mockito Imports](../../../java/testing/mockito/cleanupmockitoimports.md)
* [MockUtils To Static](../../../java/testing/mockito/mockutilstostatic.md)
* [Add Maven dependency](../../../maven/adddependency.md)
  * groupId: org.mockito
  * artifactId: mockito-junit-jupiter
  * version: 3.x
  * releasesOnly: false
  * onlyIfUsing: [org.mockito.junit.jupiter.MockitoExtension]