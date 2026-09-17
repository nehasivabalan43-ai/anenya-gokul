# anenya-gokul
calorie count AI
Build a complete, functional, modern AI-powered web application called "CalorieCount AI".
APP PURPOSE
CalorieCount AI helps users estimate the calories and nutritional values of a meal.
The user enters the ingredients in a meal along with their quantity and unit. The application uses the Gemini API to analyze the ingredients and returns an estimated calorie count and nutritional breakdown.
The application must actually work. Do not create a static mockup or placeholder buttons.
DESIGN
Create a premium, clean and minimal health-and-food themed interface.
Use:
White/light background
Green as the primary accent color
Dark text
Soft shadows
Rounded cards
Modern typography
Clean food/nutrition icons
Smooth but subtle animations
Responsive design for desktop, tablet and mobile
Plenty of whitespace
Professional startup-app appearance
The application should look like a real consumer product, not a basic student project.
HOME PAGE
At the top display:
CalorieCount AI
Tagline:
"Know what you eat."
Description:
"Enter your ingredients and quantities to get an AI-powered estimate of calories and nutrition."
Create a prominent meal analysis card.
Include:
Meal Name
A text input:
"e.g. Chicken Rice Lunch"
Ingredients
Create a dynamic ingredient list.
Each row should contain:
Ingredient name
Quantity
Unit dropdown
Units should include:
grams
kilograms
millilitres
litres
piece
teaspoon
tablespoon
cup
Example:
Ingredient: Rice
Quantity: 150
Unit: grams
Allow users to click:
+ Add Ingredient
to add additional ingredients.
Each ingredient row should have a delete/remove button.
Add:
Clear All
and a prominent:
Analyze Meal
button.
AI FUNCTIONALITY
When the user clicks "Analyze Meal":
Validate that every ingredient has a name and quantity.
If information is missing, show a friendly validation message.
Send the ingredient list to Gemini through a secure server-side API call.
Ask Gemini to estimate the nutritional information for each ingredient based on the quantity provided.
Calculate the total nutritional values.
Return structured JSON rather than unstructured text.
The AI response should contain:
{
"mealName": "",
"ingredients": [
{
"name": "",
"quantity": 0,
"unit": "",
"calories": 0,
"protein": 0,
"carbohydrates": 0,
"fat": 0
}
],
"totalCalories": 0,
"totalProtein": 0,
"totalCarbohydrates": 0,
"totalFat": 0,
"assumptions": []
}
Do not expose the Gemini API key in frontend/client-side code.
Use the secure server-side environment/secrets mechanism provided by Google AI Studio.
IMPORTANT AI RULES
The AI must treat all nutritional values as estimates.
Do not present calorie values as medically or scientifically exact.
If the ingredient is ambiguous, ask the user for clarification.
For example, if the user enters "rice", the AI should consider whether the user means cooked or uncooked rice. If necessary, ask for clarification or clearly state the assumption used.
Consider:
ingredient quantity
unit
cooked/raw state when relevant
common preparation differences
Do not invent precise nutritional information when the input is too ambiguous.
Display this disclaimer with the results:
"Nutrition values are estimates and may vary depending on the ingredient, brand, preparation method and portion size."
RESULTS PAGE
After successful analysis, display a beautiful nutrition dashboard.
At the top:
Your Meal
[Meal Name]
Then create a large highlighted card:
TOTAL CALORIES
540 kcal
The number should dynamically come from the AI result.
Below it create three nutrition cards:
Protein
45 g
Carbohydrates
52 g
Fat
15 g
These values must be dynamically generated.
INGREDIENT BREAKDOWN
Create a table/card showing:
Ingredient | Quantity | Calories | Protein | Carbs | Fat
Example:
Rice | 150 g | 195 kcal | 4 g | 42 g | 0.5 g
Chicken | 100 g | 165 kcal | 31 g | 0 g | 3.6 g
Egg | 2 pieces | 140 kcal | 12 g | 1 g | 10 g
Do not hardcode these example values. They are only examples of the interface.
VISUALIZATION
Add a simple visual nutrition breakdown.
Create a clean chart showing the approximate contribution of:
Protein
Carbohydrates
Fat
Also show the calorie contribution of each ingredient using simple horizontal bars.
Keep the visualizations clean and readable.
LOADING STATE
When Gemini is analyzing the meal, display a professional loading state.
Show:
"Analyzing your meal..."
with a subtle animated loading indicator.
Do not freeze the interface.
ERROR HANDLING
Handle:
Empty ingredient list
Missing ingredient name
Missing quantity
Invalid quantity
API errors
Gemini errors
Network errors
Invalid AI response
Ambiguous ingredients
Show clear and friendly error messages.
Never show raw technical errors to the user unless necessary.
SAVE MEAL
Add a:
Save Meal
button.
For the first version, save meals using browser localStorage.
Do not require user login.
MEAL HISTORY
Create a separate History section/page.
Show previously saved meals.
Each history item should display:
Meal name
Date
Total calories
Protein
Carbohydrates
Fat
Allow the user to:
Open a previous meal
Delete a meal
Clear history
NAVIGATION
Create a simple navigation bar:
CalorieCount AI
Home
History
On mobile, make the navigation responsive.
EMPTY STATES
If there are no saved meals, display:
"No meals yet"
"Analyze your first meal to start building your nutrition history."
Include a button:
"Analyze a Meal"
ACCESSIBILITY
Make the application accessible.
Use:
Proper labels for inputs
Keyboard-friendly controls
Good contrast
Descriptive button labels
Responsive layouts
Accessible error messages
RESPONSIVE DESIGN
The application must work properly on:
Desktop
Laptop
Tablet
Mobile phone
On mobile, ingredient rows should stack vertically rather than becoming difficult to use horizontally.
TECHNOLOGY
Use a modern React-based web application.
Use the Gemini API for AI analysis.
Keep API credentials secure on the server side.
Use clean, modular components.
Do not put everything into one large component.
Create reusable components for:
Ingredient input
Ingredient list
Nutrition summary
Ingredient breakdown
Meal history
Loading state
Error state
DATA VALIDATION
Before sending data to Gemini:
Ensure ingredient names are not empty.
Ensure quantities are positive numbers.
Ensure units are valid.
Prevent analysis when there are no ingredients.
USER EXPERIENCE
The complete flow should be:
Home
→ Enter meal name
→ Add ingredients
→ Enter quantities
→ Click Analyze Meal
→ AI analyzes ingredients
→ Show loading state
→ Display calorie and nutrition results
→ User can save the meal
→ Meal appears in History
IMPORTANT
Build the application fully and make it functional.
Do not only generate a wireframe.
Do not use fake buttons.
Do not hardcode calorie results.
Do not use placeholder AI responses.
Connect the Analyze Meal functionality to Gemini.
Make sure the application can be run and tested in the Google AI Studio preview.
Before finishing, test the major user flow and fix any runtime errors.
The final result should feel like a polished AI nutrition tracking startup MVP called CalorieCount AI.
Gemini 3.8 Flash
Ran for 232s

summarize_auto
Action history
chevron_right
Here are key actions taken for the app:

edit
Edited 13 files
metadata.json
check_circle
index.html
check_circle
src/index.css
check_circle
package.json
check_circle
src/types.ts
check_circle
server.ts
check_circle
src/components/Navbar.tsx
check_circle
src/components/MealForm.tsx
check_circle
src/components/NutritionDashboard.tsx
check_circle
src/components/MealHistory.tsx
check_circle
src/components/LoadingIndicator.tsx
check_circle
src/components/ErrorAlert.tsx
check_circle
src/App.tsx
check_circle
build
Built
I have designed and implemented CalorieCount AI, a modern, health-and-food-themed web application powered by the Gemini API for nutritional and calorie estimation.
Key Features & Design Implementation
Health-Themed Visual Identity: Crafted with a clean white and soft-stone canvas, crisp emerald green accents (emerald-600), high-contrast slate typography (Plus Jakarta Sans and Outfit), and rounded containers with subtle shadows.
Dynamic Ingredient Builder:
Allows users to enter an optional meal title and dynamic ingredient rows with customizable quantities and supported measurement units (grams, kilograms, millilitres, litres, piece, teaspoon, tablespoon, cup).
Includes quick-start meal templates (Chicken Rice Lunch, Avocado Toast with Egg, Greek Yogurt Berry Bowl) for fast testing.
Controls for adding ingredients, per-row deletion, and a clear-all action.
Secure Server-Side Gemini Integration:
Built with Express and @google/genai on the backend (gemini-3.8-flash with resilient fallback routing), ensuring API keys are never exposed to the client.
Validates all input data server-side and queries Gemini for estimated calorie counts, macronutrients (Protein, Carbohydrates, Fat), and culinary preparation assumptions.
Nutrition Results Dashboard:
Highlighted Total Calories Card: Displays total meal calories prominently in high-contrast emerald.
Macronutrient Breakdown Cards: Individual metric cards for Protein, Carbohydrates, and Fat with energy percentages.
Interactive Visualizations: A stacked energy distribution chart and horizontal ingredient calorie contribution bars.
Ingredient Detail Table: Granular breakdown of each ingredient's calories and macros, with responsive card view on mobile and full data table on desktop.
Assumptions & Disclaimers: Clarifies preparation assumptions (e.g. cooked vs. raw states, lean cuts) and includes the required nutritional disclaimer.
Local Meal History:
Saved meals are stored in browser localStorage without requiring an account or login.
The History page allows users to view past meals, reopen meal details in the dashboard, search by keyword, and delete individual meals or clear history.
Loading & Error Handling:
Reassuring loading state with rotating analysis steps during AI processing.
Client and server-side validation preventing empty inputs, negative numbers, or unselected units with clear, friendly notifications.
flag
Checkpoint
dont add chicken everytime add only when the user gives
Gemini 3.8 Flash
Ran for 110s

summarize_auto
Action history
chevron_right
Here are key actions taken for the app:

edit
Edited 3 files
src/App.tsx
check_circle
server.ts
check_circle
src/components/MealForm.tsx
check_circle
build
Built
I have updated the application so that chicken is never automatically added or assumed:
Empty Initial State: The meal form now starts completely blank with no pre-filled chicken or default ingredients, allowing you to add only the ingredients you specify.
Strict Backend Ingredient Fidelity: Added strict constraints to the AI analysis prompt and system instructions prohibiting it from injecting, assuming, or adding chicken, meats, or any unmentioned items. The nutritional analysis now matches strictly 1-to-1 with the items you enter.
Cleaned Templates & Placeholders: Removed preset bias and updated form placeholders to neutral examples (e.g., Avocado Toast, Greek Yogurt, Oatmeal).
flag
Checkpoint
give me a voice over for this content
Gemini 3.8 Flash
Ran for 3s
Here are two voiceover scripts tailored for CalorieCount AI—one designed for a product demo / walkthrough video, and a shorter 30-second version perfect for social media or ads:
Option 1: Product Demo & Walkthrough (60 Seconds)
Tone: Warm, modern, crisp, and encouraging.
Background Music: Soft, upbeat acoustic/ambient electronic with light finger snaps.
[0:00 - 0:10] The Hook
"Ever look at your plate and wonder: what am I actually eating? Counting calories shouldn't feel like doing homework."
(Visual: User looking at food or opening CalorieCount AI on their phone)
[0:10 - 0:25] The Core Feature
"Meet CalorieCount AI — know what you eat in seconds. Simply type in what’s on your plate: cooked rice, sliced avocado, or morning oats. Select your exact portion size and tap Analyze Meal."
(Visual: User typing ingredients, selecting portions in grams or cups, and tapping the emerald button)
[0:25 - 0:45] The Results
"Instantly, Gemini AI calculates your total energy and gives you a clean macro breakdown — protein, carbs, and healthy fats. No mystery guesswork, and no ingredients added that you didn’t ask for. You get clear visual charts, ingredient-by-ingredient calories, and even cooking assumptions."
(Visual: Total calorie card popping up with 540 kcal, animated macro distribution bars, and ingredient table)
[0:45 - 1:00] Save & Call to Action
"Save your favorite meals to your personal history with a single tap, completely private on your device. Take control of your nutrition. Try CalorieCount AI today — know what you eat."
(Visual: Saving meal to History tab, clean logo screen with emerald accent)
Option 2: Short Social Reel / Promo (30 Seconds)
Tone: Fast-paced, punchy, and direct.
"What’s really in your meal?
With CalorieCount AI, you don’t need to guess.
Just list your ingredients, pick your portions, and let AI do the math.
In seconds, you get total calories, macro breakdowns, and a detailed nutrition dashboard tailored strictly to what you entered.
Track it. Save it. Own your health.
CalorieCount AI — Know what you eat."
(If you would also like an interactive Text-to-Speech (TTS) audio narration or audio playback button built directly inside the application to read the meal results aloud, just let me know!)
audio voice over for this app, a female voice
Gemini 3.8 Flash
Ran for 130s

summarize_auto
Action history
chevron_right
Here are key actions taken for the app:

edit
Edited 5 files
server.ts
check_circle
src/utils/audioPlayer.ts
check_circle
src/components/VoiceoverPlayer.tsx
check_circle
src/components/NutritionDashboard.tsx
check_circle
src/components/MealForm.tsx
check_circle
build
Built
I have added an interactive female audio voiceover to CalorieCount AI, powered directly by Gemini's speech generation API (gemini-3.1-flash-tts-preview using the female voice Kore):
What Was Built:
Female AI Voiceover Generator (/api/generate-voiceover):
Secure backend endpoint using @google/genai configured with the prebuilt female voice Kore.
Speaks with a friendly, warm, clear, and encouraging tone as a nutritional health guide.
Automatically synthesizes and streams high-fidelity 24kHz audio directly to the browser.
Interactive Audio Player Component (VoiceoverPlayer):
App Audio Walkthrough: Featured on the home page with a dedicated voiceover player card. Users can tap "Generate Voiceover" or "Play Voiceover" to listen to the audio walkthrough explaining how to list ingredients, set portions, and analyze calories.
Live Meal Breakdown Narration: Once a meal is analyzed, a dedicated narration player appears on the nutritional dashboard to read aloud the specific calorie total and protein, carbohydrate, and fat metrics in a clear female voice.
Complete with animated sound-wave indicator, progress scrubber, playback time display, play/pause controls, and a re-generation action.
flag
Checkpoint
a bit detailed voiceover
Gemini 3.8 Flash
Canceled

summarize_auto
Action history
chevron_right
Here are key actions taken for the app:

edit
Edited 4 files
src/components/VoiceoverPlayer.tsx
check_circle
src/components/MealForm.tsx
check_circle
src/components/NutritionDashboard.tsx
check_circle
server.ts
check_circle
build
Built
I have updated the application to provide a detailed female voiceover:
Enhancements Made:
Detailed Script & Walkthrough (Home Page):
Explains step-by-step how to enter ingredients, how portion sizes (grams, milliliters, pieces) impact calorie precision, and how the AI calculates calories, protein, carbohydrates, and fats strictly without adding unlisted foods.
Features an interactive "Detailed Voice" vs "Quick Summary" mode toggle.
Granular Nutritional Analysis Voiceover (Results Dashboard):
Generates a custom, detailed voice narration for your specific meal.
Reads out the total calories, the exact caloric energy percentage breakdown for each macronutrient, every individual ingredient's portion and nutritional contribution, and specific culinary preparation assumptions.
Enhanced Voiceover Player:
Read Script Drawer: Added an expandable "Read Voiceover Script" panel so you can read along with the female voice (Kore) or copy the transcript with one click.
Audio Controls: Includes an interactive progress scrubber, live duration counter, mute/unmute toggle, animated sound-wave indicator, and a re-generation button.
flag
Checkpoint
The app failed to deploy. Fix the deployment error.
Gemini 3.8 Flash
Ran for 47s

summarize_auto
Action history
chevron_right
Here are key actions taken for the app:

edit
Edited 1 file
server.ts
check_circle
build
Built
I have fixed the deployment error.
Root Cause
During the production build, server.ts is bundled by esbuild into CommonJS format (dist/server.cjs). The server code contained:
code
Ts
const __filename = fileURLToPath(import.meta.url);
In a bundled CommonJS runtime, import.meta.url is undefined, causing Node.js to throw:
TypeError [ERR_INVALID_ARG_TYPE]: The "path" argument must be of type string or an instance of URL. Received undefined at fileURLToPath.
Fix Applied
Removed the incompatible fileURLToPath(import.meta.url) call from server.ts.
Confirmed that static asset resolution reliably uses path.join(process.cwd(), 'dist').
Re-compiled and verified that node dist/server.cjs boots cleanly and the application builds successfully for deployment
