# Food to Recipe Convertor

Generate recipes from food photos using AI! This app uses the Gemini API through secure Netlify functions to analyze food images and create detailed recipes.

## Features

- 🖼️ **Image Upload**: Drag & drop or click to upload food photos
- 🤖 **AI-Powered**: Uses Google's Gemini AI to analyze images and generate recipes
- 📱 **Responsive Design**: Works on desktop and mobile devices
- 🔐 **Secure API**: API keys are stored securely in environment variables
- 📝 **Markdown Support**: Recipes are formatted with rich text
- 💾 **Download**: Save generated recipes as markdown files

## Setup

### Prerequisites

- A [Netlify](https://netlify.com) account
- A [Google AI Studio](https://aistudio.google.com) account for Gemini API access

### Deployment

1. **Clone the repository**
   ```bash
   git clone https://github.com/SabhyaAggarwal/Food-to-Recipe-Convertor.git
   cd Food-to-Recipe-Convertor
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Get a Gemini API Key**
   - Go to [Google AI Studio](https://aistudio.google.com)
   - Create a new project or select an existing one
   - Enable the Gemini API
   - Generate an API key

4. **Deploy to Netlify**
   - Connect your GitHub repository to Netlify
   - In your Netlify site settings, go to "Environment variables"
   - Add: `GEMINI_API_KEY` = your Gemini API key
   - Deploy the site

### Local Development

```bash
# Install Netlify CLI if you haven't already
npm install -g netlify-cli

# Set up environment variables
echo "GEMINI_API_KEY=your_api_key_here" > .env

# Start local development server
netlify dev
```

The app will be available at `http://localhost:8888`

## Architecture

- **Frontend**: Static HTML/CSS/JavaScript
- **Backend**: Netlify Functions (serverless)
- **API Proxy**: `/api/recipe-proxy` endpoint handles secure API calls
- **AI Model**: Google Gemini 1.5 Flash for image analysis and recipe generation

## Security

- API keys are stored as environment variables (not in frontend code)
- CORS is properly configured for cross-origin requests
- Input validation on all API endpoints
- Error handling prevents information leakage

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

MIT License - see LICENSE file for details