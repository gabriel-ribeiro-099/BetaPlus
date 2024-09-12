# BetaPlus

This project was completed with two colleagues, [Wisla Argolo](https://github.com/wislaargolo) and [Caio Vitor](https://github.com/CaioVitorDM).

## About Hydatidiform Mole 

First, let’s explain, for those unfamiliar, what a molar pregnancy is. A molar pregnancy, or hydatidiform mole, is a rare pregnancy complication involving the abnormal growth of trophoblasts—the cells that normally develop into the placenta. In a molar pregnancy, the tissue that typically forms the placenta instead grows into an abnormal mass in the uterus.There are two types of molar pregnancies:

- **Complete Mole:** No normal fetal tissue develops. The placenta grows abnormally and contains cyst-like structures.
- **Partial Mole:** Some abnormal fetal tissue develops along with an abnormal placenta, but the fetus cannot survive.

### Why is it difficult to treat?

- **Invasive Growth:** A molar pregnancy can sometimes invade deeply into the uterine wall, making it difficult to fully remove. This condition is known as an invasive mole.

- **Risk of Recurrence:** After the removal of a molar pregnancy, there is a risk that the abnormal cells will continue to grow. This requires careful monitoring through blood tests to check for elevated levels of the hormone hCG (human chorionic gonadotropin), which is produced by the molar tissue.

- **Choriocarcinoma:** In rare cases, a molar pregnancy can develop into a cancerous form of gestational trophoblastic disease called choriocarcinoma, which can spread to other parts of the body, complicating treatment. Chemotherapy may be required in such cases.

- **Emotional and Physical Impact:** The treatment often involves dilation and curettage (D&C) to remove the abnormal tissue, followed by a long period of monitoring to ensure the molar tissue does not regrow. This prolonged monitoring and the potential need for chemotherapy can be physically and emotionally taxing.

Because of these factors, molar pregnancy requires specialized care, frequent follow-up, and sometimes aggressive treatment. This is where our system comes into play—to facilitate the treatment process.

## About the System

The system is a Single Page Application (SPA) built with Angular and Spring Boot, utilizing libraries such as JWT Token, Spring JPA, Spring Web, Jakarta Validation API, and Hibernate. For the database, we used PostgreSQL, with Maven as the dependency management tool. The system follows a microservices architecture.
There are two possible user roles—patient and doctor—each with unique capabilities:

- **Doctor:**
  - CRUD operations for appointments
  - CRUD operations for exams, with PDF exam upload
  - CRUD operations for treatment protocols, which can be unique or shared among patients
    
Access to a specialized GUI, including a unique dashboard and a view that gathers all patient information in one place

- **Patient:**
  - CRUD operations for hCG blood test results
  - Download treatment protocols
  - CRUD operations for exams
  - View upcoming appointments

To ensure that only users with the appropriate role can access specific parts of the system, we perform a series of validations on both the frontend and backend, ensuring security and correctness.

### About Microservices Architecture

The system is divided in six microservices:

- API-Gateway
- EurekaServer
- Auth-Server
- Exams
- Protocols
- Files

## Conclusion

BetaPlus is designed to streamline the complex treatment process of molar pregnancies by providing a secure, user-friendly system for doctors and patients alike. Through a robust microservices architecture and modern web technologies, our system ensures efficient management of appointments, exams, treatment protocols, and patient data.

By automating many aspects of treatment and ensuring secure role-based access, BetaPlus simplifies both patient care and medical workflows, providing real value to healthcare professionals.

We hope this system can be a helpful tool in improving the treatment journey for patients with molar pregnancies.

## Getting Started

To get the system up and running on your local machine, follow these steps:

1. Clone the repository.
2. Install the necessary dependencies with Maven.
3. Configure the database connection in the `application.properties` file.
4. Run the microservices individually using the provided scripts or IDE.
5. Access the SPA frontend through the Angular development server.

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.
