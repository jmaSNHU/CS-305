# CS-305
Software Security


-	**Briefly summarize your client, Artemis Financial, and its software requirements. Who was the client? What issue did the company want you to address?**

    Artemis Financial is a financial consulting company seeking to improve their software security to protect confidential client data and financial information. Specifically, Artemis Financial was looking to implement a checksum to ensure data integrity and to update their web application to require HTTPS for encrypted communications. 

-	**What did you do well when you found your client’s software security vulnerabilities? Why is it important to code securely? What value does software security add to a company’s overall well-being?**

    In order to update the existing application to use HTTPS, I first generated a TLS/SSL certificate so that the application could run as a Spring SSL server application. Developing software with secure programming practices and keeping software dependencies up to date are extremely important for protecting sensitive data that belongs to both companies and individuals, which can cause incredible monetary and legal damages for the victims of cyber-attacks. For a company like Artemis Financial, which handles sensitive financial information on behalf of itself and its clients, this is especially important. Furthermore, a commitment to security leads to better client relationships and fosters trust in the company’s competence. 

-	**Which part of the vulnerability assessment was challenging or helpful to you?**

    Although code review during this project was not especially demanding due to the minimal API, I imagine that manual code review on a large enterprise application can be a daunting task. Larger applications may have dozens or hundreds of models, controllers, and different layers from data access to services that must be reviewed to uncover security vulnerabilities. 

-	**How did you increase layers of security? In the future, what would you use to assess vulnerabilities and decide which mitigation techniques to use?**

    In addition to adding a TLS certificate to support HTTPS, I also utilized the OWASP Dependency Check tool to perform static security testing throughout the project. Utilizing these static testing tools is important to uncover new vulnerabilities as dependencies are added throughout the development process. In future projects, I would also use the Dependency Check to monitor my applications throughout the software life cycle. The best course of action is to keep software packages up to date whenever possible. 

-	**How did you make certain the code and software application were functional and secure? After refactoring the code, how did you check to see whether you introduced new vulnerabilities?**

    One of my focuses during code review was to make sure that errors are handled securely. For example, if an exception is raised when computing the SHA-256 checksum, the controller should never display stack traces or otherwise leaks the implementation details to the consumer. I also used the Dependency Check iteratively to check for new vulnerabilities after importing new dependencies, such as the MessageDigest class.

-	**What resources, tools, or coding practices did you use that might be helpful in future assignments or tasks?**

    I cannot overemphasize the importance of static testing tools like the OWASP Dependency Check tool. I also learned that this tool is available on many frameworks and languages, such as C#, and Python. This tool is also integrated into DevSecOps pipelines on platforms like Azure DevOps and GitHub. 

-	**Employers sometimes ask for examples of work that you have successfully completed to show your skills, knowledge, and experience. What might you show future employers from this assignment?**

    I would likely use artefacts from this course to demonstrate a working knowledge of security concepts, such as the importance of both self-signed and CA TLS/SSL certificates, the use case for OWASP Dependency Check, and use of the SHA2 family of hashing algorithms for verifying data integrity. 
