# Designing an Enterprise Agentic AI Scheduler in n8n

#### This repository presents  step-by-step process of how an Agentic AI Scheduler for enterprise application was desined in n8n. 

#### The repository is designed for AI Architects that prefers to follow the low-code alternative for Agentic AI integration in the enterprise offered by n8b. 

#### For a full discourse on how the Agent can be deployed in the enterprise with scalability on mind, interested readers can visit: https://github.com/manuelbomi/Enterprise-Agentic-AI---Scalable-Meeting-Orchestration-with-n8n

#### Redears can also deploy the Agent by cloning the .json file in the repo. A full discourse on how the solution architect can accomplish that is also avaialble here: https://github.com/manuelbomi/Enterprise-Agentic-AI---Scalable-Meeting-Orchestration-with-n8n

#### This is the Agentic AI Scheduler that was designed by following the procedures outlined in this discourse:

<img width="995" height="360" alt="Image" src="https://github.com/user-attachments/assets/dd82a6d4-4ac7-4d79-a12c-b4c199760e51" />

--- 

###  💬 The Agent can converse with the user as shown below:

---
```ruby

Here’s how a typical interaction looks once the workflow is deployed:

User:
"Can you schedule a 30-minute meeting with John tomorrow afternoon?"

AI Agent:
"Sure! Let me check your calendar for availability tomorrow afternoon..."

(Agent uses Google Calendar to fetch free slots)

AI Agent:
"You are free at 2:00 PM, 3:30 PM, and 4:15 PM. Which works best for you?"

User:
"Let’s go with 3:30 PM."

AI Agent:
"Perfect. Scheduling the meeting with John at 3:30 PM tomorrow. Do you want me to add a description?"

User:
"Yes — add 'Project Roadmap Discussion'."

AI Agent:
"Done! I’ve scheduled 'Project Roadmap Discussion' with John tomorrow at 3:30 PM, and added it to your Google Calendar."


```
---

#### Below are figures showing how the Agent converse with users and execute its job via the n8n user interface:

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/8a0eab77-491f-422c-b30e-6ea04a759b6d" />

---
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/4c3525f2-6fde-46d0-9602-54818b9fe41f" />

---
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/d8fd1ace-5c57-4d17-b67b-1180e77bb7be" />

---
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/b590f247-6224-4cd1-857e-97d90eadff66" />

---

## Design Procedures in n8n

#### To commennce designing the Agent in n8n, follow the set of procedures below:

#### Start with the primer workflow here: https://github.com/manuelbomi/An-Enterprise-Agentic-AI-Primer-with-n8n  and remove the calculator component:

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/35a32555-60b3-4e91-be73-d86320d4e20e" />

---
#### Search for Google Calendar under Tools
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/cb0f66d9-9344-47a0-8cb5-2e590b043092" />

----

####  Select credentials and create new credentials
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/a3cb18f0-96d2-419d-99a5-714a5a23eabf" />

---
#### Create new credential
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/15f61e42-7f49-44c7-bc19-cfc23edd2772" />

---

#### Click inside Client ID and click on Open Docs
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/732bd59e-fa03-4b95-bda2-73aeece6f777" />

---

#### If you decide to use the OAuth method, follow the instructions on Google Docs by opening Google Console and create a project on Google Console

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/1817d0a9-e63f-43e0-8233-749e8397215d" />
---

#### On Google Cloud Console go to your console

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/521751ac-1e05-459e-b2c2-e944a50701a1" />

---
#### Go to your GCP console

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/beca39c5-43d5-4a88-9d77-13276d625f28" />
---

#### Click on your current project e g the SQL-query-optimization project and create a new project

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/4ef17553-b2d3-4d40-a97b-71331730e92b" />

---

####  Give it a name and create the  project

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/3ab1fab2-3c15-444d-aad4-bd674fd914a4" />
---

#### Go back to the Set Up OAuth page on Google Docs i e Enable APIs
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/b4e272e7-ea49-4bd4-8667-73e123d5e607" />
---

####  To Enable APIs, click on your list of projects on your Google Console and select the n8n Agent project

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/8dc07c8e-29ea-44c5-993a-432bab3fa7bb" />

---

#### On the project, click on APIs and Services
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/76b7fd04-e09d-42b2-a49a-b01f301ab2e0" />
---

#### Click Enable APIs and Services
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/3106ccf0-26a2-4d67-b38d-bfbd83955d7f" />

---

#### Search for calendar
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/7e015c8c-8bd0-4f73-871f-d861121565fc" />

---

#### Select the Google Calendar API and click Enable
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/bf0a9a33-3b7c-4a01-ba1c-0ac7327f2e17" />
---

####  Click Enable and select create credentials
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/9011663c-cb72-4eec-b505-b2ef69e479e4" />
---

#### Select user data and click next
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/92d94c11-8621-4e8b-8235-313b3ea7edca" />
---

#### Give the app a name and supply user support email and developer contact info save and continue
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/20727461-32ef-42c0-b12c-4edd8b2e0e5b" />
---

####  Click save and continue again
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/ce30bd3c-41f9-493e-89f3-3534ca22be0d" />
---

#### Under OAuth Client ID select web application
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/133c6ea1-1af1-443b-80d3-e36ee101a87e" />
---

####  Give it a name eg n8n agent
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/c1a502a3-dead-4737-87ab-d88264c96617" />
---

#### Under Authorized Redirect URI click ADD URI
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/653dfe21-e9db-4247-bec0-66d373138736" />
---






















Thank you for reading

---

### **AUTHOR'S BACKGROUND**

### Author's Name:  Emmanuel Oyekanlu
```
Skillset:   I have experience spanning several years in data science, developing scalable enterprise data pipelines,
enterprise solution architecture, architecting enterprise systems data and AI applications,
software and AI solution design and deployments, data engineering, high performance computing (GPU, CUDA), machine learning,
NLP, Agentic-AI and LLM applications as well as deploying scalable solutions (apps) on-prem and in the cloud.

I can be reached through: manuelbomi@yahoo.com

Websites (professional):  http://emmanueloyekanlu.com/
Websites (application):  https://app.emmanueloyekanluprojects.com/
Publications:  https://scholar.google.com/citations?user=S-jTMfkAAAAJ&hl=en
LinkedIn:  https://www.linkedin.com/in/emmanuel-oyekanlu-6ba98616
Github:  https://github.com/manuelbomi

```
[![Icons](https://skillicons.dev/icons?i=aws,azure,gcp,scala,mongodb,redis,cassandra,kafka,anaconda,matlab,nodejs,django,py,c,anaconda,git,github,mysql,docker,kubernetes&theme=dark)](https://skillicons.dev)
