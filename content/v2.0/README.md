# Docker Workshop v2.0 - MCP Integration

Welcome to Docker Workshop version 2.0 featuring Model Context Protocol (MCP) integration with Docker and Gordon AI.

## ? What You'll Learn

This advanced module introduces you to Docker's integration with the Model Context Protocol (MCP), showcasing how containerization meets AI-powered development workflows.

### Learning Objectives
- Understand the Model Context Protocol (MCP) specification
- Set up and configure Docker MCP Toolkit
- Integrate Gordon AI with containerized applications
- Build and deploy custom MCP servers using Docker
- Create AI-enhanced development workflows
- Implement security best practices for AI-container integration

## ? Module Breakdown

### 1. Introduction to MCP
- What is Model Context Protocol?
- MCP architecture and components
- Docker's role in the MCP ecosystem
- Use cases and real-world applications

### 2. Docker MCP Toolkit
- Installing the MCP toolkit
- Understanding MCP servers and clients
- Docker Hub MCP namespace (`mcp/*`)
- Configuration with `gordon-mcp.yml`

### 3. Gordon AI Setup
- Introduction to Gordon AI assistant
- Installation and configuration
- Docker CLI integration
- Best practices for AI-assisted development

### 4. MCP Servers with Docker
- Available MCP servers on Docker Hub
- Running containerized MCP servers
- Custom server development
- Server composition with Docker Compose

### 5. Hands-on Projects
- Build a time-aware application with `mcp/time`
- Create a GitHub integration using `mcp/github`
- Develop a custom MCP server
- Multi-server orchestration

### 6. Security & Best Practices
- Container isolation for AI workloads
- Secure MCP server deployment
- API key management
- Network security considerations

## ? Prerequisites

- **Required**: Completion of Docker Workshop v1.0
- Basic understanding of REST APIs
- Familiarity with JSON configuration
- Optional: Experience with AI/ML concepts

## ? Getting Started

### Quick Setup

1. **Install Docker MCP Toolkit**:
   ```bash
   # Pull the Gordon MCP configuration
   docker pull mcp/time
   docker pull mcp/github
   ```

2. **Configure Gordon AI**:
   ```yaml
   # gordon-mcp.yml
   version: '3.8'
   services:
     time-server:
       image: mcp/time
       ports:
         - "3001:3000"
     
     github-server:
       image: mcp/github
       environment:
         - GITHUB_TOKEN=${GITHUB_TOKEN}
       ports:
         - "3002:3000"
   ```

3. **Start Interactive Learning**: Navigate to Module 2 in the main portal

## ? Hands-on Labs

### Lab 1: Time-Aware Container
Build a containerized application that uses the MCP time server for scheduling and time zone handling.

### Lab 2: GitHub Integration
Create a development workflow that integrates with GitHub using MCP servers for automated repository management.

### Lab 3: Custom MCP Server
Develop and containerize your own MCP server for a specific use case.

### Lab 4: Multi-Server Orchestration
Orchestrate multiple MCP servers using Docker Compose for complex AI workflows.

## ? Key Resources

### Docker MCP Resources
- [Docker MCP Community Portal](https://ajeetraina.github.io/docker-mcp-portal)
- [MCP Servers on Docker Hub](https://hub.docker.com/u/mcp)
- [Gordon AI Documentation](https://docs.docker.com/gordon/)

### MCP Specification
- [Model Context Protocol Specification](https://spec.modelcontextprotocol.io/)
- [Anthropic MCP Documentation](https://modelcontextprotocol.io/)
- [MCP SDK and Tools](https://github.com/modelcontextprotocol)

## ? Practical Exercises

- [ ] Set up Gordon AI with Docker integration
- [ ] Deploy your first MCP server container
- [ ] Build a multi-container MCP application
- [ ] Create a custom MCP server
- [ ] Implement secure MCP workflows
- [ ] Integrate MCP with CI/CD pipelines

## ? Security Considerations

- **Container Isolation**: MCP servers run in isolated containers
- **API Security**: Secure management of API keys and tokens
- **Network Policies**: Restrict container communication
- **Image Security**: Use verified MCP server images
- **Audit Logging**: Monitor MCP server interactions

## ? Real-world Use Cases

1. **AI-Enhanced DevOps**: Automated deployment and monitoring
2. **Smart Documentation**: Dynamic documentation generation
3. **Code Analysis**: Automated code review and suggestions
4. **Project Management**: AI-powered task management and planning
5. **Testing Automation**: Intelligent test generation and execution

## ?? What's Next?

After completing v2.0, advance to:
- **v3.0**: Advanced Topics & Production Deployment
- **Specialized Tracks**: Industry-specific MCP implementations
- **Community Projects**: Contribute to open-source MCP servers

---

*Module created by: Ajeet Singh Raina, Docker Captain*
*Special thanks to the Anthropic MCP team and Docker Inc for MCP Toolkit development*