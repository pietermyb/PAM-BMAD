# Analyze Solution Against Principles

## Purpose
Analyze and evaluate solution designs against principles and enterprise architecture standards to ensure compliance, alignment, and adherence to architectural best practices.

## Context
This task provides systematic evaluation of solution designs against established principles to ensure architectural consistency, compliance with standards, and alignment with enterprise strategy. It helps identify potential issues early and ensures solutions follow established architectural patterns.

## Workflow

### 1. Solution Design Review
- **Solution Documentation Analysis**
  - Review solution architecture documents
  - Analyze design patterns and approaches
  - Evaluate technology choices and rationale
  - Assess integration patterns and interfaces
  - Review data architecture and flows

- **Solution Context Understanding**
  - Business requirements and objectives
  - Functional and non-functional requirements
  - Stakeholder needs and expectations
  - Technical constraints and dependencies
  - Implementation timeline and resources

### 2. Principles Mapping and Analysis
- **Principles Evaluation**
  - Map solution components to applicable principles
  - Evaluate compliance with each relevant principle
  - Identify principle violations or gaps
  - Assess principle implementation approaches
  - Document principle alignment rationale

- **Enterprise Standards Compliance**
  - Technology standards compliance
  - Security standards adherence
  - Integration standards validation
  - Data standards compliance
  - Operational standards verification

### 3. Architectural Framework Analysis
- **TOGAF Compliance Assessment**
  - Business architecture alignment
  - Information systems architecture compliance
  - Technology architecture adherence
  - Architecture governance compliance
  - TOGAF artifact completeness

- **Zachman Framework Mapping**
  - Map solution to Zachman perspectives
  - Evaluate artifact completeness
  - Assess framework coverage
  - Identify missing artifacts
  - Validate framework alignment

- **EAP Methodology Validation**
  - Strategic alignment assessment
  - Capability mapping validation
  - Technology planning compliance
  - Implementation approach validation
  - Governance framework adherence

### 4. Detailed Principle Analysis
- **Business Architecture Principles (BP-BA)**
  - **BP-BA-1 Industry Standards**: Evaluate alignment with industry standards
  - **BP-BA-2 Data Autonomy**: Assess data autonomy and independence

- **Data Architecture Principles (BP-DA)**
  - **BP-DA-1 Unified Data Model**: Validate unified data model approach
  - **BP-DA-2 Data as Product**: Assess data productization strategy
  - **BP-DA-3 Responsible AI**: Evaluate AI/ML responsible usage

- **Platform Component Architecture (BP-PCA)**
  - **BP-PCA-1 Coherent Platform**: Assess platform coherence
  - **BP-PCA-2 Component Standards**: Validate component standardization
  - **BP-PCA-3 Localizable Capabilities**: Evaluate localization support
  - **BP-PCA-4 Employee Persona**: Assess employee experience consideration
  - **BP-PCA-5 Composable Functionality**: Validate composability approach
  - **BP-PCA-6 Configure Extend Build**: Assess configuration strategy
  - **BP-PCA-7 Headless Architecture**: Validate headless approach
  - **BP-PCA-8 Design for Production**: Assess production readiness

- **Technology Architecture (BP-TA)**
  - **BP-TA-1 Governed Technology**: Validate technology governance
  - **BP-TA-2 Multi-tenancy**: Assess multi-tenancy design

- **Engagement Management (EM)**
  - **EM-BA-1 Engagement Banking**: Validate engagement banking approach
  - **EM-DA-1 Golden Data Sync**: Assess data synchronization
  - **EM-PCA-1 Replaceable Orchestration**: Validate orchestration replaceability
  - **EM-PCA-2 Single Flow Per Type**: Assess flow separation

- **Integration (I-PCA)**
  - **I-PCA-1 Replaceable Integration**: Validate integration replaceability
  - **I-PCA-2 Out of Box Integration**: Assess default integration
  - **I-PCA-3 Platform Orchestration**: Validate platform orchestration

- **Identity and Access Management (IAM-SA)**
  - **IAM-SA-01 Standards Based Auth**: Validate authentication standards
  - **IAM-SA-02 Selective Identity Flexibility**: Assess identity flexibility

### 5. Compliance Scoring and Assessment
- **Principle Compliance Scoring**
  - Full compliance (Green)
  - Partial compliance (Yellow)
  - Non-compliance (Red)
  - Not applicable (Gray)

- **Risk Assessment**
  - High-risk principle violations
  - Medium-risk compliance gaps
  - Low-risk recommendations
  - Compliance opportunities

- **Impact Analysis**
  - Business impact of compliance gaps
  - Technical impact of violations
  - Operational impact assessment
  - Strategic alignment impact

### 6. Recommendations and Remediation
- **Compliance Recommendations**
  - Specific actions to achieve compliance
  - Alternative approaches and solutions
  - Best practice recommendations
  - Implementation guidance

- **Remediation Planning**
  - Priority-based remediation plan
  - Resource requirements for fixes
  - Timeline for compliance achievement
  - Success criteria and metrics

- **Alternative Solutions**
  - Compliant alternative approaches
  - Technology alternatives
  - Architecture pattern alternatives
  - Integration approach alternatives

## Outputs
1. **Principle Compliance Report** - Detailed analysis of solution against principles
2. **Compliance Scorecard** - Visual representation of compliance status
3. **Risk Assessment Report** - Analysis of compliance risks and impacts
4. **Remediation Plan** - Actionable plan to achieve compliance
5. **Recommendations Document** - Specific recommendations for improvement

## Success Criteria
- Comprehensive evaluation against all applicable principles
- Clear identification of compliance gaps and violations
- Actionable recommendations for improvement
- Stakeholder alignment on compliance requirements
- Clear path to achieve full compliance

## Dependencies
- Solution design documentation
- PAM principles and standards
- Enterprise architecture standards
- Stakeholder requirements and constraints
- Technical and business context

## Risks and Mitigation
- **Risk**: Incomplete solution documentation
  - **Mitigation**: Request additional documentation and clarification

- **Risk**: Subjective principle interpretation
  - **Mitigation**: Use objective criteria and stakeholder validation

- **Risk**: Overly strict compliance requirements
  - **Mitigation**: Balance compliance with practical implementation

- **Risk**: Insufficient stakeholder engagement
  - **Mitigation**: Proactive stakeholder communication and validation

## Related Tasks
- `analyze-current-state.md` - Understanding current architecture baseline
- `create-target-state.md` - Defining compliant target architecture
- `gap-analysis.md` - Identifying compliance gaps
- `document-enterprise.md` - Comprehensive enterprise documentation 