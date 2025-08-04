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

## Recent Updates & Current Structure

### NAIL LAB Navigation (Dropdown Menu)
The site now features a comprehensive NAIL LAB dropdown menu with the following sections:
- **Team Members** (`/team-members/`) - Lab director, PhD students, master students, undergrad projects, and alumni
- **Lab Resources** (`/resources/`) - Equipment, facilities, and capabilities showcase
- **Demonstrations** (`/demonstrations/`) - Research videos and project demos
- **Outreach** (`/outreach/`) - Community engagement and educational programs

### Lab Resources Page (`_pages/resources.md`)
- **Multi-Robotic Platform**: 9 robotic platforms including drones, ground robots, and quadruped
  - 3x ModalAI Seeker SLAM Drones, ModalAI Sentinel 5G drone, 3x ROSbot 2.0 Pro, Jackal J100, Custom drone, Unitree Go2
- **Edge Computing & Development Platforms**: NVIDIA Jetson devices, MAX78000, STM32F746NG kits
- **Advanced Sensors & Equipment**: OptiTrack motion capture, RealSense cameras, LiDAR, 3D printer
- **Testing Arena**: 800 sq ft research space with 24×24×8 ft OptiTrack volume
- All sections use card-based layouts with images from `assets/img/facilities/`
- Dark mode compatible with CSS variables

### Team Members Page (`_pages/Hu_Lab.md`)
- **Lab Director**: Dr. Bin Hu with larger photo (200px) and UH red color scheme
- **PhD Students**: Richie, Shaharyar, Benedictus with updated research interests
- **Master Students**: Tony Tran (current)
- **Alumni**: Organized by degree level (Master/Undergraduate) with graduation years
- **Color scheme**: UH red (#C8102E) for names and links, blue (#007bff) for research tags
- **Photos**: Gray borders that turn red on hover

### Demonstrations Page (`_pages/demonstrations.md`)
- **Lab Equipment Capabilities** (3 videos): Multi-robot coordination, SLAM demos, autonomous navigation
- **Research Projects & Publications** (4 videos): ICRA 2025 papers and submissions
- **Student Research Projects** (1 video): Undergraduate capstone project
- All videos embedded from YouTube with responsive 16:9 containers

### Outreach Page (`_pages/outreach.md`)
- **Educational Programs**: K-12 visits, summer camps, teacher development
- **Community Events**: Science fair judging, public demos, engineering week
- Images sourced from actual outreach activities in corresponding folders

### Data Files Updated
- `_data/phd_members.yml`: Updated research interests for all PhD students
- `_data/master_members.yml`: Removed graduated students, kept current members
- Alumni moved from data files to static lists in Team Members page

### Image Organization
- **Facilities**: `assets/img/facilities/` - All lab equipment images (JPG format)
- **Members**: `assets/img/members/` - Team member photos
- **Outreach**: `assets/img/outreach/` - Community engagement photos
- **Equipment images**: jetson_orin.jpg, jetson_xavier.jpg, jetson_nano.jpg, max78000.jpg, stm32f746.jpg, optitrack.jpg, realsense_d435i.jpg, livox_mid360.jpg, hokuyo_ust10lx.jpg, prusa_mk4.jpg

### Contact Information
- Primary contact: bhu12@uh.edu (used throughout site for contact links)
- All "contact us" links point to this email address

### Development Environment
- Ruby 3.1.2 with rbenv
- Jekyll ~4.3 with al-folio theme
- Local development: `bundle exec jekyll serve --lsi`