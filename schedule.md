---
layout: page
title: Schedule
# How many rows of the schedule are published, per section.
# Increase these to release more of the term. Content lives in _data/schedule.yml.
show_schedule: true
mw_rows: 2
tr_rows: 2
---

The meeting-by-meeting schedule will be posted here and updated throughout the term.

<div class="sched">
<input type="radio" name="sec" id="sec-mw" checked>
<input type="radio" name="sec" id="sec-tr">

<div class="sched-toggle">
  <label for="sec-mw">Section 001 &middot; Mon/Wed</label>
  <label for="sec-tr">Sections 002 &amp; 003 &middot; Tue/Thu</label>
</div>

{% assign content = site.data.schedule.content %}
{% assign readings = site.data.schedule.readings %}

<table class="sched-table sched-mw">
  <thead><tr><th>Date</th><th>Topic</th><th>Reading<br><span class="th-note">to be completed before the class meeting on which it is listed</span></th></tr></thead>
  <tbody>
  {% for row in site.data.schedule.mw limit: page.mw_rows %}
    {% assign i = row.c | minus: 1 %}
    <tr{% if row.special == "MIDTERM" %} class="is-exam"{% elsif row.special == "NO CLASS" %} class="is-noclass"{% endif %}>
      <td class="nowrap">{{ row.date }}</td>
      <td>{% if row.special == "MIDTERM" %}<strong>MIDTERM</strong>{% elsif row.special %}{{ row.special }}{% else %}{{ content[i] }}{% endif %}</td>
      <td>{% if row.c %}{{ readings[i] }}{% endif %}</td>
    </tr>
  {% endfor %}
  </tbody>
</table>

<table class="sched-table sched-tr">
  <thead><tr><th>Date</th><th>Topic</th><th>Reading<br><span class="th-note">to be completed before the class meeting on which it is listed</span></th></tr></thead>
  <tbody>
  {% for row in site.data.schedule.tr limit: page.tr_rows %}
    {% assign i = row.c | minus: 1 %}
    <tr{% if row.special == "MIDTERM" %} class="is-exam"{% elsif row.special == "NO CLASS" %} class="is-noclass"{% endif %}>
      <td class="nowrap">{{ row.date }}</td>
      <td>{% if row.special == "MIDTERM" %}<strong>MIDTERM</strong>{% elsif row.special %}{{ row.special }}{% else %}{{ content[i] }}{% endif %}</td>
      <td>{% if row.c %}{{ readings[i] }}{% endif %}</td>
    </tr>
  {% endfor %}
  </tbody>
</table>
</div>

## Key dates

| | |
|---|---|
| First day of class | 001: Mon Aug 31; 002 & 003: Tue Sep 1 |
| Labor Day — no class | Mon Sep 7 |
| **Midterm** | **TBD** |
| **Project due** | **Fri Nov 6, 11:59pm** — all sections |
| Last day of class | 001: Mon Nov 9; 002 & 003: Thu Nov 5 |
| Oral Exams/Project Interviews | Week of Mon Nov 10: scheduled individually |
