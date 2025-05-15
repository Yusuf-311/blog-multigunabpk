# Around - Multipurpose Bootstrap Template with Interactive Data Visualization

Around is a feature-rich Bootstrap template that combines modern UI components with interactive data visualization capabilities. It provides a comprehensive set of UI elements, custom JavaScript functionality, and data visualization tools to build responsive web applications.

The template offers extensive customization options through modular components and plugins. Key features include masonry grid layouts, sticky navigation, form validation, file upload handling, and interactive data visualizations powered by D3.js. The template uses modern web technologies and follows best practices for performance and maintainability.

## Repository Structure
```
vendor/                      # Third-party dependencies and libraries
├── flatpickr/              # Date/time picker component
├── imagesloaded/           # Image loading handling library
├── jarallax/               # Parallax scrolling effects
├── lightgallery.js/        # Lightbox gallery component
├── nouislider/             # Range slider component
├── prismjs/                # Syntax highlighting
├── shufflejs/              # Filtering/sorting for grids
├── simplebar/              # Custom scrollbar implementation
├── smooth-scroll/          # Smooth scrolling functionality
└── tiny-slider/           # Lightweight carousel/slider
js/
├── theme.js               # Core template functionality
├── theme.min.js          # Minified core JavaScript
├── jaringan.js           # D3.js visualization implementation
└── mailto.js             # Email handling utilities
css/
├── theme.css             # Core template styles
├── theme.min.css         # Minified core styles
├── style.css             # Custom styles
└── jaringan.css         # Visualization-specific styles
```

## Usage Instructions
### Prerequisites
- Node.js 12+ for development tools
- Modern web browser with JavaScript enabled
- Basic understanding of Bootstrap 5
- Familiarity with D3.js for visualization customization

### Installation
1. Clone the repository:
```bash
git clone [repository-url]
cd around-template
```

2. Install dependencies:
```bash
npm install
```

3. Include required CSS files in your HTML:
```html
<link rel="stylesheet" href="vendor/bootstrap/dist/css/bootstrap.min.css">
<link rel="stylesheet" href="css/theme.min.css">
<link rel="stylesheet" href="css/style.css">
```

4. Include required JavaScript files:
```html
<script src="vendor/bootstrap/dist/js/bootstrap.bundle.min.js"></script>
<script src="js/theme.min.js"></script>
```

### Quick Start
1. Create a basic page layout:
```html
<!DOCTYPE html>
<html>
<head>
    <!-- Include CSS files -->
</head>
<body>
    <div class="page-wrapper">
        <!-- Add your content here -->
    </div>
    <!-- Include JavaScript files -->
</body>
</html>
```

2. Add components using provided classes:
```html
<!-- Masonry Grid -->
<div class="masonry-grid">
    <div class="masonry-grid-item">...</div>
</div>

<!-- Sticky Navbar -->
<header class="navbar navbar-sticky">...</header>
```

### More Detailed Examples
1. Implementing a masonry grid with filtering:
```html
<div class="masonry-filterable">
    <div class="masonry-filters">
        <button data-group="all">All</button>
        <button data-group="category1">Category 1</button>
    </div>
    <div class="masonry-grid">
        <div class="masonry-grid-item" data-groups='["category1"]'>...</div>
    </div>
</div>
```

2. Adding form validation:
```html
<form class="needs-validation" novalidate>
    <div class="form-group">
        <input type="text" class="form-control" required>
        <div class="invalid-feedback">Please fill out this field.</div>
    </div>
</form>
```

### Troubleshooting
Common issues and solutions:

1. Masonry grid not initializing:
- Ensure all images are loaded using imagesLoaded plugin
- Check console for JavaScript errors
- Verify correct class names are used

2. Sticky navbar not working:
- Confirm navbar has `navbar-sticky` class
- Check scroll offset settings
- Verify no conflicting position styles

3. Data visualization issues:
- Check browser console for D3.js errors
- Verify data format matches expected structure
- Ensure SVG container has correct dimensions

## Data Flow
The template processes user interactions and data through a component-based architecture, with centralized state management for UI components.

```ascii
[User Input] -> [Event Handlers] -> [Component State] -> [DOM Updates]
     ^                                    |                    |
     |                                    v                    v
[Data Sources] <- [Data Processing] <- [Visualization] <- [Rendering]
```

Key component interactions:
- Event handlers capture user interactions
- Component state manages UI updates
- Data processing transforms raw data for visualization
- D3.js handles visualization rendering
- DOM updates reflect state changes
- Event system enables component communication
- Error handling provides user feedback
- Async operations manage data loading