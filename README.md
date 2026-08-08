# AI Travel Planner with Multi-Agent Architecture

An AI-powered travel planning system that leverages a **multi-agent architecture** to coordinate trip planning through specialized AI agents. The application demonstrates agent-to-agent (A2A) communication, where a root agent orchestrates multiple domain-specific agents to generate comprehensive travel recommendations.

---

## Project Overview

This project simulates an intelligent travel assistant capable of coordinating multiple AI agents to answer complex travel planning requests.

Instead of relying on a single monolithic agent, the system delegates tasks to specialized agents responsible for:

- ✈️ Flight recommendations
- 🏨 Hotel recommendations
- 🌤️ Weather forecasts
- 🗺️ Tourist attractions

Each agent focuses on a specific domain and communicates through the **Agent-to-Agent (A2A) protocol**, allowing the root agent to aggregate results into a unified travel itinerary.

---

## Features

### Flight Planning

- Search flights between cities
- Retrieve flight information from a mock dataset
- Return flight options based on user requests

---

### Hotel Recommendations

- Recommend hotels based on destination
- Search city-specific hotel data
- Return hotel availability and pricing

---

### Tourist Attractions

- Suggest popular attractions
- Recommend sightseeing locations
- Provide destination-specific recommendations

---

### Weather Forecast

- Retrieve real-time weather forecasts
- Integrate with the OpenWeatherMap API
- Include weather information in travel planning

---

### Multi-Agent Coordination

Rather than solving every task independently, the application demonstrates:

- Root agent orchestration
- Agent-to-Agent communication
- Task delegation
- Response aggregation
- Modular AI architecture

---

# System Architecture

```
                    User Request
                          │
                          ▼
                    Root AI Agent
                          │
      ┌───────────────────┼────────────────────┐
      │                   │                    │
      ▼                   ▼                    ▼
 Flight Agent        Hotel Agent       Attraction Agent
      │                   │                    │
      └──────────────┬────┴──────────────┬─────┘
                     │                   │
                     ▼                   ▼
               Weather Agent      External API
                     │
                     ▼
             Final Travel Plan
```

---

# Project Structure

```
travel-planner/
│
├── agent.py                 # Root orchestration agent
├── cli.py                   # Command-line interface
│
├── agents/
│   ├── weather_agent/
│   │   ├── agent.py
│   │   ├── agent.json
│   │   └── mock_weather.json
│   │
│   ├── flight_agent/
│   ├── hotel_agent/
│   └── attraction_agent/
│
├── flights_dataset.json
├── mock_hotels.json
├── .env
│
└── README.md
```

---

# Workflow

1. User submits a travel request.

2. The Root Agent analyzes the request.

3. Tasks are delegated to specialized agents.

4. Individual agents process their domain-specific responsibilities.

5. Results are returned to the Root Agent.

6. The Root Agent combines responses into a complete travel itinerary.

---

# Technologies

| Technology | Purpose |
|------------|---------|
| Python | Application Development |
| Google ADK | Multi-Agent Framework |
| A2A Protocol | Agent Communication |
| OpenWeatherMap API | Weather Forecast |
| JSON | Mock Data Storage |
| dotenv | Environment Configuration |

---

# AI Concepts Demonstrated

This project showcases several modern AI engineering concepts:

- Multi-Agent Systems
- Agent Orchestration
- Agent-to-Agent Communication (A2A)
- Tool Calling
- Modular AI Design
- API Integration
- Intelligent Task Routing

---

# Skills Demonstrated

- AI Agent Development
- Multi-Agent Architecture
- Python Development
- API Integration
- Prompt Orchestration
- Software Design
- JSON Data Processing
- Command-Line Applications

---

# Running the Project

Clone the repository:

```bash
git clone https://github.com/yourusername/ai-travel-planner.git
cd ai-travel-planner
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Configure your environment variables:

```bash
OPENWEATHER_API_KEY=YOUR_API_KEY
```

Run the application:

```bash
python cli.py
```

---

# Example Request

```
Plan a 5-day trip to Seattle.

Include:

- Flight options
- Hotel recommendations
- Tourist attractions
- Weather forecast
```

Example response:

```
Destination: Seattle

Flight:
United Airlines
Non-stop
$298

Hotel:
Downtown Seattle Hotel
4.6 ★

Weather:
High: 72°F
Low: 58°F
Partly Cloudy

Top Attractions:
• Pike Place Market
• Space Needle
• Museum of Pop Culture
• Kerry Park
```

---

# Future Improvements

- Real-time flight search APIs
- Google Maps integration
- Restaurant recommendation agent
- Budget optimization agent
- Calendar integration
- Memory-enabled travel assistant
- LLM-powered itinerary generation
- Streamlit or React web interface

---

# Learning Outcomes

This project demonstrates how a multi-agent AI system can coordinate specialized agents to solve complex user requests through intelligent task delegation and communication. It highlights modern AI application design patterns including orchestration, modularity, and external tool integration, providing a foundation for building scalable agentic AI applications.
