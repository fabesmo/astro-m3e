# Astro M3E

A modern Astro UI component library based on **Material 3 Expressive** design system. Components are pre-rendered on the server and then hydrated with Web Components to prevent layout shifts while maintaining full interactivity.

## Features

- 🎨 **Material 3 Expressive Design** - Beautiful, modern UI components
- ⚡ **Server-Side Rendering** - Components are pre-rendered for optimal performance
- 🔧 **Web Components Hydration** - Interactive components without layout shifts
- 🎯 **TypeScript Support** - Full type safety and IntelliSense
- 📱 **Responsive Design** - Mobile-first, accessible components
- 🔍 **Rich Icon Library** - 1000+ Material Design symbols included

## Installation

```bash
npm install astro-m3e
```

## Quick Start

1. Add the component library to your Astro project:

```astro
---
import { TextField } from 'astro-m3e';
---

<TextField 
  label="Email" 
  type="email" 
  icon="email" 
  supportingText="Enter your email address"
/>
```

2. Import the global styles in your layout:

```astro
---
import 'astro-m3e/globals.css';
---
```

## Components

### Input Components

#### TextField
A versatile text input component with Material 3 styling.

```astro
---
import { TextField } from 'astro-m3e';
---

<!-- Basic usage -->
<TextField label="Name" />

<!-- With icon and supporting text -->
<TextField 
  label="Email" 
  type="email" 
  icon="email" 
  supportingText="We'll never share your email"
/>

<!-- With custom attributes -->
<TextField 
  label="Password" 
  type="password" 
  required 
  maxlength="50"
/>
```

**Props:**
- `label` (string, required) - The label text for the input
- `icon` (string, optional) - Material Design icon name
- `iconSrc` (string, optional) - Custom icon source URL
- `supportingText` (string, optional) - Helper text below the input
- All standard HTML input attributes are supported

#### TextAreaField
A multi-line text input component.

```astro
---
import { TextAreaField } from 'astro-m3e';
---

<TextAreaField 
  label="Message" 
  rows="4" 
  supportingText="Share your thoughts"
/>
```

**Props:**
- `label` (string, required) - The label text for the textarea
- `icon` (string, optional) - Material Design icon name
- `iconSrc` (string, optional) - Custom icon source URL
- `supportingText` (string, optional) - Helper text below the textarea
- All standard HTML textarea attributes are supported

#### SelectField
A styled select dropdown component.

```astro
---
import { SelectField } from 'astro-m3e';
---

<SelectField 
  label="Country" 
  icon="location_on"
  supportingText="Choose your country"
>
  <option value="us">United States</option>
  <option value="ca">Canada</option>
  <option value="mx">Mexico</option>
</SelectField>
```

**Props:**
- `label` (string, required) - The label text for the select
- `icon` (string, optional) - Material Design icon name
- `iconSrc` (string, optional) - Custom icon source URL
- `supportingText` (string, optional) - Helper text below the select
- All standard HTML select attributes are supported

### Icon Component

#### Symbol
Renders Material Design icons with customizable styling.

```astro
---
import { Symbol } from 'astro-m3e';
---

<!-- Basic icon -->
<Symbol name="home" />

<!-- Filled variant -->
<Symbol name="favorite" fill />

<!-- Custom size and color -->
<Symbol 
  name="star" 
  size="32px" 
  color="#FFD700" 
/>
```

**Props:**
- `name` (string, required) - Material Design icon name
- `fill` (boolean, optional) - Use filled variant of the icon
- `size` (string, optional) - Icon size (default: "24px")
- `color` (string, optional) - Icon color
- Additional HTML attributes are supported

## Icon Library

The package includes 1000+ Material Design symbols in both outlined and filled variants. Icons are automatically optimized and tree-shaken for minimal bundle size.

Popular icons include:
- `home`, `menu`, `search`, `person`, `settings`
- `email`, `phone`, `location_on`, `favorite`, `star`
- `add`, `edit`, `delete`, `close`, `check`
- `arrow_back`, `arrow_forward`, `expand_more`, `expand_less`

For a complete list of available icons, check the `/src/assets/symbols/rounded/` directory.

## Styling

### CSS Custom Properties

Components use CSS custom properties for theming. You can customize the appearance by overriding these variables:

```css
:root {
  --md-sys-color-primary: #6750a4;
  --md-sys-color-on-primary: #ffffff;
  --md-sys-color-surface: #fffbfe;
  --md-sys-color-on-surface: #1c1b1f;
  /* ... additional theme variables */
}
```

### Global Styles

Import the global stylesheet to get Material 3 design tokens and base styles:

```astro
---
import 'astro-m3e/globals.css';
---
```

## TypeScript Support

All components are fully typed with TypeScript. Import types for enhanced development experience:

```typescript
import type { Props as TextFieldProps } from 'astro-m3e/TextField';
```

## Browser Support

- Chrome/Edge 88+
- Firefox 87+
- Safari 14+
- iOS Safari 14.4+

## Contributing

Contributions are welcome! Please read our [Contributing Guide](CONTRIBUTING.md) for details on our code of conduct and development process.

## License

MIT © [fabesmo](https://github.com/fabesmo)

## Links

- [Repository](https://github.com/fabesmo/astro-m3e)
- [Issues](https://github.com/fabesmo/astro-m3e/issues)
- [Material 3 Design](https://m3.material.io/)
- [Astro Documentation](https://docs.astro.build/)