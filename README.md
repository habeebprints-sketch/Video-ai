# Prompt2Video AI

A GitHub-ready starter for an AI video generator that accepts:

- Text prompts
- Public website URLs
- Video duration
- Video aspect ratio

## Run locally

Install Node.js, then:

```bash
npm install
npm start
```

Open:

```text
http://localhost:3000
```

## Connect an AI video provider

The frontend calls:

```text
POST /api/generate
```

Edit `server.js` and connect your chosen video-generation API.

The backend should eventually return:

```json
{
  "videoUrl": "https://your-storage.example/video.mp4"
}
```

### Security

Never put your AI provider secret/API key in `app.js`, `index.html`, or other frontend files. Store secrets in environment variables such as:

```text
VIDEO_API_KEY=your_secret_key
```

For website input, only process pages you are allowed to access and respect robots.txt, terms, copyright, and rate limits.
