# 🏃 Trail Running AI Agent — n8n Workflow

An AI-powered agent built with n8n that automatically decides whether you should go for a trail run today — and recommends the best trail based on real-time weather, air quality, and your schedule.

---

## 🤖 What It Does

Every day, this agent automatically:

1. **Checks your Google Calendar** — looks for a "Trail Run" event scheduled today
2. **Gets real-time weather** — fetches current temperature and conditions via OpenWeatherMap
3. **Checks air quality** — fetches PM2.5-based AQI for your city
4. **Reads your trail list** — pulls trail data from Google Sheets
5. **Makes a smart decision** — picks the best trail based on weather and shade level
6. **Sends you an email** — delivers a personalized recommendation via Gmail

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| [n8n](https://n8n.io) | Workflow automation platform |
| [Groq](https://groq.com) + LLaMA 3.3 | AI model (free) |
| [OpenWeatherMap API](https://openweathermap.org/api) | Real-time weather & air quality |
| Google Calendar | Check if a trail run is scheduled |
| Google Sheets | Store the list of trails |
| Gmail | Send the daily recommendation |

---


## 📧 Example Output

```
Subject: 🏃 Trail Run Recommendation for Today

Weather: 63°F, Clear sky
Air Quality: Moderate
Recommended Trail: Lower Falls via Bell Canyon
Distance: 4.8 miles
Elevation: 1515 feet
Estimated Time: 1h 20m
Shade Level: Some Shade
Reason: This trail fits your schedule and matches today's weather conditions.
```

---





---

## 🙌 Built By

**Roudeyna Bouznif** — Computer Science Engineering Student | AI & ML Enthusiast  
[LinkedIn](https://www.linkedin.com/in/roudeyna-bouznif-31115a316/) • École Nationale d'Ingénieurs de Carthage
