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

#### Go back to ur n8n and copy your OAuth Redirect URL
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/a645e11a-b270-42a4-b540-cd25910d6474" />

---

#### Paste it on the GCP Authorized URI and click on create
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/96d94078-23e1-4ead-81bf-2a793d3bcd5a" />

---

#### Now, copy the client ID it gave you
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/267eedda-6fbe-42c2-a769-48848513550e" />

---

#### Paste it onto client ID on your n8n
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/9dfb953a-b371-42bf-ac54-a3f89d05857a" />

---

#### Now click Done on your GCP
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/07c3bf9d-ba55-4f6b-8863-dd37079d2755" />

---

####  Go to credentials on your GCP
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/dbbd3a1b-b11e-49d8-8b18-2e95a164966f" />

---

####  Click the Edit OAuth client button
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/80783532-7c1c-4823-b38b-52a4813cc21e" />

---

#### Copy the client secret
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/3f3a4eab-176c-4d67-8316-b932d282c41e" />

---

#### Put it under secrets in your n8n workflow
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/ccb22fc2-e22b-4be2-a794-0ad69bfc99e1" />

---

#### Now, click on sign in with Google and select your Google account
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/a2e5af16-3b20-4d95-a2d2-1310d9f1f3dd" />

---

#### Some error block
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/19e06206-6b73-4024-b5db-71bbd01d274e" />

---

#### Under the test users section, click add user
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/9f704b83-81f5-4f36-9c99-10967ba01006" />

---

#### It will run through some housekeeping details
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/623bcda7-8f12-44aa-bfc8-3eb5247c93bc" />

---

#### You will now see connection successfull

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/ca4da432-8e33-496d-a27a-ecfc06493326" />

---

####  You will also see account connected on your n8n
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/5f1c8d27-959e-4c32-8d9c-debd31819297" />

---

#### You will now see that you can connect to your google calendar thru OAuth2
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/07baf221-2c4a-41f6-a386-6fe9b6ab46a5" />

---

#### Select Tool Description Description Resources Operations Calendar as shown
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/8bfa10f8-acdf-4faf-906e-fcffedd4e5b2" />

---

#### For the start and end date, hover on the link to include an expression
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/8b832729-d4ad-46be-88d1-d7ee7bb20af2" />

---

#### Include the start end data rage expression as shown
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/174ec36c-9e37-4ae5-93dd-40b4b2a269f6" />

---

####  Under Add field include Summmary or any other details that you want such as the number of guests
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/b169e11a-af40-4d6f-a596-605565656eba" />

---

#### You can also add a description field under expression
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/c3d7d1ae-d634-436e-99f5-073a1d8a138b" />

---

#### Click back to canvas
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/1635b8f5-35cf-4ef5-8355-bc5577e293f3" />

---

#### The calendar agent in its current state
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/86a4eb66-6f96-490a-8ea5-51f667d8f54a" />

---

####  The previous calendar can only add event to our calendar. Click on the plus button again and add another calendar tool that can see what is happening on our calendar

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/dafb828d-912f-47e9-b909-4fe28ce3cdc6" />

---

#### Set the tool description resources operations and calendar to your personal calendar
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/fb06e183-3066-4086-bcd9-46355b9d2b9f" />

---

#### Set the tool description to manually and the description to searching for availanble time slot as shown
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/362b3eeb-c505-4f27-895f-4083fd256880" />

---

#### Click back to canvas
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/31d3c905-d8e3-4bb0-90bc-a31193841e69" />

---

#### The current Agent

<img width="790" height="382" alt="Image" src="https://github.com/user-attachments/assets/3390260f-535c-4a03-8336-e26269757c7a" />

---

####  To add prompt to the AI Agent, double click on it and select System Messaging

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/d1984687-370e-46aa-8bb5-c55d45c62d05" />

---

#### Prompt design

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/b4704bb0-e674-4837-bb5f-a7904623c70e" />

---

#### The current Agent 
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/89f14b0b-baf5-42cc-b74c-30817bae0231" />

---

#### Test the agent. No available time slot for the rest of the month
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/15c63b3e-d18f-4aa8-993c-df1eea1bef8f" />

---

#### Error source, it searched my calendar for 2023 time range
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/ca26c479-2fa4-47c8-9c52-0ec6bfeb1f22" />

---

#### Flip to expressions to add today's date in Java format and click on the learn more tab
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/8fa2f5e7-6e46-4e64-b13b-b20c3a88edd5" />

---

#### The learn more tab will bring you here. Copy everything and put into ChatGPT with more instructions to obtain the appropriate date format
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/6d9d5705-8960-48e3-997f-55aafd8fb080" />

---

#### Chatgtp query
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/f669f53c-f8de-4b72-80f1-aeb5b371ccec" />

---

#### Inputting the expression on the AI Agent shows that the correct date and time is being pulled

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/8fc5a5a8-5a57-47e3-8ae4-6519e3f0f4d9" />

---

#### Conversationally try again! Still no output
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/b21ae347-d248-4a23-9304-8ba5ece413d5" />

---

####  That is even when the right date on the calendar is being pulled
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/7324fc77-801d-452d-8734-8c3ab07873cf" />

----

#### Click on Availability for Google Calendars and click on Add Options and select Output Format an dTime Zone

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/2c30f454-b8d7-4017-9ff9-e74c62fa28de" />

---

####  Select New York EST for the Time Zone
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/547ae4b1-9878-43ca-8931-9823ccffaaf1" />

---


#### Raw output format 

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/1c05a1d8-0000-425a-8f2a-6d9eecadc226" />

---

####  Another conversational query and the Agent can now get all my available time slots
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/8485d753-4708-4a1d-9bde-f5185bb8c5ee" />

---

#### All time slot obtained
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/fb585085-c449-495a-aac8-ff4d9e33ed90" />

---

#### Agents final look
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/06b8ccae-9012-485c-acbc-9369e0f752d9" />

---

#### Rename the agent node as Create Event
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/8a1482d0-72ad-479b-8719-2f16267e04cb" />

---

####  Rename another node to search available dates
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/44af0c11-4793-4273-aefc-fb81648744e8" />

---

####  Now schedule a meeting on my calendar with specific date and time

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/0c6b8462-0041-47af-be84-bcf209ea0232" />

---

#### Click to see the scheduled event 

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/c194b2fb-ab3a-4a1c-bc90-a883655e99d8" />

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
