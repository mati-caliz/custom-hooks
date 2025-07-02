## 🧩 Hooks Library

> Todos los hooks están agrupados por temática y presentados en bloques plegables `<details>` para que tu README quede limpio.  
> Haz clic en cada título para ver la descripción.

---

### 📡 Network & Async
<details>
<summary><strong>useFetch</strong> – peticiones HTTP con ciclo de vida</summary>
Encapsula `fetch` y devuelve <code>{ loading, error, data }</code>.  
Internamente usa <code>useAsync</code>.
</details>

<details>
<summary><strong>useAsync</strong> – wrapper genérico para promesas</summary>
Gestiona cualquier `Promise` y expone <code>{ loading, error, value }</code>.
</details>

<details>
<summary><strong>useScript</strong> – carga de scripts externos</summary>
Inyecta un &lt;script&gt; en el DOM y controla sus estados `loading / éxito / error` (basado en <code>useAsync</code>).
</details>

---

### 💾 State & Storage
<details>
<summary><strong>useArray</strong> – helpers para arrays</summary>
Provee operaciones <code>push · filter · update · remove · clear</code> sin reescribir lógica.
</details>

<details>
<summary><strong>useCookie</strong> – estado ↔️ cookie</summary>
Sincroniza un valor React con cookies usando **js-cookie**.
</details>

<details>
<summary><strong>useCopyToClipboard</strong> – portapapeles fácil</summary>
Copia texto y devuelve el último valor copiado + flag de éxito.
</details>

<details>
<summary><strong>useDarkMode</strong> – tema claro/oscuro persistente</summary>
Togglea dark mode, respeta <code>prefers-color-scheme</code> y guarda la preferencia.
</details>

<details>
<summary><strong>useToggle</strong> – booleano con switch</summary>
Encapsula <code>useState</code> y te da <code>toggle()</code> o fuerza <code>true/false</code>.
</details>

<details>
<summary><strong>useTimeout</strong> – setTimeout seguro</summary>
Helpers <code>reset</code> y <code>clear</code>; evita fugas y callbacks obsoletos.
</details>

<details>
<summary><strong>useStorage</strong> – local/session storage</summary>
Serializa/des-serializa automáticamente y devuelve <code>[value, set, remove]</code>.
</details>

<details>
<summary><strong>useStateWithValidation</strong> – estado + <em>isValid</em></summary>
Recalcula la validez cada vez que cambias el valor.
</details>

<details>
<summary><strong>useStateWithHistory</strong> – undo / redo</summary>
Mantiene historial limitado (por defecto 10) con <code>back · forward · go</code>.
</details>

<details>
<summary><strong>useTranslation</strong> – i18n básico</summary>
Persiste idioma en <code>localStorage</code> y busca claves anidadas en tu objeto `translations`.
</details>

---

### 🖼️ UI & DOM Observation
<details>
<summary><strong>useSize</strong> – dimensiones de un nodo</summary>
Usa `ResizeObserver` y devuelve el rectángulo <code>{ width, height, top, … }</code>.
</details>

<details>
<summary><strong>useOnScreen</strong> – visibilidad en viewport</summary>
Devuelve `true/false` según <code>IntersectionObserver</code> (ideal para lazy load).
</details>

<details>
<summary><strong>useWindowSize</strong> – ancho × alto de ventana</summary>
Mantiene <code>{ width, height }</code> reactivo en cada `resize`.
</details>

<details>
<summary><strong>useMediaQuery</strong> – match de media query</summary>
Escucha cualquier media query CSS y devuelve un booleano.
</details>

<details>
<summary><strong>useDeepCompareEffect</strong> – <em>effect</em> con comparación profunda</summary>
Re-ejecuta solo si el contenido de las dependencias cambia (usa <code>lodash/fp/isEqual</code>).
</details>

<details>
<summary><strong>useDebugInformation</strong> – diagnósticos de render</summary>
Muestra render count, props cambiadas y tiempo entre renders.
</details>

<details>
<summary><strong>useRenderCount</strong> – cuántos renders</summary>
Devuelve un número que se incrementa cada render.
</details>

<details>
<summary><strong>usePrevious</strong> – valor previo</summary>
Guarda el valor anterior de cualquier variable/estado.
</details>

---

### 🎯 Events & Interaction
<details>
<summary><strong>useClickOutside</strong> – click/touch fuera de un nodo</summary>
Ejecuta callback cuando el usuario hace click fuera del elemento.
</details>

<details>
<summary><strong>useLongPress</strong> – pulsación larga</summary>
Dispara callback tras mantener presionado <i>(delay por defecto 250 ms)</i>.
</details>

<details>
<summary><strong>useHover</strong> – estado <code>hovered</code></summary>
Booleano <code>true</code> mientras el puntero está encima del elemento.
</details>

<details>
<summary><strong>useEventListener</strong> – listener universal</summary>
Añade / quita listeners sin fugas, manteniendo la última versión del callback.
</details>

<details>
<summary><strong>useDebounce</strong> – debounce de callbacks</summary>
Retrasa la ejecución hasta que las dependencias no cambien durante <code>delay</code>.
</details>

<details>
<summary><strong>useEffectOnce</strong> – efecto solo al montar</summary>
Azúcar sintáctico para <code>useEffect(cb, [])</code>.
</details>

<details>
<summary><strong>useUpdateEffect</strong> – efecto que ignora el primer render</summary>
Útil para reaccionar solo a actualizaciones.
</details>

---

### 🌐 Browser & Device
<details>
<summary><strong>useOnlineStatus</strong> – online / offline</summary>
Booleano reactivo basado en <code>navigator.onLine</code>.
</details>

<details>
<summary><strong>useGeolocation</strong> – coordenadas del usuario</summary>
Devuelve <code>{ loading, error, data /* coords */ }</code> y sigue los movimientos con <code>watchPosition</code>.
</details>
