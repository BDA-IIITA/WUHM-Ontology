**Project Overview**

The Wheelchair Users’ Health Monitoring (WUHM) project is an ontology-driven cyber-physical healthcare system designed to monitor, analyze, and support the health needs of wheelchair users. The system integrates IoT sensor data, Complex Event Processing (CEP), 
and semantic reasoning to enable real-time alerts, disease detection, and intelligent decision support. A key feature of this system is that health-related SPARQL queries are executed after CEP-based event detection, ensuring that only meaningful and clinically 
relevant events are semantically analyzed.


📂 How to use 
WUHM/
│── ontology/
│   └── wuhm.owl
│
│── data/
│   └── sensor_data.rdf
│
│── cep/
│   └── disease_rules.txt
│
│── queries/
│   └── health_monitoring.sparql


🧠 Component Description
🔹 ontology/

wuhm.owl

Core WUHM ontology defined in OWL
Models concepts such as WheelchairUser, Sensor, VitalSign, Activity, Symptom, Disease, Alert, and Assistance
Integrates sensor observations with medical knowledge for reasoning

🔹 data/

sensor_data.rdf

RDF representation of real-time and historical sensor data
Includes physiological parameters such as heart rate, temperature, posture, and activity status
Acts as input for CEP and semantic reasoning

🔹 cep/

disease_rules.txt

Contains Complex Event Processing (CEP) rules
Defines threshold-based and pattern-based health events (e.g., abnormal heart rate, prolonged inactivity)
Filters raw sensor streams and generates high-level health events
Only CEP-detected events are forwarded for semantic querying

🔹 queries/

health_monitoring.sparql
SPARQL queries executed after CEP processing
Operates on ontology-enriched event data

Used for:
Disease identification
Emergency detection
Personalized alerts and recommendations
Caregiver and clinician decision support
