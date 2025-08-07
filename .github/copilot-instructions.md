# Copilot Instructions for Health Tech ISMS Policy Repository

## Project Overview
This is a **Jekyll-based documentation site** containing **SOC 2 and HIPAA/HITECH** compliant Information Security Management System (ISMS) policy and procedure templates for health tech companies. The content is structured as **template documents with placeholder values** that organizations customize for their specific needs. Documents use **enterprise auditor-grade language** while remaining accessible to all organizational stakeholders.

## Architecture & Structure

### Content Organization
- **Jekyll Collections**: Each domain has separate `_[domain]_policies/` and `_[domain]_procedures/` directories
- **Naming Convention**: Files use format `[DOMAIN]-[TYPE]-[###].md` (e.g., `AC-POL-001.md`, `SEC-PROC-005.md`)
- **Templates**: Located in `/Templates/` - serve as base structure for new documents
- **Navigation**: Main categories defined via parent pages (`Security.md`, `Access Control.md`) with `has_children: true`

### Document Structure Pattern
Every policy/procedure follows a strict template:
```yaml
---
title: [Document Title] ([Document ID])
parent: [Domain] [Policies|Procedures]
nav_order: [number]
---
```

**Policies** always include:
1. Objective, 2. Scope, 3. Policy (with numbered subsections), 4. Standards Compliance, 5. Definitions, 6. Responsibilities

**Procedures** always include:
1. Purpose, 2. Scope, 3. Overview, 4. Procedure (step table format), 5. Standards Compliance

## Key Development Patterns

### Placeholder System
- All customizable values use `**[Bracket Format]**` (e.g., `**[Company Name]**`, `**[Number, e.g., 90]**`)
- Duration placeholders include examples: `**[Duration, e.g., 15 minutes]**`
- Role placeholders specify context: `**[Role Title, e.g., Security Officer]**`

### Standards Compliance Tables
Every document maps requirements to regulatory frameworks, emphasizing **SOC 2 Trust Services Criteria**:
```markdown
| **Policy Section** | **Standard/Framework** | **Control Reference** |
| ------------------ | ---------------------- | --------------------- |
| **3.2, 3.5**       | SOC 2 Trust Services Criteria | CC6.1 - Logical Access Security |
| **3.2, 3.5**       | HIPAA Security Rule    | 45 CFR § 164.312(a)(1) |
```

### Procedure Step Tables
All procedures use consistent tabular format:
```markdown
| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1**    | [Role]  | [Action] |
```

## Development Workflows

### Adding New Documents
1. Copy appropriate template from `/Templates/`
2. Follow naming convention: `[PREFIX]-[TYPE]-[###].md`
3. Update frontmatter with correct parent collection
4. Replace template placeholders with domain-specific content
5. Add compliance mappings in standards table

### Local Development
```bash
bundle install
bundle exec jekyll serve
# Site available at http://localhost:4000/health-tech
```

### Collection Management
Each domain requires two collections in `_config.yml`:
- `[domain]_policies` and `[domain]_procedures`
- Both need `output: true` and `permalink: /:collection/:path/`
- Defaults section must specify `layout: "page"` for each collection

## Theme & Styling Architecture

### Jekyll Configuration (`_config.yml`)
- **Base Theme**: Hydejack v9.2.1 via `remote_theme: "hydecorp/hydejack@v9.2.1"`
- **Color Scheme**: Solid gray accent `#bababa` for professional appearance
- **Typography**: Latin Modern Roman font family for academic/legal document aesthetic
- **Navigation**: Custom `sidebar_links` configuration for main domain categories

### Custom Font Implementation
Located in `_includes/my-head.html` and `/assets/fonts/`:
```html
@font-face {
    font-family: 'Latin Modern Roman';
    src: url('/health-tech/assets/fonts/latinmodernroman_10regular_macroman/lmroman10-regular-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;
    font-display: swap;
}
```
- **Font Variants**: Regular, Bold, Italic, Bold-Italic
- **Global Override**: `* { font-family: 'Latin Modern Roman', serif !important; }`
- **Icon Font Exception**: Preserves `icomoon` for social media icons

### Visual Design System (`_sass/my-style.scss`)
- **Sidebar**: Dark gray with 40% transparency (`rgba(64, 64, 64, 0.4)`)
- **Backdrop Effects**: `backdrop-filter: blur(10px)` with rounded corners (`border-radius: 8px`)
- **Color Scheme**: 
  - Main content: Black text (`#000`) on white background
  - Sidebar: White text on translucent dark background
  - Accent: `#bababa` for links and highlights
- **Typography**: Line height 1.6 for readability, letter-spacing 0.5px for headings

### Layout Overrides
- **Title Suppression**: `hide_title: true` and `no_page_title: true` in defaults
- **Content Structure**: Forces all collections to use `layout: "page"`
- **Print Styles**: Removes sidebar/navigation, adds URL references for links

## Content Guidelines

### HITRUST CSF Compliance Focus
- **Primary Framework**: HITRUST Common Security Framework (CSF) v11.2.0 with detailed control mappings
- **Control Domains**: Information Protection (01), Endpoint Protection (02), Portable Media Security (03), Mobile Device Security (04), Wireless Network Security (05), Configuration Management (06), Vulnerability Management (07), Network Protection (08), Transmission Protection (09), Password Protection (10), Access Control (11), Audit Logging and Monitoring (12), Education, Training and Awareness (13), Third Party Assurance (14), Incident Response (15), Business Continuity Management (16), Risk Management (17), Physical and Environmental Security (18), Data Protection and Privacy (19)
- **Control References**: Use specific format `01.a - Information Security Management Program` with descriptive titles
- **Maturity Levels**: Documents address Implementation (Level 1), Management (Level 2), and Oversight (Level 3) requirements
- **Assessment Readiness**: Content structured to support HITRUST validated assessments and certifications

### SOC 2 Compliance Focus
- **Primary Framework**: SOC 2 Trust Services Criteria with detailed control mappings
- **Trust Services Categories**: Security (CC6.x), Availability (A1.x), Confidentiality (C1.x), Processing Integrity (PI1.x)
- **Control References**: Use specific format `CC6.1 - Logical Access Security` with descriptive titles
- **Auditor Language**: Documents written at senior enterprise auditor level with formal compliance terminology

### Language & Tone Standards
- **Accessibility**: Complex compliance concepts explained clearly for all organizational levels
- **Precision**: Use specific regulatory citations (e.g., "45 CFR § 164.312(a)(1)")
- **Authority**: Declarative statements using "shall" for mandatory requirements
- **Examples**: 
  - Enterprise: "Administrative access shall be granted on a limited, as-needed basis"
  - Accessible: "For accounts with the highest level of administrative privilege (e.g., 'root' or 'global administrator')"

### HIPAA/HITECH Integration
- All policies reference **ePHI (electronic Protected Health Information)**
- Business Associate Agreement (BAA) requirements for third parties
- Specific timing requirements for high-risk scenarios (e.g., immediate access revocation)

### Template Customization
- Never remove placeholder brackets from template files
- Maintain section numbering consistency across related documents
- Keep compliance mapping tables accurate and complete
- Preserve formal tone and legal language structure

### Cross-References
- Policies reference other policies by ID: "as defined in the Password Policy (SEC-POL-002)"
- Procedures reference parent policies in scope/overview sections
- Maintain document hierarchy: supplements → policies → procedures

## Integration Points
- **GitHub Pages**: Auto-deploys via Jekyll when pushed to main branch
- **Jekyll Collections**: Content organization via `_config.yml` collections
- **Navigation**: Automatic via frontmatter `parent` and `nav_order` properties
- **Styling**: Custom SCSS in `_sass/` overrides default theme

When editing documents, preserve the formal compliance language and maintain consistency with established templates and naming patterns.
