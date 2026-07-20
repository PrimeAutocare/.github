<div align="center">

# 🚗 PrimeAutocare

### A self-sustaining simulated vehicle service management, invoicing, and automated reporting ecosystem

*Built as a portfolio project by a two-person team — deployed, scheduled, and reporting on its own.*

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

## ⚙️ How it works

The project is designed to **run itself**. The app is live on Vercel; twice a
month a GitHub Actions cron reads the database, builds five Excel business
reports, and commits them — no human in the loop.

```mermaid
flowchart LR
    A["🌐 PrimeAutocare app<br/>(Vercel)"] --> DB[("🐘 Postgres<br/>(Neon)")]
    B["⏰ Reporting_Automation<br/>(Actions cron — 1st &amp; 15th)"] -- reads --> DB
    B -- "commits .xlsx" --> C["📊 Generated_Reports"]
```

## 📦 Repositories

| Repository | What it is |
| --- | --- |
| 🚗 [PrimeAutocare](https://github.com/PrimeAutocare/PrimeAutocare) | The application — FastAPI + SQLAlchemy backend, React 19 + Vite + Tailwind frontend, Postgres schema |
| 🤖 [Reporting_Automation](https://github.com/PrimeAutocare/Reporting_Automation) | Scheduled Groovy scripts that build five Excel reports (payroll, utilization, receivables, revenue, WIP) from the database |
| 📊 [Generated_Reports](https://github.com/PrimeAutocare/Generated_Reports) | Where those reports land — current workbook per report, with every past period archived |

Start with the [PrimeAutocare README](https://github.com/PrimeAutocare/PrimeAutocare#readme)
for the full picture.

## 👥 Team

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/InukaWijerathna">
        <img src="https://github.com/InukaWijerathna.png" width="80" style="border-radius: 50%" alt=""/><br/>
        <b>Inuka Wijerathna</b>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/SenukaWijerathna">
        <img src="https://github.com/SenukaWijerathna.png" width="80" style="border-radius: 50%" alt=""/><br/>
        <b>Senuka Wijerathna</b>
      </a>
    </td>
  </tr>
</table>
