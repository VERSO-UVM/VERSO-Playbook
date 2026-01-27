# VERSO Playbook

*An open, continually evolving guide to building and sustaining open‑source ecosystems in academia.*

The **VERSO Playbook** documents the methods, practices, philosophy, and lessons learned from operating the **Open Source Program Office (OSPO)** at the University of Vermont. It powers the published site at:  
 **<https://verso-uvm.github.io/VERSO-Playbook/>** [\[github.com\]](https://github.com/VERSO-UVM/VERSO-Playbook)

This repository contains the source materials that generate the public site, including instructional content, case studies, metrics, and documentation supporting VERSO and the ORCA program.

***

## About VERSO

VERSO is the official **Open Source Program Office (OSPO)** at UVM. Its mission is to build open‑source capacity through:

*   High‑impact research software
*   Community and partnership development
*   Student training and open‑source workforce preparation
*   Open data publishing and open research practices

More about VERSO’s broader work can be found through the VERSO site and project listings. [\[gitlab.uvm.edu\]](https://gitlab.uvm.edu/verso)

***

## Repository Structure

According to the GitHub listing, the repository contains:

*   `book/` — Source content for the Jupyter Book site
*   `.github/workflows/` — automation for building/deploying the site via GitHub Actions
*   `requirements.txt` — Build dependencies
*   `LICENSE` — MIT License    [\[github.com\]](https://github.com/VERSO-UVM/VERSO-Playbook)

***

# Working With the VERSO Playbook (Jupyter Book)

The Playbook is built using **Jupyter Book**, a static site generator for notebooks, Markdown files, and narrative documentation. Below is a full workflow for cloning, editing, building, and contributing to the Playbook.

***

## 1. Clone the Repository

From your terminal:

```bash
git clone https://github.com/VERSO-UVM/VERSO-Playbook.git
cd VERSO-Playbook
```

If you plan to contribute changes, create a feature branch:

```bash
git checkout -b your-feature-name
```

***

## 2. Install Dependencies

The repository includes a `requirements.txt` file for building the book. Install dependencies in a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate   # macOS / Linux
# OR
.venv\Scripts\activate      # Windows

pip install -r requirements.txt
```

This prepares your environment with Jupyter Book and other necessary tools.

***

## 3. Editing the Playbook

### All editable content lives in:

    book/

Inside you will find Markdown (`.md`) files and potentially Jupyter notebooks (`.ipynb`). You can:

*   Edit Markdown directly in your text editor
*   Use JupyterLab or VS Code to edit notebooks
*   Add new pages and update the `_toc.yml` file to include them in the site navigation

To open the environment with Jupyter:

```bash
jupyter lab
```

***

## 4. Build the Jupyter Book Locally

The command to build a Jupyter Book is:

```bash
jupyter-book build book/
```

This generates a static website in:

    book/_build/html/

Open it locally:

```bash
open book/_build/html/index.html  # macOS
xdg-open book/_build/html/index.html  # Linux
start book\_build\html\index.html  # Windows
```

***

## 5. Commit and Push Changes

Once you’ve edited and tested your changes:

```bash
git add .
git commit -m "Describe your changes"
git push origin your-feature-name
```

Then open a Pull Request on GitHub.

***

## 6. Deployment (GitHub Actions)

The Playbook uses GitHub Actions to automatically rebuild and deploy the site when updates are pushed to the main branch. You can review these workflows in:

    .github/workflows/

These automate the deployment to GitHub Pages. [\[github.com\]](https://github.com/VERSO-UVM/VERSO-Playbook)

***

# License

This repository is licensed under the MIT License. See the `LICENSE` file for details.    [\[github.com\]](https://github.com/VERSO-UVM/VERSO-Playbook)

***

# Contributing

Contributions are welcome! Whether you’re improving documentation, adding examples, or expanding guidance, feel free to submit a Pull Request. The Playbook is intended to be a living document shaped by its community.

For those involved in VERSO or ORCA, contributions align with the broader collaborative ethos described across VERSO’s open work. [\[verso-uvm.github.io\]](https://verso-uvm.github.io/ORCA/)

