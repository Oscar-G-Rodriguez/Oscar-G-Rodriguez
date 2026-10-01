# Oscar Rodriguez

Hi, I'm Oscar. I'm a freshman studying computer science at the University of Florida. I'm interested in machine learning and AI, and I enjoy working with data. Most of my projects bring models and data into applications that someone can use and explore.

## Projects

### [SeekR](https://github.com/Hemanka/Shellhacks-X)

SeekR is the project I feel best represents my interests right now. I worked on it with a team to help blind users find objects and navigate a room using a phone camera and voice guidance. We chose vision models so the person navigating can use a phone camera without having to carry or set up a separate sensor device. The phone captures the view and speaks the guidance, while a Windows dashboard runs the analysis.

A user says what they're looking for, and Gemini examines the camera view to identify the target and its position. A segmentation model marks likely walkable areas and obstacles. SeekR uses those model outputs to choose a short movement instruction, which the phone speaks before sending a new view for the next step. During testing, I used SeekR to navigate classrooms and living rooms, move around obstacles, and reach the objects I was looking for.

### [ROMULUS](https://github.com/Oscar-G-Rodriguez/ROMULUS)

ROMULUS is a local financial research app I built to compare trading strategies over time. Each strategy runs on the same point-in-time data in its own simulated portfolio, which makes it possible to compare their decisions and results side by side. ROMULUS considers returns, risk-adjusted performance, and the current market regime when choosing a strategy for a separate portfolio to follow. The best strategy isn't necessarily the one with the highest profit; I wanted the comparison to account for the risks taken to get there.

The app also includes ML forecasts for returns and volatility. Its desktop interface lets me inspect the forecasts, strategy rankings, portfolio changes, and the evidence behind each selection. Building that decision trail was an important part of the project for me because it lets me follow how a result was reached. The [validation report](https://github.com/Oscar-G-Rodriguez/ROMULUS/blob/main/VALIDATION_REPORT.md) shows how I checked the backtester and its model outputs.

### [Florida Policy Advisor](https://github.com/Oscar-G-Rodriguez/florida_policy_advisor)

Florida Policy Advisor is a local app I built to help someone explore Florida labor, housing, and fiscal indicators. It brings data from sources such as BLS, Census, and FRED into one place, checks each refresh for quality and coverage, and keeps the source and retrieval date attached to the results. The app also compares forecasting baselines over historical data and lets someone explore policy options using visible weights.

I wanted the analysis to be something a person could follow for themselves. Someone using the app can move from a result back to the underlying data and see how a comparison was produced. That work gave me more experience with the full path from collecting data to presenting an answer. The project's [evidence and checks](https://github.com/Oscar-G-Rodriguez/florida_policy_advisor/blob/main/portfolio_evidence/README.md) are documented in its repository.

## Skills and direction

Across these projects, I've used Python to prepare and check data, integrate models into applications, and evaluate predictions on time-ordered data. I've also worked on the parts around a model: interfaces, tests, and records that make its output easier to understand. I enjoy that whole process, especially the work with data and ML.

Moving forward, I'd like to work on frontier models in any way I can. I want to keep building useful applications while learning more about how models are trained, evaluated, and improved.

