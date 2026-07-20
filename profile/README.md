# PrimeAutocare

**Full-stack, serverless, and self-sustaining — a zero-touch platform with automated CI/CD and cron-driven reporting.**

A vehicle service center management system, built as a portfolio project by a
two-person team: [Inuka Wijerathna](https://github.com/InukaWijerathna) and
[Senuka Wijerathna](https://github.com/SenukaWijerathna).

The project is designed to run itself. The app is deployed on Vercel, and a
scheduled pipeline reads the live database twice a month, builds Excel business
reports, and commits them — no human in the loop.

## Repositories

| Repository | What it is |
| --- | --- |
| [PrimeAutocare](https://github.com/PrimeAutocare/PrimeAutocare) | The application — FastAPI + SQLAlchemy backend, React 19 + Vite + Tailwind frontend, Postgres schema |
| [Reporting_Automation](https://github.com/PrimeAutocare/Reporting_Automation) | Scheduled Groovy scripts that build five Excel reports (payroll, utilization, receivables, revenue, WIP) from the database |
| [Generated_Reports](https://github.com/PrimeAutocare/Generated_Reports) | Where those reports land — current workbook per report, with every past period archived |

## How it fits together

```
PrimeAutocare app (Vercel)          Reporting_Automation (GitHub Actions cron,
        │                            1st and 15th at 06:00 UTC)
        ▼                                   │
   Postgres (Neon)  ◄───── reads ───────────┘
                                            │ commits .xlsx
                                            ▼
                                    Generated_Reports
```

Start with the [PrimeAutocare README](https://github.com/PrimeAutocare/PrimeAutocare#readme)
for the full picture.
