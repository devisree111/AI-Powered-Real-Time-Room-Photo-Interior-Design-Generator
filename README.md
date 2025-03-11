# AI-Powered-Real-Time-Room-Photo-Interior-Design-Generator

## Project Structure
This project is an AI-powered furniture interior designing system that generates customized designs based on user input. It integrates Replicative API for generating designs, with a React.js front-end and a Node.js/Express.js backend. Users can upload images, take a quiz for design preferences, view 3D renders of furniture, and provide ratings for the designs.

### Folder Structure
- `frontend/` - Contains the React.js front-end code.
- `backend/` - Contains the Node.js/Express.js backend code.

## Prerequisites
Ensure you have the following installed:
- [Node.js](https://nodejs.org/)
- [npm](https://www.npmjs.com/)
- [Visual Studio Code (VSCode)](https://code.visualstudio.com/)

## Setup and Deployment

### 1. Clone the Repository
Clone the repository to your local machine:
```bash
git clone https://github.com/2711-amsi/AI-Powered-Real-Time-Room-Photo-Interior-Design-Generator.git
```

### 2. Backend Setup
- Open your project folder in VSCode.
- Open the terminal and run the following commands:
```bash
cd backend
npm install
npm start
```

### 3. Frontend Setup
- Open another terminal and run the following commands:
```bash
cd frontend
npm install
npm start
```

### 4. Access the Application
Once both the frontend and backend are running, open your browser and go to:
```
http://localhost:5000
```

## Features
- **User Input Quiz**: Collects user preferences for generating furniture designs.
- **Image Upload**: Users can upload images for inspiration.
- **History**: View previously generated designs along with ratings.
- **Ratings**: Users can rate the designs generated by the AI.

## Technologies Used
- **Frontend**: React.js
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **AI**: Replicative API for generating furniture designs
## API Details
The backend of this project communicates with Replicative API to generate AI-powered interior designs. The model used for image generation is **ControlNet**, which allows for controlled and precise image generation based on user inputs.

**Replicative API Website:** [https://replicate.com/](https://replicate.com/)

### API Endpoints
#### 1. Generate Design
**Endpoint:** `/api/generate`
**Method:** POST
**Description:** Sends user preferences and image inputs to the AI model and returns generated designs.
**Request Body:**
```json
{
  "image": "base64_encoded_image",
  "preferences": {
    "model": "modern",
    "roomtype": "bedroom",
    "budget": "50000",
    "colour":"red"
  }
}
```
**Response:**
```json
{
  "design_url": "https://generated-image-url.com",
  "confidence": 0.98
}
```

#### 2. Fetch History
**Endpoint:** `/api/history`
**Method:** GET
**Description:** Retrieves previously generated designs for a user.
**Response:**
```json
[
  {
    "design_url": "https://generated-image1.com",
    "rating": 4.5,
    "timestamp": "2025-03-09T12:00:00Z"
  },
  {
    "design_url": "https://generated-image2.com",
    "rating": 5.0,
    "timestamp": "2025-03-08T14:30:00Z"
  }
]
```

## License
This project is licensed under the [MIT License](LICENSE).
