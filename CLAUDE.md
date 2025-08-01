# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is an academic personal website built with the al-folio Jekyll theme. It's an academic portfolio site for Dr. Bin Hu featuring publications, CV, lab information, news, and projects. The site is hosted on GitHub Pages.

## Architecture

The site follows Jekyll's standard structure with several key directories:

- `_config.yml` - Main Jekyll configuration file with site settings, theme options, and plugin configurations
- `_pages/` - Main site pages (about, publications, CV, projects, teaching, lab)
- `_posts/` - Blog posts in markdown format
- `_news/` - News announcements displayed on the homepage
- `_projects/` - Project pages with descriptions and images
- `_bibliography/` - BibTeX files for publications (`hu.bib` is the main bibliography)
- `_data/` - YAML data files for CV, lab members, repositories, slides, and venue information
- `_layouts/` - HTML templates for different page types
- `_includes/` - Reusable HTML components
- `_sass/` - SCSS stylesheets for theme customization
- `assets/` - Static assets including images, PDFs, and JavaScript files

## Development Commands

### Local Development
```bash
# Standard Jekyll development (requires Ruby and Bundler)
bundle install
bundle exec jekyll serve --lsi

# Using Docker (recommended on Windows)
docker-compose up

# Build Docker image locally
docker-compose -f docker-local.yml up
```

### Building and Deployment
```bash
# Build site for production
bundle exec jekyll build --lsi

# Deploy to GitHub Pages (manual deployment script)
./bin/deploy

# Build for CI
./bin/cibuild
```

### Docker Commands
```bash
# Run with pre-built Docker image
./bin/dockerhub_run.sh

# Build and run custom Docker image
./bin/docker_build_image.sh
./bin/docker_run.sh
```

## Key Configuration

- **Jekyll version**: ~4.3
- **Theme**: al-folio (academic portfolio theme)
- **Hosting**: GitHub Pages with automatic deployment
- **Bibliography**: Uses jekyll-scholar plugin with `hu.bib` file
- **Analytics**: Google Analytics enabled
- **Features**: Dark mode, math typesetting (MathJax), image optimization, social media integration

## Content Management

### Publications
- Edit `_bibliography/hu.bib` for publications
- Publication images go in `assets/img/publication_preview/`
- Venue abbreviations defined in `_data/venues.yml`
- Author information in `_data/coauthors.yml`

### News and Announcements
- Add markdown files to `_news/` directory
- News items automatically appear on homepage

### Lab Information
- Lab member data in `_data/phd_members.yml`, `_data/master_members.yml`, `_data/undergrad_members.yml`
- Lab images in `assets/img/lab/` and `assets/img/members/`

### CV
- CV data structured in `_data/cv.yml`
- PDF version at `assets/pdf/cv.pdf`

## Important Notes

- The site uses GitHub Actions for automatic deployment to `gh-pages` branch
- Images are automatically optimized and converted to WebP format
- Math equations supported via MathJax
- Bibliography formatting handled by jekyll-scholar plugin
- Dark/light theme toggle available
- Mobile-responsive design with Bootstrap 4.6.1