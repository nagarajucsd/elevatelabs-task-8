# Hello Java Maven

This is a simple Java project built using **Maven** and integrated with **Jenkins** for CI/CD demonstration.

## 🚀 Project Structure
```
hello-java-maven/
 ├── pom.xml
 └── src/main/java/HelloWorld.java
```

### HelloWorld.java
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Jenkins + Maven!");
    }
}
```

### pom.xml
Uses Maven Compiler Plugin to compile Java 1.8 source code.

## ⚙️ Build Instructions (Local)
1. Install Java (JDK 8 or 11) and Maven.
2. Run:
   ```bash
   mvn clean package
   ```
3. Execute the program:
   ```bash
   java -cp target/hello-1.0.jar HelloWorld
   ```

## 🛠 Jenkins Integration
1. Start Jenkins (`docker run -p 8080:8080 jenkins/jenkins:lts`).
2. Configure JDK and Maven in **Manage Jenkins → Global Tool Configuration**.
3. Create a **Freestyle Project** in Jenkins.
4. In **Build** step, add **Invoke top-level Maven targets** with goals:
   ```
   clean package
   ```
5. Build → Console Output should show:
   ```
   [INFO] BUILD SUCCESS
   ```

## 📸 Deliverables
- Jenkins job configuration screenshot.
- Console output showing `BUILD SUCCESS`.
- Project structure confirmation.

---
Made with ❤️ for learning CI/CD with Jenkins + Maven.
