# AI Agentic Demo

Multi-agent system that takes a project description and automatically:

1. Generates detailed tasks
2. Creates a GitHub repository
3. Creates GitHub issues for each task

## Architecture

```output
Project → Task Generator → Issue Creator → GitHub Issues
```

## Setup

**Prerequisites:** Python 3.12+, Docker, GitHub token, Azure OpenAI access

1. **Install:**

   ```bash
   pip install -e .
   ```

2. **Environment Variables** (create `.env` file):

   ```bash
   GITHUB_PERSONAL_ACCESS_TOKEN=your_github_token
   AZURE_API_KEY=your_azure_api_key  
   AZURE_API_BASE=https://your-azure-endpoint.cognitiveservices.azure.com
   AZURE_API_VERSION=2025-04-01-preview
   ```

3. **Run:**

   ```bash
   python hello.py
   ```

4. **Access:** Open dashboard at `http://localhost:8000`

## Usage

Submit a project via the dashboard:

- **Title:** Your project name
- **Description:** What you want to build

The system will automatically create a GitHub repo with structured issues ready for development.

1. **Input**: You provide a project title and description
2. **Task Generation**: The task generator agent creates up to 5 detailed tasks including:
   - Implementation steps
   - Acceptance criteria
   - Test cases
3. **Repository Creation**: A new GitHub repository is created for the project
4. **Issue Creation**: Each task is converted into a GitHub issue with all details
5. **Output**: You get a fully set up GitHub repository with structured issues ready for development

## Key Features

- **Multi-Agent Coordination**: Agents work together through Flock's orchestration
- **Concurrent Processing**: Multiple issue creator agents work in parallel
- **Structured Output**: Rich data models ensure consistent task and issue formats
- **GitHub Integration**: Full integration with GitHub via MCP server
- **Real-time Monitoring**: Dashboard provides visibility into agent activities

## Use Cases

- **Project Planning**: Automatically generate structured development tasks
- **Repository Setup**: Quickly bootstrap new projects with organized issues
- **Team Coordination**: Create clear, detailed issues for development teams
- **Workflow Automation**: Reduce manual overhead in project initialization

This demo showcases how AI agents can work together to automate complex workflows involving external services and structured data processing.
