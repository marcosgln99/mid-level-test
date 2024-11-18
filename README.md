# Simplekyc mid-level Tecnical test Exercise.

# Technical Test Instructions

## Fork and Modify

Fork this repository and make the necessary changes in your repository. As a final step, generate a pull request with the changes.

## Rules

1. **The use of AI is allowed for specific tasks.**  
   If used, indicate in comments which section it was applied to and why.  
   If the entire exercise is completed with AI, the test will be considered invalid.

2. **You are free to use any technologies you deem fit to solve the problem.**  
   However, the technologies requested in the job application will be valued more.

3. **The test must be completed within one week (7 days).**  
   This period starts from the moment the technical test is communicated and accepted.

4. **Minimum security and usability criteria must be met.**  
   Hardcoded values, passwords, or similar items in the code will automatically invalidate the test.

5. **If the test requires passwords or SSH keys.**  
   Indicate them as `<PASSWORD>` and `<SSH KEY>` in the code and send them separately to the reviewer.

6. **The evaluator may ask questions about the test in a live, face-to-face interview.**

7. **Minimum and maximum scope considerations:**  
   - Meeting the minimum requirements will score up to **7/10**.  
   - Meeting the maximum scope can score up to **10/10**.

8. **Evaluation is based on completeness.**  
   It is better to achieve 100% of the minimum scope than 70% of the maximum scope.

---

## Scenario

### Minimum Scenario:

You have two Linux machines running **Ubuntu 20.04** or **22.04**:

- **First machine**:
  - Install:
    - **Apache = 2.4 / Nginx = latest**
    - **PHP = 8.2**
    - **Node.js = 20.16**
    - **MySQL > 8.0**
  - Create a simple PHP page that displays:  
    `"Hi, I am the host: <HOSTNAME>"`, where `<HOSTNAME>` is dynamically retrieved by PHP.

- **Second machine**:
  - Install:
    - **Grafana**
    - **Prometheus**
  - Configure both to be accessible via HTTP and capable of monitoring the **CPU, RAM, and disk usage** of the first machine.

---

### Maximum Scenario:

- Provide **Infrastructure as Code (IaC)** to provision both machines.
- The platform is your choice (**VMware**, **VirtualBox**, **Proxmox**, **Azure**, **AWS**, **GCP**, etc.).
- Implement the same scenario with **high availability** for the PHP application.
