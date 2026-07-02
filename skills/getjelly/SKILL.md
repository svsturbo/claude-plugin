---
name: getjelly
description: Access GetJelly creator search, profile spy, and content analysis
---

# GetJelly API Integration

## Authentication

Get your API token from: https://app.getjelly.ai/ai-integration

All requests require:
```
Authorization: Bearer YOUR_API_TOKEN
```

## Available Endpoints

### 1. Spy Profile
Look up Instagram/TikTok creator profile with engagement metrics.

```bash
curl -X POST https://api.getjelly.ai/api/spy/import/ \
  -H "Authorization: Bearer YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"url": "https://instagram.com/username"}'
```

**Response**: Profile data with followers, engagement rate, recent posts

### 2. Search Creators
Semantic search for creators by description.

```bash
curl -X POST https://api.getjelly.ai/api/conversation/search/ \
  -H "Authorization: Bearer YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"query": "fitness micro-influencer under 50K followers", "top_k": 5}'
```

**Response**: Ranked list of matching creators with similarity scores

### 3. Analyze Content (Coming Soon)
Deep content analysis for posts (JEL-515).

```bash
curl -X POST https://api.getjelly.ai/api/jelly-brain/analyze/ \
  -H "Authorization: Bearer YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"post_url": "https://instagram.com/p/ABC123/", "mode": "analyze"}'
```

## Error Handling

- **401 Unauthorized**: Invalid or missing API token
- **400 Bad Request**: Invalid URL or missing required fields
- **429 Too Many Requests**: Rate limit exceeded

## Examples

User: "spy the profile @username on Instagram"
Claude: Calls /api/spy/import/ with full URL, returns profile summary

User: "find vegan lifestyle creators with high engagement"
Claude: Calls /api/conversation/search/ with semantic query
