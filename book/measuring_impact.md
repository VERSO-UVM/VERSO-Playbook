
# Measuring Impact

Measuring impact is more than an exercise in reporting numbers—it is about telling the story of why VERSO matters. From the beginning, we understood that building an Open Source Program Office inside a university was an experiment, and like any experiment, it required evidence to validate its success.

However, the path to measurement was far from straightforward. What we assumed would be easy to track turned out to be irrelevant, incomplete, or misleading. In some cases, the data simply did not exist. Even our initial survey, which revealed that most respondents did not know what open source was, highlighted a fundamental challenge: we were trying to measure progress in a landscape where the baseline was unclear.

One of the earliest examples of this difficulty came from trying to gather statistics from the UVM‑hosted GitLab instance about the number of public repositories. A first‑pass query showed 43 repositories with open‑source licenses—yet one repository, upon inspection, consisted solely of a README stating: *“I had no idea we had a GitLab.”* The situation on GitHub was even more complicated: while we found nearly 14,000 public repositories referencing “UVM,” attributing them to actual UVM faculty, staff, or students was nearly impossible because most people used personal GitHub accounts. Attempts to catalogue those accounts raised important questions around privacy, autonomy, and the role of a university office in indexing individuals’ digital identities.

Beyond this, broader ecosystem metrics were opaque. UVM’s GitLab instance had low adoption, GitHub attribution was unreliable, and large open‑source projects involving UVM were often co‑owned by collaborators at many institutions. In these cases, what did “UVM ownership” even mean?

Ultimately, we recognized that measuring the entire “open‑source ecosystem” was neither concrete nor functional. Instead, we pivoted toward creating our own projects—initiatives where we could define measurable goals, control data quality, and document clear outcomes.

---

# Key Metrics

From the earliest days of VERSO, we understood that enthusiasm alone could not sustain an academic Open Source Program Office. To justify long‑term investment—financial, organizational, and cultural—we needed metrics that demonstrated real, defensible impact. Over time, our approach evolved into a multidimensional framework reflecting not only program activity but also ecosystem growth, cultural transformation, and lasting institutional value.

## 1. Student Engagement & Workforce Development

Students are the engine of VERSO and ORCA. Their participation and professional growth offer some of the most direct evidence of our success.

**Core metrics include:**

- **Total ORCA student participants per year** - Unique count of students in the program each year, includes all semesters
    -   2023 - 5
    -   2024 - 25
    -   2025 - 30
- **Hours students contribute to real open work in ORCA** - Total hours worked for paid projects (this does not include volunteer work)
    -   2023 - 338 hours
    -   2024 - 4414 hours
    -   2025 - 3166 hours
- **Retention** - Students returning for multiple semesters by year, this includes if a student continued from a previous year or went into the next year
    -   2023 - 60% (3/5 students)
    -   2024 - 72% (18/25 students)
    -   2025 - 73% (22/30 students)
- **Career outcomes** - Including internships, research positions, or employment related to open‑source skills
    - This is a qualitative metric as student's post-graduation are not required to send back any information to ORCA, but in once case a student actually works in UVM in IT, another from the zoning atlas team joined a Town Planning Office, another went to be a Public Works Intern, another to be a Field Geologist. 

These metrics illuminate how VERSO prepares students for open‑source practice and supports a workforce trained in real production‑quality tools and methods.

```{code-cell} ipython3
:tags: [hide-input]

import matplotlib.pyplot as plt
import numpy as np

# Create figure with subplots
fig, ((ax1, ax2), (ax3, ax4)) = plt.subplots(2, 2, figsize=(14, 10))
fig.suptitle('ORCA Student Engagement & Growth Metrics', fontsize=16, fontweight='bold')

# 1. Student Growth Over Time
years = [2023, 2024, 2025]
students = [5, 25, 30]
ax1.plot(years, students, marker='o', linewidth=2, markersize=10, color='#2E7D32')
ax1.fill_between(years, students, alpha=0.3, color='#2E7D32')
ax1.set_title('ORCA Student Participants', fontweight='bold')
ax1.set_xlabel('Year')
ax1.set_ylabel('Number of Students')
ax1.grid(True, alpha=0.3)
ax1.set_ylim(0, 35)
for i, v in enumerate(students):
    ax1.text(years[i], v + 1, str(v), ha='center', fontweight='bold')

# 2. Student Hours Contributed
hours = [338, 4414, 3166]
colors = ['#1976D2', '#1976D2', '#1976D2']
bars = ax2.bar(years, hours, color=colors, alpha=0.8, edgecolor='black')
ax2.set_title('Hours Contributed to Open Work', fontweight='bold')
ax2.set_xlabel('Year')
ax2.set_ylabel('Total Hours')
ax2.grid(True, alpha=0.3, axis='y')
for bar, hour in zip(bars, hours):
    height = bar.get_height()
    ax2.text(bar.get_x() + bar.get_width()/2., height + 100,
             f'{hour:,}', ha='center', va='bottom', fontweight='bold')

# 3. Retention Rates
retention = [60, 72, 73]
bars = ax3.bar(years, retention, color='#F57C00', alpha=0.8, edgecolor='black')
ax3.set_title('Student Retention Rate', fontweight='bold')
ax3.set_xlabel('Year')
ax3.set_ylabel('Retention Rate (%)')
ax3.set_ylim(0, 100)
ax3.axhline(y=70, color='red', linestyle='--', alpha=0.5, label='70% Target')
ax3.grid(True, alpha=0.3, axis='y')
ax3.legend()
for bar, rate in zip(bars, retention):
    height = bar.get_height()
    ax3.text(bar.get_x() + bar.get_width()/2., height + 2,
             f'{rate}%', ha='center', va='bottom', fontweight='bold')

# 4. Growth Summary - Total student-hours over time
total_student_hours = [5*338/5, 25*4414/25, 30*3166/30]  # Avg hours per student
ax4.plot(years, total_student_hours, marker='s', linewidth=2, markersize=10, color='#6A1B9A')
ax4.fill_between(years, total_student_hours, alpha=0.3, color='#6A1B9A')
ax4.set_title('Average Hours per Student', fontweight='bold')
ax4.set_xlabel('Year')
ax4.set_ylabel('Hours per Student')
ax4.grid(True, alpha=0.3)
for i, v in enumerate(total_student_hours):
    ax4.text(years[i], v + 5, f'{v:.0f}', ha='center', fontweight='bold')

plt.tight_layout()
plt.show()
```

---

## 2. Project Portfolio & Research Output

As VERSO’s work expanded, the number and diversity of open‑source projects became a tangible measure of impact. We began tracking:

- **Total active VERSO and ORCA projects** - All repositories (public and private) by year, and approximate projects that had some form of contribution that year. This includes ORCA and Non-ORCA supported projects
    -   2022 - 1 total repos (private and public) ~1 being actively worked on during that year
    -   2023 - 4 total repos (private and public) ~4 being actively worked on during that year
    -   2024 - 23 total repos (private and public) ~17 being actively worked on during that year
    -   2025 - 42 total repos (private and public) ~14 being actively worked on during that year
- **Project categories** - Approximate count of projects by category as of 2026.
    -   Community Tool - 10 Projects
    -   Research Tool - 4 Projects
    -   Data Collection or Visualization - 10 projects
    -   Documentation - 7 projects
    -   Class Exercise - 3 projects
- **Project maturity metrics** - Metrics of completed milestones, release cycles, or adoption by users beyond UVM would be ideal to collect, but developing the api call to receive these stats has not happened yet

These indicators help quantify VERSO’s ability to produce high‑quality, open, and reusable software aligned with academic research needs.
```{code-cell} ipython3
:tags: [hide-input]

import matplotlib.pyplot as plt
import numpy as np

# Create figure with subplots
fig, (ax1, ax2) = plt.subplots(1, 2, figsize=(14, 5))
fig.suptitle('Project Portfolio & Research Output', fontsize=16, fontweight='bold')

# 1. Repository Growth
years = [2022, 2023, 2024, 2025]
total_repos = [1, 4, 23, 42]
active_repos = [1, 4, 17, 14]

ax1.plot(years, total_repos, marker='o', linewidth=2, markersize=10, 
         color='#1976D2', label='Total Repositories')
ax1.plot(years, active_repos, marker='s', linewidth=2, markersize=10, 
         color='#F57C00', label='Active Projects')
ax1.fill_between(years, total_repos, alpha=0.2, color='#1976D2')
ax1.set_title('Repository & Project Growth', fontweight='bold')
ax1.set_xlabel('Year')
ax1.set_ylabel('Count')
ax1.legend(loc='upper left')
ax1.grid(True, alpha=0.3)
ax1.set_ylim(0, 45)

# 2. Project Categories (Pie Chart)
categories = ['Community\nTool', 'Research\nTool', 'Data Collection/\nVisualization', 
              'Documentation', 'Class\nExercise']
values = [10, 4, 10, 7, 3]
colors_pie = ['#2E7D32', '#1976D2', '#F57C00', '#6A1B9A', '#C62828']
explode = (0.05, 0, 0.05, 0, 0)

wedges, texts, autotexts = ax2.pie(values, labels=categories, autopct='%1.0f%%',
                                     colors=colors_pie, explode=explode,
                                     startangle=90, textprops={'fontweight': 'bold'})
ax2.set_title('Project Categories (2026)', fontweight='bold')

# Make percentage text more visible
for autotext in autotexts:
    autotext.set_color('white')
    autotext.set_fontsize(11)

plt.tight_layout()
plt.show()
```
---

## 3. Partnerships & Ecosystem Connectivity

A healthy open ecosystem can only thrive through collaboration. Over time, VERSO built relationships across UVM and beyond.

**Metrics include:**

- **Number of UVM research collaborators** - Count of institutes, labs, or a researcher if there is just one by year. This is approximate, this is not stored in an easy to find system. This can also range from consulting conversations to submitting grants to running an ORCA team on a project.
    -   2023 - 25 (1 ORCA Research Project)
    -   2024 - 45 (2 research ORCA project)
    -   2025 - 60 (4 research ORCA projects)
- **External partners** - Collaboration with nonprofits, state agencies, local governments, and other universities either from project exploration to building software. This is approximate, this is not stored in an easy to find system, especially year to year as once a partnership is created it may be in a semi-active state.
    -   2023 - Unknown
    -   2024 - 14 (3 Community ORCA project)
    -   2025 - 25 (4 Community ORCA project)

These metrics reflect how well VERSO strengthens UVM’s connections to regional, national, and international open‑source communities.
```{code-cell} ipython3
:tags: [hide-input]

import matplotlib.pyplot as plt
import numpy as np

# Create figure
fig, ax = plt.subplots(1, 1, figsize=(12, 6))
fig.suptitle('Partnership & Ecosystem Growth', fontsize=16, fontweight='bold')

# Partnership data
years = [2023, 2024, 2025]
uvm_collaborators = [25, 45, 60]
external_partners = [0, 14, 25]  # 2023 was unknown, using 0 for chart

# Create grouped bar chart
x = np.arange(len(years))
width = 0.35

bars1 = ax.bar(x - width/2, uvm_collaborators, width, label='UVM Research Collaborators',
               color='#2E7D32', alpha=0.8, edgecolor='black')
bars2 = ax.bar(x + width/2, external_partners, width, label='External Partners',
               color='#1976D2', alpha=0.8, edgecolor='black')

ax.set_xlabel('Year', fontweight='bold')
ax.set_ylabel('Number of Partners', fontweight='bold')
ax.set_title('Expansion of Collaborative Network', fontweight='bold', pad=20)
ax.set_xticks(x)
ax.set_xticklabels(years)
ax.legend()
ax.grid(True, alpha=0.3, axis='y')

# Add value labels on bars
for bars in [bars1, bars2]:
    for bar in bars:
        height = bar.get_height()
        if height > 0:  # Only show label if value exists
            ax.text(bar.get_x() + bar.get_width()/2., height + 1,
                   f'{int(height)}',
                   ha='center', va='bottom', fontweight='bold')

# Add note about 2023 external partners
ax.text(0.02, 0.98, 'Note: 2023 external partners data not tracked',
        transform=ax.transAxes, fontsize=9, va='top', style='italic',
        bbox=dict(boxstyle='round', facecolor='wheat', alpha=0.5))

plt.tight_layout()
plt.show()
```
---

## 4. Open Data Adoption & Dataverse Utilization

With the launch of the UVM Dataverse, VERSO gained new visibility into open‑data practices across campus. The UVM Dataverse was only launched in 2025, metrics only will go back to that year

**Key metrics include:**

- **Datasets published** - Count of datasets and dataverses published by faculty, students, and research units  
    -   2025 - 4 Dataverses and 57 datasets
- **Download and access counts** - Count of Downloads, this is a rough estimate based on estimates given a sample size until API reporting is implemented
    -   2025 - ~195 downloads
- **Number of Users** - Count of users and superusers
    -   2025 - 16 users
- **Citation and reuse metrics** - Count of citations where available, showing downstream influence 
    -   2025 - Unknown

These measures help track the spread of open‑data culture and provide evidence of real‑world impact.

---

## 5. Institutional Presence & Cultural Change

Building an open culture is long‑term work, and many of its indicators do not appear immediately. As awareness grew, however, VERSO began monitoring:

- **New GitHub/GitLab organizations** - Count of created Gitlab or Github organizations by labs or research groups where VERSO was involved in the setup or maintenance. Each organization is only counted once
    -   2022 - 1
    -   2023 - 1
    -   2024 - 3
    -   2025 - 4
- **Growth of openly licensed repositories** -  Count of Gitlab or Github openly licensed repositories.This is more a minimum as it is impossible to see all repos and while we have unknown here, we do no
    -   2022 - unknown
    -   2023 - unknown
    -   2024 - unknown
    -   2025 - unknown
- **Requests for consultations** - Count of class guest lectures by VERSO
    -   2022-2023 Academic Year - 8
    -   2023-2024 Academic Year - 6
    -   2024-2025 Academic Year - 7
- **Faculty and staff participation** - Cumulative count of participants from UVM in open‑work initiatives, workshops, and conferences
    -   2022 - ~10
    -   2023 - ~30
    -   2024 - ~20
    -   2025 - ~30

These indicators provide insight into how open‑source thinking is taking root across the university.

---

## 6. Events, Training & Community Engagement

As VERSO expanded its educational programs, event‑based metrics became valuable for understanding reach and community dynamics.

**Metrics include:**

- **Workshops, Presenations, and Conferences** - Count of all presentations both internal and external to UVM from small events to big events 
    -   2022 - 2
    -   2023 - 7
    -   2024 - 20
    -   2025 - 11
- **Attendance levels** - Cumulative number of total attendees to VERSO organized events
    -   2022 - ~20
    -   2023 - ~150
    -   2024 - ~120
    -   2025 - ~240   

These metrics highlight VERSO’s role in cultivating a vibrant, informed, and engaged open‑source community.
```{code-cell} ipython3
:tags: [hide-input]

import matplotlib.pyplot as plt
import numpy as np

# Create figure with subplots
fig, (ax1, ax2) = plt.subplots(1, 2, figsize=(14, 5))
fig.suptitle('Events, Training & Community Engagement', fontsize=16, fontweight='bold')

# 1. Workshops and Conferences
years = [2022, 2023, 2024, 2025]
events = [2, 7, 20, 11]

colors_events = ['#1976D2' if e < 15 else '#2E7D32' for e in events]
bars = ax1.bar(years, events, color=colors_events, alpha=0.8, edgecolor='black')
ax1.set_title('Workshops, Presentations & Conferences', fontweight='bold')
ax1.set_xlabel('Year')
ax1.set_ylabel('Number of Events')
ax1.grid(True, alpha=0.3, axis='y')

for bar, event_count in zip(bars, events):
    height = bar.get_height()
    ax1.text(bar.get_x() + bar.get_width()/2., height + 0.3,
             str(event_count), ha='center', va='bottom', fontweight='bold')

# 2. Cumulative Attendance
attendance = [20, 150, 120, 240]
ax2.plot(years, attendance, marker='o', linewidth=3, markersize=12, 
         color='#F57C00')
ax2.fill_between(years, attendance, alpha=0.3, color='#F57C00')
ax2.set_title('Total Event Attendance', fontweight='bold')
ax2.set_xlabel('Year')
ax2.set_ylabel('Cumulative Attendees')
ax2.grid(True, alpha=0.3)

for i, v in enumerate(attendance):
    ax2.text(years[i], v + 10, f'{v}', ha='center', fontweight='bold', fontsize=11)

plt.tight_layout()
plt.show()
```
---

# Beyond Numbers

While metrics provide snapshots of progress, they cannot capture transformation on their own. The number of workshops held or repositories created illustrates activity but not meaning. To fully understand VERSO’s impact, we must also embrace stories, testimonials, unexpected outcomes, and culture shifts—forms of impact that numbers alone cannot quantify.

Metrics matter. But ultimately, they are only one part of a broader narrative about building a sustainable, equitable, and open ecosystem at UVM.
``
