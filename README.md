# ng-hub-ui-action-sheet

[Español](./README.es.md) | **English**

[![NPM Version](https://img.shields.io/npm/v/ng-hub-ui-action-sheet.svg)](https://www.npmjs.com/package/ng-hub-ui-action-sheet)
[![License](https://img.shields.io/npm/l/ng-hub-ui-action-sheet.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Pre--release-orange.svg)](https://github.com/carlos-morcillo/ng-hub-ui-action-sheet)

> Modern, accessible, mobile-first action sheet components for Angular, part of the Hub UI ecosystem.

> ⚠️ **Pre-release notice (v0.0.1)**
> This library is an early scaffold. The published package currently ships a single
> placeholder standalone component and does **not** yet implement a working action sheet.
> The API described under [Planned API](#-planned-api) is a design target and is **not
> available yet**. Pin an exact version and expect breaking changes before `1.0.0`.

## Documentation and Live Examples

This package is part of [Hub UI](https://hubui.dev/en/), a collection of Angular component libraries for standalone apps.

- Docs: https://hubui.dev/en/action-sheet/overview/
- Live examples: https://hubui.dev/en/action-sheet/examples/
- Hub UI: https://hubui.dev/en/

> **Note:** Documentation pages and live examples are being prepared while the library is in development.

## 🧩 Library Family `ng-hub-ui`

This library is part of the **ng-hub-ui** ecosystem:

- [**ng-hub-ui-accordion**](https://www.npmjs.com/package/ng-hub-ui-accordion) (deprecated — use ng-hub-ui-panels)
- [**ng-hub-ui-action-sheet**](https://www.npmjs.com/package/ng-hub-ui-action-sheet) ← You are here
- [**ng-hub-ui-avatar**](https://www.npmjs.com/package/ng-hub-ui-avatar)
- [**ng-hub-ui-board**](https://www.npmjs.com/package/ng-hub-ui-board)
- [**ng-hub-ui-breadcrumbs**](https://www.npmjs.com/package/ng-hub-ui-breadcrumbs)
- [**ng-hub-ui-calendar**](https://www.npmjs.com/package/ng-hub-ui-calendar)
- [**ng-hub-ui-dropdown**](https://www.npmjs.com/package/ng-hub-ui-dropdown)
- [**ng-hub-ui-ds**](https://www.npmjs.com/package/ng-hub-ui-ds)
- [**ng-hub-ui-forms**](https://www.npmjs.com/package/ng-hub-ui-forms)
- [**ng-hub-ui-history**](https://www.npmjs.com/package/ng-hub-ui-history)
- [**ng-hub-ui-milestones**](https://www.npmjs.com/package/ng-hub-ui-milestones)
- [**ng-hub-ui-modal**](https://www.npmjs.com/package/ng-hub-ui-modal)
- [**ng-hub-ui-nav**](https://www.npmjs.com/package/ng-hub-ui-nav)
- [**ng-hub-ui-paginable**](https://www.npmjs.com/package/ng-hub-ui-paginable)
- [**ng-hub-ui-panels**](https://www.npmjs.com/package/ng-hub-ui-panels)
- [**ng-hub-ui-portal**](https://www.npmjs.com/package/ng-hub-ui-portal)
- [**ng-hub-ui-skeleton**](https://www.npmjs.com/package/ng-hub-ui-skeleton)
- [**ng-hub-ui-sortable**](https://www.npmjs.com/package/ng-hub-ui-sortable)
- [**ng-hub-ui-stepper**](https://www.npmjs.com/package/ng-hub-ui-stepper)
- [**ng-hub-ui-utils**](https://www.npmjs.com/package/ng-hub-ui-utils)

---

## 📦 Description

`ng-hub-ui-action-sheet` aims to provide modern, accessible action sheets (bottom sheets)
for Angular standalone applications — ideal for presenting contextual actions on mobile
interfaces where screen space is limited. It is designed to integrate cleanly with
Bootstrap utilities and the Hub UI design system.

The library is built as a **standalone-component** Angular package (no NgModules).

## 🚦 Status

This package is in **pre-release (`0.0.1`)**. The action sheet feature set is still being
built. What ships today is a placeholder component used to bootstrap the package; the rich
action-sheet API is planned and not yet implemented.

### What exists today

| Symbol         | Selector           | Status              | Notes                                          |
| -------------- | ------------------ | ------------------- | ---------------------------------------------- |
| `ActionSheet`  | `lib-action-sheet` | ✅ Available (stub) | Placeholder standalone component. Renders static markup only — no inputs, outputs, or behavior yet. |

### Planned features

- 📱 **Mobile-first design** with optional swipe-to-close gestures
- 🎯 **Bootstrap-compatible** structure and utility-class friendly markup
- ♿ **Accessibility** (WCAG 2.1 AA target): focus management, keyboard navigation, screen reader support
- 🎭 **Multiple variants** (e.g. iOS-style, Material-style, Bootstrap-modal-like)
- 🧩 **Grouped actions**, headers, footers, and cancel actions
- 🎨 **CSS variable theming** via `--hub-*` design tokens
- 🌳 **Tree-shakeable** standalone components

> All planned features above are design targets and are **not yet available** in `0.0.1`.

## 🚀 Installation

```bash
npm install ng-hub-ui-action-sheet
```

## ⚙️ Usage

> The only component currently exported is a placeholder. The example below reflects what
> is **actually available** in `0.0.1`.

```typescript
import { Component } from '@angular/core';
import { ActionSheet } from 'ng-hub-ui-action-sheet';

@Component({
	selector: 'app-example',
	standalone: true,
	imports: [ActionSheet],
	template: `<lib-action-sheet></lib-action-sheet>`
})
export class ExampleComponent {}
```

## 🪄 API Reference

### `ActionSheet` component

- **Selector:** `lib-action-sheet`
- **Type:** standalone component
- **Change detection:** default
- **Inputs:** none
- **Outputs:** none
- **Content:** renders a static placeholder template

There is no other public API at this stage. The interfaces below illustrate the **intended**
shape of the upcoming API and are documented here only to communicate direction — they are
**not exported** yet.

```typescript
// 🔮 Planned (not available in 0.0.1)
interface ActionSheetAction {
	title: string;
	icon?: string;
	handler?: () => void;
	variant?: 'default' | 'primary' | 'secondary' | 'success' | 'danger' | 'warning' | 'info';
	disabled?: boolean;
}

interface ActionSheetConfig {
	title?: string;
	cancelText?: string;
	swipeToClose: boolean;
	backdropDismiss: boolean;
	animation: 'slide' | 'fade' | 'none';
	position: 'bottom' | 'center';
}
```

## 🤝 Contribution

Contributions are welcome — this is an early-stage library and help shaping the API is
especially valuable.

```bash
# Clone the repository
git clone https://github.com/carlos-morcillo/ng-hub-ui-action-sheet.git

# Install dependencies
npm install

# Build the library
ng build action-sheet

# Run unit tests
ng test action-sheet
```

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/amazing-feature`
3. **Add tests** for your changes
4. **Commit** your changes: `git commit -m 'feat: add amazing feature'`
5. **Push** to your branch: `git push origin feature/amazing-feature`
6. **Open** a pull request

## ☕ Support

Do you like this library? You can support its development by buying a coffee ☕:
[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://buymeacoffee.com/carlosmorcillo)

- [Report a bug](https://github.com/carlos-morcillo/ng-hub-ui-action-sheet/issues)
- [Request a feature](https://github.com/carlos-morcillo/ng-hub-ui-action-sheet/issues/new)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

MIT © ng-hub-ui contributors
