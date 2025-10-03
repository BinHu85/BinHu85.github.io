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

# Build for CI (used by GitHub Actions)
./bin/cibuild

# Pre-commit hooks (linting and validation)
pre-commit install
pre-commit run --all-files
```

### GitHub Pages Deployment Process
**IMPORTANT**: This repository uses **GitHub Actions workflow** for deployment, NOT the standard GitHub Pages Jekyll build.

```bash
# Push changes to trigger GitHub Actions deployment (correct workflow)
git push origin main

# Force push if needed (when branches are out of sync)
git push origin main --force

# Check deployment status
# Look for "Jekyll Build and Deploy" workflows in GitHub Actions at:
# https://github.com/BinHu85/BinHu85.github.io/actions
```

**Deployment Process:**
1. Push to `main` branch triggers GitHub Actions workflow
2. GitHub Actions builds the site and deploys to `gh-pages` branch
3. GitHub Pages serves from `gh-pages` branch
4. Changes may take 2-5 minutes to appear on live site

**If Changes Don't Appear:**
1. **Check build status** - Go to GitHub Actions tab and verify the workflow completed successfully
2. **Hard refresh browser** - Use Ctrl+F5 (Windows) or Cmd+Shift+R (Mac) to bypass cache
3. **Clear browser cache** - Clear cache for the specific site
4. **Try incognito/private mode** - This bypasses all browser caching
5. **Wait 5-10 minutes** - GitHub Pages can have deployment delays

**Common Issues:**
- Problematic demo posts with custom Liquid tags (`{% twitter %}`, `{% mermaid %}`)
- Ruby gem conflicts (especially `uri` gem) - current Gemfile includes explicit uri dependency for compatibility
- Build failures: Check GitHub Actions logs for specific error messages
- Caching issues: Always try hard refresh before assuming build failed

**Working Configuration:**
- Use the current Gemfile with explicit uri dependency (>= 0.10.1) for compatibility
- Deployment workflow uses Ruby 3.0.2 while local development uses 3.1.2
- Only remove problematic demo posts, don't modify gem dependencies unless necessary
- Make incremental changes and test each one individually

**Important Gems:**
- `jekyll-scholar` for bibliography management
- `jekyll-imagemagick` for automatic image optimization
- `mini_racer` for JavaScript execution
- `classifier-reborn` for LSI (Latent Semantic Indexing)

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
- **Hosting**: GitHub Pages with GitHub Actions deployment workflow
- **Ruby version**: 3.0.2 (GitHub Actions), 3.1.2 (local development)
- **Bibliography**: Uses jekyll-scholar plugin with `hu.bib` file
- **Analytics**: Google Analytics enabled
- **Features**: Dark mode, math typesetting (MathJax), image optimization, social media integration
- **Pre-commit hooks**: Enabled for trailing whitespace, YAML validation, and large file checks

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

## Development Environment

### Local Setup
- **Ruby**: 3.1.2 with rbenv (local), 3.0.2 (GitHub Actions)
- **Jekyll**: ~4.3 with al-folio theme
- **Node.js**: Required for mermaid.cli (GitHub Actions)

### Development Workflow

#### Complete Local Development Procedure
**IMPORTANT**: Follow these exact steps to build the website locally:

```bash
# Step 1: Ensure correct Ruby version is active
eval "$(rbenv init -)"
ruby --version                  # Should show: ruby 3.1.2p20

# Step 2: Install dependencies (first time or when Gemfile changes)
eval "$(rbenv init -)" && bundle install

# Step 3: Start local development server
eval "$(rbenv init -)" && bundle exec jekyll serve --lsi

# Server will be available at: http://127.0.0.1:4000
# Build typically takes 3-4 seconds with image optimization
# Auto-regeneration is enabled - changes reflect automatically
```

#### Troubleshooting Local Development
If you encounter Ruby version issues:
```bash
# Check available Ruby versions
rbenv versions

# Ensure Ruby 3.1.2 is selected (should be automatic via .ruby-version)
rbenv local 3.1.2

# Verify rbenv is properly initialized
eval "$(rbenv init -)"
ruby --version
which ruby                     # Should point to ~/.rbenv/shims/ruby
```

#### Daily Development Workflow
```bash
# Start development session
eval "$(rbenv init -)" && bundle exec jekyll serve --lsi

# Make changes to files
# Website auto-regenerates on file changes

# Before committing (optional)
pre-commit run --all-files      # Runs linting and validation
git add .
git commit -m "Your message"
git push origin main            # Triggers GitHub Actions deployment
```

### Testing Changes
- **Local testing**: Server runs at http://127.0.0.1:4000 (not localhost:4000)
- **Build time**: Expect 3-4 seconds for full build with image optimization
- **Auto-regeneration**: Enabled - changes reflect automatically without restart
- **Image processing**: ImageMagick automatically creates WebP versions at multiple resolutions
- **Production testing**: Push to main branch and check GitHub Actions deployment
- **Build validation**: Run `eval "$(rbenv init -)" && bundle exec jekyll build --lsi` to check for errors

## Recent Development Session Progress

### SOLAR Publication Image Implementation (Latest Session)
Successfully implemented high-quality preview image for SOLAR paper publication with the following key achievements:

#### Problem Resolution
- **Issue**: SOLAR.jpg publication preview had poor content visibility and caused layout collisions with publications below
- **Root Cause**: Image dimensions (2007×1970 pixels, nearly square) didn't fit Jekyll's publication layout constraints (120px height limit)
- **Solution**: Implemented SOLAR_final.jpg (5861×2888 pixels, 966,860 bytes) providing ultra-high resolution for crisp display when scaled down

#### Technical Implementation
- **File Location**: `assets/img/publication_preview/SOLAR.jpg` (replaced with SOLAR_final.jpg)
- **CSS Constraints**: Maintained existing `.preview` class styling with 120px max-height
- **Image Properties**: High-resolution source ensures crisp rendering at all scaling levels
- **Layout Compatibility**: Fits perfectly within existing publication grid without overlapping

#### CSS Configuration
Final working CSS in `_sass/_base.scss`:
```scss
.preview {
  width: 95%;
  min-width: 80px;
  max-width: 200px;
  min-height: 120px;
  max-height: 120px;
  background-color: #f5f5f5;
  object-fit: contain;
  overflow: hidden;
}
```

#### Expandable Image Functionality (Attempted & Reverted)
- **Attempt**: Implemented zoom functionality using existing medium-zoom library
- **Changes Made**: Modified `_layouts/bib.html` with preview containers, zoom icons, and data-zoomable attributes
- **Outcome**: User feedback indicated implementation was problematic
- **Resolution**: Completely reverted all zoom-related changes to restore clean, simple layout
- **Current State**: Publications use standard preview images without expandable functionality

#### Key Files Modified
- `assets/img/publication_preview/SOLAR.jpg` - Replaced with high-resolution version
- `_layouts/bib.html` - Temporarily modified for zoom, then reverted to original structure
- `_sass/_base.scss` - Temporarily added zoom CSS, then reverted to clean preview styling

#### Development Environment Status
- **Local Server**: Running at http://127.0.0.1:4001 with all changes applied
- **Build Status**: All image optimizations and layout changes working correctly
- **Current State**: SOLAR image displays properly with high quality and no layout issues