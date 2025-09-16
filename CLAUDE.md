# Personal Assistant Project - Configuration

<!-- Updated: 2025-09-17 - Added task-schedule-manager agent information -->

## Project Overview

This is a Personal Assistant application designed to integrate with GitHub and other services to provide automated assistance and workflow management capabilities. The project includes agent-based architecture for specialized task handling and secure credential management.

### Repository Information
- **Repository URL**: https://github.com/tot0rokr/PersonalAssistant.git
- **Repository Name**: PersonalAssistant
- **Owner**: tot0rokr

## Communication Preferences

- **Primary Language**: Korean for all communication and responses
- **Response Style**: Clear, concise, and focused on requested tasks only
- **Principle**: Do what has been asked; nothing more, nothing less

## Project Structure and Architecture

### Core Components
- **Agent System**: Specialized agents in `.claude/agents/` for different functionalities
  - `git-workflow-manager`: Handles Git operations and repository management
  - `claude-md-manager`: Manages long-term configuration and instruction persistence
  - `task-schedule-manager`: Handles Linear task management and Google Calendar integration
- **Environment Configuration**: `.env` file for secure credential storage
- **Security Layer**: `.gitignore` properly configured to exclude sensitive files

### Directory Structure
```
PersonalAssistant/
├── .claude/
│   └── agents/
│       ├── git-workflow-manager.md
│       ├── claude-md-manager.md
│       └── task-schedule-manager.md
├── .env (excluded from version control)
├── .gitignore
└── CLAUDE.md (this file)
```

## Security Guidelines

### Credential Management
- **NEVER commit sensitive data** like API tokens, passwords, or private keys
- **Always use .env files** for environment-specific credentials
- **Verify .gitignore coverage** before committing any new sensitive files
- **Use absolute file paths** in all operations due to environment constraints

### GitHub Integration
- **GitHub PAT Token**: Stored securely in .env file
- **Repository Access**: Use MCP tools for GitHub operations when available
- **Branch Protection**: Follow git-workflow-manager policies strictly

## Coding Standards and Preferences

### General Principles
- **Code Quality**: Prioritize readable, maintainable code
- **Error Handling**: Implement comprehensive error handling for all external integrations
- **Documentation**: Code should be self-documenting with clear variable and function names
- **Testing**: Include appropriate tests for critical functionality

### File Management
- **Prefer editing existing files** over creating new ones
- **Never create documentation files** unless explicitly requested
- **Use absolute paths** for all file operations
- **Maintain existing file structure** and conventions

### Version Control
- **Branch Management**: Create feature branches for all new work
- **Commit Messages**: Use detailed, descriptive commit messages
- **Push Policy**: Immediately push commits to remote repository
- **Code Review**: Always review changes before committing

## Agent-Specific Requirements

### Git Workflow Manager
- Must create new branches for any feature work
- Never allow direct commits to main branch
- Require detailed commit messages with context
- Automatically push after successful commits
- Handle merge conflicts proactively

### Claude MD Manager
- Update this CLAUDE.md file for persistent instructions
- Maintain clear section organization
- Add timestamp comments for all updates
- Preserve existing instructions unless explicitly told otherwise
- Ensure instructions are actionable and specific

### Task Schedule Manager
- Integrate with Linear for issue and task management
- Manage Google Calendar events and scheduling
- Handle task scheduling and calendar integration workflows
- Support both one-time tasks and recurring scheduled activities
- Coordinate between Linear tasks and calendar events for comprehensive project management

## GitHub Integration Guidelines

### API Usage
- Use GitHub PAT token from environment variables
- Implement rate limiting awareness
- Handle API errors gracefully with appropriate fallbacks
- Log API interactions for debugging purposes

### Repository Operations
- Follow established branch naming conventions
- Use meaningful commit messages following conventional commit format
- Maintain clean commit history with logical groupings
- Ensure all pushes include comprehensive change descriptions

## Development Workflow

### Starting New Features
1. Create descriptive feature branch from main
2. Implement changes with comprehensive error handling
3. Test functionality thoroughly
4. Document any new environment variables or dependencies
5. Commit with detailed messages explaining changes and rationale
6. Push immediately to remote repository

### Code Review Process
- Review all changes using `git diff` before committing
- Ensure no unintended files are included
- Verify security guidelines are followed
- Confirm documentation is updated if needed

### Deployment Considerations
- Ensure all environment variables are documented
- Verify .gitignore excludes all sensitive files
- Test integration points before finalizing changes
- Maintain backward compatibility where possible

## Environment Setup

### Required Environment Variables
- `GITHUB_PAT`: GitHub Personal Access Token for API operations
- `LINEAR_API_KEY`: Linear API key for task and issue management
- `GOOGLE_CALENDAR_CREDENTIALS`: Google Calendar API credentials for event management
- Additional variables to be documented as the project grows

### Development Dependencies
- Git workflow management requires proper Git configuration
- MCP server integration for enhanced GitHub operations
- Agent system requires proper .claude directory structure
- Linear API integration for task management capabilities
- Google Calendar API integration for scheduling functionality

## Project-Specific Constraints

### Technical Limitations
- Agent threads reset cwd between bash calls - use absolute paths only
- No emoji usage in code or communication unless explicitly requested
- File creation should be minimal and only when absolutely necessary

### Operational Guidelines
- Focus on requested functionality without additional features
- Maintain existing project structure and conventions
- Preserve security boundaries and access controls
- Follow established patterns for consistency

---

*This configuration file serves as the persistent memory for the Personal Assistant project. All agents and future interactions should reference and follow these guidelines.*