<div align="center">
  <h1>🎬 ScreenScape API</h1>
  <p><strong>Free Movies, TV Series & Anime API Platform</strong></p>
  
  [![Website](https://img.shields.io/badge/Website-totu.me-blue?style=for-the-badge&logo=web&logoColor=white)](https://totu.me)
  [![API Status](https://img.shields.io/badge/API-Online-green?style=for-the-badge&logo=api&logoColor=white)](https://totu.me/dashboard)
  [![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge&logo=opensource&logoColor=white)](LICENSE)
  [![Made with Next.js](https://img.shields.io/badge/Made%20with-Next.js-black?style=for-the-badge&logo=next.js&logoColor=white)](https://nextjs.org/)

  <br/>
  
  <p><em>Access thousands of movies, TV shows, and anime with our comprehensive API platform</em></p>
  
  [🚀 Get Started](#-quick-start) • 
  [📖 Documentation](#-api-documentation) • 
  [🔥 Features](#-features) • 
  [💡 Examples](#-examples) • 
  [🤝 Contributing](#-contributing)
</div>

---

## 🌟 Features

<div align="center">
  <table>
    <tr>
      <td align="center" width="33%">
        <h3>🎭 Multiple Sources</h3>
        <p>Access content from 8+ popular platforms including VegaMovies, AllMoviesHub, KMmovies, and more</p>
      </td>
      <td align="center" width="33%">
        <h3>⚡ Fast & Reliable</h3>
        <p>Optimized API endpoints with caching and rate limiting for consistent performance</p>
      </td>
      <td align="center" width="33%">
        <h3>🔐 Secure Access</h3>
        <p>API key authentication with usage tracking and request limits</p>
      </td>
    </tr>
    <tr>
      <td align="center" width="33%">
        <h3>📱 Developer Friendly</h3>
        <p>RESTful API with JSON responses, comprehensive docs, and code examples</p>
      </td>
      <td align="center" width="33%">
        <h3>🎯 Real-time Data</h3>
        <p>Fresh content with real-time scraping and automatic updates</p>
      </td>
      <td align="center" width="33%">
        <h3>🆓 Free to Use</h3>
        <p>Generous free tier with 1000+ requests per month</p>
      </td>
    </tr>
  </table>
</div>

## 🎯 Supported Content Types

- **🎬 Movies** - Latest releases, classics, regional cinema
- **📺 TV Series** - Popular shows, seasons, episodes
- **🎌 Anime** - Sub/dub content with episode tracking
- **🎭 Regional Content** - Hindi, Tamil, Telugu, Malayalam movies
- **📱 Multiple Qualities** - 480p to 4K content
- **🌍 Multi-language** - Support for various languages and subtitles

## 🚀 Quick Start

### 1. Get Your API Key
Visit [totu.me](https://totu.me) and sign up for a free account to get your API key.

### 2. Make Your First Request

```bash
curl -X GET "https://totu.me/api/posts" \
  -H "x-api-key: YOUR_API_KEY" \
  -H "Content-Type: application/json"
```

### 3. Start Building! 🎉

## 📖 API Documentation

### Base URL
```
https://totu.me/api
```

### Authentication
All requests require an API key in the header:
```javascript
headers: {
  'x-api-key': 'YOUR_API_KEY',
  'Content-Type': 'application/json'
}
```

### Available Endpoints

<details>
<summary><strong>🎬 Movies API</strong></summary>

#### Get Movies
```http
GET /api/moviesdrive
```

#### Search Movies
```http
GET /api/moviesdrive?search=avengers
```

#### Get Movie Details
```http
GET /api/moviesdrive/episode?url=MOVIE_URL
```

#### Extract Download Links
```http
GET /api/hubcloud?url=HUBCLOUD_URL
```

</details>

<details>
<summary><strong>📺 Anime API</strong></summary>

#### Get All Anime
```http
GET /api/posts
```

#### Search Anime
```http
GET /api/posts?search=naruto
```

#### Get Episode Details
```http
GET /api/episodes/anime-id
```

#### Get Streaming Links
```http
GET /api/video?url=EPISODE_URL
```

</details>

<details>
<summary><strong>🎭 Multiple Platform APIs</strong></summary>

- **VegaMovies**: `/api/vegamovies`
- **AllMoviesHub**: `/api/allmovieshub`
- **KMmovies**: `/api/kmmovies`
- **DesireMovies**: `/api/desiremovies`
- **10BitClub**: `/api/10bitclub`
- **VidSrc**: `/api/vidsrc`

</details>

## 💡 Examples

### JavaScript/Node.js
```javascript
const response = await fetch('https://totu.me/api/posts?search=demon slayer', {
  headers: {
    'x-api-key': 'YOUR_API_KEY',
    'Content-Type': 'application/json'
  }
});

const data = await response.json();
console.log(data.posts);
```

### Python
```python
import requests

url = "https://totu.me/api/moviesdrive"
headers = {
    "x-api-key": "YOUR_API_KEY",
    "Content-Type": "application/json"
}

response = requests.get(url, headers=headers)
data = response.json()
print(data["posts"])
```

### cURL
```bash
curl -X GET "https://totu.me/api/vegamovies?search=spider-man" \
  -H "x-api-key: YOUR_API_KEY" \
  -H "Content-Type: application/json"
```

## 📊 Response Format

All endpoints return standardized JSON responses:

```json
{
  "success": true,
  "count": 20,
  "posts": [
    {
      "id": "123",
      "title": "Movie Title (2024)",
      "imageUrl": "https://example.com/poster.jpg",
      "postUrl": "https://example.com/movie-page",
      "qualities": ["480p", "720p", "1080p"],
      "languages": ["Hindi", "English"],
      "releaseYear": "2024"
    }
  ],
  "remainingRequests": 995
}
```

## 🛠️ Tech Stack

- **Framework**: Next.js 14 with App Router
- **Database**: PostgreSQL with Drizzle ORM
- **Authentication**: Firebase Auth
- **Styling**: Tailwind CSS + shadcn/ui
- **Web Scraping**: Cheerio + Axios
- **Deployment**: Vercel
- **Language**: TypeScript

## 🎨 Features in Detail

### 🔍 Advanced Search
- Full-text search across multiple platforms
- Filter by quality, language, year
- Category-based browsing
- Real-time suggestions

### 📈 Analytics Dashboard
- Request usage tracking
- API key management
- Performance metrics
- Rate limit monitoring

### 🔐 Security Features
- API key authentication
- Rate limiting
- Request validation
- Error handling

### 🎯 Developer Tools
- Interactive API explorer
- Code generation
- Response examples
- Comprehensive documentation

## 🚦 Rate Limits

| Plan | Requests/Month | Rate Limit |
|------|----------------|------------|
| Free | 1,000 | 100/hour |
| Pro | 10,000 | 500/hour |
| Enterprise | Unlimited | Custom |

## 🌐 Browser Support

- ✅ Chrome (Latest)
- ✅ Firefox (Latest)
- ✅ Safari (Latest)
- ✅ Edge (Latest)
- ✅ Mobile browsers

## 📝 Changelog

### v2.0.0 (Latest)
- 🎉 Added VegaMovies API support
- 🔧 Improved error handling
- ⚡ Enhanced performance
- 📱 Better mobile responsiveness

### v1.5.0
- 🎌 Added Anime API
- 🔐 Implemented API key system
- 📊 Added analytics dashboard

[View Full Changelog](CHANGELOG.md)

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

### Development Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/screenscape-api.git
   cd screenscape-api
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env.local
   # Edit .env.local with your configuration
   ```

4. **Run the development server**
   ```bash
   npm run dev
   ```

5. **Open [http://localhost:3000](http://localhost:3000)**

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚠️ Disclaimer

This API is for educational purposes only. Users are responsible for complying with applicable laws and terms of service of content providers.

## 🙋‍♂️ Support

- 📧 **Email**: support@totu.me
- 💬 **Discord**: [Join our community](https://discord.gg/screenscape)
- 🐛 **Issues**: [GitHub Issues](https://github.com/yourusername/screenscape-api/issues)
- 📖 **Docs**: [totu.me/docs](https://totu.me/docs)

## 🌟 Show Your Support

If this project helps you, please consider:

- ⭐ Starring this repository
- 🐛 Reporting bugs
- 💡 Suggesting new features
- 🤝 Contributing to the code

---

<div align="center">
  <p>Made with ❤️ by the ScreenScape Team</p>
  <p>
    <a href="https://totu.me">Website</a> •
    <a href="https://totu.me/docs">Documentation</a> •
    <a href="https://github.com/yourusername/screenscape-api">GitHub</a>
  </p>
</div>
