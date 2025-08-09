# AGENTS.md - Repository Guidelines

This document provides comprehensive guidelines for developers and agents contributing to this GitHub Pages personal website repository.

## <general_rules>

### Coding Conventions
- **HTML**: Use semantic HTML5 elements with proper indentation (2 spaces)
- **CSS**: Follow BEM methodology for custom classes, maintain consistent spacing
- **JavaScript**: Use modern ES6+ syntax, prefer const/let over var
- **File Organization**: Keep all assets inline or use CDN links to maintain simplicity

### Script Execution Guidelines
- **No Linters/Formatters**: This repository does not use automated linting or formatting tools
- **Manual Code Review**: Ensure code follows web standards and accessibility guidelines
- **Browser Compatibility**: Test across modern browsers (Chrome, Firefox, Safari, Edge)

### Code Organization and Reuse
- Keep custom styles in `<style>` tags within HTML files for this simple static site
- Use SLDS utility classes whenever possible to maintain consistency
- Minimize custom CSS by leveraging the Salesforce Lightning Design System
- Maintain clean, readable code structure with appropriate comments for complex sections

</general_rules>

## <repository_structure>

### Technical Overview
This is a **GitHub Pages personal website** repository hosted at `cstarlea.github.io`. The site is a static HTML page showcasing personal information and professional experience.

### Directory and File Organization
```
cstarlea.github.io/
├── index.html          # Main landing page with personal portfolio content
├── README.md           # Basic project information and description
├── .gitignore          # Node.js patterns (legacy, no Node.js currently used)
└── AGENTS.md           # This documentation file
```

### Key Components
- **`index.html`**: Single-page application using Salesforce Lightning Design System
  - Personal hero section with avatar and introduction
  - Skills and experience sections
  - Contact information
  - Responsive design with SLDS components
- **`README.md`**: Minimal project description
- **`.gitignore`**: Contains Node.js patterns for potential future development

### Hosting
- **Platform**: GitHub Pages
- **URL**: https://cstarlea.github.io
- **Deployment**: Automatic deployment from main branch

</repository_structure>

## <dependencies_and_installation>

### Dependency Management Approach
This repository uses a **CDN-based approach** with no local package management required.

### External Dependencies
- **Salesforce Lightning Design System (SLDS)**: v2.23.7
  - Source: `https://cdn.jsdelivr.net/npm/@salesforce-ux/design-system@2.23.7/assets/styles/salesforce-lightning-design-system.min.css`
  - Purpose: UI framework providing consistent styling and components

### Installation Instructions
1. **Clone the repository**:
   ```bash
   git clone https://github.com/cstarlea/cstarlea.github.io.git
   cd cstarlea.github.io
   ```

2. **Serve locally** (choose one method):
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Node.js (if available)
   npx serve .
   
   # Using PHP (if available)
   php -S localhost:8000
   ```

3. **Access**: Open `http://localhost:8000` in your browser

### Package Managers
- **None required**: This project intentionally avoids build tools and package managers
- **Future considerations**: If Node.js dependencies are added, use `npm` or `yarn`

</dependencies_and_installation>

## <testing_instructions>

### Testing Framework Status
- **No automated testing frameworks** are currently configured for this static website
- **Manual testing approach** is recommended for this simple site

### Testing Guidelines
1. **Browser Testing**:
   - Test in Chrome, Firefox, Safari, and Edge
   - Verify responsive design on mobile, tablet, and desktop viewports
   - Check accessibility using browser dev tools

2. **Visual Testing**:
   - Ensure SLDS components render correctly
   - Verify custom styling doesn't conflict with SLDS
   - Test all interactive elements (links, hover states)

3. **Performance Testing**:
   - Check page load times
   - Verify CDN resources load properly
   - Test with slow network connections

### Manual Test Checklist
- [ ] Page loads without errors
- [ ] All sections display correctly
- [ ] Links work and open appropriately
- [ ] Responsive design functions on different screen sizes
- [ ] SLDS styling is consistent
- [ ] Contact information is accurate

### Future Testing Considerations
If the site grows in complexity, consider adding:
- Lighthouse CI for performance monitoring
- Accessibility testing tools
- Cross-browser testing automation

</testing_instructions>

## <pull_request_formatting>

### General GitHub Best Practices
Since no specific PR templates exist, follow these standard guidelines:

### PR Title Format
- Use clear, descriptive titles
- Start with action verb (Add, Update, Fix, Remove)
- Examples:
  - `Add new skills section to portfolio`
  - `Update contact information`
  - `Fix responsive layout on mobile devices`

### PR Description Template
```markdown
## Description
Brief description of changes made.

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Content update
- [ ] Documentation update
- [ ] Style/UI improvement

## Testing
- [ ] Tested locally in multiple browsers
- [ ] Verified responsive design
- [ ] Checked accessibility

## Screenshots (if applicable)
Include before/after screenshots for visual changes.
```

### Review Guidelines
- **Self-review**: Test changes locally before submitting
- **Small PRs**: Keep changes focused and atomic
- **Documentation**: Update this AGENTS.md file if workflow changes
- **Accessibility**: Ensure changes maintain or improve accessibility

### Merge Strategy
- Use **squash and merge** for clean commit history
- Delete feature branches after merging
- Ensure main branch always represents deployable state

</pull_request_formatting>
