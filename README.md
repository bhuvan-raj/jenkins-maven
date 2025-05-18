

---

```markdown
# Jenkins Maven Demo Project

This is a simple Java project built with Maven. It's intended to demonstrate Jenkins Freestyle project integration with GitHub and Maven build automation.

---

## 📁 Project Structure

```

java-hello-maven/
├── src/
│   └── main/
│       └── java/
│           └── com/
│               └── example/
│                   └── HelloApp.java
├── pom.xml

````

---

## 🚀 Technologies Used

- Java 8+
- Maven
- Git
- Jenkins

---

## 📦 How to Build

You can build this project using Maven:

```bash
mvn clean install
````

The compiled `.jar` file will be located in the `target/` directory.

---

## 🤖 Jenkins Setup (Freestyle)

1. Create a **Freestyle project** in Jenkins.
2. Under **Source Code Management**, choose **Git** and provide this repo URL:
   `https://github.com/bhuvan-raj/jenkins-maven.git`
3. Under **Build**, add step:

   ```
   Invoke top-level Maven targets
   Goals: clean install
   ```
4. (Optional) Under **Post-build Actions**, add:

   ```
   Archive the artifacts: target/*.jar
   ```

---

## 🧪 Sample Code (`HelloApp.java`)

```java
package com.example;

public class HelloApp {
    public static void main(String[] args) {
        System.out.println("Hello from Maven + Jenkins!");
    }
}
```

---

## 🧾 Sample `pom.xml`

```xml
<project xmlns="http://maven.apache.org/POM/4.0.0" 
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 
         http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.example</groupId>
    <artifactId>helloapp</artifactId>
    <version>1.0-SNAPSHOT</version>

    <properties>
        <maven.compiler.source>1.8</maven.compiler.source>
        <maven.compiler.target>1.8</maven.compiler.target>
    </properties>

    <build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>3.8.1</version>
            </plugin>
        </plugins>
    </build>
</project>
```

---

## 📄 Sample Output

```bash
Hello from Maven + Jenkins!
```

---

## 🙋‍♂️ Author

Maintained by **[Bhuvan Raj](https://github.com/bhuvan-raj)**

```

---


```
