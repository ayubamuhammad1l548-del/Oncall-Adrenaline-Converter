## Overview

This PR introduces two smart contracts that transform on-call incident management into structured, blockchain-backed retrospectives with predictive analytics capabilities.

## Changes

### New Contracts

#### 1. `postmortem-lorem-ipsum`
A comprehensive incident retrospective management system that provides:

- **Template System**: Create reusable postmortem templates with customizable sections
- **Retrospective Generation**: Generate incident retrospectives from templates with automatic tracking
- **Action Item Management**: Track follow-up tasks with assignees and due dates
- **Status Tracking**: Monitor retrospective completion status
- **Immutable Audit Trail**: All incident data stored permanently on-chain

**Key Functions:**
- `create-template` - Create new postmortem templates
- `add-template-section` - Define template sections with content and ordering
- `create-retrospective` - Generate a new retrospective from a template
- `update-retrospective-section` - Fill in retrospective sections
- `add-action-item` - Create follow-up action items
- `complete-action-item` - Mark actions as completed
- `update-retrospective-status` - Change retrospective status (draft/completed/etc.)

**Data Structures:**
- Templates with metadata (name, creator, description, status)
- Template sections with ordering and required flags
- Retrospectives with incident details and severity levels
- Action items with assignees and due dates

#### 2. `am3-metric-psychic`
A predictive monitoring system that helps prevent 3am alerts through pattern analysis:

- **Metric Recording**: Store system metrics with thresholds and anomaly detection
- **Alert Management**: Define and track alert conditions
- **Predictive Analytics**: Create predictions based on historical patterns
- **Threshold Configuration**: Set warning and critical thresholds per metric type
- **Alert Acknowledgment**: Track who acknowledged which alerts

**Key Functions:**
- `record-metric` - Log system metrics with automatic anomaly detection
- `create-alert-definition` - Define alerting rules
- `trigger-alert` - Record alert triggers when thresholds are exceeded
- `acknowledge-alert` - Mark alerts as acknowledged
- `create-prediction` - Generate predictions with confidence scores
- `set-system-threshold` - Configure warning and critical thresholds

**Data Structures:**
- Metrics with values, thresholds, and metadata
- Metric history for pattern analysis
- Alert definitions with activation status
- Alert triggers with acknowledgment tracking
- Predictions with confidence scores and validation

### Technical Details

**Language:** Clarity (Smart Contract Language for Stacks blockchain)

**Clarity Version:** 3

**Lines of Code:**
- `postmortem-lorem-ipsum.clar`: 268 lines
- `am3-metric-psychic.clar`: 323 lines

**Validation:** Both contracts pass `clarinet check` with only expected warnings for unchecked data inputs

### Design Decisions

1. **No Cross-Contract Calls**: Contracts are independent, reducing complexity and attack surface
2. **Access Controls**: Creator-based authorization for modifications
3. **Immutable Records**: Incident data and metrics cannot be deleted
4. **Flexible Sections**: Template system allows customization for different incident types
5. **Timestamp Tracking**: All records include blockchain height for chronological ordering
6. **Optional Fields**: Support for optional assignees and due dates in action items

### Benefits

**For On-Call Engineers:**
- Structured incident documentation reduces cognitive load during stressful events
- Predictive alerts help prevent surprises
- Historical pattern analysis improves system understanding

**For Engineering Teams:**
- Consistent retrospective format across all incidents
- Immutable audit trail for compliance and learning
- Actionable insights from aggregated incident data

**For Organizations:**
- Reduced incident frequency through pattern recognition
- Improved knowledge retention and sharing
- Transparent incident history for stakeholders

## Testing

- [x] Contracts pass `clarinet check` validation
- [x] Syntax is valid Clarity 3
- [x] All functions have proper error handling
- [x] Read-only functions marked appropriately
- [x] Line endings converted to LF (Unix format)

## Configuration Updates

- Updated `Clarinet.toml` with both contract definitions
- Contract names follow Clarity naming conventions
- Clarity version set to 3 for latest features

## Future Enhancements

- Integration with monitoring tools (Datadog, Prometheus, PagerDuty)
- Machine learning model for better predictions
- Aggregate analytics across multiple incidents
- Team rotation and on-call scheduling
- Automated root cause analysis suggestions

## Related Issues

This addresses the core need for structured incident management and proactive monitoring in production systems.

## Deployment Considerations

Both contracts are self-contained with no external dependencies. They can be deployed independently or together. Consider:

- Setting appropriate gas limits for metric recording operations
- Implementing rate limiting for high-frequency metric updates
- Configuring appropriate thresholds for your specific systems
