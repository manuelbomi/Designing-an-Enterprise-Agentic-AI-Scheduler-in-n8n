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
#### Serch for Google Calendar under Tools
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/9a0eac1e-9461-4746-829e-fba3d60ba61a" />

----

####  Select credentials and create new credentials
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/dfc23e45-f446-4f9f-ba32-6f7289fe83f8" />

---
#### Create new credential

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/4e3ea6eb-c2f1-4896-908c-b340f304740e" />

---

#### Click inside Client ID and click on Open Docs

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/f783f56c-689d-4f95-825a-4e312421179a" />

---

#### Ff you decide to use the OAuth method, follow the instructions on Google Docs by opening Google Console and create a project on Google Console


<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/bc73a87c-1149-4c81-ae39-d81a0106dfaa" />

---

#### On Google Cloud Console go to your console

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/7de85d68-0283-432e-8fe0-588202a3c80a" />
---
#### Go to your GCP console
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/4ca63dec-1e0c-473d-a40c-18ba5df6bb92" />






<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/b010fde2-ae3e-4608-b10f-b62191944acf" />
















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
