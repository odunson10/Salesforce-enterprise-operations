# Employee Onboarding — Salesforce Portfolio Module

## Overview

The Employee Onboarding module was built in Salesforce Lightning to manage new-hire onboarding from initial setup through training, equipment provisioning, manager approval, and completion.

## Business Requirements

The solution needed to:

- Track new employee onboarding in one centralized system.
- Associate onboarding records with employees, departments, and managers.
- Track required equipment and training.
- Prevent onboarding from being marked Completed until required tasks are finished.
- Automatically populate the Completion Date when onboarding is completed.
- Provide reporting and dashboard visibility into onboarding progress.

## Salesforce Object

### Employee Onboarding

Key fields include:

- Onboarding Number
- Employee
- Department
- Manager
- Start Date
- Onboarding Status
- Job Title
- Work Location
- Equipment Required
- Training Required
- Onboarding Notes
- Laptop Provisioned
- Badge Issued
- Training Completed
- Manager Approved
- Completion Date

## Validation Rule

A validation rule prevents an onboarding record from being marked Completed unless all required completion tasks are finished.

Required tasks include:

- Laptop Provisioned
- Badge Issued
- Training Completed
- Manager Approved

## Automation

### Set Onboarding Completion Date

A record-triggered Flow runs when an Employee Onboarding record is created or updated with:

- Onboarding Status = Completed

The Flow automatically sets:

- Completion Date = Current Date

## Testing

### Validation Rule Test

An onboarding record was set to Completed while Manager Approved remained unchecked.

Salesforce blocked the save and displayed the validation error.

After Manager Approved was checked, the record saved successfully.

### Completion Date Automation Test

A completed onboarding record was created with all required tasks checked.

The Flow automatically populated the Completion Date.

## Reports

Created reports include:

- Employee Onboarding by Status
- Employee Onboarding by Department
- Completed Employee Onboardings
- Employee Onboarding by Manager

## Dashboard

The Employee Onboarding Dashboard provides:

- Onboarding distribution by status
- Onboarding workload by department
- Completed onboarding count
- Onboarding workload by manager
