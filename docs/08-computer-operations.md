# 08 — Computer operations

> **In plain English:** This domain keeps the lights on — the scheduled jobs run and are watched, data is backed up and can be restored, problems get tracked and fixed, and the physical (or cloud) home of the systems is protected.

Computer operations covers the day-to-day running of the IT environment. If [access](05-access-to-programs-and-data.md) is the front door and [change](06-change-management.md) is renovation, operations is the building's utilities and daily upkeep.

## A real-world analogy

Think of a hospital's facilities team. Automated systems must run on schedule (like scheduled medication rounds), there's a backup generator in case the power fails, every incident is logged and investigated, and the building itself is secured and climate-controlled so sensitive equipment doesn't fail. Nobody notices operations when it works — but everyone notices the moment it doesn't.

## The core controls in this domain

### 1. Batch job scheduling and monitoring

Many financial processes run as automated **batch jobs** — for example, an overnight job that posts the day's transactions or generates invoices. Controls ensure these jobs are scheduled correctly, run in the right order, and are **monitored** so that failures are detected and resolved. A job that silently fails could mean transactions never posted — a completeness problem for the financials.

### 2. Backup and recovery

**Backups** are saved copies of data and systems. But a backup you can't restore is useless, so the real control is **backup *and* recovery**: backups run on schedule, are stored safely (often offsite/geographically separate), and are **periodically test-restored** to prove they actually work. This protects the completeness and availability of financial records.

### 3. Incident and problem management

When something goes wrong, an **incident** is logged, prioritized, worked, and resolved — with a record of what happened. **Problem management** goes a step further: it looks for the *root cause* of recurring incidents so they stop happening. These practices (heavily influenced by [ITIL](03-frameworks.md)) generate tickets that double as audit evidence that issues are handled in a controlled way.

### 4. Physical and environmental controls

The systems live somewhere — a data center or a cloud provider's facilities. **Physical controls** restrict who can physically reach the servers (badge access, cameras, visitor logs). **Environmental controls** protect against non-human threats: fire suppression, cooling, and backup power (UPS/generators). In the cloud, much of this is handled by the provider, so the control becomes reviewing the provider's independent assurance report (e.g., a SOC report) rather than walking the data-center floor yourself.

## The cloud twist

More and more infrastructure runs in the cloud, which shifts *who* performs some of these controls. Physical security and environmental protection become the cloud provider's responsibility, and the organization relies on the provider's third-party attestation reports. But job monitoring, backups (of the organization's own data), and incident management usually remain the organization's job. Auditors adapt by reviewing the provider's assurance reports and confirming the organization's own operational controls still function.

## Why an auditor cares

Operations controls protect two things auditors care about deeply: **completeness** (did all the transactions actually get processed and recorded?) and **availability/integrity** (is the data still there and uncorrupted?). A failed overnight posting job or a lost month of backups can directly misstate the financials. So auditors check that jobs are monitored and failures resolved, that backups run and can be restored, and that the environment is protected.

## Concrete control examples

- **Job monitoring:** A failed nightly billing job automatically raises an alert and a ticket that must be resolved before the next cycle.
- **Backup testing:** Backups run nightly and a sample restore is tested quarterly, with results documented.
- **Incident management:** All production incidents are logged in a ticketing tool with severity, owner, and resolution.
- **Physical/cloud:** Data-center access requires a badge and is logged; for cloud services, the team annually reviews the provider's SOC report.

## Key terms

- **[Backup](../glossary.md)** — a restorable copy of data.
- **Batch job** — an automated process that runs on a schedule (see [glossary](../glossary.md)).
- **Incident / problem management** — logging and resolving issues, and fixing root causes.
- **Physical & environmental controls** — protecting the systems' physical home.

Next up: **[09 — How controls are tested](09-how-controls-are-tested.md)**
