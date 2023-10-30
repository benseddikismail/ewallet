# eWallet
***eWallet*** is a digital wallet and mobility and expenses manager application. It, essentially, targets Renault clients with the aim to ease the burden of monitoring their vehicles’ needs off their shoulders. Through the mobile application, the user gets to plan for vehicle check-ups and services, survey mobility requirements, locate reputable service providers and product vendors, pay for the services/products and manage their expenses. One principal motivation underlying the solution is customer fidelization. Besides, in recent years, mobile payment ecosystems are blessed and backed by Moroccan government bodies as they have the potential to bring about socioeconomic prosperity in the form of financial inclusion and social isolation breakage.
## System Architecture
The solution fulfills the following intents: forecasting and setting the necessary budgets corresponding to mobility-related expenses, defining and planning the available mobility services, locating service providers, comparing prices, enabling the user to pay through the platform, presenting commercial offers and deals, and logging and analyzing all transactions. The architectural process consisted of the following phases: 
- **Pre-framing:** requirements gathering and requirements specification as well as finding the most adequate solution for the problem at hand (buying a solution, refining an existing solution or building a solution). During this phase, an eye-level solution is presented on the basis of understanding and short-listing the product owners’ business processes, constraints, risks and the potential value of the project.
- **Framing:** architectural conception. This represents the design phase in which the story map is populated with user stories, guidelines and standards are set to be adhered to, and important particulars such as business processes, functional building blocks, data models, system architecture and technology stack are planned for. Experts’ feedback is anticipated throughout this critical stage.
- **Execution:** this is the implementation phase. Nevertheless, architectural rectification and continuous update takes place during this stage as part of the agile framework adopted by Renault. A checklist of architectural compliance is to be respected to the fullest. 
- **Running:** deployment, shipping and maintenance of the product. Changes to the architecture are highly considered during this phase based on experts’ and product owners’ remarks and judgement. 

pic

| **ID** | **Entity/Actor**         | **OS**        | **Infrastructure**  | **Hosting** | **Technology**                     |
| ------ | ------------------------ | ------------- | ------------------- | ----------- | ---------------------------------- |
| **1**  | Renault Client           | iOS + Android | Mobile Device       | Internet    | React Native (mobile device)       |
| **2**  | Back-Office Users        | Windows       | ACE2 (VM)           | Intranet    | React (browser)                    |
| **3**  | Front-End (Back-Office)  | Linux         | GKE/Docker          | GCP         | React + Apache httpd reverse proxy |
| **4**  | Server-Side Runtime      | Linux         | GKE/Docker          | GCP         | Spring Boot + embedded Tomcat      |
| **5**  | Database                 | Linux         | GKE/Docker          | GCP         | PostgreSQL                         |
| **6**  | Integration Interfaces   | Linux         | GKE/Docker          | GCP         | Spring Boot + embedded Tomcat      |
| **7**  | Firebase                 | NA            | GCP Managed Service | GCP         | Firebase Cloud Messaging           |
| **8**  | Renault IDP              | NA            | Various Platforms   | DMZ INET    | Renault IDP                        |
| **9**  | Vault                    | NA            | Various Platforms   | GCP         | Vault by HashiCorp                 |
| **10** | Load Balancer            | NA            | Various Platforms   | GCP         | Google Cloud Load Balancer         |