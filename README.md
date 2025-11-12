# Oncall-Adrenaline-Converter

> Turns pager anxiety into incident retrospectives

## Overview

The Oncall-Adrenaline-Converter is a blockchain-based system built on the Stacks blockchain using Clarity smart contracts. This project transforms the chaotic experience of on-call engineering into structured, actionable retrospectives and predictive analytics.

## Purpose

When engineers are on-call, they face constant uncertainty about system health and potential incidents. This project provides two core capabilities:

1. **Post-Incident Documentation**: Automatically structure and store incident postmortems with key learnings
2. **Predictive Alerting**: Track and predict system behavior patterns to reduce surprise incidents

## Smart Contracts

### postmortem-lorem-ipsum

Pre-fills 'we'll improve monitoring' sections - A contract for managing incident retrospectives and postmortem documentation. It provides structured storage for incident details, root causes, and action items, ensuring teams capture critical learnings from production incidents.

**Key Features:**
- Store incident reports with timestamps and severity levels
- Track action items and improvement suggestions
- Maintain historical record of incidents for pattern analysis
- Immutable audit trail of system failures and responses

### 3am-metric-psychic

Predicts which graph drops right before you sleep - A contract for tracking system metrics and predicting anomalies before they trigger alerts. It helps on-call engineers stay ahead of incidents by identifying patterns in historical data.

**Key Features:**
- Record system metrics and thresholds
- Track anomaly patterns and alert triggers
- Predict potential issues based on historical trends
- Provide early warning signals for degrading systems

## Architecture

This project uses Clarity smart contracts deployed on the Stacks blockchain, ensuring:
- **Immutability**: Incident records cannot be altered or deleted
- **Transparency**: All stakeholders can verify system behavior history
- **Decentralization**: No single point of failure for critical incident data
- **Auditability**: Complete history of system health and incidents

## Technology Stack

- **Language**: Clarity (Smart Contract Language)
- **Blockchain**: Stacks
- **Development Framework**: Clarinet
- **Testing**: Clarinet Test Suite

## Getting Started

### Prerequisites

- [Clarinet](https://github.com/hirosystems/clarinet) installed
- Node.js and npm (for package dependencies)
- Git

### Installation

```bash
# Clone the repository
git clone <repository-url>
cd Oncall-Adrenaline-Converter

# Install dependencies
npm install

# Check contract syntax
clarinet check

# Run tests
clarinet test
```

### Development

```bash
# Create a new contract
clarinet contract new <contract-name>

# Check all contracts
clarinet check

# Run interactive console
clarinet console
```

## Project Structure

```
Oncall-Adrenaline-Converter/
├── contracts/          # Clarity smart contracts
├── tests/             # Contract test files
├── settings/          # Network configuration
├── Clarinet.toml      # Project configuration
├── package.json       # Node dependencies
└── README.md          # This file
```

## Contract Interaction

### Deploying Contracts

```bash
# Deploy to devnet
clarinet integrate

# Deploy to testnet
clarinet deploy --testnet
```

### Testing

```bash
# Run all tests
clarinet test

# Run specific test file
clarinet test tests/<test-file>.ts
```

## Use Cases

1. **Incident Management Teams**: Store and analyze postmortem data across multiple incidents
2. **Site Reliability Engineers**: Track system patterns to prevent recurring issues
3. **Engineering Leadership**: Review historical incident trends for team planning
4. **Compliance Teams**: Maintain immutable records of system incidents for audits

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Security Considerations

- All contract functions include proper access controls
- Input validation prevents malformed data
- Read-only functions marked appropriately
- No external contract dependencies to minimize attack surface

## Future Enhancements

- Integration with popular monitoring tools (Datadog, New Relic, PagerDuty)
- Machine learning models for incident prediction
- Automated root cause analysis suggestions
- Team rotation scheduling with blockchain verification
- On-call compensation tracking

## License

MIT License - see LICENSE file for details

## Support

For issues, questions, or contributions, please open an issue in the GitHub repository.

## Acknowledgments

Built for on-call engineers who deserve better tools to manage the chaos of production systems.

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
