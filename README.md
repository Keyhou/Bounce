This project does not work but I wanted to submit anyways.
It was nice to participate though. Thank you! 

# Bounce: Autonomous Commute Agent

**Built for Pioneers AI Lab Hackathon**

## 🏆 Features

- Simulates commute delays.
- Uses Mistral AI to suggest optimized routes.
- Explains time and CO₂ savings.

## 🛠 Tech Stack

- **Mistral**: AI route optimization.
- **N8n**: Autonomous workflow.
- **Lovable**: Front.

## 🎥 Demo

[Loom Video Link](your-loom-link)

## 🏅 Judging Criteria

| Criterion          | How We Hit It                          |
|--------------------|----------------------------------------|
| Execution          | Working demo with delay simulation.   |
| AI & Agents        | Mistral + N8n automation.              |
| Scalability        | Serverless, minimal ops.               |
| Problem & Impact   | Saves time + CO₂.                      |
| Demo & Narrative   | Clear story, polished UI.              |
| Partner Tech       | Mistral, N8n, Figma.                   |

## 🚀 Getting Started

### Prerequisites

- Node.js (v18 or higher)
- npm or yarn
- N8n installed globally
- Mistral API key

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd bounce-hackathon/bounce
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up N8n workflow:
   - Follow the instructions in `N8N_SETUP.md`
   - Import the workflow from `n8n-workflow.json`
   - Configure your Mistral API key

4. Start the development server:
   ```bash
   npm run dev
   ```

5. Start N8n (in a separate terminal):
   ```bash
   n8n start
   ```

6. Open your browser and navigate to the URL shown in the terminal (typically `http://localhost:5173`)

## 📁 Project Structure

```
bounce/
├── src/
│   ├── App.jsx          # Main application component
│   ├── index.css        # Tailwind CSS directives
│   └── main.jsx         # Application entry point
├── n8n-workflow.json    # N8n workflow configuration
├── N8N_SETUP.md         # N8n setup instructions
├── ENV_SETUP.md         # Environment variables guide
└── README.md            # This file
```

## 🔧 Configuration

### Environment Variables

Create a `.env` file in the `bounce` directory (optional):

```env
VITE_N8N_WEBHOOK_URL=http://localhost:5678/webhook/delay
```

If not set, the app defaults to `http://localhost:5678/webhook/delay`.

### Mistral API Key

Configure your Mistral API key in the N8n workflow:
1. Open the "Call Mistral API" node
2. Update the Authorization header with your API key
3. Get your key from https://console.mistral.ai/

## 🎯 How It Works

1. User selects origin and destination
2. User clicks "Simulate Delay" button
3. Frontend sends request to N8n webhook
4. N8n workflow calls Mistral AI API
5. Mistral analyzes the delay and suggests an optimized route
6. Response is returned to frontend and displayed

## 📝 License

This project was built for the Pioneers AI Lab Hackathon.
