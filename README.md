# custom-hooks

Colección de hooks de React reutilizables. Cada carpeta de `src/` trae el hook y un componente
de ejemplo; se copian sueltos, sin instalar nada más que sus dependencias (`js-cookie`,
`lodash` o `copy-to-clipboard`, según el hook).

## Red y asincronía

| Hook | Qué hace |
|---|---|
| `useAsync` | Envuelve cualquier promesa y expone `{ loading, error, value }` |
| `useFetch` | `fetch` con el mismo ciclo de vida, sobre `useAsync` |
| `useScript` | Inyecta un `<script>` externo y sigue su carga |

## Estado y almacenamiento

| Hook | Qué hace |
|---|---|
| `useToggle` | Booleano con `toggle()` o valor forzado |
| `useArray` | `push`, `filter`, `update`, `remove` y `clear` sobre un array |
| `useStorage` | Estado sincronizado con `localStorage` o `sessionStorage` |
| `useCookie` | Estado sincronizado con una cookie |
| `useStateWithHistory` | Estado con deshacer y rehacer (`back`, `forward`, `go`) |
| `useStateWithValidation` | Estado más un `isValid` recalculado en cada cambio |
| `useDarkMode` | Tema oscuro persistente que respeta `prefers-color-scheme` |
| `useTranslation` | i18n básico con el idioma guardado en `localStorage` |
| `useCopyToClipboard` | Copia texto y devuelve lo copiado y si salió bien |
| `useTimeout` | `setTimeout` con `reset` y `clear`, sin fugas |

## DOM y ciclo de vida

| Hook | Qué hace |
|---|---|
| `useSize` | Las dimensiones de un nodo, con `ResizeObserver` |
| `useOnScreen` | Si un nodo está en el viewport, con `IntersectionObserver` |
| `useWindowSize` | El ancho y el alto de la ventana |
| `useMediaQuery` | Si matchea una media query |
| `useEffectOnce` | Efecto sólo al montar |
| `useUpdateEffect` | Efecto que ignora el primer render |
| `useDeepCompareEffect` | Efecto con comparación profunda de dependencias |
| `usePrevious` | El valor del render anterior |
| `useRenderCount` | Cuántas veces renderizó |
| `useDebugInformation` | Renders, props cambiadas y tiempo entre renders |

## Eventos y navegador

| Hook | Qué hace |
|---|---|
| `useEventListener` | Agrega y saca listeners con el callback siempre al día |
| `useClickOutside` | Click o toque fuera de un nodo |
| `useHover` | Si el puntero está encima |
| `useLongPress` | Pulsación larga (250 ms por defecto) |
| `useDebounce` | Ejecuta cuando las dependencias dejan de cambiar |
| `useOnlineStatus` | Si hay conexión |
| `useGeolocation` | Las coordenadas del usuario, siguiéndolo con `watchPosition` |
