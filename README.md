 <div align="center">
  <img src="./logo.svg" width="180" height="180" alt="GitDocs Logo">

  <h1>GitDocs</h1>
  <p><strong>Transform GitHub repositories into polished technical blog posts using AI</strong></p>

  <p>
    <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT"></a>
    <a href="https://www.python.org/downloads/"><img src="https://img.shields.io/badge/Python-3.8+-green.svg" alt="Python"></a>
    <a href="https://nextjs.org/"><img src="https://img.shields.io/badge/Next.js-13+-000000.svg?logo=next.js&logoColor=white" alt="Next.js"></a>
    <a href="https://flask.palletsprojects.com/"><img src="https://img.shields.io/badge/Flask-2.0+-000000.svg?logo=flask&logoColor=white" alt="Flask"></a>
  </p>
</div>

## 🎥 Video Demo

A video showcasing the tool and explaining how to use it will be released soon.

## 🌟 Features

- **One-Click Blog Generation:** Enter a GitHub repository URL and generate a complete technical blog post.
- **Smart Repository Analysis:** Automatically detects the tech stack, parses the README, and extracts meaningful code snippets.
- **AI-Powered Content:** Uses modern language models to generate coherent and informative technical content.
- **Clean Next.js Frontend:** A modern, responsive interface built with Next.js and Tailwind CSS.
- **Local Fallback:** Continues to function when AI services are unavailable.

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Node.js 14+
- Git

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/Niti06/GIT-DOCS-.git
cd GIT-DOCS--2026
```

**2. Set up the backend**

```bash
cd backend
python -m venv venv
```

Activate the virtual environment:

```bash
# Windows
venv\Scripts\activate

# macOS/Linux
source venv/bin/activate
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

**3. Configure environment variables**

Create a `.env` file inside the `backend` directory and add your OpenRouter API key:

```env
OPENROUTER_API_KEY=your_api_key_here
```

**4. Set up the frontend**

```bash
cd ../frontend
npm install
```

## ▶️ Running the Application

**1. Start the backend server**

From the project root:

```bash
cd backend
python -u app.py
```

The backend will be available at `http://localhost:5000`.

**2. Start the frontend**

Open a new terminal from the project root and run:

```bash
cd frontend
npm run dev
```

The frontend will be available at `http://localhost:3000`.

## 🔧 How It Works

GitDocs operates in three main stages.

**1. Repository Analysis**

- Clones the target repository.
- Identifies the technology stack based on file extensions and dependencies.
- Extracts README content and representative code snippets.

**2. Content Generation**

- Sends repository metadata to an AI model through the OpenRouter API.
- Structures the blog with sections for introduction, features, technical details, and code examples.
- Falls back to template-based generation if the API is unavailable.

**3. Presentation**

- Renders Markdown blog content with syntax highlighting.
- Provides download and copy options.

## 📚 API Documentation

### Generate Blog

```http
POST /generate-blog
```

**Request Body**

```json
{
  "repo_url": "https://github.com/Niti06/GIT-DOCS-"
}
```

**Response**

```json
{
  "blog": "# Generated Markdown Content..."
}
```

## 🤝 Contributing

Contributions are welcome! Feel free to submit a pull request.

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/amazing-feature`).
3. Commit your changes (`git commit -m 'Add some amazing feature'`).
4. Push your branch (`git push origin feature/amazing-feature`).
5. Open a pull request.

## 👩‍💻 Author

**Nitisha Gaurh**

GitHub: [@Niti06](https://github.com/Niti06)

Project Repository: [GIT-DOCS-](https://github.com/Niti06/GIT-DOCS-)

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- OpenRouter API for AI integration.
- Next.js and Flask communities for their excellent documentation.
- All the open-source libraries that made this project possible.
