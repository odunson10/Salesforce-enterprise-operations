# Salesforce Enterprise Operations Management

## Overview

Salesforce Enterprise Operations Management is a portfolio project designed to demonstrate practical Salesforce Administrator skills through real-world enterprise workflows.

The solution combines IT operations, cybersecurity incident management, and employee onboarding into a centralized Salesforce Lightning application using custom objects, relationships, Flow automation, validation rules, reports, and dashboards.

## Completed Modules

### 1. IT Help Desk

Designed an internal IT support solution for submitting, assigning, tracking, escalating, and reporting on employee support requests.

Key features:

- Custom Support Ticket object
- Employee and Department relationships
- Ticket assignment and status tracking
- SLA Due Date automation
- Scheduled SLA escalation
- Resolution Notes validation
- Priority-based reporting
- Technician workload reporting
- IT Help Desk Dashboard

[View IT Help Desk Documentation](01-it-help-desk/README.md)

---

### 2. Security Incident Management

Built a cybersecurity incident tracking solution to manage incidents from reporting through investigation, escalation, containment, and resolution.

Key features:

- Custom Security Incident object
- Severity and incident classification
- Employee assignment relationships
- Resolution documentation validation
- Automatic escalation of unresolved High and Critical incidents
- Positive and negative Flow testing
- Security incident reports
- Security Operations Dashboard

[View Security Incident Management Documentation](02-security-incident-management/README.md)

---

### 3. Employee Onboarding

Developed an employee onboarding workflow to track new-hire setup, equipment provisioning, training, approvals, and completion.

Key features:

- Custom Employee Onboarding object
- Employee, Department, and Manager relationships
- Equipment and training tracking
- Completion validation rules
- Automated Completion Date
- Onboarding status reporting
- Department and manager workload reporting
- Employee Onboarding Dashboard

[View Employee Onboarding Documentation](03-employee-onboarding/README.md)

---

## Salesforce Skills Demonstrated

- Salesforce Lightning Experience
- Custom Objects and Fields
- Lookup Relationships
- Auto Number Fields
- Formula Fields
- Picklists and Multi-Select Picklists
- Validation Rules
- Record-Triggered Flows
- Before-Save Automation
- Scheduled Paths
- Decision Logic
- Assignment Elements
- Update Records
- Custom Report Types
- Reports
- Dashboards
- Lightning App Configuration
- Data Modeling
- Business Process Automation
- Workflow Testing

## Solution Architecture

The application uses shared enterprise objects to support multiple operational workflows.

```text
Department
|
+---- Employee
|
+---- Support Ticket
|
+---- Security Incident
|
+---- Employee Onboarding
```

## Automation Highlights

### IT Help Desk SLA Automation

Support Ticket due dates are automatically calculated based on priority:

- Critical — 4 hours
- High — 8 hours
- Medium — 24 hours
- Low — 48 hours

A scheduled Flow evaluates unresolved tickets at their SLA Due Date and automatically marks them as escalated.

### Security Incident Escalation

High and Critical severity incidents are automatically escalated when they remain unresolved.

### Employee Onboarding Completion

Salesforce prevents onboarding records from being marked Completed until required onboarding tasks are finished.

Once onboarding is completed, Salesforce automatically populates the Completion Date.

## Testing

Each module includes functional testing to verify:

- Validation rules
- Flow decisions
- Record updates
- Escalation behavior
- Positive and negative test scenarios
- Dashboard and report accuracy

## Dashboards

The project includes:

- IT Help Desk Dashboard
- Security Operations Dashboard
- Employee Onboarding Dashboard

These dashboards provide visibility into operational workload, ticket severity, escalations, onboarding progress, and team assignments.

## Project Status

### Completed

- IT Help Desk
- Security Incident Management
- Employee Onboarding

### Future Enhancements

Potential future modules include:

- Asset Management
- Sales Pipeline CRM
- Database Change Management

## Business Value

This project demonstrates how Salesforce can be used beyond traditional CRM to support enterprise operations through automation, data quality controls, centralized reporting, and role-based business processes.

The solution reduces manual processing, improves data consistency, provides operational visibility, and standardizes workflows across multiple departments.
