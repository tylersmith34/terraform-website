---
layout: "enterprise"
page_title: "Scheduling - Runs - Terraform Enterprise (legacy)"
sidebar_current: "docs-enterprise-runs-schedule"
description: |-
  Schedule periodic plan runs in Terraform.
---


# Schedule Periodic Plan Runs

!> **Deprecation warning**: Terraform Enterprise (Legacy) features of Atlas will no longer be actively developed or maintained and will be fully decommissioned on Thursday, May 31, 2018. Please see our [Upgrading From Terraform Enterprise (Legacy)](https://www.terraform.io/docs/enterprise/upgrade/index.html) guide to migrate to the new Terraform Enterprise.

Terraform can automatically run a plan against your infrastructure on a
specified schedule. This option is disabled by default and can be enabled by an
organization owner on a per-environment basis.

On the specified interval, a plan can be run that for you, determining any
changes and sending the appropriate notifications.

When used with [automatic applies](/docs/enterprise-legacy/runs/automatic-applies.html), this feature can help converge
changes to infrastructure without human input.

Runs will not be queued while another plan or apply is in progress, or if the
environment has been manually locked. Se
[Environment Locking](/docs/enterprise-legacy/runs#environment-locking) for more
 information.

## Enabling Periodic Plans

To enable periodic plans for an environment, visit the environment settings page
and select the desired interval and click the save button to persist the
changes. An initial plan may immediately run, depending on the state of your
environment, and then will automatically plan at the specified interval.

If you have manually run a plan separately, a new plan will not be queued until
the allotted time after the manual plan ran. This means that the platform simply
ensures that a plan has been executed at the specified schedule.
