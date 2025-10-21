# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Release Coordination
The **Release Manager** coordinates the release process and facilitates the release readiness review. Key responsibilities include:
- Schedule and communicate deployment windows
- Verify all pre-release requirements are met
- Facilitate go/no-go decision meeting
- Monitor deployment progress and coordinate rollback if needed
- Ensure all stakeholders are informed of release status

See [Roles and Personas](octoacme-roles-and-personas.md) for detailed Release Manager responsibilities and interaction patterns.

## Pre-release requirements
- All acceptance criteria met and PRs merged (Developers + Product Manager)
- Passing CI and security scans (Developers)
- Release notes drafted (Technical Writer + Product Manager)
- Documentation updated and published (Technical Writer)
- Rollback / mitigation plan documented (Release Manager + Developers)
- Smoke tests prepared (QA)
- Customer support team briefed (Customer Support Lead)

## Deployment Checklist
- [ ] Deployment window scheduled (Release Manager coordinates)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests (QA + Developers)
- [ ] Deploy to production (automated pipeline preferred, Release Manager oversees)
- [ ] Run post-deploy verifications (QA + Developers)
- [ ] Technical documentation published and updated (Technical Writer)
- [ ] Release notes finalized and distributed (Technical Writer + Product Manager)
- [ ] Customer Support team briefed on changes (Customer Support Lead coordinates)
- [ ] Announce release to stakeholders and support (Release Manager + Product Manager)

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
