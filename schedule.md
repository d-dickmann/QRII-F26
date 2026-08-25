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

<table class="sched-table">
  <thead>
    <tr><th>Date</th><th>#</th><th>Topic</th><th>Reading</th><th>Due</th></tr>
  </thead>
  <tbody>
  {% for m in site.data.schedule %}
    <tr>
      <td class="nowrap"><span class="d-mw">{{ m.mw }}</span><span class="d-tr">{{ m.tr }}</span></td>
      <td>{{ m.n }}</td>
      <td>{{ m.topic | markdownify | remove: '<p>' | remove: '</p>' }}</td>
      <td>{{ m.reading }}</td>
      <td>{{ m.due }}</td>
    </tr>
  {% endfor %}
  </tbody>
</table>
</div>

## Key dates

| | |
|---|---|
| First day of class | Section 001 — Mon Aug 31 · Sections 002 & 003 — Tue Sep 1 |
| Labor Day — no class | Mon Sep 7 |
| Last day of class | Section 001 — Mon Nov 9 · Sections 002 & 003 — Thu Nov 5 |

Section 001 does not meet on Labor Day and makes up that meeting on **Mon Nov 9**.
