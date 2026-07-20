<div align="center">

# PrimeAutocare

**A self-sustaining simulated vehicle service management, invoicing, and automated reporting ecosystem**

Built as a portfolio project by a two-person team — deployed, scheduled, and reporting on its own.

[![React](https://img.shields.io/badge/React_19-20232A?logo=react&logoColor=61DAFB)](https://github.com/PrimeAutocare/PrimeAutocare)
[![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white)](https://github.com/PrimeAutocare/PrimeAutocare)
[![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?logo=tailwindcss&logoColor=white)](https://github.com/PrimeAutocare/PrimeAutocare)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)](https://github.com/PrimeAutocare/PrimeAutocare)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)](https://github.com/PrimeAutocare/PrimeAutocare)
[![Groovy](https://img.shields.io/badge/Apache_Groovy-4298B8?logo=apachegroovy&logoColor=white)](https://github.com/PrimeAutocare/Reporting_Automation)
[![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white)](https://github.com/PrimeAutocare/Reporting_Automation)
[![Vercel](https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white)](https://github.com/PrimeAutocare/PrimeAutocare)

</div>

---

## Overview

PrimeAutocare is a vehicle service center management system that tracks
customers, vehicles, service visits, job assignments, invoices, and payments.
The system is designed to run without intervention: the application is deployed
on Vercel, and a scheduled pipeline reads the live database twice a month,
builds Excel business reports, and publishes them to a dedicated repository.

```mermaid
flowchart LR
    A["PrimeAutocare app<br/>(Vercel)"] --> DB[("Postgres<br/>(Neon)")]
    B["Reporting_Automation<br/>(Actions cron — 1st &amp; 15th)"] -- reads --> DB
    B -- "commits .xlsx" --> C["Generated_Reports"]
```

## Repositories

| Repository | Description |
| --- | --- |
| [PrimeAutocare](https://github.com/PrimeAutocare/PrimeAutocare) | The application — FastAPI + SQLAlchemy backend, React 19 + Vite + Tailwind frontend, Postgres schema |
| [Reporting_Automation](https://github.com/PrimeAutocare/Reporting_Automation) | Scheduled Groovy scripts that build five Excel reports — payroll, utilization, receivables, revenue, and WIP — from the database |
| [Generated_Reports](https://github.com/PrimeAutocare/Generated_Reports) | Published reports — the current workbook per report, with every past period archived |

Start with the [PrimeAutocare README](https://github.com/PrimeAutocare/PrimeAutocare#readme)
for the full picture.

## Team

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/InukaWijerathna">
        <img src="https://github.com/InukaWijerathna.png" width="80" alt=""/><br/>
        <b>Inuka Wijerathna</b>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/SenukaWijerathna">
        <img src="https://github.com/SenukaWijerathna.png" width="80" alt=""/><br/>
        <b>Senuka Wijerathna</b>
      </a>
    </td>
  </tr>
</table>
