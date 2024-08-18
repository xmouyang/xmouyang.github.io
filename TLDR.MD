# Structure
```
.
├── 📂 assets/
│   └── 📂 img/: all images
├── 📂 _bibliography/
│   └── 📄 papers.bib: bibliography in BibTeX format(**please open it to see details**)
├── 📄 _config.yml: the configuration file of the template
├── 📂 _includes/: contains code parts that are included in the main HTML file(**can modify for customization**)
├── 📂 _layouts/: contains the layouts to choose from in the frontmatter of the Markdown files(**can modify for customization**)
├── 📂 _news/: the news that will appear in the news section in the about page (**Edit news in this directory**)
├── 📂 _pages/: contains the pages of the website
|   ├── 📄 404.md: 404 page (page not found)
|   ├── 📄 about.md: main page for personal information
|   ├── 📄 awards.md
|   ├── 📄 news.md: invoke news from `_news/`
|   ├── 📄 opening.md
|   ├── 📄 publications.md: invoke papers from `_bibliography/papers.bib/`
|   ├── 📄 service.md
|   ├── 📄 teaching.md
│   └── 📄 team.md
└── 📂 _sass/: contains the SASS files that define the style of the website(**can modify for customization**)
```

# Deploying local server
For installation and deployment details please refer to [INSTALL.md](INSTALL.md).

# Deploying by github actions
Just push the commit to the `master` branch, the github actions will deployment the webpage automatically.


1. Create a new repository named`<your-github-username>.github.io`.
2. Clone this repository and push two branches(`master`, `gh-pages`) to the new repo.
2. In this new repository, go to `Settings -> Actions -> General -> Workflow permissions` and give `Read and write permissions` to GitHub Actions.
3. Open file `_config.yml`, set `url` to `https://<your-github-username>.github.io` and leave `baseurl` **empty** (do NOT delete it).
4. Wait until the GitHub actions finish (check your repository **Actions** tab). Now, in addition to the master branch, your repository has a newly built gh-pages branch.
5. Finally, in the repository page go to `Settings -> Pages -> Build and deployment`, make sure that `Source` is set to `Deploy from a branch` and set the branch to `gh-pages` (NOT to master).
6. Wait until the GitHub actions finish (check your repository **Actions** tab)