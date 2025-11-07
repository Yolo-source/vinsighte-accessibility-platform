**Vinsighte – System Architecture**

**Overview**
Vinsighte is built as a mobile-first platform designed to help visually impaired, deaf, and deaf-mute users read and communicate easily.  
The architecture connects a **mobile app frontend** to a **backend API**, which manages authentication, data storage, and AI processing.

**Technical Stack**
| Layer | Technology | Purpose 

| Frontend | Flutter | Cross-platform mobile app for Android & iOS 

| Backend | Node.js + Express | Handles API requests, authentication, and data exchange 

| Database | MongoDB Atlas | Stores user data, reading logs, and community uploads 

| AI Layer | TensorFlow Lite, Google Cloud Vision API | Processes OCR, TTS, and gesture recognition 

| Hosting | Render / Firebase | For backend hosting and real-time database sync 

**System Workflow**

1. **User Input Layer**
   - The user opens the mobile app.
   - They can choose between “Read Text,” “Speak,” or “Sign Communicate.”

2. **Processing Layer**
   - The app uses the device camera or mic to capture input.
   - OCR converts images of text into digital text.
   - TTS and STT engines process audio and convert accordingly.
   - AI model recognizes sign language gestures and translates them into text or audio.

3. **Database Layer**
   - MongoDB stores user profiles, history, preferences, and shared materials.
   - Data syncs securely with the backend API using JWT authentication.

4. **Output Layer**
   - Processed information (audio, text, or translation) is displayed or played back.
   - Users can save or share the output in the Learning Hub.

**Component Interaction Diagram (Simplified)**

User → Mobile App (Flutter)
→ API Gateway (Express.js)
→ OCR / TTS / Sign Models (TensorFlow Lite)
→ Database (MongoDB)
← Response (Audio/Text/Translation

**Why This Approach Works**
- **Scalable:** The API and AI services can be expanded as more features are added.  
- **Offline Capability:** Some features (like text scanning and reading) can work without internet.  
- **Inclusive Design:** Built with accessibility-first principles for diverse disabilities.  
- **Feasible:** Uses existing frameworks and APIs, making it realistic for a small local startup to develop and maintain.

**-My Personal Setup Effort**
I set up my GitHub repository manually using VS Code and Git commands. I structured the folders for `frontend`, `backend`, and `docs` and created these two Markdown files to guide the next phase of development.  

I wanted the documentation to be easy to understand — not filled with heavy tech terms — so that anyone, even non-tech teammates, can get the vision of what I’m building.

**Future Enhancements**
- Add real-time sign language recognition using camera input.  
- Integrate with Braille readers for enhanced accessibility.  
- Build a lightweight web version for schools and NGOs.

***Author: Chidera David Umeji***
