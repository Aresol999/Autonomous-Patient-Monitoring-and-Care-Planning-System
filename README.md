# Autonomous Patient Monitoring and Care Planning System  
### (A2A and MCP Based Multi-Agent Distributed System)

## Overview

This project is a multi-agent autonomous healthcare monitoring system that dynamically analyzes patient vitals and generates adaptive care plans.

It uses:
- A2A (Agent-to-Agent communication) for messaging
- MCP (Model Context Protocol) for dynamic tool discovery
- LLM-based orchestration for non-hardcoded execution

---

## Key Features

- Dynamic workflow planning (no hardcoding)
- Multi-agent architecture
- Event-driven communication
- Hybrid intelligence (LLM + rule-based safety)
- Real-time alerts to caregivers and doctors
- Fault-tolerant design with fallbacks

---

## How It Works

1. Monitoring Agent streams patient vitals  
2. Orchestrator dynamically decides execution plan using LLM  
3. Analysis Agent evaluates risk  
4. CarePlan Agent generates care instructions  
5. A2A Bus broadcasts alerts  
6. Doctor and Caregiver agents respond  

---

## Tech Stack

Backend:
- Python
- FastAPI
- AsyncIO

AI / Agents:
- Model Context Protocol (MCP)
- Google Gemini API

Communication:
- Custom A2A message bus

---

## Core Concepts

- Distributed multi-agent systems  
- Dynamic tool discovery (MCP)  
- Autonomous task planning  
- Event-driven architecture  
- Hybrid AI (rules + LLM)  

---

## How to Run

1. Clone repo:
   git clone <your-repo-link>  
   cd <repo-name>

2. Install dependencies:
   pip install -r requirements.txt

3. Add environment variables (.env):
   GOOGLE_API_KEY=your_api_key_here

4. Run system:
   python run_all.py

5. (Optional) Run dashboard:
   streamlit run dashboard.py

---

## Example Output

[1. Sensed Vitals] {'heart_rate': 110, 'spo2': 82}  
[2. Plan] analyze_vitals -> plan  
[3. Executing analyze_vitals] → {'risk': 'CRITICAL'}  
[3. Executing plan] → {'action': 'CRITICAL'}  
[ALERT] Sent CRITICAL to A2A bus  

---

## Safety Features

- Hard safety rules (e.g., low SpO2 → CRITICAL)
- LLM fallback handling
- Guardrails against unsafe outputs
- Resilient communication

---

## Limitations

- In-memory message bus (not production-grade)
- No persistent database
- Simulated vitals (no real IoT)
- No authentication/security

---

## Future Improvements

- Replace A2A bus with Kafka / Redis Streams  
- Add database (PostgreSQL / MongoDB)  
- Introduce Redis caching  
- Enable horizontal scaling  
- Add observability (metrics/logging)  
- Integrate real IoT devices  

---

## Use Cases

- Smart hospitals  
- Remote patient monitoring  
- ICU alert systems  
- Autonomous healthcare workflows  

---

## 👨‍💻 Author

Arnav Kadyan  
B.Tech CSE, VIT Vellore  

GitHub: https://github.com/Aresol999  
LinkedIn: https://www.linkedin.com/in/arnav-kadyan-32366928a  
