# 🌟 Daily Quotes Automation (n8n + Docker)

This project demonstrates an **automation workflow** built using [n8n](https://n8n.io/).  
The workflow fetches random quotes from an API, filters them based on conditions, and reformats the results into a clean, readable format.

---

## 📌 Features
- ✅ Fetches random quotes from the [Quotable API](https://api.quotable.io)  
- ✅ Filters quotes based on conditions (e.g., length, tags)  
- ✅ Reformats quotes into `"Quote content" - Author`  
- ✅ Runs inside **n8n**, powered by **Docker**  
- ✅ Ready to extend for email, Slack, or WhatsApp delivery  

---

## 🛠️ Tools & Technologies
- [n8n](https://n8n.io/) – Automation tool  
- [Docker](https://www.docker.com/) – Containerization  
- [Quotable API](https://api.quotable.io) – Source of quotes  

---

## ⚙️ Workflow Steps
1. **Trigger Node (Manual Execute)**  
   - Starts the workflow manually.  

2. **HTTP Request Node**  
   - Method: `GET`  
   - URL: `https://api.quotable.io/quotes/random?limit=5`  
   - Fetches 5 random quotes.  

3. **Filter Node**  
   - Keeps only the quotes matching certain conditions (e.g., length < 150).  

4. **Edit Fields (Set Node)**  
   - Reformats output into the form:  
     ```
     "Quote content" - Author
     ```

5. **Execution & Output**  
   - Final formatted quotes are generated and displayed.  

---

## 📂 Project Structure
