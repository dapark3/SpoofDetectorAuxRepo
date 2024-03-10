# Functional Requirements  

The functional requirements are loosely grouped by concept.  

## Platform (Registration, Security)  

- FR101: Users can register for an account via email and log in using that 
email.  
  - High priority  
  - BR1  

- FR102: Implement OAuth2 for user authentication and authorization.  
  - High priority  
  - BR1  

- FR103: Implement robust security measures to protect sensitive data and user information.   
  - High priority  
  - BR1  

- FR104: Maintain detailed logs and an audit trail of all user interactions and system activities for security and accountability.   
  - Medium priority  
  - BR1  

## Anomaly and Spoof Detection  

- FR201: Develop and implement algorithms for anomaly detection, statistical analysis, machine learning, and cryptographic validation to identify and verify drone anomalies.   
  - High priority  
  - BR1  

- FR202: Use attribute data to detect for spoofing.   
  -  High priority  
  -  BR1  

- FR203: Facilitate the simulation of synthetic spoofing attacks for evaluating the framework's effectiveness.   
  - Medium priority  
  - BR1  

- FR204: Exclude drones with spoofed Remote ID from being displayed to regular end-users.  
  - Medium priority  
  - BR2  

- FR205: Integrate a 3D mapping system, such as Cesium, to illustrate flight paths and present data to end-users.     
  - Medium priority  
  - BR2  

## Data Preprocessing System

- FR301: Apply advanced data preprocessing to remove outliers and reduce noise to ensure the quality of input data.
  - High priority
  - BR1

- FR302: Integrate selected algorithms into a prototype data curation system for efficient data processing.
  - Medium priority
  - BR1

## Performance Requirements

- FR401: Conduct experiments using real-world datasets and simulated spoofing attacks to validate performance. Evaluation metrics include detection accuracy, false positive rate, and response time. 
  - Medium priority
  - BR1

- FR402: Meet real-time requirements to ensure timely response in anomaly detection and data presentation.   
  - High priority  
  - BR1  

## Non-functional Requirements

- NR1: Address ethical considerations in the techniques used to simulate spoofing attacks, ensuring responsible and legal use. 
  - Medium priority
  - BR1

- NR2: Design the system with the ability to scale to accommodate an increasing number of users and data sources. 
  - High priority
  - BR1

- NR3: Provide training and documentation for end-users to effectively use the application.
  - Medium priority
  - BR2

- NR4: Include a maintenance and support plan to address updates, bug fixes, and user inquiries. 
  - Medium priority
  - BR1

- NR5: Provide comprehensive technical documentation for developers and administrators.   
  - Medium priority
  - BR1

- NR6: The displayed information will be accessible on a smart device.
  - Medium priority
  - BR2

- NR7: The User Interface allows for customization of the types of UAS data displayed. 
  - Low priority
  - BR2
