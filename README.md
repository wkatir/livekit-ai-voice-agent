# LiveKit AI Voice Agent - Hotel Receptionist

A sophisticated AI voice agent built with LiveKit that serves as a virtual hotel receptionist. The agent can handle hotel inquiries, book rooms, check availability, and provide customer service through natural voice interactions.

## 🏨 Project Overview

This project implements an AI-powered voice agent named **Sarah** who serves as a virtual receptionist for "The Grand Luxe" hotel. The agent uses LiveKit for real-time voice communication and integrates with various services to provide a complete hotel booking experience.

## ✨ Features

### 🎯 Core Capabilities
- **Voice Interaction**: Real-time voice communication using LiveKit
- **Hotel Receptionist**: Professional hotel assistant persona
- **Room Booking**: Complete booking workflow with availability checking
- **Google Calendar Integration**: Automatic room availability management
- **Email Confirmations**: Automated booking confirmation emails
- **Web Page Navigation**: Opening relevant hotel service pages

### 🛏️ Room Types & Pricing
- **Executive Suite**: $450/night - King bed, private balcony, spacious living area
- **Deluxe Room**: $280/night - Queen bed, private balcony, spacious living area  
- **Presidential Suite**: $800/night - King bed, private balcony, butler service, private terrace with jacuzzi

### 🔧 Technical Features
- **MCP Integration**: Model Context Protocol for dynamic tool loading
- **Noise Cancellation**: Enhanced audio quality with LiveKit Cloud
- **OpenAI Integration**: Powered by OpenAI's real-time voice model
- **Modular Architecture**: Clean separation of concerns

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- LiveKit account
- OpenAI API key
- Google Calendar API access
- Gmail API access

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd livekit-ai-voice-agent
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**
   Create a `.env` file in the project root:
   ```env
   N8N_MCP_SERVER_URL=your_mcp_server_url_here
   OPENAI_API_KEY=your_openai_api_key
   LIVEKIT_API_KEY=your_livekit_api_key
   LIVEKIT_API_SECRET=your_livekit_api_secret
   ```

4. **Run the agent**
   ```bash
   python agent.py
   ```

## 📁 Project Structure

```
livekit-ai-voice-agent/
├── agent.py              # Main agent implementation
├── prompts.py            # Agent instructions and prompts
├── requirements.txt      # Python dependencies
├── mcp_client/          # MCP integration module
│   ├── agent_tools.py   # Tool integration utilities
│   ├── server.py        # MCP server implementation
│   ├── util.py          # Utility functions
│   └── __init__.py
├── tools.py             # Custom tools (placeholder)
├── server.py            # Server implementation (placeholder)
└── .gitignore          # Git ignore rules
```

## 🎙️ How It Works

### Agent Workflow
1. **User Interaction**: Customer speaks to Sarah via voice
2. **Intent Recognition**: Agent understands user requests
3. **Service Provision**: 
   - Hotel information and amenities
   - Room availability checking
   - Booking process management
   - Email confirmations
   - Web page navigation

### Booking Process
1. **Information Gathering**: Collect check-in/out dates, guests, room type
2. **Availability Check**: Verify room availability via Google Calendar
3. **Booking Creation**: Create calendar event with booking details
4. **Confirmation**: Send email confirmation to customer
5. **Web Navigation**: Open booking confirmation page

## 🔧 Configuration

### Environment Variables
- `N8N_MCP_SERVER_URL`: URL for the MCP server
- `OPENAI_API_KEY`: OpenAI API key for voice model
- `LIVEKIT_API_KEY`: LiveKit API credentials
- `LIVEKIT_API_SECRET`: LiveKit API secret

### MCP Server Integration
The agent integrates with MCP servers to provide dynamic tool capabilities:
- Google Calendar tools for room management
- Gmail tools for email confirmations
- Browser tools for web page navigation

## 🛠️ Development

### Adding New Features
1. **New Tools**: Add to MCP server integration
2. **New Prompts**: Update `prompts.py`
3. **New Capabilities**: Extend the `Assistant` class in `agent.py`

### Testing
```bash
# Test agent compilation
python -m py_compile agent.py

# Test imports
python -c "import agent"
```

## 📋 Dependencies

### Core Dependencies
- `livekit-agents`: LiveKit agent framework
- `livekit-plugins-openai`: OpenAI integration
- `livekit-plugins-noise-cancellation`: Audio enhancement
- `pydantic-ai-slim[openai,mcp]`: AI model integration
- `flask[async]`: Web server capabilities
- `python-dotenv`: Environment management

### Optional Dependencies
- `livekit-agents[tavus]`: Tavus integration
- `flask-cors`: CORS support for web applications

## 🎯 Use Cases

### Hotel Operations
- **Front Desk**: 24/7 virtual receptionist
- **Booking Management**: Automated room reservations
- **Customer Service**: Hotel information and assistance
- **Amenities**: Spa, fitness center, and service information

### Integration Points
- **Google Calendar**: Room availability and booking management
- **Gmail**: Automated booking confirmations
- **Web Services**: Hotel website integration
- **Voice Communication**: Real-time customer interaction

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 🆘 Support

For issues and questions:
- Check the project documentation
- Review the LiveKit documentation
- Open an issue in the repository
