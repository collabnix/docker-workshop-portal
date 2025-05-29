# Contributing to Docker Workshop Portal

Thank you for your interest in contributing to the Docker Workshop Portal! ?

This document provides guidelines for contributing to our interactive Docker learning platform. We welcome contributions from the community to help make Docker education more accessible and effective.

## ? Ways to Contribute

### ? Bug Reports
- Check existing issues before creating a new one
- Use the bug report template
- Include screenshots and environment details
- Provide clear steps to reproduce

### ? Feature Requests
- Search existing discussions first
- Use the feature request template
- Explain the use case and benefit
- Consider the impact on all user types

### ? Content Contributions
- **Workshop Modules**: Add new learning modules
- **Exercises**: Create hands-on labs and challenges
- **Documentation**: Improve setup guides and explanations
- **Translations**: Help make content accessible globally

### ? Technical Contributions
- **UI/UX Improvements**: Enhance the learning experience
- **Performance**: Optimize loading and interaction speed
- **Accessibility**: Improve support for all users
- **Infrastructure**: Docker, CI/CD, deployment improvements

## ? Getting Started

### Prerequisites
- Node.js 18+
- Docker 24.0+
- Git
- Basic knowledge of HTML, CSS, JavaScript

### Setup Development Environment
```bash
# Fork the repository
git clone https://github.com/YOUR_USERNAME/docker-workshop-portal.git
cd docker-workshop-portal

# Install dependencies
npm install

# Start development server
npm start

# Open http://localhost:8000
```

### Testing Your Changes
```bash
# Run tests
npm test

# Run linting
npm run lint

# Test Docker build
docker build -t workshop-test .
docker run -p 8080:80 workshop-test

# Test with docker-compose
docker-compose up workshop-portal
```

## ? Contribution Process

### 1. **Create an Issue** (Optional but Recommended)
- Discuss your idea before starting work
- Get feedback from maintainers
- Avoid duplicate efforts

### 2. **Fork & Branch**
```bash
# Create feature branch
git checkout -b feature/your-feature-name

# Or for bug fixes
git checkout -b bugfix/issue-description
```

### 3. **Make Changes**
- Follow our coding standards
- Write clear commit messages
- Test your changes thoroughly
- Update documentation if needed

### 4. **Submit Pull Request**
- Use the PR template
- Link related issues
- Provide clear description
- Include screenshots for UI changes

## ? Coding Standards

### HTML/CSS
- Use semantic HTML5 elements
- Follow BEM methodology for CSS classes
- Ensure responsive design (mobile-first)
- Maintain accessibility standards (WCAG 2.1)

### JavaScript
- Use ES6+ features
- Follow ESLint configuration
- Write clear, self-documenting code
- Add comments for complex logic

### Documentation
- Use clear, concise language
- Include code examples
- Add screenshots for visual features
- Update README if needed

## ? Content Guidelines

### Workshop Modules
- **Progressive Learning**: Build on previous concepts
- **Hands-on Focus**: Include practical exercises
- **Real-world Examples**: Use relevant use cases
- **Clear Objectives**: State what users will learn

### Exercise Creation
- **Step-by-step Instructions**: Clear, numbered steps
- **Expected Outputs**: Show what users should see
- **Troubleshooting**: Include common issues and solutions
- **Completion Criteria**: Clear success indicators

### Writing Style
- **Conversational Tone**: Friendly and approachable
- **Beginner-Friendly**: Explain technical terms
- **Inclusive Language**: Welcome all skill levels
- **Action-Oriented**: Use active voice

## ?? Issue Labels

We use labels to categorize issues:

- `bug` - Something isn't working
- `enhancement` - New feature or request
- `documentation` - Improvements to docs
- `good first issue` - Good for newcomers
- `help wanted` - Extra attention is needed
- `question` - Further information is requested
- `content` - Related to workshop content
- `ui/ux` - User interface improvements
- `performance` - Performance improvements
- `accessibility` - Accessibility improvements

## ? Review Process

### What We Look For
- **Code Quality**: Clean, readable, maintainable
- **Functionality**: Features work as intended
- **Testing**: Changes are properly tested
- **Documentation**: Appropriate docs are updated
- **Accessibility**: Maintains or improves accessibility
- **Performance**: Doesn't negatively impact performance

### Timeline
- **Initial Response**: Within 2-3 days
- **Review Completion**: Within 1 week for most PRs
- **Large Features**: May require additional discussion

## ? Priority Areas

We're particularly interested in contributions to:

1. **MCP Integration Examples**: More real-world MCP server usage
2. **Interactive Elements**: Enhanced learning experiences
3. **Mobile Experience**: Better mobile optimization
4. **Accessibility**: WCAG compliance improvements
5. **Performance**: Faster loading and smoother interactions
6. **Internationalization**: Multi-language support
7. **Advanced Exercises**: Complex real-world scenarios

## ? Content Structure

### Adding New Modules
```
content/
??? v1.0/           # Fundamentals
??? v2.0/           # MCP Integration
??? v3.0/           # Advanced (planned)
    ??? README.md   # Module overview
    ??? lessons/    # Individual lessons
    ??? exercises/  # Hands-on labs
```

### Exercise Template
```markdown
# Exercise N: Title

## ? Objectives
- Learning objective 1
- Learning objective 2

## ? Prerequisites
- Required knowledge
- Required tools

## ? Steps
1. Step one with code
2. Step two with expected output
3. etc.

## ? Completion Checklist
- [ ] Task 1 completed
- [ ] Task 2 completed

## ? Next Steps
Links to related content
```

## ? Questions?

### Getting Help
- **GitHub Discussions**: For general questions
- **Slack Community**: [Join Collabnix](https://collabnix.slack.com)
- **Email**: ajeetraina@gmail.com

### Maintainer Contact
- **Ajeet Singh Raina**: [@ajeetraina](https://github.com/ajeetraina)
- **Docker Captain & Senior Developer Advocate @ Docker Inc**

## ? Recognition

Contributors will be:
- Listed in our README
- Mentioned in release notes
- Invited to special Docker community events
- Considered for Docker Community Leader program

## ? Code of Conduct

We follow the [Contributor Covenant](https://www.contributor-covenant.org/) Code of Conduct. By participating, you agree to uphold this code. Please report unacceptable behavior to ajeetraina@gmail.com.

---

**Thank you for helping make Docker education better for everyone! ?**