# GitHub Profile README Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a polished, concise, English GitHub profile README for Yuri Santos.

**Architecture:** This is a single Markdown artifact backed by the approved design spec. The README will use concise sections, Shields.io badges, compact tables, and GitHub stats cards while avoiding sensitive employer details and long biography blocks.

**Tech Stack:** Markdown, Shields.io badges, GitHub Readme Stats.

---

## File Structure

- Create: `README.md`
  - Public GitHub profile README content.
  - Uses GitHub username `yuricavalcanti06`.
  - Uses LinkedIn URL `https://linkedin.com/in/yuri--cavalcanti`.
- Existing: `docs/superpowers/specs/2026-05-25-github-profile-readme-design.md`
  - Approved design reference.

### Task 1: Create README Content

**Files:**
- Create: `README.md`

- [x] **Step 1: Add the hero section**

Create a centered intro with name, positioning, contact badges, and a concise value statement:

```markdown
<h1 align="center">Hi, I'm Yuri Santos</h1>

<p align="center">
  Computer Science student focused on <strong>Data Automation</strong>, <strong>Audit Analytics</strong>, and <strong>Data Quality</strong>.
</p>

<p align="center">
  <a href="https://github.com/yuricavalcanti06">
    <img src="https://img.shields.io/badge/GitHub-yuricavalcanti06-181717?style=for-the-badge&logo=github" alt="GitHub profile" />
  </a>
  <a href="https://linkedin.com/in/yuri--cavalcanti">
    <img src="https://img.shields.io/badge/LinkedIn-Yuri%20Cavalcanti-0A66C2?style=for-the-badge&logo=linkedin" alt="LinkedIn profile" />
  </a>
</p>
```

- [x] **Step 2: Add concise technical sections**

Add `What I'm Building`, `Technical Focus`, `Current Roadmap`, `Featured Project Direction`, and `Career Direction` using short bullets and compact tables.

- [x] **Step 3: Add GitHub stats and contact section**

Use at most two GitHub stats cards:

```markdown
<p>
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=yuricavalcanti06&show_icons=true&theme=github_dark&hide_border=true" alt="Yuri's GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=yuricavalcanti06&layout=compact&theme=github_dark&hide_border=true" alt="Top languages" />
</p>
```

### Task 2: Review Markdown Quality

**Files:**
- Review: `README.md`

- [x] **Step 1: Check for sensitive disclosure**

Run:

```powershell
Select-String -Path README.md -Pattern 'Amarante|R\\$|Unimed|SulAm|Swile|prejudice'
```

Expected: no matches.

- [x] **Step 2: Check for unresolved template markers**

Run:

```powershell
Select-String -Path README.md -Pattern 'TBD|TODO|your-|example.com|lorem'
```

Expected: no matches.

- [x] **Step 3: Check file presence**

Run:

```powershell
Get-Item README.md | Select-Object Name,Length
```

Expected: `README.md` exists and has non-zero length.
