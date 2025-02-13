# Technical Context

## Technology Stack

### Core Technologies
- Node.js runtime environment
- TypeScript for type safety
- Docker for containerization

### External APIs
1. **Firecrawl API**
   - Web search functionality
   - Content extraction capabilities
   - Rate limiting considerations
   - Optional self-hosted setup

2. **OpenAI API**
   - Language model processing (o3 mini model)
   - Query generation
   - Result analysis
   - Custom endpoint support

## Development Setup

### Local Development
1. **Prerequisites**
   - Node.js environment
   - npm package manager
   - API keys:
     - Firecrawl API key
     - OpenAI API key

2. **Environment Configuration**
   ```bash
   # Required in .env.local
   FIRECRAWL_KEY="your_firecrawl_key"
   OPENAI_KEY="your_openai_key"

   # Optional for self-hosted Firecrawl
   FIRECRAWL_BASE_URL="http://localhost:3002"

   # Optional for custom LLM setup
   OPENAI_ENDPOINT="custom_endpoint"
   OPENAI_MODEL="custom_model"
   ```

### Docker Deployment
1. **Container Setup**
   - Docker Compose configuration
   - Environment variable management
   - Volume mapping

2. **Execution Commands**
   ```bash
   # Start container
   docker compose up -d

   # Run in container
   docker exec -it deep-research npm run docker
   ```

## Dependencies

### Core Dependencies
- axios for HTTP requests
- TypeScript compiler
- Docker runtime (optional)

### Development Dependencies
- npm for package management
- prettier for code formatting
- TypeScript configuration

## Configuration Options

### Concurrency Settings
- Adjustable concurrency limits
- Rate limiting considerations
- Performance optimization

### API Configuration
1. **Firecrawl Options**
   - Base URL configuration
   - API key management
   - Rate limit handling

2. **OpenAI Options**
   - Endpoint customization
   - Model selection
   - Local LLM support

## Performance Considerations

### Optimization
- Concurrent processing
- Memory management
- Rate limit handling

### Scalability
- Docker containerization
- Configurable concurrency
- Resource management
