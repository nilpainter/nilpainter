# Nil Painter Site Setup Guide

## 🎨 Theme: Gruvbox-Inspired Dark & Cozy

Your site now uses a custom Gruvbox color scheme with:
- Dark background (#282828)
- Off-white text (#ebdbb2)
- Warm orange accents (#fe8019)
- Natural wood tones

## 📁 Content Structure

### Blog Posts (`content/blog/`)
Daily studio journal entries - "Today I..."

**To create a new blog post:**
```bash
hugo new content/blog/my-post-title.md
```

### Projects (`content/projects/`)
Individual art pieces with their own stories and updates.

**To create a new project:**
```bash
hugo new content/projects/my-painting-name.md
```

**To add updates to a project:**
Use the same `series` name in the front matter:
```yaml
---
title: "My Painting: Update 2"
date: 2026-01-16
series: ["My Painting Name"]
---
```

All posts with the same series name will be grouped together!

## 🖼️ Header Images

### To add rotating header images:

1. Add your studio photos to `static/img/`:
   - `studio-1.jpg`
   - `studio-2.jpg`
   - `paints.jpg`
   - `workspace.jpg`
   - etc.

2. Edit `config/_default/params.toml` and change:
```toml
homepageImage = "img/studio-1.jpg"
```

3. For individual posts, add to front matter:
```yaml
---
title: "My Post"
featureImage: "img/studio-2.jpg"
---
```

## 🎨 Color Customization

Colors are defined in `assets/css/schemes/custom.css`

Current Gruvbox palette:
- Background: `#282828` (dark warm gray)
- Text: `#ebdbb2` (off-white)
- Primary (links, accents): `#fe8019` (warm orange)
- Secondary: `#fabd2f` (warm yellow)

Feel free to adjust these to match your studio aesthetic!

## 🚀 Development

**Local preview:**
```bash
hugo server -D
```
Then visit `http://localhost:1313`

**Build for production:**
```bash
hugo --gc --minify
```

**Deploy:**
```bash
git add .
git commit -m "Update content"
git push
```

GitHub Actions will automatically build and deploy!

## 📝 Writing Tips

### Front Matter Examples

**Blog post:**
```yaml
---
title: "Today I mixed the perfect burnt umber"
date: 2026-01-16
draft: false
tags: ["studio-life", "color-mixing"]
---
```

**Project start:**
```yaml
---
title: "Autumn Landscape"
date: 2026-01-16
draft: false
tags: ["oil", "landscape"]
series: ["Autumn Landscape"]
featureImage: "img/autumn-sketch.jpg"
---
```

**Project update:**
```yaml
---
title: "Autumn Landscape: First Layers"
date: 2026-01-17
draft: false
series: ["Autumn Landscape"]
tags: ["work-in-progress"]
---
```

## 🎯 Next Steps

1. Add your studio photos to `static/img/`
2. Update `config/_default/params.toml` with your header image
3. Delete the example posts once you've added your own
4. Start documenting your painting journey!

Happy painting! 🎨

