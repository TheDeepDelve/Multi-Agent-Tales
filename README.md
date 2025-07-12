# Multi-Agent-Tales

<img src="Architecture%20Diagram.jpg" alt="Architecture Diagram" width="500"/>

An advanced AI storytelling platform where multiple specialized agents collaborate to generate dynamic, multi-perspective narratives. Powered by Google Gemini models, intelligent rate limiting, and orchestrated story progression.

---

## Interface Previews


### Story Build-Up Input
![Story Build-Up Input](Interface%20Images/Story%20Build-Up%20Input.png)

### Terminal Snap - Story Generation
![Terminal Snap - Story Generation](Interface%20Images/Terminal%20Snap%20-%20Story%20Generation.png)

### Generated Story
![Generated Story](Interface%20Images/Generated%20Story.png)

---

## Features

- **Multi-Agent Architecture**: Narrator, Protagonist, Antagonist, Scene Builder, Dialogue Generator
- **Intelligent Rate Limiting**: Sophisticated request management across Gemini models
- **Dynamic Story Progression**: Alternating perspectives and plot development
- **Configurable Genres**: Horror, fantasy, mystery, sci-fi, and more
- **Professional API Integration**: Google Gemini with optimized model selection

---

## Architecture

### Agent Roles
- **Narrator**: Sets the scene, third-person perspective
- **Protagonist**: First-person protagonist actions/thoughts
- **Antagonist**: Antagonist responses/motivations
- **Scene Builder**: Constructs vivid scenes
- **Dialogue Generator**: Produces natural conversations

---

## Quick Start

### 1. Clone the Repository
```bash
git clone https://github.com/TheDeepDelve/Multi-Agent-Tales.git
cd MultiAgentTales
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Set Up Environment Variables
Create a `.env` file in the project root:
```
GOOGLE_API_KEY=your_google_api_key_here
```
Get your API key from Google AI Studio.

### 4. Run the Example
```bash
python setup_models.py
```

---

## Usage

Use the `generate_story` function from `setup_models.py`:
```python
from setup_models import generate_story

story = generate_story(
    "Begin a horror story featuring Alex and Maya in an abandoned hospital",
    num_elements=5,
    ending_type='suspense'
)

for i, element in enumerate(story, 1):
    print(f"\n--- Part {i} ---")
    print(element)
```

### Available Ending Types
- `suspense` - Cliffhanger ending
- `dramatic` - High-stakes resolution
- `happy` - Satisfying conclusion
- `tragic` - Emotional loss
- `twist` - Unexpected plot twist
- `cliffhanger` - Unanswered questions
- `mysterious` - Open interpretation
- `bittersweet` - Mixed emotions

---

## 🔧 Configuration

Each agent can be configured with:
- **Temperature**: Controls creativity (0.0-1.0)
- **Top_p**: Nucleus sampling parameter
- **Top_k**: Limits vocabulary diversity
- **Max Output Tokens**: Response length limit

### Rate Limiting
- **RPM (Requests Per Minute)**: Prevents API throttling
- **RPD (Requests Per Day)**: Daily usage tracking
- **Automatic Retry**: Exponential backoff on failures

---

## Development

### Project Structure
```
MultiAgentTales/
├── app.py
├── requirements.txt
├── setup_models.py
├── static/
├── storyweaver/
├── templates/
├── Interface Images/
│   ├── Story Build-Up Input.jpg
│   ├── Terminal Snap - Story Generation.jpg
│   └── Generated Story.jpg
├── Architecture Diagram.jpg
```

### Adding New Agents
1. Define agent configuration in `MODEL_CONFIGS`
2. Create agent class inheriting from `BaseAgent`
3. Add to `StoryOrchestrator.agents`

---

## Security

- API keys stored in environment variables
- `.env` excluded from version control
- Rate limiting prevents API abuse
- Error handling with graceful degradation

---

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## Contact

Harsh Deep - [LinkedIn](https://www.linkedin.com/in/harshdeep7199/) - [Email](harshdeep7199@gmail.com)