# ng-hub-ui-action-sheet

**Español** | [English](./README.md)

[![Versión NPM](https://img.shields.io/npm/v/ng-hub-ui-action-sheet.svg)](https://www.npmjs.com/package/ng-hub-ui-action-sheet)
[![Licencia](https://img.shields.io/npm/l/ng-hub-ui-action-sheet.svg)](LICENSE)
[![Estado](https://img.shields.io/badge/Estado-Pre--release-orange.svg)](https://github.com/carlos-morcillo/ng-hub-ui-action-sheet)

> Componentes de action sheet modernos, accesibles y mobile-first para Angular, parte del ecosistema Hub UI.

> ⚠️ **Aviso pre-release (v0.0.1)**
> Esta biblioteca es un esqueleto inicial. El paquete publicado incluye actualmente un único
> componente standalone de marcador de posición y **todavía no** implementa un action sheet
> funcional. La API descrita en [API planificada](#-api-planificada) es un objetivo de diseño
> y **aún no está disponible**. Fija una versión exacta y espera cambios disruptivos antes de `1.0.0`.

## Documentación y ejemplos en vivo

Este paquete forma parte de [Hub UI](https://hubui.dev/en/), una colección de bibliotecas de componentes Angular para aplicaciones standalone.

- Documentación: https://hubui.dev/en/action-sheet/overview/
- Ejemplos en vivo: https://hubui.dev/en/action-sheet/examples/
- Hub UI: https://hubui.dev/en/

> **Nota:** Las páginas de documentación y los ejemplos en vivo se están preparando mientras la biblioteca está en desarrollo.

## 🧩 Familia `ng-hub-ui`

Esta biblioteca forma parte del ecosistema **ng-hub-ui**:

- [**ng-hub-ui-accordion**](https://www.npmjs.com/package/ng-hub-ui-accordion) (obsoleto — usa ng-hub-ui-panels)
- [**ng-hub-ui-action-sheet**](https://www.npmjs.com/package/ng-hub-ui-action-sheet) ← Estás aquí
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

## 📦 Descripción

`ng-hub-ui-action-sheet` busca ofrecer action sheets (paneles inferiores) modernos y accesibles
para aplicaciones Angular standalone — ideales para presentar acciones contextuales en interfaces
móviles donde el espacio en pantalla es limitado. Está diseñado para integrarse limpiamente con
las utilidades de Bootstrap y el sistema de diseño de Hub UI.

La biblioteca se construye como un paquete Angular basado en **componentes standalone** (sin NgModules).

## 🚦 Estado

Este paquete está en **pre-release (`0.0.1`)**. El conjunto de funcionalidades del action sheet
todavía se está construyendo. Lo que se publica hoy es un componente de marcador de posición usado
para inicializar el paquete; la API completa del action sheet está planificada y aún no implementada.

### Qué existe hoy

| Símbolo        | Selector           | Estado                  | Notas                                          |
| -------------- | ------------------ | ----------------------- | ---------------------------------------------- |
| `ActionSheet`  | `lib-action-sheet` | ✅ Disponible (esqueleto) | Componente standalone de marcador de posición. Solo renderiza marcado estático — todavía sin inputs, outputs ni comportamiento. |

### Funcionalidades planificadas

- 📱 **Diseño mobile-first** con gestos opcionales de deslizar para cerrar
- 🎯 **Compatible con Bootstrap**: estructura y marcado amigable con clases de utilidad
- ♿ **Accesibilidad** (objetivo WCAG 2.1 AA): gestión del foco, navegación por teclado, soporte de lectores de pantalla
- 🎭 **Múltiples variantes** (p. ej. estilo iOS, estilo Material, tipo modal de Bootstrap)
- 🧩 **Acciones agrupadas**, cabeceras, pies y acciones de cancelación
- 🎨 **Tematización con variables CSS** mediante tokens de diseño `--hub-*`
- 🌳 **Tree-shakeable**: componentes standalone

> Todas las funcionalidades planificadas anteriores son objetivos de diseño y **aún no están disponibles** en `0.0.1`.

## 🚀 Instalación

```bash
npm install ng-hub-ui-action-sheet
```

## ⚙️ Uso

> El único componente exportado actualmente es un marcador de posición. El ejemplo siguiente
> refleja lo que está **realmente disponible** en `0.0.1`.

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

## 🪄 Referencia de API

### Componente `ActionSheet`

- **Selector:** `lib-action-sheet`
- **Tipo:** componente standalone
- **Detección de cambios:** por defecto
- **Inputs:** ninguno
- **Outputs:** ninguno
- **Contenido:** renderiza una plantilla de marcador de posición estática

No hay ninguna otra API pública en esta etapa. Las interfaces siguientes ilustran la forma
**prevista** de la próxima API y se documentan aquí solo para comunicar la dirección — **no se
exportan** todavía.

```typescript
// 🔮 Planificado (no disponible en 0.0.1)
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

## 🤝 Contribución

¡Las contribuciones son bienvenidas! Esta es una biblioteca en etapa temprana y la ayuda para
dar forma a la API es especialmente valiosa.

```bash
# Clona el repositorio
git clone https://github.com/carlos-morcillo/ng-hub-ui-action-sheet.git

# Instala las dependencias
npm install

# Construye la biblioteca
ng build action-sheet

# Ejecuta los tests unitarios
ng test action-sheet
```

1. **Haz un fork** del repositorio
2. **Crea** una rama de feature: `git checkout -b feature/amazing-feature`
3. **Añade tests** para tus cambios
4. **Haz commit** de tus cambios: `git commit -m 'feat: add amazing feature'`
5. **Sube** tu rama: `git push origin feature/amazing-feature`
6. **Abre** un pull request

## ☕ Soporte

¿Te gusta esta biblioteca? Puedes apoyar su desarrollo invitando a un café ☕:
[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://buymeacoffee.com/carlosmorcillo)

- [Reportar un error](https://github.com/carlos-morcillo/ng-hub-ui-action-sheet/issues)
- [Solicitar una funcionalidad](https://github.com/carlos-morcillo/ng-hub-ui-action-sheet/issues/new)

## 📄 Licencia

Este proyecto está licenciado bajo la Licencia MIT - consulta el archivo [LICENSE](LICENSE) para más detalles.

MIT © ng-hub-ui contributors
