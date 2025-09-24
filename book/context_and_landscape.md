# Context and Landscape

Understanding the environment in which VERSO was created is essential to appreciating its purpose and impact. This chapter explores the broader open-source movement in research, the unique characteristics of the University of Vermont, and the institutional and cultural factors that shaped VERSO’s design.

## The Open Source Movement in Research

Open source has become a cornerstone of modern science and technology. From machine learning frameworks like [**TensorFlow**](https://www.tensorflow.org/) to bioinformatics platforms such as [**Bioconductor**](https://www.bioconductor.org/), open-source tools accelerate discovery by making knowledge transparent, reproducible, and widely accessible. These tools enable researchers to build on each other’s work, reduce duplication of effort, and foster innovation at a global scale.

The benefits of open source can include:

- **Reproducibility**: Open code and data allow others to validate findings and build upon them, addressing the reproducibility crisis in science.
- **Collaboration**: Shared tools and standards break down disciplinary silos, enabling cross-institutional and international partnerships.
- **Equity and Access**: Open source reduces barriers for under-resourced institutions and researchers, democratizing participation in cutting-edge science.
- **Innovation**: By lowering entry costs and encouraging community contributions, open source accelerates the pace of technological advancement.

Despite these advantages adoption in academia remains uneven. Many researchers release code informally as supplementary material or in personal repositories without clear licensing, governance, or documentation {cite}`alzahrani_encoding_2024` as further efforts cost too much {cite}`cadwallader_survey_2022`. This lack of structure limits reuse, creates compliance risks, and undermines sustainability. Projects frequently disappear when a grant ends or a key contributor graduates, resulting in lost value for the scientific community.

The reasons for this behavior is broad and often a set of complex interactions. Incentives for going above just publishing code to making it functional for others is often lacking, either in prestige, recognition for metrics to get tenure to purely the lack of financial incentive to keep a project active after grant funding has expired. In addition the skills necessary to run an open source project are not taught, or even fully understood. The emergence of the National Science Foundation programs like [Pathways to enable Open Source Ecosystems (POSE)](https://www.nsf.gov/funding/opportunities/pose-pathways-enable-open-source-ecosystems) start to recognize and support the work required for successful open source research software.

The open-source movement in research is not just about technology; it represents a cultural shift toward transparency, collaboration, and shared stewardship of knowledge. Universities have a unique opportunity to lead this transformation by embedding open-source practices into the research lifecycle. This is the context in which VERSO was created: to provide the infrastructure, policies, and community support needed to make open source a strategic asset for academic research.

---

##  The University of Vermont Research Ecosystem

The [University of Vermont (UVM)](https://www.uvm.edu/) is a **public land-grant research university** with a mission rooted in accessibility, community engagement, and the advancement of knowledge for the public good. Founded in **1791**, UVM combines the scale of a research-intensive institution with the collaborative spirit of a smaller university. Its research enterprise spans a wide range of disciplines, reflecting both global priorities and Vermont’s unique needs.

### Research Strengths
UVM’s research portfolio is diverse and interdisciplinary, with notable strengths in:
- **Life Sciences**: Genomics, microbiology, health sciences, and biomedical engineering.
- **Data Science and AI**: Machine learning, computational modeling, and big data analytics.
- **Environmental and Climate Research**: Sustainability, renewable energy, and climate adaptation.
- **Agriculture and Food Systems**: Precision agriculture, soil health, and food security.
- **Social and Behavioral Sciences**: Public health, education, and rural community development.

This breadth of expertise positions UVM as a leader in addressing complex, real-world challenges that require cross-disciplinary collaboration in the state of Vermont.

### Institutional Context
As a **land-grant university**, UVM has a statutory obligation to ensure that its research and educational outputs benefit the people of Vermont. This includes a strong emphasis on community engagement, applied research, and knowledge dissemination. [UVM Extension](https://www.uvm.edu/extension) and the [Office of Engagement](https://www.uvm.edu/engagement) maintain deep partnerships with local communities, businesses, and nonprofits, creating a natural bridge between academic research and societal needs.

### The Gap in Open Source Support
Despite this vibrant research ecosystem, UVM had a minimal formal systems to support open-source software development. While the institution had a Gitlab, individual labs often released code informally on alternative platforms, without standardized licensing, governance, or sustainability planning. There was no institutional open data repository either, meaning there was no clear pathway for data access or sustainability. There was no community activities that recognized open source work where norms, collaboration and recognition could be shared.

These gaps highlighted the need for an institutional framework—one that could enable open-source practices, foster collaboration, and ensure long-term impact. VERSO was designed to fill this void and position UVM as a national leader in academic open source.

---

## Why Open Source Matters for Academia

Open source is more than a technical choice—it is a cultural and strategic shift that aligns closely with the core values of higher education: transparency, collaboration, and public good. In the context of academic research, open source offers several critical benefits:

### Reproducibility
Science depends on reproducibility, yet many research findings cannot be replicated because the underlying code or data is inaccessible. Open source addresses this by making research artifacts transparent and verifiable. When code and workflows are openly shared, other researchers can validate results, identify errors, and build upon prior work, strengthening the integrity of science.

### Collaboration
Modern research problems—climate change, public health, artificial intelligence—are too complex for any single discipline to solve alone. Open source fosters **interdisciplinary collaboration** by providing shared tools and platforms where researchers from different fields can contribute. It also enables partnerships beyond academia, connecting universities with industry, government, and community organizations.

### Impact
Academic publications are essential, but their reach is often limited to scholarly audiences. Open-source software, by contrast, can have immediate and widespread impact. Tools developed in a university lab can be adopted by other researchers, integrated into industry workflows, or used by nonprofits and governments to address real-world challenges. This amplifies the societal value of academic research.

### Funding and Policy Alignment
Funding agencies increasingly expect open science practices. Organizations like the **National Science Foundation (NSF)** and **National Institutes of Health (NIH)** now require data and software sharing plans in grant proposals. Open source is not just encouraged—it is becoming a compliance requirement. Universities that support open-source practices position their researchers for success in securing competitive funding.

---

## Barriers to Adoption

Despite the promise of open source in research, its adoption in academia has been anything but straightforward. The challenges are deeply rooted in the culture, policies, and structures of universities.

Culturally, many researchers still see software as a secondary byproduct of their work rather than a primary research output. This perception means that code often lacks documentation, testing, or governance, and contributions to open source rarely count toward tenure or promotion. Without incentives, researchers have little reason to invest in practices that make their work reusable by others.

Legal uncertainty adds another layer of complexity. Questions about licensing and intellectual property frequently stall projects before they even begin. Researchers wonder which license to choose, whether their university will allow open release, or if future commercialization might be compromised. In the absence of clear guidance, many opt for the safest route—keeping code private or releasing it informally without proper licensing, which creates compliance risks and limits impact.

Technical barriers are equally significant. Open source thrives on infrastructure—version control systems, continuous integration pipelines, and standardized documentation—but these tools are not always readily available or supported in academic environments. Researchers often lack the time or expertise to set up these systems, leaving projects fragmented and difficult to maintain.

Finally, sustainability remains the most persistent challenge. Academic projects are typically tied to short-term grants and rely heavily on graduate students or postdocs. When funding ends or key contributors move on, projects often stagnate or disappear entirely. Without governance structures or long-term support, even promising tools can become “abandonware,” eroding the potential benefits of open science.

These barriers illustrate why an institutional approach is essential. Without dedicated support, open source in academia will remain ad hoc and fragile—an afterthought rather than a strategic asset.

---

## The Opportunity

VERSO emerged at a pivotal moment for both academia and the broader research ecosystem. Across the United States, federal agencies were rolling out open science mandates, requiring researchers to share data, code, and other digital artifacts as part of their funding agreements. These policies signaled a fundamental shift: openness was no longer optional—it was becoming a core expectation of publicly funded research.

At the same time, industry had already demonstrated the power of structured open-source governance. Companies like Google, Microsoft, and IBM had established Open Source Program Offices (OSPOs) to manage compliance, foster collaboration, and strategically leverage open source for innovation. These offices showed that open source could be more than a collection of ad hoc projects; with the right infrastructure, it could become a driver of organizational success. Yet, in academia, similar structures were almost nonexistent.

Within UVM, leadership was actively seeking ways to enhance research impact and visibility. The university’s land-grant mission emphasized public engagement and knowledge dissemination, making open source a natural fit. However, without institutional support, researchers faced cultural, legal, and technical barriers that limited their ability to share and sustain their work. This gap presented a unique opportunity: to create one of the first academic OSPOs in the country, positioning UVM as a leader in open science and providing a model for other universities to follow.

VERSO was conceived as a response to this convergence of forces—federal policy shifts, industry best practices, and institutional priorities. It aimed to transform open source from an informal, fragmented activity into a strategic asset for research, education, and community engagement.
