# Oncall-Adrenaline-Converter

**Turns pager anxiety into incident retrospectives**

## Overview

Oncall-Adrenaline-Converter is a blockchain-based system built on the Stacks blockchain using Clarity smart contracts. This project transforms the stressful experience of on-call incident management into structured, valuable post-incident analysis and documentation.

## Purpose

The system addresses a common problem in DevOps and SRE teams: the anxiety and chaos of on-call incidents often leads to poor documentation and missed learning opportunities. By capturing incident data on-chain and automating retrospective generation, we ensure that every midnight page becomes a learning experience.

## Smart Contracts

### 1. postmortem-lorem-ipsum

Pre-fills the standard sections of incident retrospectives with intelligent templates and suggestions. This contract helps teams quickly structure their post-incident reviews without missing critical elements.

**Key Features:**
- Template management for common incident types
- Automated section generation (timeline, impact, root cause, action items)
- Version control for retrospective templates
- Team-specific customization support

### 2. 3am-metric-psychic

Analyzes historical incident patterns and metrics to predict potential issues before they wake you up. This predictive contract helps teams stay ahead of incidents.

**Key Features:**
- Historical incident pattern analysis
- Metric threshold tracking and prediction
- Alert fatigue reduction through intelligent filtering
- Trend analysis for proactive monitoring improvements

## Architecture

The system consists of two independent smart contracts that work together to transform incident management:

1. **Data Layer**: Both contracts store incident data, metrics, and retrospective information on-chain, ensuring immutability and transparency.

2. **Logic Layer**: Smart contract functions handle template management, pattern recognition, and predictive analytics.

3. **Interface Layer**: External systems can interact with these contracts through standard Clarity function calls.

## Technology Stack

- **Blockchain**: Stacks
- **Smart Contract Language**: Clarity
- **Development Framework**: Clarinet
- **Testing**: Clarinet test suite

## Getting Started

### Prerequisites

- Clarinet installed on your system
- Node.js and npm (for development dependencies)
- Git for version control

### Installation

```bash
# Clone the repository
git clone <repository-url>

# Navigate to project directory
cd Oncall-Adrenaline-Converter

# Check contract syntax
clarinet check

# Run tests
clarinet test
```

### Development

To add or modify contracts:

```bash
# Create a new contract
clarinet contract new <contract-name>

# Check syntax
clarinet check

# Run tests
clarinet test
```

## Contract Interactions

### postmortem-lorem-ipsum

```clarity
;; Create a new retrospective template
(create-template template-name template-content)

;; Generate a retrospective from template
(generate-retrospective incident-id template-id)

;; Update template sections
(update-template-section template-id section-name new-content)
```

### 3am-metric-psychic

```clarity
;; Record incident metrics
(record-incident-metrics incident-id metrics-data)

;; Analyze patterns
(analyze-incident-patterns time-range)

;; Get predictions
(get-alert-predictions metric-type)
```

## Use Cases

1. **Incident Response Teams**: Quickly generate comprehensive post-mortems after incidents
2. **SRE Teams**: Predict potential issues based on historical patterns
3. **DevOps Engineers**: Reduce alert fatigue with intelligent filtering
4. **Engineering Managers**: Track incident trends and team response effectiveness

## Benefits

- **Consistency**: Standardized retrospective format across all incidents
- **Learning**: Transform every incident into documented knowledge
- **Proactive**: Predict issues before they cause outages
- **Transparency**: On-chain record of all incidents and learnings
- **Collaboration**: Team-accessible incident history and patterns

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run `clarinet check` to validate
5. Submit a pull request

## Testing

Run the full test suite:

```bash
clarinet test
```

Run specific test files:

```bash
clarinet test tests/<test-file>.ts
```

## Deployment

To deploy to testnet:

```bash
clarinet deployments generate --testnet
clarinet deployments apply -p <deployment-plan>
```

## License

MIT License - feel free to use this project for your team's incident management needs.

## Support

For questions, issues, or feature requests, please open an issue on GitHub.

## Roadmap

- [ ] Integration with popular monitoring tools (Datadog, Prometheus, etc.)
- [ ] Machine learning model improvements for better predictions
- [ ] Mobile app for on-call engineers
- [ ] Slack/PagerDuty integration
- [ ] Custom metric threshold configuration UI

## Acknowledgments

Built with Clarity on Stacks blockchain, empowering teams to learn from every incident and sleep better at night.

---

*Because every 3am page should lead to a better tomorrow.*
