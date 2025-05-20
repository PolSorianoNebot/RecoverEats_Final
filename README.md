# README

## **Description**
Recover Eats is a health-monitoring web application that connects WHOOP fitness
data with tailored meal recommendations. By integrating recovery metrics, workout
data, sleep tracking, and nutritional APIs, Recover Eats provides users with
personalized diet suggestions that align with their physical condition and fitness
goals.

### Business Solution
In the growing health and fitness market, individuals use wearables like WHOOP to
monitor sleep, recovery, heart rate, and strain. However, this raw data is often
underutilized, lacking actionable feedback especially in nutrition.

#### Recover Eats bridges this gap by:
- Interpreting WHOOP metrics to provide tailored dietary advice.
- Encouraging data-driven meal planning.
- Delivering recipe suggestions and ingredients via email for easy action.
- Supporting fitness goals such as bulking, cutting, or maintaining.
- “Bridging the Gap Between Fitness Recovery and Personalized Nutrition.”

### App Features
Intelligent meal suggestions based on recovery score and workout intensity.

- Diet goal customization: bulk, cut, or maintain.
- Integration of WHOOP data: sleep, strain, body measurements.
- Email delivery of suggested recipes.
- Secure OAuth-based login.


## API Endpoints & Their Utility
### 🧬 **WHOOP API**
* 🔐 **`/oauth/oauth2/auth`**
Initiates the OAuth flow. It redirects the user to sign in and authorize access to
WHOOP data.
* 🔑 **`/oauth/oauth2/token`**
Exchanges the authorization code for an access token needed to fetch data.
* 💚 **`/developer/v1/recovery?limit=25`**
Retrieves recovery data, including recovery score, resting heart rate, and skin
temperature.
* 💪 **`/developer/v1/cycle?limit=7`**
Gets recent strain/cycle metrics, including strain score and heart rate during daily
activity
* 🏋 **`/developer/v1/activity/workout?limit=25`**
Returns detailed information on recent workouts tracked by WHOOP.
* 😴 **`/developer/v1/activity/sleep?limit=7`**
Provides sleep data including performance, efficiency, and consistency.
* 📏 **`/developer/v1/user/measurement/body`**
Delivers body measurements like height and weight.
* 🙋 **`/developer/v1/user/profile/basic`**
Basic user profile details, such as first name and last name.

### 🍽 **TheMealDB API**
* 📂 **`/filter.php?c={category}`**
Fetches a list of meals within a specific category (e.g., Beef, Vegetarian).
* 📄 **`/lookup.php?i={meal_id}`**
Returns detailed information about a specific meal, including ingredients and
instructions.


### Current Limitations
- No token refresh for WHOOP login (requires manual re-login).
- No error handling for missing API data.
- No persistent storage for user sessions or preferences.


### Future Improvements
- Add daily/weekly summary email scheduling.
- Enhance visuals with Plotly or Altair.
- Provide AI-based recommendations (e.g., trends in sleep or recovery).
- Support multi-language UI.
- Add user account system for persistence.


### Contact Us
For any questions, feature requests, or collaboration ideas, feel free to reach out:
✉️ recover.eats.team@gmail.com

GitHub: https://github.com/PolSorianoNebot/RecoverEats_Final
