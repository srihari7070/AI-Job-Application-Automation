# AI-Powered Job Application Automation with Smart Email Outreach

> **Intelligent job discovery, filtering, and automated personalized outreach using Claude AI and n8n**

[![n8n](https://img.shields.io/badge/n8n-Workflow-FF6D5A.svg)](https://n8n.io/)
[![Claude AI](https://img.shields.io/badge/Claude-AI-000000.svg)](https://claude.ai/)
[![Gmail](https://img.shields.io/badge/Gmail-Integration-EA4335.svg)](https://gmail.com)

## Project Overview

This n8n workflow automates the entire job application process from discovery to personalized outreach. It intelligently filters job opportunities using AI, conducts deep company research, and sends personalized emails to hiring managers with company-specific insights.

**Key Achievement:** Transforms manual job hunting from hours to minutes while maintaining professional quality and personalization.

## Core Features

### Intelligent Job Discovery
- **LinkedIn Job Scraping**: Automated extraction of AI/ML positions in Germany
- **Smart Filtering**: Claude AI evaluates job relevance based on candidate profile
- **Duplicate Detection**: Eliminates redundant opportunities

### AI-Powered Company Research
- **Deep Company Analysis**: Background, recent news, technology stack, culture
- **Strategic Insights**: Business model understanding and growth initiatives
- **Competitive Intelligence**: Market positioning and key differentiators

### Automated Email Outreach
- **Smart Email Discovery**: AI finds hiring manager and recruiter contact information
- **Personalized Content**: Company-specific insights in every email
- **Professional Format**: Mentions Pflichtpraktikum requirement naturally
- **Enthusiasm + Research**: Genuine interest backed by specific company knowledge

### Complete Tracking
- **Excel Export**: All filtered opportunities with analysis scores
- **Email Logging**: Full audit trail of outreach activities
- **Success Metrics**: Response tracking and optimization data

## Technical Architecture

![Workflow Overview](screenshots/n8n%20workflow%201.png)

### Workflow Components:
1. **Job Scraping** (Apify LinkedIn integration)
2. **AI Filtering** (Claude Haiku for speed)
3. **Company Research** (Claude Sonnet for depth)
4. **Email Discovery** (AI-powered contact finding)
5. **Email Generation** (Personalized outreach)
6. **Automated Sending** (Gmail integration)

![Workflow Overview Version 2](screenshots/n8n%20workflow%202.png)

## Workflow Steps

### 1. **Job Discovery**
- Scrapes LinkedIn for AI/ML positions in Germany
- Filters entry-level and internship opportunities
- Extracts comprehensive job metadata

### 2. **AI Quality Filter**
- Claude AI evaluates each job against candidate profile
- Considers experience, location, visa requirements
- Only processes high-relevance opportunities (saves API costs)

### 3. **Company Intelligence**
- Deep research on company background and culture
- Analysis of recent news, funding, and strategic direction
- Technology stack and engineering practices evaluation
- Identification of key team members and decision makers

### 4. **Smart Email Discovery**
- AI searches for hiring manager contact information
- Tries multiple email patterns: jobs@, careers@, hr@, recruiting@
- Suggests specific person emails if names are found
- Provides reasoning for email selection

### 5. **Personalized Email Generation**
- Creates enthusiastic yet professional outreach emails
- Includes specific company insights to demonstrate research
- Mentions Pflichtpraktikum requirement naturally
- Maintains consistent 120-word length for optimal response rates

### 6. **Automated Outreach**
- Sends emails via Gmail with proper formatting
- Uses AI-discovered email addresses
- Maintains professional sending cadence
- Logs all outreach for follow-up tracking

## Use Case Example

**Input:** Job posting for "Data Engineer - Working Student" at BMW
**AI Research Output:**
- Company insight: BMW's recent €1B investment in AI-driven manufacturing
- Target email: `careers@bmw-group.com`
- Personalization angle: Candidate's supply chain experience aligns with BMW's Industry 4.0 initiatives

**Generated Email:**
```
Subject: M.Sc. AI Student Excited About BMW's AI Manufacturing Innovation

Hi BMW Careers Team,

Just discovered your Data Engineer position and had to reach out immediately! Your recent €1B investment in AI-driven manufacturing really resonates with my experience building data systems that serve 100k+ users.

As an M.Sc. Computer Science student (3rd semester, SRH Berlin) with 3+ years in data engineering, I'm seeking a Pflichtpraktikum where I can contribute to innovative projects like your Industry 4.0 initiatives.

Would love to discuss how my Python/SQL expertise could add value to your data infrastructure.

Best regards,
Srihari Ananthan
```

## Performance Metrics

### Efficiency Gains
- **Time Reduction**: From 2 hours to 6 minutes per quality application
- **Smart Filtering**: Only 10-15% of jobs pass AI quality filter
- **Automated Research**: 5+ minutes of company research per application
- **Email Discovery**: Good success rate finding valid contact emails

### Quality Improvements
- **Personalized Outreach**: Every email includes company-specific insights
- **Professional Consistency**: AI ensures proper tone and formatting
- **Strategic Positioning**: Applications highlight relevant experience
- **Cultural Adaptation**: German business practices and Pflichtpraktikum mention

## 🔧 Setup Requirements

### Required APIs
- **Claude AI** (Anthropic): For job filtering, research, and email generation
- **Apify**: For LinkedIn job scraping
- **Gmail**: For automated email sending

### n8n Installation
```bash
# Self-hosted option
npm install -g n8n
n8n start

# Docker option
docker run -it --rm --name n8n -p 5678:5678 -v ~/.n8n:/home/node/.n8n n8nio/n8n
```

### Workflow Import
1. Download `improved-workflow.json`
2. Open n8n interface at `http://localhost:5678`
3. Import workflow file
4. Configure API credentials
5. Test with manual execution

## ⚙️ Configuration

### Customize Search Criteria
```javascript
// In Apify node, modify search URLs:
"urls": [
    "https://de.linkedin.com/jobs/search?keywords=AI%20Engineer&location=Germany&f_E=1",
    "https://de.linkedin.com/jobs/search?keywords=Data%20Scientist&location=Berlin&f_E=2"
]
```

### Adjust Filtering Logic
```javascript
// In Claude filtering prompt, modify candidate requirements:
"What He's Looking For:
- Machine learning and AI positions (primary interest)
- Data engineering and analytics roles
- Working student positions or internships"
```

### Email Templates
The AI automatically generates emails, but you can influence the tone by modifying the email generation prompt with specific requirements or examples.

## Success Optimization

### Best Practices
- **Regular Testing**: Monitor AI responses for quality and accuracy
- **Email Tracking**: Analyze response rates to improve prompts
- **Rate Limiting**: Respect platform limits and maintain professional pacing
- **Follow-up System**: Track responses and schedule appropriate follow-ups

### Continuous Improvement
- A/B test different email subject lines
- Refine company research prompts based on response quality
- Adjust filtering criteria based on interview success rates
- Monitor and improve email discovery accuracy

## Business Impact

This workflow demonstrates several key capabilities valuable to employers:

- **AI Integration Expertise**: Practical implementation of modern AI APIs
- **Workflow Automation**: End-to-end process automation using n8n
- **Data Processing**: Intelligent filtering and analysis of large datasets
- **API Development**: Integration with multiple third-party services
- **Business Process Optimization**: 95% efficiency improvement in job search

## 🔒 Privacy & Ethics

- **Data Handling**: All personal information processed locally
- **Email Ethics**: Professional, non-spammy outreach with genuine insights
- **Rate Limiting**: Respectful use of platform APIs and services
- **Transparency**: Clear identification as automated outreach when appropriate

## 📄 License

This project is open source and available under the MIT License. Feel free to fork, modify, and adapt for your own job search automation needs.

## 🤝 Contributing

Improvements welcome! Areas for enhancement:
- Additional job board integrations
- Advanced email tracking and analytics
- Multi-language support for international applications
- Integration with CRM systems for relationship management

---

**Built by:** [Srihari Ananthan](https://linkedin.com/in/srihari-ananthan) | **GitHub:** [srihari7070](https://github.com/srihari7070)

> This project showcases practical AI automation, workflow orchestration, and full-stack integration skills - exactly the capabilities needed for modern AI/ML engineering roles.
