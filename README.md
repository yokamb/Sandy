# 🛡️ Sandy – Microsoft 365 Audit Framework (CIS-based)

**Sandy** is a modular Microsoft 365 auditing framework powered by [Pester](https://github.com/pester/Pester).  
It implements security checks based on the **CIS Microsoft 365 Foundations Benchmark** and follows the [Maester](https://github.com/maester) convention.

---

## 📁 Project Structure

| Folder      | Contents                                      |
|-------------|-----------------------------------------------|
| `cis/`      | `.Tests.ps1` scripts for CIS checks           |
| `config/`   | Metadata like `maester-config.json`           |
| `output/`   | Generated test results (XML, JSON, HTML)      |
| `docs/`     | GitHub Pages content (Sankey diagram, etc.)   |

---

## 🧪 Running the Tests

Open PowerShell in this folder and run:

```powershell
Invoke-Pester -Path ./cis -OutputFormat NUnitXml -OutputFile ./output/results.xml
```

You can also convert results to JSON:

```powershell
Invoke-Pester -Path ./cis -PassThru | ConvertTo-Json -Depth 10 | Out-File ./output/results.json
```

---

## 📊 Visualize Your Workflow

View the full CIS audit workflow diagram here:  
👉 [workflow.html](./docs/workflow.html)

---

## 📦 GitHub Pages

This repo is configured to serve documentation via GitHub Pages from the `/docs` folder.

---

## ✅ To-Do

- [ ] Add Maester-based test coverage for other frameworks (CISA, ORCA)
- [ ] Add CI/CD integration with GitHub Actions
- [ ] Build dashboard in Power BI or HTML

---

## 👤 Author

Built by Yogesh Kamble – powered by Maester + Pester
