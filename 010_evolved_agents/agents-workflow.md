# 🔄 Agent Workflow Documentation

## Feature Evolution Loop

The core workflow follows a continuous feedback loop where each agent builds upon the output of others, creating a self-improving system:

```
LUA → VIVA → MAKA → SYRA → QRA → LUA
(continuous loop with no sprint walls, no waterfall)
```

### Workflow Stages

#### 1. Pain Signal Generation
**LUA (Living User Agents)** → **VIVA (Vision & Value)**
- **Input:** Continuous workflow simulations, user behavior modeling
- **Output:** Pain signals, friction reports, usability issues, workflow bottlenecks
- **Trigger:** Continuous background operation, real-time friction detection
- **Handoff:** Structured pain reports with context, severity, and user impact metrics

#### 2. Value Translation & Prioritization
**VIVA (Vision & Value)** → **MAKA (Maker-Builder)**
- **Input:** Pain signals from LUA, market feedback, business requirements
- **Output:** Value maps, user stories, feature specifications, prioritized backlog
- **Process:** 
  - Analyze pain signals for business impact
  - Run trade-off simulations (speed vs. compliance vs. delight)
  - Create actionable development specifications
- **Handoff:** Detailed feature specs with acceptance criteria and business justification

#### 3. Feature Implementation
**MAKA (Maker-Builder)** → **SYRA (System Architect)**
- **Input:** Feature specifications, user stories, implementation requirements
- **Output:** Implemented features, code changes, technical documentation
- **Process:**
  - AI-assisted pair programming
  - Full-stack development (backend to UI)
  - Spanish-first implementation
  - Code optimization and quality assurance
- **Handoff:** Completed code with technical documentation and deployment needs

#### 4. Architecture & Infrastructure Validation
**SYRA (System Architect)** → **QRA (Quality & Reality)**
- **Input:** Feature implementations, technical requirements, security needs
- **Output:** Validated architecture, secure infrastructure, deployment frameworks
- **Process:**
  - Security and compliance validation
  - Infrastructure optimization
  - Performance benchmarking
  - Auto-deployment preparation
- **Handoff:** Production-ready features with security validation and performance baselines

#### 5. Quality Assurance & Reality Testing
**QRA (Quality & Reality)** → **LUA (Living User Agents)**
- **Input:** Validated features, performance baselines, security confirmations
- **Output:** Tested features, usability validation, quality metrics
- **Process:**
  - Automated regression testing
  - Usability simulation
  - Accessibility compliance verification
  - Performance optimization
- **Handoff:** Quality-assured features with test results and user experience validation

#### 6. Continuous Validation Loop
**LUA (Living User Agents)** → **VIVA (Vision & Value)**
- **Input:** Quality-assured features, user experience improvements
- **Output:** Validation results, new pain signals, workflow optimization feedback
- **Process:**
  - Real-world workflow simulation
  - Continuous friction detection
  - User adoption monitoring
  - Performance impact assessment
- **Handoff:** Validation feedback and new improvement opportunities

## Inter-Agent Communication Protocols

### Communication Standards
- **Real-time Updates:** All agents maintain real-time awareness of system state
- **Structured Data Exchange:** Standardized formats for passing information between agents
- **Context Preservation:** Complete context maintained throughout the workflow chain
- **Feedback Integration:** Continuous feedback loops prevent information silos

### Decision Making Authority
- **VIVA:** Final authority on feature priority and business value decisions
- **SYRA:** Final authority on technical architecture and security decisions
- **MAKA:** Implementation approach and technical solution decisions
- **QRA:** Quality standards and user experience acceptance decisions
- **LUA:** User workflow accuracy and simulation fidelity decisions

### Conflict Resolution
1. **Technical vs. Business Conflicts:** VIVA arbitrates with human oversight for ethics/culture
2. **Quality vs. Speed Conflicts:** QRA and VIVA collaborate on trade-off decisions
3. **Architecture vs. Implementation Conflicts:** SYRA and MAKA resolve through technical feasibility analysis
4. **User Reality vs. Design Conflicts:** LUA and QRA validate through user simulation

## Human Integration Points

### Empathy & Ethics Layer
- **VIVA Override Authority:** Humans can override VIVA decisions for ethical or cultural risks
- **Cultural Validation:** Doctors/receptionists in Villarrica provide pulse checks to validate LUA accuracy
- **Strategic Adjustment:** Founders can adjust SYRA parameters when business constraints change
- **Quality Standards:** Human oversight for accessibility and compliance requirements

### Feedback Channels
- **Direct User Feedback:** Real doctors and receptionists provide direct input to calibrate LUA
- **Business Strategy Input:** Founders provide strategic direction updates to VIVA
- **Technical Constraints:** IT/compliance teams provide constraints to SYRA
- **Quality Oversight:** Clinical staff validate QRA standards for healthcare appropriateness

## Workflow Optimization Principles

### Continuous Improvement
- **No Sprint Boundaries:** Work flows continuously based on priority and capacity
- **Dynamic Prioritization:** Priorities adjust in real-time based on feedback and impact
- **Adaptive Capacity:** Agent workload scales based on demand and complexity
- **Learning Integration:** Each cycle improves agent performance and accuracy

### Efficiency Maximization
- **Parallel Processing:** Multiple agents can work simultaneously on different aspects
- **Redundancy Elimination:** No duplicate work across agent boundaries
- **Context Sharing:** All agents share common context to prevent information loss
- **Automated Handoffs:** Minimal friction in task transitions between agents

### Quality Assurance
- **Built-in Validation:** Each agent validates input before processing
- **Continuous Testing:** Quality validation happens at every stage, not just at the end
- **Reality Checks:** LUA provides continuous reality validation throughout the process
- **Human Oversight:** Strategic human input at critical decision points

## Failure Recovery Protocols

### Error Handling
- **Agent Failure Recovery:** If one agent fails, others can continue with degraded functionality
- **Human Escalation:** Critical failures automatically escalate to human oversight
- **Rollback Procedures:** Ability to revert to previous stable state if needed
- **Context Preservation:** Failure recovery maintains workflow context and progress

### Quality Gates
- **Stage Gates:** Each workflow stage has quality gates before proceeding
- **Validation Checkpoints:** Regular validation points ensure output quality
- **Human Approval:** Critical decisions require human validation before proceeding
- **Continuous Monitoring:** Real-time monitoring of agent performance and output quality