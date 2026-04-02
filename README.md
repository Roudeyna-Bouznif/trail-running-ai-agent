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

## 📊 Google Sheets Structure

Your sheet should have these columns:

| Name | Miles | Elevation | Estimated Time | Shade Level |
|------|-------|-----------|----------------|-------------|
| Trail Name | 5.4 | 1023 | 1h 20m | Shady / Some Shade / Exposed |

---

## ⚙️ How to Set It Up

### 1. Clone the workflow
- Download `workflow.json` from this repo
- Import it into your n8n instance: **Menu → Import from file**

### 2. Configure credentials
You need to add the following credentials in n8n:

- **Groq API Key** — get it free at [console.groq.com](https://console.groq.com)
- **OpenWeatherMap API Key** — get it free at [openweathermap.org](https://openweathermap.org/api)
- **Google OAuth2** — for Gmail and Google Calendar
- **Google Sheets OAuth2** — for reading your trail list

### 3. Set your city
In the **OpenWeatherMap** node, set the **City** field to your city (e.g. `Tunis`).

### 4. Set up your Google Sheet
Create a Google Sheet with the structure above and link it in the **Google Sheets** node.

### 5. Schedule it
The **Schedule Trigger** runs the workflow automatically every day. You can configure the time in the trigger settings.

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

## ⚠️ Important Notes

- This workflow uses **free tiers only** — no paid subscriptions needed
- Groq has a rate limit of ~30 requests/minute on the free tier
- OpenWeatherMap free tier allows 1,000 API calls/day
- Never commit your API keys to GitHub — n8n does not export credentials in the JSON file

---

## 📁 Files

```
├── README.md          # This file
├── workflow.json      # n8n workflow (export from n8n)
└── trails.xlsx        # Sample trail list for Google Sheets
```

---

## 🙌 Built By

**Roudeyna Bouznif** — Computer Science Engineering Student | AI & ML Enthusiast  
[LinkedIn](https://www.linkedin.com/in/roudeyna-bouznif-31115a316/) • École Nationale d'Ingénieurs de Carthage
