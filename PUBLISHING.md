# Publishing Workflow

Guide for publishing PicoCTF writeups across GitHub, Medium, and aerobytes.io.

## Pre-Publishing Checklist

- [ ] Challenge completed and flag verified
- [ ] Writeup follows TEMPLATE.md structure
- [ ] All code snippets tested and working
- [ ] Screenshots/images optimized (PNG preferred, <500KB)
- [ ] Links verified and defanged where appropriate
- [ ] Spell check and grammar review completed

## Publishing Order

### 1. GitHub (Primary)

**Location**: `PicoCTF-Writeups/[category]/[challenge-name].md`

**Steps**:
1. Open GitHub Desktop
2. Navigate to your PicoCTF-Writeups repository
3. Create writeup in appropriate category folder
4. Add images to `assets/images/[challenge-name]/`
5. In GitHub Desktop:
   - Review changes in the left panel
   - Write commit message: `Add [Challenge Name] writeup`
   - Click "Commit to main"
   - Click "Push origin"

**Naming convention**: Use kebab-case for files (e.g., `buffer-overflow-1.md`)

### 2. Medium (For Visibility)

**Steps**:
1. Copy content from GitHub markdown
2. Convert to Medium's editor:
   - Upload images directly to Medium
   - Format code blocks with Medium's code formatting
   - Add pull quote for the intro paragraph
3. Add SEO elements:
   - **Title**: `[Challenge Name] - PicoCTF [Year] Writeup`
   - **Subtitle**: One-line summary (140 chars max)
   - **Tags**: `Cybersecurity`, `CTF`, `PicoCTF`, `[Category]`, `[Technique]`
4. Add canonical URL at bottom: Link to GitHub version
5. Add footer:
   ```
   More writeups: https://aerobytes.io/writeups
   GitHub: https://github.com/Aeronique/PicoCTF-Writeups
   ```

**Timing**: Publish Tuesday-Thursday, 9-11 AM EST for maximum visibility

**Series**: Add to "PicoCTF Writeups" series/collection

### 3. aerobytes.io (Long-term SEO)

**Location**: `/writeups/picoctf/[challenge-name]/`

**Frontmatter** (if using static site generator):
```yaml
---
title: "[Challenge Name] - PicoCTF [Year]"
date: YYYY-MM-DD
category: CTF
tags:
  - picoctf
  - [category]
  - [technique]
difficulty: [Easy/Medium/Hard]
points: [value]
---
```

**Steps**:
1. Convert GitHub markdown to site format
2. Ensure images use correct path: `/assets/images/picoctf/[challenge-name]/`
3. Add breadcrumb navigation
4. Include related writeups section at bottom
5. Deploy and verify rendering

## SEO Optimization

### For All Platforms

**Title format**: `[Challenge Name] - PicoCTF [Year] Writeup`
- Includes primary keyword (challenge name)
- Includes platform (PicoCTF)
- Includes year for freshness signals
- Includes "writeup" for search intent

**First paragraph must include**:
- Challenge name
- PicoCTF + year
- Category
- Brief description of what's learned

**Image alt text**: Always descriptive (e.g., "Screenshot showing buffer overflow in GDB debugger")

### Medium-Specific

**Tags strategy**:
1. `Cybersecurity` (broad reach)
2. `CTF` (community)
3. `PicoCTF` (specific platform)
4. Category tag: `Web Exploitation`, `Forensics`, etc.
5. Technique tag: `Buffer Overflow`, `SQL Injection`, etc.

**Distribution**:
- Submit to InfoSec Write-ups publication (if accepted)
- Share in relevant Reddit communities (r/netsec, r/hacking)
- Cross-post to LinkedIn with professional framing

### aerobytes.io-Specific

**Internal linking**:
- Link to related writeups in same category
- Link to tool documentation/homelab posts where relevant
- Update writeup index page

**Metadata**:
- Schema.org markup for technical articles
- Open Graph tags for social sharing
- Twitter card tags

## Cross-Linking Strategy

Each writeup should link to the other two versions:

**In GitHub README**:
```markdown
Also published on [Medium](link) and [aerobytes.io](link)
```

**In Medium post** (bottom):
```markdown
📝 Full technical version on GitHub: [link]
🌐 More writeups: https://aerobytes.io/writeups
```

**On aerobytes.io**:
```markdown
GitHub: [Repository link]
Medium: [Article link]
```

## Quality Standards

**Before publishing**:
- No AI-generated fluff or buzzwords
- Commands are tested and reproducible
- Code follows human patterns (no over-commenting)
- Screenshots show relevant information clearly
- No excessive formatting (keep it clean)
- Technical accuracy verified

**Writing style**:
- Technical but accessible
- Some personality, not dry
- No "breakthrough", "game-changing", "leverage" unless genuinely appropriate
- Active voice preferred
- Short paragraphs for readability

**Flag formatting**:
- Use `<details>` spoiler tags on GitHub and aerobytes.io
- Medium doesn't support HTML details tags, use bold warning instead:
  ```
  **Flag** (spoiler ahead):
  
  picoCTF{flag_goes_here}
  ```

## Post-Publishing

- [ ] Verify all links work on all platforms
- [ ] Check mobile rendering on aerobytes.io
- [ ] Monitor Medium stats (engagement, reads)
- [ ] Update main README if it's a particularly notable writeup
- [ ] Share on social media (if desired)

## Notes

- GitHub is source of truth - always update there first
- Medium gets immediate traffic and SEO juice
- aerobytes.io builds long-term domain authority
- Keep all three synchronized when making updates
- Track which writeups perform best on Medium for future content strategy
