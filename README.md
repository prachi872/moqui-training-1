# Assignment: Create Custom Moqui Component

This assignment tests your ability to:
- Read documentation and follow instructions.
- Create a new custom Moqui component.
- Add a new entity definition in the component.
- Demonstrate working knowledge of Git and GitHub for managing source code.

---

## Tasks

### 1. **Learn Moqui and Related Technologies**
- **Objective**: Familiarize yourself with the Moqui framework and its components to complete the assignment tasks.

---

### 2. **Configure the Moqui Framework**
- **Steps**:
  1. Ensure you have the prerequisites installed (see below).
  2. Clone the Moqui framework repository:
     ```bash
     git clone -b master https://github.com/moqui/moqui-framework.git
     ```
  3. Navigate to the `moqui-framework` directory and run:
     ```bash
     ./gradlew getRuntime
     ```
  4. Start the application:
     ```bash
     ./gradlew run
     ```
  5. Verify the application is up and running.

---

### 3. **Configure IDE**
- **Steps**:
  - Set up Moqui in IntelliJ IDEA or your preferred IDE.
  - Configure XML schema locations for Entity Definition, Service Definition, and Service REST API.

---

### 4. **Clone Repository**
- Clone the `moqui-training` repository into the `runtime/component` folder under the Moqui framework:
  ```bash
  git clone <your-repository-url> runtime/component/moqui-training
  ```

---

### 5. **Add Configuration Files**
- Create the following configuration files with basic templates:
  1. `component.xml`:
     ```xml
     <component name="moqui-training"/>
     ```
  2. `MoquiConf.xml`:
     ```xml
     <moqui-conf>
       <entity-facade entity-package="moqui.training"/>
     </moqui-conf>
     ```

---

### 6. **Add Entity Definition**
- Create a new entity definition named `MoquiTraining` with the following attributes:
  | Attribute        | Data Type  | Description                  |
  |------------------|------------|------------------------------|
  | `trainingId`     | Primary Key | Unique identifier            |
  | `trainingName`   | String     | Name of the training         |
  | `trainingDate`   | Date       | Date of the training         |
  | `trainingPrice`  | Decimal    | Price of the training        |
  | `trainingDuration` | Integer   | Duration (in hours)          |

- Sample `entity` definition in XML:
  ```xml
  <entity entity-name="MoquiTraining" package-name="moqui.training">
    <field name="trainingId" type="id"/>
    <field name="trainingName" type="text"/>
    <field name="trainingDate" type="date"/>
    <field name="trainingPrice" type="currency-amount"/>
    <field name="trainingDuration" type="number-integer"/>
  </entity>
  ```

---

### 7. **Run Moqui**
- Start the Moqui application and verify that the new `MoquiTraining` entity is visible in the Entity Tools list in the Moqui UI.

---

### 8. **Push Changes to GitHub**
- Add and commit your changes to the `moqui-training` repository:
  ```bash
  git add .
  git commit -m "Added MoquiTraining entity and configuration files."
  git push origin main
  ```

---

## Prerequisites

1. **Git**
   - Ensure Git is installed.

2. **JDK 11 or Compatible JDK**
   - Verify Java version:
     ```bash
     java -version
     ```

3. **Terminal Navigation**
   - Familiarity with navigating file directories on your machine using a terminal.

4. **GitHub Account**
   - Create a new repository named `moqui-training` for assignment submissions.

---

## Additional Resources

- **Official Documentation**: [Moqui Documentation](https://moqui.org)
- **Tutorial Videos**:
  - [Introduction to Moqui](https://www.youtube.com/watch?v=d_ZiTjzZ-Qs&list=PL6JSOz3-TrFSMiuGounNRnje-JQDi8l8g&index=2&t=3s)
  - [Entity Definitions](https://www.youtube.com/watch?v=rvi9_ELXDHc&list=PL6JSOz3-TrFSMiuGounNRnje-JQDi8l8g&index=10&t=3s)
  - [Service Definitions](https://www.youtube.com/watch?v=BEhQH0lVW08&list=PL6JSOz3-TrFSMiuGounNRnje-JQDi8l8g&index=15&t=1s)
- **Playlist**: [Moqui Tutorials Playlist](https://www.youtube.com/playlist?list=PL6JSOz3-TrFSBQFDVSyjuZ49BUENd4bH6)
