# Exno.7-Develop a prompt-based application tailored to their personal needs, fostering creativity and practical problem-solving skills while leveraging the capabilities of large language models.

### Date: 
### Register no: 212222240052

# Aim: To develop a prompt-based application using ChatGPT - To demonstrate how to create a prompt-based application to organize daily tasks, showing the progression from simple to more advanced prompt designs and their corresponding outputs.

## AI Tools Required:

## AI Tools Required  


- ChatGPT (OpenAI LLM) – for natural language understanding and response generation. 


# Explanation: 


Prompt:


"Design a personal productivity assistant that can help manage daily tasks, schedule reminders, suggest wellness tips, and answer general queries. The assistant should interact using natural language and be adaptable to the user’s changing preferences over time."


---

## Procedure  

1. **Define core requirements**  
   - Daily task manager  
   - Smart scheduler  
   - Wellness suggestions  
   - General query answering  
   - Adaptability to user preferences  

2. **Construct prompts for each feature**  
   - **Task Manager Prompt:**  
     ```
     Add a task: Remind me to call mom at 6 PM and categorize it as high priority.
     ```
   - **Scheduler Prompt:**  
     ```
     Schedule a meeting with John tomorrow at 4 PM and warn me if it clashes with another event.
     ```
   - **Wellness Prompt:**  
     ```
     Suggest a short break activity based on my preference for light exercises.
     ```
   - **Query Prompt:**  
     ```
     What’s the weather like tomorrow?
     ```

3. **Simulate natural interaction**  
   - Build a simple CLI or chatbot interface where the user types commands.  
   - ChatGPT responds in conversational style.  

4. **Collect feedback/adapt responses**  
   - Store user preferences (e.g., prefers yoga over jogging).  
   - Modify future responses accordingly.  

5. **(Optional) Add memory simulation**  
   - Maintain a small JSON file/dictionary for user tasks and preferences.  

---
## Personal Productivity Assistant Features:
1. Daily Task Manager:
o Accept tasks via natural language (e.g., "Remind me to call mom at 6 PM").
o Organize tasks by priority and deadline.
o Provide daily summaries and pending items.
2. Smart Scheduler:
o Schedule events and set reminders using contextual understanding.
o Notify user of overlapping appointments or free time slots.
3. Wellness Tips Generator:
o Suggest daily wellness advice (hydration, exercise, screen-time breaks).
o Adapt suggestions based on past user preferences and responses.


## Expected Output  


## Sample Python Code (CLI Simulation)  

```python
import datetime

tasks = []
preferences = {"wellness": "exercise"}

def add_task(task, time=None, priority="Normal"):
    tasks.append({"task": task, "time": time, "priority": priority})
    print(f"✅ Task added: '{task}' at {time}, Priority: {priority}")

def show_tasks():
    if not tasks:
        print("📌 No tasks scheduled.")
    else:
        print("\n📅 Your Task List:")
        for i, t in enumerate(tasks, 1):
            print(f"{i}. {t['task']} - {t['time']} - Priority: {t['priority']}")

def wellness_tip():
    if preferences["wellness"] == "exercise":
        print("💡 Wellness Tip: Take a 5-minute walk to stretch your legs.")
    elif preferences["wellness"] == "hydration":
        print("💡 Wellness Tip: Drink a glass of water to stay refreshed.")
    else:
        print("💡 Wellness Tip: Take a deep breath and relax your eyes.")

def query_handler(query):
    if "weather" in query.lower():
        print("🌤️ The weather tomorrow is expected to be sunny with mild temperatures.")
    elif "time" in query.lower():
        now = datetime.datetime.now()
        print(f"⏰ Current time is {now.strftime('%H:%M:%S')}")
    else:
        print("🤖 I'm not sure, but I can try to help with more details!")

def assistant():
    print("🤖 Welcome to your Personal Productivity Assistant!")
    print("Type 'help' to see options.\n")

    while True:
        user_input = input("👉 Enter command: ")

        if user_input.lower() == "exit":
            print("👋 Goodbye! Stay productive!")
            break
        elif user_input.lower() == "help":
            print("\nAvailable Commands:")
            print(" add - Add a new task")
            print(" show - Show all tasks")
            print(" wellness - Get a wellness tip")
            print(" query - Ask a general question")
            print(" exit - Quit assistant\n")
        elif user_input.lower() == "add":
            task = input("Enter task: ")
            time = input("Enter time (e.g., 6 PM): ")
            priority = input("Enter priority (High/Normal/Low): ")
            add_task(task, time, priority)
        elif user_input.lower() == "show":
            show_tasks()
        elif user_input.lower() == "wellness":
            wellness_tip()
        elif user_input.lower() == "query":
            query = input("Ask your question: ")
            query_handler(query)
        else:
            print("⚠️ Unknown command. Type 'help' to see options.")

if __name__ == "__main__":
    assistant()
```

## EXPECTED OUTPUT:
```
🤖 Welcome to your Personal Productivity Assistant!
Type 'help' to see options.

👉 Enter command: add
Enter task: Call mom
Enter time (e.g., 6 PM): 6 PM
Enter priority (High/Normal/Low): High
✅ Task added: 'Call mom' at 6 PM, Priority: High

👉 Enter command: show
📅 Your Task List:
1. Call mom - 6 PM - Priority: High

👉 Enter command: wellness
💡 Wellness Tip: Take a 5-minute walk to stretch your legs.

👉 Enter command: query
Ask your question: What is the time now?
⏰ Current time is 15:42:10

👉 Enter command: exit
👋 Goodbye! Stay productive!

```
# Output (Example Response by LLM):

<img width="630" height="495" alt="image" src="https://github.com/user-attachments/assets/3330ac52-9833-4793-93b1-19f68bac40e2" />




# Result: 
The lab exercise resulted in the creation of a prototype concept for a personal assistant powered by large language models. Students were able to:
 Understand how to tailor LLM prompts to real-life applications.
 Foster creativity by designing features suited to their personal or academic lives.
 Learn prompt engineering techniques for optimal interaction with AI tools.
 Experience the versatility and utility of generative AI in solving everyday problems.
