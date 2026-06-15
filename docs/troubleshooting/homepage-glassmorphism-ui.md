# Homepage Glassmorphism UI Customization

## Goal

The default Homepage interface was functional but did not align with the visual style envisioned for Archer's Homelab.

The objective was to create a modern glassmorphism-inspired dashboard featuring:

* A custom background image
* Transparent interface elements
* Blur effects
* Dark glass-style panels

## Initial State

Homepage was fully operational using the default appearance.

A custom background image had already been implemented successfully, providing the foundation for further visual customization.

## Challenge

Creating a consistent glassmorphism effect across the entire dashboard proved more challenging than expected.

While some interface elements immediately responded to CSS modifications, others continued using their default styling.

Examples included:

* Service cards
* Information widgets
* Search components
* Header sections

As a result, the dashboard appeared visually inconsistent despite multiple CSS adjustments.

## Investigation

Several iterations of custom CSS were tested throughout the troubleshooting process.

Browser Developer Tools were used extensively to inspect Homepage elements and identify the CSS classes responsible for specific components.

The investigation focused on locating the correct selectors for elements that continued to ignore custom styling.

## Solution

Custom styling was implemented using selectors such as:

```css
.service-card
.info-widget
```

Additional selectors were later identified and customized for:

* Header components
* Information widgets
* Search elements

Glassmorphism effects were achieved using CSS properties such as:

```css
backdrop-filter: blur(...)
```

combined with semi-transparent backgrounds:

```css
rgba(...)
```

These changes created a consistent visual design across the dashboard.

## Result

The final dashboard includes:

* A custom background image
* Glassmorphism-style service cards
* Transparent information panels
* Blur effects throughout the interface
* A consistent dark visual theme

The customized Homepage dashboard now serves as the primary entry point for Archer's Homelab.

## Additional Finding

A significant portion of the troubleshooting process was complicated by browser-side caching.

Several configuration and CSS changes appeared to have no effect, despite the underlying files already being updated correctly.

This initially led to the assumption that the issue was related to Homepage configuration, Docker volumes, file paths or CSS selectors.

After clearing the browser cache and performing a hard refresh, the latest assets and styling changes loaded correctly.

## Lessons Learned

* Browser Developer Tools are invaluable when customizing modern web interfaces.
* A consistent visual design may require multiple CSS selectors rather than a single global change.
* Browser caching can make successful configuration changes appear ineffective.
* Troubleshooting should include both server-side and client-side verification.
* Not every issue originates from the application itself.
* Sometimes the problem is simply the cache.
