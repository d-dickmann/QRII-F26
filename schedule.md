---
layout: page
title: Schedule
---

# Schedule

Pick your section to see your dates. **This schedule is subject to change** — this page is authoritative.

<div class="sched">
<input type="radio" name="sec" id="sec-mw" checked>
<input type="radio" name="sec" id="sec-tr">

<div class="sched-toggle">
  <label for="sec-mw">Section 001 &middot; Mon/Wed</label>
  <label for="sec-tr">Sections 002 &amp; 003 &middot; Tue/Thu</label>
</div>

{% assign content = site.data.schedule.content %}

<table class="sched-table sched-mw">
  <thead><tr><th>Date</th><th>Topic</th><th>Reading</th><th>Due</th></tr></thead>
  <tbody>
  {% for row in site.data.schedule.mw %}
    <tr{% if row.special == "MIDTERM" %} class="is-exam"{% endif %}>
      <td class="nowrap">{{ row.date }}</td>
      <td>{% if row.special == "MIDTERM" %}<strong>MIDTERM</strong>{% elsif row.special == "REVIEW" %}Review &amp; synthesis{% elsif row.special == "CLINIC" %}Project clinic{% else %}{{ content[row.c | minus: 1] }}{% endif %}</td>
      <td>{{ row.reading }}</td>
      <td>{{ row.due }}</td>
    </tr>
  {% endfor %}
  </tbody>
</table>

<table class="sched-table sched-tr">
  <thead><tr><th>Date</th><th>Topic</th><th>Reading</th><th>Due</th></tr></thead>
  <tbody>
  {% for row in site.data.schedule.tr %}
    <tr{% if row.special == "MIDTERM" %} class="is-exam"{% endif %}>
      <td class="nowrap">{{ row.date }}</td>
      <td>{% if row.special == "MIDTERM" %}<strong>MIDTERM</strong>{% elsif row.special == "REVIEW" %}Review &amp; synthesis{% elsif row.special == "CLINIC" %}Project clinic{% else %}{{ content[row.c | minus: 1] }}{% endif %}</td>
      <td>{{ row.reading }}</td>
      <td>{{ row.due }}</td>
    </tr>
  {% endfor %}
  </tbody>
</table>
</div>

## Key dates

| | |
|---|---|
| First day of class | 001 — Mon Aug 31 · 002 & 003 — Tue Sep 1 |
| Labor Day — no class | Mon Sep 7 |
| **Midterm** | **001 — Wed Oct 14 · 002 & 003 — Thu Oct 15** |
| **Project due** | **Fri Nov 6, 11:59pm** — all sections |
| Last day of class | 001 — Mon Nov 9 · 002 & 003 — Thu Nov 5 |
| Oral exams | Week of Mon Nov 10 — scheduled individually |

Section 001 does not meet on Labor Day and makes up that meeting on **Mon Nov 9**.
