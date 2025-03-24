# 🛠️ **Agentic AI Project: AI vs ML vs DL vs Data Science**

## 🚀 **Project Overview**
This project is an **Agentic AI system** built using the **`crewai`** library. It automates the process of **researching and writing blog content** on the topic:  
**"AI vs ML vs DL vs Data Science"**. 

The project showcases the use of **multiple autonomous agents** working together in a crew, efficiently performing sequential tasks to deliver a high-quality blog article.

---

## ⚙️ **Technologies Used**
- **Python** 🐍
- **CrewAI** 🚀 (Autonomous agent framework)
- **Agent-based Task Execution**
- **Memory & Caching** for improved performance

---

## 🔥 **Project Structure**
The project consists of the following core components:

### 1. **Agents**
- `blog_researcher`:  
  ✅ Responsible for researching the given topic.  
- `blog_writer`:  
  📝 Uses the research data to write a detailed blog article.

### 2. **Tasks**
- `research_task`:  
  🔍 Task assigned to the **`blog_researcher`** for information gathering.  
- `write_task`:  
  🖊️ Task assigned to the **`blog_writer`** to create the blog content based on the research.

### 3. **Crew Formation**
- The agents are assembled into a **crew** using the `Crew()` class.  
- The **task execution** follows a **sequential process**.  
- Features like **memory** and **caching** are enabled for improved efficiency and context retention.  
- `max_rpm=100`: Limits the rate of requests per minute.  
- `share_crew=True`: Allows the agents to share information.

---

## ⚙️ **Code Execution Flow**
1. **Initialize the Crew:**  
   The `Crew()` object is instantiated with the agents and tasks, along with memory and caching configurations.

2. **Kickoff the Execution:**  
   The process starts with the `crew.kickoff()` method, which takes the **`inputs`** parameter with the blog topic:
   ```python
   result = crew.kickoff(inputs={'topic': 'AI VS ML VS DL vs Data Science'})
