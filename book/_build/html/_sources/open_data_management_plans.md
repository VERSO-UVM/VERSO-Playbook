# Making Open Data Management Plans

An Open Data Management Plan (DMP) is a living document that describes how research data will be created, processed, archived, and shared throughout the research lifecycle and beyond. Data management planning is a critical component of research excellence, enabling reproducibility, transparency, and broad research impact. This guide provides practical guidance for creating effective open data management plans.

This resource combines best practices in data management planning with practical guidance from the NASA Open Science initiative, including how to develop Open Science and Data Management Plans (OSDMPs) that satisfy funder requirements while supporting reproducible research.

---

## Quick Reference Links

- **Open Science 101 (OS101):** https://openscience101.org/
- **NASA Science Mission Directorate (SMD) Open Science policy (SPD-41a):** https://science.nasa.gov/researchers/open-science/science-information-policy/
- **NASA SMD Open-Source Science Guidance (includes OSDMP templates):** https://github.com/nasa/smd-open-science-guidelines
- **DMPTool:** https://dmptool.org
- **UVM Dataverse:** https://dataverse.uvm.edu

---

## What is Open Science?

> **Open Science** is the principle and practice of making research products and processes available to all, while respecting diverse cultures, maintaining security and privacy, and fostering collaborations, reproducibility, and equity.

Open science aims to make research:

- **Accessible** – Available to all researchers and the public
- **Reproducible** – Methods, data, and code are documented sufficiently for others to verify results
- **Inclusive** – Benefits broader participation and collaboration

Implementing open science practices often leads to:

- More collaboration and citation impact
- More equitable research systems
- Increased participation and reuse
- Greater transparency and accountability
- Enhanced reproducibility and reusability

---

## Why Data Management Plans Matter

Data management plans serve multiple important functions:

**Research Excellence**: Well-organized, documented data improves research quality, reduces errors, and supports reproducibility. A clear DMP helps teams maintain consistency and follow best practices from project inception.

**Compliance and Funding**: Major funding agencies including the National Science Foundation (NSF), National Institutes of Health (NIH), Department of Energy (DOE), and NASA now require data management plans as part of grant proposals. NASA's Scientific Information Policy (SPD-41a) and the White House OSTP memo on "Ensuring Free, Immediate, and Equitable Access to Federally Funded Research Data" emphasize the importance of open science planning. These requirements aim to make science open, accessible, and secure while minimizing burden on researchers.

**Data Preservation**: Without a plan, valuable research data can be lost due to storage failures, format obsolescence, or simply institutional memory loss. A DMP ensures data survival and accessibility for future researchers.

**Sharing and Reuse**: Open data creates opportunities for other researchers to build upon your work, increasing research impact and preventing duplicate efforts. A DMP articulates how data will be shared and what conditions apply.

**Institutional Knowledge**: DMPs document decisions about data management, making it easier for team members to understand the approach and for new team members to onboard into projects.

---

## Understanding Open Science and Data Management Plans (OSDMPs)

An **Open Science and Data Management Plan (OSDMP)** is a comprehensive component of certain proposals (such as NASA ROSES grants) that describes how proposed work will comply with open science policies while managing multiple research products.

An OSDMP differs from traditional data management plans by covering not just data, but also:

- **Data management** – How data will be created, archived, and shared
- **Software management** – How code and software tools will be developed and maintained
- **Publications and open results** – How research findings and products will be disseminated
- **Project governance** – Roles, responsibilities, and decision-making processes

### Minimum Viable vs. Integrated Plans

You can approach an OSDMP as:

- **Minimum Viable Product (MVP):** Adheres strictly to funder policy requirements—no more, no less. Useful when page limits are tight.
- **Integrated Plan:** Goes beyond minimum requirements to provide practical detail on *how* the work will actually be done. Often results in better project execution and greater research impact.

Both approaches are valid; choose based on funder guidance, page limits, and your project's needs.

---

## Core Components of an Open Data Management Plan

### 1. Data Description

Provide a clear, comprehensive description of the data your research will produce or use:

- **What data will be collected or created?** Describe the types of data: raw experimental measurements, simulations, surveys, images, genomic sequences, geospatial data, qualitative interviews, etc.
- **How much data?** Estimate the volume in appropriate units (GB, TB, number of files, etc.).
- **What format?** Specify file formats (e.g., CSV, NetCDF, HDF5, TIFF, PDF). Prefer open, non-proprietary formats when possible.
- **What metadata?** Describe the information that will accompany the data (timestamps, units, calibration information, geographic coordinates, experimental parameters, etc.).
- **Data lifecycle**: When will data be generated, processed, analyzed, and archived?

### 2. Data Access and Sharing

Define how data will be made available to the research community:

- **Open vs. Restricted**: Will all data be made openly available? Are there legitimate reasons to restrict access (privacy, security, intellectual property)? If restricted, describe the access process and timeline for opening data.
- **Repositories**: Where will data be deposited? Choose repositories appropriate to your discipline:
  - Multidisciplinary: Zenodo, Figshare, DRYAD, OSF
  - Domain-specific: GenBank (genomics), NOAA (climate/weather), Pangaea (geosciences), ICPSR (social science), etc.
  - Institutional: University repositories, including UVM Dataverse
- **Embargo periods**: If not immediately open, specify the embargo period and conditions for release.
- **Licensing**: What license will apply to the data? Recommend CC0, CC-BY, or other permissive licenses that enable maximum reuse.
- **Documentation for reuse**: What documentation (README files, data dictionaries, codebooks) will accompany the data to enable others to understand and use it?
- **Sharing timeline**: When will data be shared? Typically no later than publication or the end of the project's funding period.

### 2a. FAIR Data Principles (Practical Checklist)

Ensure your data management plan addresses the FAIR principles:

**Findable**
- Deposit data in searchable repositories
- Assign persistent identifiers (PIDs) like DOIs
- Create rich, self-describing metadata
- Register metadata in discovery catalogs

**Accessible**
- Archive in repositories with standardized access protocols
- Document clear access procedures
- Ensure standardized, open-source tools can access the data

**Interoperable**
- Use community-standard, non-proprietary formats
- Employ standardized metadata and controlled vocabularies
- Ensure compatibility with other tools and systems

**Reusable**
- Provide accurate, detailed metadata and variable descriptions
- Specify clear usage licenses
- Record provenance and processing information
- Include sufficient metadata for proper attribution and citation

### 3. Data Storage and Backup

Describe how data will be stored, backed up, and protected during active research:

- **Storage location**: Where will working copies be stored (local workstations, shared network drives, cloud storage)?
- **Backup strategy**: How often will backups occur? Where will backups be stored (off-site, in cloud services)?
- **Security and access control**: How will data be protected from unauthorized access? Who has permission to access data?
- **Version control**: How will different versions of data be managed? Consider version control systems (Git with Git LFS) or centralized management.
- **Hardware and infrastructure**: What computing infrastructure will be used?

### 4. Data Standards and Quality

Define standards to ensure data quality and consistency:

- **Naming conventions**: Establish clear, machine-readable file naming conventions (e.g., `ProjectName_DataType_YYYYMMDD_versionNumber.csv`).
- **Metadata standards**: Adopt established metadata standards relevant to your discipline (e.g., Dublin Core, Darwin Core for biodiversity data, MIAME for microarray data).
- **Quality assurance**: Describe processes for validating data accuracy, completeness, and consistency.
- **Documentation standards**: Specify how data will be documented (standardized forms, templates, automated logging).

### 5. Roles and Responsibilities

Clarify who is responsible for data management activities:

- **Data steward**: Who oversees overall data management?
- **Collection/generation**: Who collects or creates the data?
- **Processing and analysis**: Who processes, cleans, and analyzes the data?
- **Archiving and preservation**: Who ensures data is properly archived and preserved?
- **Metadata creation**: Who documents the data?
- **Access management**: Who manages permissions and access requests?

Assign specific roles and include contact information when possible.

### 6. Data Retention and Preservation

Address long-term data preservation:

- **Retention period**: How long will data be retained? Consider funder requirements (typically 3-5 years minimum) and discipline norms.
- **Format migration**: Plan for preserving data as file formats become obsolete. Include strategies for converting data to open, archival-quality formats.
- **Preservation strategy**: Will data be preserved in a certified digital repository? How will preservation metadata be maintained?
- **Access after project ends**: How will researchers access data after the project concludes?

### 7. Budget and Resources

Include costs associated with data management:

- **Storage costs**: Cloud storage, institutional repository space, external hard drives.
- **Personnel time**: Effort for data management tasks (collection, quality assurance, documentation, archiving).
- **Software and tools**: Licenses for data management software, version control systems, or analysis tools.
- **Training**: Time and resources for team training on data management practices.

---

## Part 2: Software Management

An OSDMP should address how software and code will be managed throughout your project.

### What is Open Code?

Open code means software is developed transparently, often on platforms like GitHub, where:

- **More eyes review code** – Increasing bug detection and code quality
- **Reproducibility is enhanced** – Others can verify and replicate computational results
- **Community reuse increases** – Code becomes a research output with lasting impact
- **Visibility and credit grow** – Software contributions are recognized and cited
- **Educational value emerges** – Others learn from your code and methodology

### What to Cover in Software Management

Your software management component should address:

- **What software will you create?** Programming languages, types (libraries, tools, applications), scale, and complexity
- **How will it be managed?** Version control systems (e.g., Git), code review processes, release cycles
- **Contributing guidelines:** Can others contribute? If so, how? (CONTRIBUTING.md file, code of conduct)
- **Public visibility:** When and where will code be publicly available? (GitHub, GitLab, institutional repository)
- **Archiving and preservation:** Where will releases be archived for long-term access? (GitHub with DOI via Zenodo, institutional archive)
- **Licensing:** What open-source license will apply? (MIT, Apache 2.0, GPL, etc.)
- **Maintenance and support:** Who will maintain the code? For how long? What support will be provided?
- **Roles and responsibilities:** Who writes the code? Who reviews? Who manages releases?

### Software Data Formats and Standards

When applicable:

- Prefer community-supported, open, non-proprietary formats
- Ensure compatibility with standard tools and workflows
- Document dependencies and system requirements
- Provide example notebooks or scripts demonstrating usage

---

## Part 3: Publications and Open Results

An OSDMP should describe how research findings and products will be shared beyond traditional publications.

### What are Open Results?

Open results extend far beyond the final peer-reviewed article. They include:

- **Peer-reviewed articles** – Published open-access or in journals allowing immediate public access
- **Preprints** – Early-stage work shared on community servers (arXiv, bioRxiv, etc.)
- **Technical reports and white papers** – Detailed documentation of methods and findings
- **Computational notebooks** – Jupyter notebooks, R Markdown files demonstrating analyses
- **Project documentation** – README files, contributing guidelines, code of conduct, publication policies
- **Datasets with papers** – "Data papers" or "software papers" describing resources
- **Blog posts, videos, podcasts** – Public communication of findings
- **Conference abstracts and presentations** – Early dissemination and community feedback
- **Forum discussions and community engagement** – Open dialogue about research

### Licensing and Copyright for Open Results

When planning to share research products:

- **Identify timing** – What can be made open immediately vs. after embargo periods?
- **Understand publisher policies** – Different journals have different policies on open access and copyright
- **Choose appropriate licenses** – Different licenses apply to data, software, and written works
- **Document restrictions** – If material cannot be openly shared (third-party content, patents), document why and for how long
- **Plan for attribution** – Ensure proper citation and credit pathways are clear

---

## Part 4: Project Governance and Roles

An OSDMP should clearly define who is responsible for implementing open science practices.

### Key Roles to Clarify

- **Principal Investigator:** Overall responsibility for compliance and execution
- **Project lead/coordinator:** Day-to-day management of open science activities
- **Data steward:** Ensures data quality, metadata, and archiving
- **Software lead:** Oversees code development, version control, releases
- **Documentation manager:** Creates and maintains README files, guides, and metadata
- **Community manager:** Engages contributors, responds to issues, manages communications
- **Budget manager:** Allocates resources for open science infrastructure and training

Assign specific roles, include contact information, and clarify decision-making processes.

---

## Best Practices for Open Data Management

### Make Data FAIR

Ensure your data are:

- **Findable**: Use descriptive metadata, standard identifiers (DOIs), and deposit in searchable repositories.
- **Accessible**: Provide clear, documented access procedures. Make data available in open formats without unnecessary restrictions.
- **Interoperable**: Use standard data formats and metadata standards compatible with other tools and systems.
- **Reusable**: Include comprehensive documentation, clear licenses, and sufficient information for others to understand and use the data.

### Prioritize Open Formats

- Use non-proprietary, open file formats (CSV, JSON, NetCDF, GeoTIFF) instead of proprietary formats (Excel, Stata, proprietary software formats).
- Open formats ensure long-term accessibility even if software becomes unavailable.
- Include data in formats suitable for both human and machine reading.

### Create Comprehensive Documentation

- Write detailed README files explaining what the data contains, how it was collected, and any known limitations.
- Create data dictionaries describing each variable: name, type, units, valid ranges, definitions.
- Document any data processing steps, including code used to generate derived datasets.
- Include information about any missing data, outliers, or quality issues.

### Use Persistent Identifiers

- Assign Digital Object Identifiers (DOIs) to datasets, making them citable and permanently locatable.
- Use persistent identifiers for related resources (code repositories, publications, grants).

### Plan for Sensitive Data

- Identify any sensitive data early (personal information, health data, location of endangered species, etc.).
- Document how sensitive data will be de-identified, anonymized, or restricted.
- Provide clear guidance on how researchers can request access to restricted data.
- Ensure compliance with relevant regulations (HIPAA, FERPA, GDPR, etc.).

### Version Your Data

- Use version control for datasets, especially as corrections or updates occur.
- Document changes in each version in a CHANGELOG file.
- Clearly indicate which version is the canonical/recommended version.

### Engage Your Team

- Involve all team members in developing the DMP. Data management is everyone's responsibility.
- Provide training on data management practices and tools.
- Establish regular check-ins to review and update the DMP as project needs evolve.

---

## Tools and Resources for Data Management Planning

### DMP Tools

- **DMPTool** (https://dmptool.org) - Free, web-based tool for creating NSF, NIH, and other funder-compliant DMPs
- **DMPonline** (https://dmponline.dcc.ac.uk) - European tool with institutional support and feedback
- **Madmp** (https://github.com/DMPRoadmap/madmp) - Machine-actionable DMP tool
- **UVM Dataverse** (https://dataverse.uvm.edu) - UVM's institutional repository for open data

### Data Repository Options

- **Zenodo** (https://zenodo.org) - Multidisciplinary, open-access repository
- **Figshare** (https://figshare.com) - Multidisciplinary data sharing platform
- **DRYAD** (https://datadryad.org) - Curated data archive for research data
- **Open Science Framework** (https://osf.io) - Project management and data sharing
- **Discipline-specific repositories**: Identify repositories relevant to your field

### Data Documentation and Standards

- **Data Stewardship Wizard** (https://ds-wizard.org) - Interactive tool for creating machine-actionable DMPs
- **MIAOW** - Machine-readable, actionable open science workflows
- **Frictionless Data Standards** (https://frictionlessdata.io) - Standards for data packaging and validation

### Related Resources

- **Software Carpentries** (https://software-carpentry.org) - Training in data management and analysis
- **FORCE11** (https://www.force11.org) - Community organization advancing scholarly communication
- **ICPSR Data Curation** (https://www.icpsr.umich.edu) - Data curation best practices
- **Research Data Management (RDM) guides** - Check with your institution's library

---

## Creating Your DMP: A Step-by-Step Process

### Phase 1: Planning (Before Research Starts)

1. **Understand funder requirements**: Review funder-specific DMP guidelines and mandatory elements.
2. **Assess your data**: Consider what data your research will generate, approximate volume, and format.
3. **Identify stakeholders**: Involve team members, collaborators, and data stewards.
4. **Draft the DMP**: Use a template or tool appropriate for your funder and discipline.
5. **Get feedback**: Review the DMP with advisors, colleagues, and your institution's data steward.
6. **Include in proposal**: Ensure the DMP is submitted as required by your funding agency.

### Phase 2: Implementation (During Research)

1. **Establish infrastructure**: Set up storage, backup, and version control systems.
2. **Implement documentation**: Begin creating metadata, READMEs, and data dictionaries as data are generated.
3. **Monitor and adjust**: Regularly review whether the DMP is being followed. Adjust as needed.
4. **Train your team**: Ensure all team members understand data management procedures.
5. **Maintain version control**: Document any changes to data and update the DMP accordingly.

### Phase 3: Archiving and Sharing (As Research Concludes)

1. **Prepare data for archiving**: Organize files, finalize documentation, and quality-check datasets.
2. **Choose repositories**: Select appropriate repositories for your data based on discipline and funder requirements.
3. **Create metadata**: Develop comprehensive metadata for discovery and reuse.
4. **Assign licenses**: Apply appropriate open licenses to all data.
5. **Deposit and publish**: Upload data to repositories and obtain DOIs.
6. **Document access procedures**: Provide clear guidance for data access and reuse.

### Phase 4: Preservation and Access (After Research)

1. **Monitor preservation**: Ensure data remain accessible in chosen repositories.
2. **Track citations**: Monitor how your data are cited and reused.
3. **Provide support**: Be available to answer questions from researchers using your data.
4. **Plan for updates**: Consider whether data need updates, corrections, or versioning.
5. **Evaluate impact**: Assess the research impact enabled by your open data.

---

## Common Challenges and Solutions

### Challenge: "We don't have funding for data management."

**Solution**: Data management costs are often eligible expenses in grant proposals. Include them in your budget. Additionally, many repositories and tools are free or low-cost. Focus on practices that improve research efficiency, reducing overall costs.

### Challenge: "Our data are too sensitive to share."

**Solution**: Sensitive data can often be de-identified or anonymized while preserving research value. Publish a "data paper" describing the dataset and its potential uses. Consider controlled-access repositories for sensitive data. Consult your IRB or legal team on appropriate sharing approaches.

### Challenge: "Our team doesn't have time for data management."

**Solution**: Data management takes time upfront but saves time later by preventing errors, duplicate work, and lost data. Automate what you can (automated backups, version control). Make data management everyone's responsibility rather than one person's burden.

### Challenge: "We're not sure which repository to use."

**Solution**: Start by checking funder requirements and discipline standards. Use registry.org to discover repositories. Ask your institution's data steward for recommendations. Many repositories provide guidance on suitability for different data types.

### Challenge: "Our data contain copyrighted material."

**Solution**: If your data incorporate existing copyrighted material, ensure your use complies with copyright law. Open licenses apply to your original work; restricted material must be licensed appropriately. Clearly document any restrictions in your metadata.

---

## Example DMPs

The following simplified examples illustrate how DMPs might look for different types of research:

### Example 1: Climate/Environmental Data

**Data Description**: Hourly weather station data (temperature, precipitation, wind speed) from five stations in Vermont, collected over five years. Approximately 50 GB total.

**Access & Sharing**: Data will be made immediately open via NOAA's Data Integration Platform and UVM Dataverse with CC0 license.

**Storage**: Working copies on university network drive with daily automated backups to cloud storage.

**Documentation**: Standardized metadata using Climate and Forecast (CF) conventions. README files documenting station locations, measurement methods, and data quality.

**Roles**: Graduate student collects data; postdoc processes and validates; faculty member serves as principal investigator and data steward.

**Retention**: Data will be retained indefinitely in NOAA archives.

### Example 2: Qualitative Research (Interviews)

**Data Description**: Transcripts of 50 semi-structured interviews with Vermont residents about community planning (approximately 2 GB text files).

**Access & Sharing**: De-identified transcripts will be made available after one-year embargo via OSF. Coded analysis will be published separately.

**Storage**: Encrypted storage with restricted access to research team. Identifiable data (names, locations) stored separately from transcripts.

**Documentation**: Codebook describing qualitative coding scheme, research protocol, and de-identification procedures.

**Roles**: Graduate student conducts interviews; faculty member manages IRB compliance and data security.

**Retention**: De-identified transcripts retained for 10 years; identifiable data destroyed after 5 years per IRB protocol.

### Example 3: Software and Code

**Data Description**: Python code for hydrological modeling; approximately 5,000 lines across 20 files.

**Access & Sharing**: Code on GitHub (public repository) with associated publications. Releases tagged with DOIs via Zenodo.

**Storage**: GitHub with local backups. Contributor access controlled via GitHub team permissions.

**Documentation**: README with installation instructions, API documentation, example notebooks demonstrating usage.

**Roles**: Lead developer manages repository; all contributors follow branching strategy and code review procedures.

**Retention**: Code retained indefinitely with version history preserved.

---

## Getting Started with Your Open Data Management Plan

1. **Check requirements**: Identify funder and institutional requirements for your research.
2. **Gather your team**: Meet with collaborators and your institution's data steward.
3. **Use a template**: Start with a funder-specific template or the DMPTool.
4. **Think through your data**: Document what data you'll create, how you'll manage it, and how you'll share it.
5. **Plan for compliance**: Ensure your plan addresses privacy, licensing, and preservation needs.
6. **Build in flexibility**: Create a living document that evolves with your research.
7. **Make it actionable**: Include specific, concrete steps your team can follow.
8. **Get feedback**: Share your draft DMP with colleagues and data professionals.
9. **Implement consistently**: Follow your DMP throughout the research lifecycle.
10. **Celebrate impact**: Track how your open data are used and the research impact they enable.

An effective open data management plan is an investment in research quality, reproducibility, and impact. By planning early and implementing consistently, you ensure that the valuable data your research generates will benefit the broader scientific community for years to come.
