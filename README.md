# AI Chatbot

A modern, beautiful AI chatbot application built with React, Node.js, and OpenAI's GPT API. Features a responsive design with real-time messaging, conversation history, and a sleek user interface.

## ✨ Features

- 🤖 **AI-Powered Conversations**: Powered by OpenAI's GPT-3.5-turbo model
- 💬 **Real-time Messaging**: Instant responses with typing indicators
- 📱 **Responsive Design**: Works perfectly on desktop, tablet, and mobile
- 🎨 **Modern UI**: Beautiful gradient design with smooth animations
- 💾 **Conversation Memory**: Maintains context throughout the conversation
- ⚡ **Fast & Lightweight**: Optimized for performance
- 🔒 **Secure**: API key management with environment variables

## 🚀 Quick Start

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- OpenAI API key

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd chatbot
   ```

2. **Install dependencies**
   ```bash
   # Install backend dependencies
   npm install
   
   # Install frontend dependencies
   cd client
   npm install
   cd ..
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the root directory:
   ```env
   OPENAI_API_KEY=your-openai-api-key-here
   PORT=5000
   ```
   
   **Important**: Replace `your-openai-api-key-here` with your actual OpenAI API key. You can get one from [OpenAI's website](https://platform.openai.com/api-keys).

4. **Start the application**
   ```bash
   # Development mode (runs both frontend and backend)
   npm run dev
   
   # Or run them separately:
   # Backend only
   npm run server
   
   # Frontend only (in another terminal)
   npm run client
   ```

5. **Open your browser**
   
   Navigate to `http://localhost:3000` to see the chatbot in action!

## 🛠️ Available Scripts

- `npm start` - Start the production server
- `npm run dev` - Start both frontend and backend in development mode
- `npm run server` - Start only the backend server
- `npm run client` - Start only the React frontend
- `npm run build` - Build the React app for production

## 📁 Project Structure

```
chatbot/
├── client/                 # React frontend
│   ├── public/            # Static files
│   │   ├── App.js         # Main app component
│   │   ├── App.css        # App styles
│   │   └── index.js       # React entry point
│   └── package.json       # Frontend dependencies
├── server.js              # Express backend server
├── package.json           # Backend dependencies
└── README.md              # This file
```

## 🔧 Configuration

### Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `OPENAI_API_KEY` | Your OpenAI API key | Yes |
| `PORT` | Server port (default: 5000) | No |

### API Endpoints

- `POST /api/chat` - Send a message to the AI
- `GET /api/health` - Health check endpoint

## 🎨 Customization

### Changing the AI Model

In `server.js`, you can modify the OpenAI model:

```javascript
const completion = await openai.chat.completions.create({
  model: 'gpt-4', // Change to gpt-4 for better responses
  messages: messages,
  max_tokens: 500,
  temperature: 0.7,
});
```

### Styling

The app uses CSS custom properties and can be easily customized by modifying:
- `client/src/App.css` - Main styling
- `client/src/index.css` - Global styles

### System Prompt

You can customize the AI's behavior by modifying the system prompt in `server.js`:

```javascript
{
  role: 'system',
  content: 'Your custom system prompt here...'
}
```

## 🚀 Deployment

### Heroku

1. Create a Heroku app
2. Set environment variables in Heroku dashboard
3. Deploy using:
   ```bash
   git push heroku main
   ```

### Vercel

1. Connect your GitHub repository to Vercel
2. Set environment variables in Vercel dashboard
3. Deploy automatically on push

### Docker

1. Build the Docker image:
   ```bash
   docker build -t ai-chatbot .
   ```

2. Run the container:
   ```bash
   docker run -p 3000:3000 -e OPENAI_API_KEY=your-key ai-chatbot
   ```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [OpenAI](https://openai.com/) for providing the GPT API
- [React](https://reactjs.org/) for the frontend framework
- [Express](https://expressjs.com/) for the backend framework
- [Lucide React](https://lucide.dev/) for the beautiful icons

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/yourusername/chatbot/issues) page
2. Create a new issue with detailed information
3. Contact the maintainers

---

**Happy chatting! 🤖💬** 